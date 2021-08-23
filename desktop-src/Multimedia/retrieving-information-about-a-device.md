---
title: Abrufen von Informationen zu einem Gerät
description: Abrufen von Informationen zu einem Gerät
ms.assetid: d038d3fb-43d0-4d9d-836c-205f6d8c98e3
keywords:
- MCI_GETDEVCAPS Befehl
- MCI_STATUS Befehl
- MCI_INFO Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412ccfb8819ac1c76cd3f0114fa114c877280de959f605535fd4bb83d224a91e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689090"
---
# <a name="retrieving-information-about-a-device"></a>Abrufen von Informationen zu einem Gerät

Jedes Gerät antwortet auf die Befehle [**"Capability"**](capability.md) [**(MCI \_ GETDEVCAPS),**](mci-getdevcaps.md) [**"status"**](status.md) [**(MCI \_ STATUS)**](mci-status.md)und [**"info"**](info.md) [**(MCI \_ INFO).**](mci-info.md) Diese Befehle erhalten Informationen zum Gerät. Der folgende Befehl gibt beispielsweise "true" zurück, wenn ein **cdaudio-Gerät** den Datenträger auswerfen kann:


```C++
mciSendString(
    "capability cdaudio can eject", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



Die flags, die für die erforderlichen und grundlegenden Befehle aufgeführt sind, stellen eine Mindestmenge an Informationen zu einem Gerät zur Verfügung. Viele Geräte ergänzen die erforderlichen und grundlegenden Befehle durch erweiterte Flags, um zusätzliche Informationen zum Gerät zu liefern.

 

 




