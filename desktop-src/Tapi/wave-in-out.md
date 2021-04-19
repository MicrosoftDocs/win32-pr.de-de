---
description: Die Geräteklasse "Wave/in/out" besteht aus vollständigen Duplex Audiogeräten.
ms.assetid: 1b49c9ae-da64-4415-95ce-785ffedc65bc
title: Wave/in/out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0e814cf2e8de1c3c5700a7570d2ed2b4c428572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349940"
---
# <a name="waveinout"></a>Wave/in/out

Die Geräteklasse "Wave/in/out" besteht aus vollständigen Duplex Audiogeräten. Sie greifen auf diese Geräte mithilfe der Wave-Funktionen zu, die im Platform Software Development Kit (SDK) beschrieben werden. Geräte in dieser Klasse sind Zeilen Geräten zugeordnet, die den Typ linemediamode \_ automatedvoice unterstützen, der im **dwmediamodes** -Member der [**linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) -Struktur für das liniengerät angegeben wird.

Die Funktionen " [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) " und " [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) " füllen eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur aus, indem Sie das Element " **dwstringformat** " auf den binären Wert "StringFormat" festlegen \_ und zwei zusätzliche Member anhängen:

``` syntax
DWORD DeviceInId;  // identifier of wave in audio device
DWORD DeviceOutId;  // identifier of wave out audio device
```

Die Member " **de viceingeid** " und " **deviceoutid** " sind Bezeichner eines geschlossenen Audiogeräts. Sie verwenden diese Bezeichner in einem Aufrufe der [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) -Funktion, um das Gerät für die Ausgabe zu öffnen. Sie können das resultierende Geräte Handle verwenden, um digitalisierte Audiodaten an der Zeile oder dem Telefongerät wiederzugeben.

Weitere Informationen zu den Wave-Funktionen finden Sie unter [**Multimedia Functions**](../multimedia/multimedia-functions.md).

 

 
