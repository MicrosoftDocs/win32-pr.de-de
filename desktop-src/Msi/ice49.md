---
description: ICE49 prüft standardmäßige Registrierungseinträge, bei denen es sich nicht um einen reg \_ SZ-Typ handelt.
ms.assetid: 53d976fe-07d2-4b68-ae21-1dbd00d76942
title: ICE49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edc5ba319380e92fe7d1b7410673c1c688eb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867295"
---
# <a name="ice49"></a>ICE49

ICE49 prüft standardmäßige Registrierungseinträge, bei denen es sich nicht um einen **reg \_ SZ** -Typ handelt.

## <a name="result"></a>Ergebnis

ICE49 gibt eine Warnung aus, wenn ein Standard Registrierungs Eintrag vorhanden ist, bei dem es sich nicht um einen **reg \_ SZ** -Typ handelt.

## <a name="example"></a>Beispiel

ICE49 meldet die folgende Warnung für das gezeigte Beispiel.

``` syntax
Reg Entry 'Reg1' is not of type REG_SZ. Default types must be REG_SZ 
    on Win95 Systems. Make sure the component is conditionalized 
    to never be installed on Win95 machines.
```

Der Wert " \# 123" ist ein **DWORD** -Registrierungs Wert.

[Registrierungs Tabelle](registry-table.md) (partiell)



| Registrierung | Name | Wert |
|----------|------|-------|
| Reg1     |      | \#123 |



 

Um diese Warnung zu beheben, ändern Sie den Wert in Typ **reg \_ SZ**.

Komponenten mit nicht-**reg- \_ SZ** sind gültig.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Syntax der bedingten Anweisung](conditional-statement-syntax.md)
</dt> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



