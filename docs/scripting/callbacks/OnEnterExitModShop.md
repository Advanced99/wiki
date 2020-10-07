---
id: OnEnterExitModShop
title: OnEnterExitModShop
description: This callback is called when a player enters or exits a mod shop.
tags: []
---

:::Aviso

Este callback foi adicionado no SA-MP 0.3a e não funcionará nas versões anteriores!

:::

## Descrição 

Este callback é chamado quando um jogador entra ou sai de um mod shop.

| Nome       | Descrição                                                                    |
| ---------- | ---------------------------------------------------------------------------- |
| playerid   | O ID do jogador que entrou ou saiu do modshop                                |
| enterexit  | 1 se o jogador entrou ou 0 se saiu                                           |
| interiorid | O ID interior do modshop em que o jogador está entrando (ou 0 se se for sair)|

## Retornos

É sempre chamado primeiro nos filterscripts.

## Exemplos

```c
public OnEnterExitModShop(playerid, enterexit, interiorid)
{
    if(enterexit == 0) // If enterexit is 0, this means they are exiting
    {
        SendClientMessage(playerid, COLOR_WHITE, "Nice car! You have been taxed $100.");
        GivePlayerMoney(playerid, -100);
    }
    return 1;
}
```

## Notas

:::Aviso

Bug(s) conhecido(s): Os jogadores colidem quando entram na mesma loja de mods.

:::

## Funções Relacionadas

- [AddVehicleComponent](../functions/AddVehicleComponent.md): Adiciona um componente a um veículo.
