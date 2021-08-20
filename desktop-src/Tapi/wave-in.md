---
description: Die Wave-/In-Geräteklasse besteht aus Audiogeräten für die Low-Level-Wave-Audioeingabe.
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

Die Wave-/In-Geräteklasse besteht aus Audiogeräten für die Low-Level-Wave-Audioeingabe. Sie greifen auf diese Geräte zu, indem Sie die Wavefunktionen verwenden, die im Platform Software Development Kit (SDK) beschrieben werden. Geräte in dieser Klasse sind Zeilengeräten zugeordnet, die den \_ LINEMEDIAMODE AUTOMATEDVOICE-Medientyp unterstützen, der im **dwMediaModes-Member** der [**LINEDEVCAPS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) für das Zeilengerät angegeben ist.

Die Funktionen [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) und [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) füllen eine [**VARSTRING-Struktur**](/windows/desktop/api/Tapi/ns-tapi-varstring) aus, legen den **dwStringFormat-Member** auf den STRINGFORMAT \_ BINARY-Wert fest und fügen diesen zusätzlichen Member an:

``` syntax
DWORD DeviceId;  // identifier of audio device
```

Der **DeviceId-Member** ist der Bezeichner eines geschlossenen Audiogeräts. Sie verwenden diesen Bezeichner in einem Aufruf der [**waveInOpen-Funktion,**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) um das Gerät für die Eingabe zu öffnen. Sie können das resultierende Gerätehandle verwenden, um digitalisierte Audiodaten von der Leitung oder dem Telefongerät aufzuzeichnen.

Obwohl auch eine "Wave"-Geräteklasse für Wellenaudiogeräte auf niedriger Ebene vorhanden ist, sollten Sie immer die Geräteklasse wave/in für wellenbasierte Eingaben verwenden.

Weitere Informationen zu wave-Funktionen finden Sie unter [**Multimediafunktionen.**](../multimedia/multimedia-functions.md)

 

 
