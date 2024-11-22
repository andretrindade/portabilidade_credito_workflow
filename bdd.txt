Feature: Transcorrido 3 dias uteis após recebimento da solicitação de portabilidade pela Credora

Background:

    Given o cliente tenha realizado uma solicitação de portabilidade para o Proponente

    And o cliente tenha recebido uma mensagem de sucesso de recebimento da solicitação de portabilidade pelo proponente

    And o Proponente tenha enviado a solciitação de portabilidade para a Credora

And a Credora tenha recebido a solicitação de portabilidade com sucesso

 

Scenario: Proponente atualiza situação da proposta para ACCEPTED_SETTLEMENT_IN_PROGRESS após os 3 dias uteis a partir do recebimento da solicitação da proposta pela Credora e sem manifestação de seguir com uma contra-proposta por parte do Cliente ou Credora.

    Given uma solicitação de portabilidade com situação “RECEIVED“

    When o 4˚ dia util após o recebimento da solicitação de portabilidade de credito pela Credora se realiza

    And a credora juntamente com o cliente não se manifestam sobre uma possível contra-proposta

    Then o proponente segue atualizado a solicitação de portabilidade para “ACCEPTED_SETTLEMENT_IN_PROGRESS“