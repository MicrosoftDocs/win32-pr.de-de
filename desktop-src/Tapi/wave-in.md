---
description: Die Wellen-/In-Geräteklasse besteht aus Audiogeräten für die Audioeingabe auf niedriger Ebene.
ms.assetid: b2f32019-088f-4805-af7e-559a8179b1e6
title: wave/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24cc80d41f402abf1886e063563f272abf7992768dd62f03e64b327a7e199360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002528"
---
# <a name="wavein"></a>wave/in

Die Wellen-/In-Geräteklasse besteht aus Audiogeräten für die Audioeingabe auf niedriger Ebene. Sie greifen auf diese Geräte mithilfe der Wellenfunktionen zu, die im Platform Software Development Kit (SDK) beschrieben sind. Geräte in dieser Klasse sind Liniengeräten zugeordnet, die den LINEMEDIAMODE AUTOMATEDVOICE-Medientyp unterstützen, der im \_ **dwMediaModes-Member** der [**LINEDEVCAPS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) für das Liniengerät angegeben ist.

Die [**Funktionen lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) und [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) füllen eine [**VARSTRING-Struktur**](/windows/desktop/api/Tapi/ns-tapi-varstring) aus, legen den **dwStringFormat-Member** auf den STRINGFORMAT BINARY-Wert und fügen diesen \_ zusätzlichen Member an:

``` syntax
DWORD DeviceId;  // identifier of audio device
```

Der **DeviceId-Member** ist der Bezeichner eines geschlossenen Audiogeräts. Sie verwenden diesen Bezeichner in einem Aufruf der [**waveInOpen-Funktion,**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) um das Gerät für die Eingabe zu öffnen. Mithilfe des resultierenden Gerätehandpunkts können Sie digitalisierte Audiodaten von der Linie oder dem Telefongerät aufzeichnen.

Obwohl auch für Low-Level-Wave-Audiogeräte eine "Wave"-Geräteklasse vorhanden ist, sollten Sie immer die Wave-/In-Geräteklasse für Welleneingaben auf niedriger Ebene verwenden.

Weitere Informationen zu den Wellenfunktionen finden Sie unter [**Multimediafunktionen.**](../multimedia/multimedia-functions.md)

 

 
