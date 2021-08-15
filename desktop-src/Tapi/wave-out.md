---
description: Die Wave/Out-Geräteklasse besteht aus Audiogeräten für die Audioausgabe auf niedriger Ebene.
ms.assetid: 85894134-e8ad-43e2-8b97-09b80bfd36d5
title: wave/out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f3e8a82b8345e8f50e1ad18f527c82f4ece241e03c0ea7cd083dd2d2ae79282
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760175"
---
# <a name="waveout"></a>wave/out

Die Wave/Out-Geräteklasse besteht aus Audiogeräten für die Audioausgabe auf niedriger Ebene. Sie greifen auf diese Geräte mithilfe der Wellenfunktionen zu, die im Platform Software Development Kit (SDK) beschrieben werden. Geräte in dieser Klasse sind Liniengeräten zugeordnet, die den LINEMEDIAMODE AUTOMATEDVOICE-Medientyp unterstützen, der im \_ **dwMediaModes-Member** der [**LINEDEVCAPS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) für das Liniengerät angegeben ist.

Die [**Funktionen lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) und [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) füllen eine [**VARSTRING-Struktur**](/windows/desktop/api/Tapi/ns-tapi-varstring) aus, legen den **dwStringFormat-Member** auf den STRINGFORMAT BINARY-Wert und fügen diesen \_ zusätzlichen Member an:

``` syntax
DWORD DeviceId;  // identifier of audio device
```

Der **DeviceId-Member** ist der Bezeichner eines geschlossenen Audiogeräts. Sie verwenden diesen Bezeichner in einem Aufruf der [**waveOutOpen-Funktion,**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) um das Gerät für die Ausgabe zu öffnen. Sie können den resultierenden Gerätehandpunkt verwenden, um digitalisierte Audiodaten auf der Linie oder dem Telefongerät wieder zu geben.

Obwohl eine "Wave"-Geräteklasse auch für Low-Level-Wave-Audiogeräte vorhanden ist, sollten Sie immer die Wave/Out-Geräteklasse für die Ausgabe niedrigerEr ebener Wellen verwenden.

Weitere Informationen zu den Wellenfunktionen finden Sie unter [**Multimediafunktionen.**](../multimedia/multimedia-functions.md)

 

 
