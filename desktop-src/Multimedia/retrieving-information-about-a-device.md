---
title: Abrufen von Informationen zu einem Gerät
description: Abrufen von Informationen zu einem Gerät
ms.assetid: d038d3fb-43d0-4d9d-836c-205f6d8c98e3
keywords:
- MCI_GETDEVCAPS-Befehl
- MCI_STATUS-Befehl
- MCI_INFO-Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10acb53fa1a961fe7a70042350f8d889d9fdf572
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948038"
---
# <a name="retrieving-information-about-a-device"></a>Abrufen von Informationen zu einem Gerät

Jedes Gerät antwortet auf die [**Funktionen**](capability.md) ([**MCI \_ getdevcaps**](mci-getdevcaps.md)), [**Status**](status.md) ([**MCI- \_ Status**](mci-status.md)) und [**Info**](info.md) -Befehle ([**MCI- \_ Info**](mci-info.md)). Mit diesen Befehlen werden Informationen zum Gerät abgerufen. Der folgende Befehl gibt z. b. "true" zurück, wenn ein **CDAudio** -Gerät die Festplatte Auswerfen kann:


```C++
mciSendString(
    "capability cdaudio can eject", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



Die Flags, die für die erforderlichen und grundlegenden Befehle aufgelistet sind, stellen eine minimale Menge an Informationen zu einem Gerät bereit. Viele Geräte ergänzen die erforderlichen und grundlegenden Befehle mit erweiterten Flags, um zusätzliche Informationen über das Gerät bereitzustellen.

 

 




