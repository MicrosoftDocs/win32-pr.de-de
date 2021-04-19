---
description: Die TAPI/Terminal-Geräteklasse besteht aus den Telefongeräten, die jedem Terminal in einer Zeile oder dem Terminal in jeder mit einem Telefongerät verknüpften Zeile zugeordnet sind. Sie greifen auf diese Geräte über das TAPI-Geräte Gerät oder über Telefongeräte Funktionen zu.
ms.assetid: 466ed2cd-f737-4df4-8633-4fb5c95b4b6c
title: TAPI/Terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce64da984f766e8ca3c0c47f1b60db6e9d7d8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373185"
---
# <a name="tapiterminal"></a>TAPI/Terminal

Die TAPI/Terminal-Geräteklasse besteht aus den Telefongeräten, die jedem Terminal in einer Zeile oder dem Terminal in jeder mit einem Telefongerät verknüpften Zeile zugeordnet sind. Sie greifen auf diese Geräte über das TAPI-Geräte [Gerät](line-device-functions.md) oder über [Telefongeräte Funktionen](phone-device-functions.md)zu.

Die [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) -Funktion füllt eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur aus, legt den **dwstringformat** -Member auf den "StringFormat" \_ -Binärwert fest und fügt diesen zusätzlichen Member an:

``` syntax
DWORD adwDeviceId[];  // array of phone device identifiers
```

Der **adwentviceid** -Member ist ein Array von Telefongeräte bezeichnerbezeichner. Es gibt ein Array-Element für jedes Terminal, das vom **dwnumterminals** -Member in der [**linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) -Struktur für das angegebene Zeilen Gerät angegeben wird. Jedes-Element gibt den Bezeichner des Telefon Geräts an, das dem entsprechenden Terminal in der Zeile zugeordnet ist. Wenn einem Terminal kein Telefongerät zugeordnet ist, wird das-Element auf – 1 (0xFFFFFFFF) festgelegt.

Die [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) -Funktion füllt eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur aus, legt den **dwstringformat** -Member auf den "StringFormat" \_ -Binärwert fest und fügt diesen zusätzlichen Member an:

``` syntax
DWORD adwTerminalID[];  // array of terminal identifiers
```

Der **adwterminalid-** Member ist ein Array von Terminal bezeichlern. Es gibt ein Array-Element für jeden Zeilen Geräte Bezeichner, der von der [**lineinitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) -oder [**lineinitializeex**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) -Funktion angegeben wird. Jedes Array Element enthält den Terminal Bezeichner, der dem Telefongerät für das angegebene liniengerät zugeordnet ist. Wenn kein Telefongerät vorhanden ist, wird das-Element auf – 1 (0xFFFFFFFF) festgelegt. Der Bereich der Terminal-IDs liegt zwischen null und eins kleiner als die Zahl, die durch den **dwnumterminals** -Member in der [**linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) -Struktur angegeben wird.

 

 



