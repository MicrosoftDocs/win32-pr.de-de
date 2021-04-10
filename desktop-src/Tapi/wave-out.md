---
description: Die Geräteklasse "Wave/Out" besteht aus Audiogeräten für die Ausgabe von Wave-Audiodaten auf niedriger Ebene.
ms.assetid: 85894134-e8ad-43e2-8b97-09b80bfd36d5
title: Wave/Out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975a3308b6f0b29e130ad07534494e1cb1d991a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869187"
---
# <a name="waveout"></a>Wave/Out

Die Geräteklasse "Wave/Out" besteht aus Audiogeräten für die Ausgabe von Wave-Audiodaten auf niedriger Ebene. Sie greifen auf diese Geräte mithilfe der Wave-Funktionen zu, die im Platform Software Development Kit (SDK) beschrieben werden. Geräte in dieser Klasse sind Zeilen Geräten zugeordnet, die den Typ linemediamode \_ automatedvoice unterstützen, der im **dwmediamodes** -Member der [**linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) -Struktur für das liniengerät angegeben wird.

Die Funktionen [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) und [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) füllen eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur aus, indem Sie das Element **dwstringformat** auf den Binär Wert StringFormat festlegen \_ und diesen zusätzlichen Member anhängen:

``` syntax
DWORD DeviceId;  // identifier of audio device
```

Der Member " **enviceid** " ist der Bezeichner eines geschlossenen Audiogeräts. Sie verwenden diesen Bezeichner in einem Aufrufe der [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) -Funktion, um das Gerät für die Ausgabe zu öffnen. Sie können das resultierende Geräte Handle verwenden, um digitalisierte Audiodaten an der Zeile oder dem Telefongerät wiederzugeben.

Obwohl eine "Wave"-Geräteklasse auch für Wellen Audiogeräte auf niedriger Ebene vorhanden ist, sollten Sie immer die Wave/Out-Geräteklasse für eine Wellen Ausgabe auf niedriger Ebene verwenden.

Weitere Informationen zu den Wave-Funktionen finden Sie unter [**Multimedia Functions**](../multimedia/multimedia-functions.md).

 

 
