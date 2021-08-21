---
description: Die Geräteklasse wave/in/out besteht aus Vollduplex-Audiogeräten.
ms.assetid: 1b49c9ae-da64-4415-95ce-785ffedc65bc
title: Wave/In/Out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f526caf461cbf0bb5c3fb5490cf5e9141d9735e37e10ab632749006135a1cc9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118860409"
---
# <a name="waveinout"></a>Wave/In/Out

Die Geräteklasse wave/in/out besteht aus Vollduplex-Audiogeräten. Sie greifen auf diese Geräte zu, indem Sie die Wavefunktionen verwenden, die im Platform Software Development Kit (SDK) beschrieben werden. Geräte in dieser Klasse sind Zeilengeräten zugeordnet, die den \_ LINEMEDIAMODE AUTOMATEDVOICE-Medientyp unterstützen, der im **dwMediaModes-Member** der [**LINEDEVCAPS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) für das Zeilengerät angegeben ist.

Die Funktionen [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) und [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) füllen eine [**VARSTRING-Struktur**](/windows/desktop/api/Tapi/ns-tapi-varstring) aus, legen den **dwStringFormat-Member** auf den STRINGFORMAT \_ BINARY-Wert fest und fügen zwei zusätzliche Member an:

``` syntax
DWORD DeviceInId;  // identifier of wave in audio device
DWORD DeviceOutId;  // identifier of wave out audio device
```

Die Member **DeviceInId** und **DeviceOutId** sind Bezeichner eines geschlossenen Audiogeräts. Sie verwenden diese Bezeichner in einem Aufruf der [**waveOutOpen-Funktion,**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) um das Gerät für die Ausgabe zu öffnen. Sie können das resultierende Gerätehandle verwenden, um digitalisierte Audiodaten an der Leitung oder auf dem Smartphone wiederzuspielen.

Weitere Informationen zu wave-Funktionen finden Sie unter [**Multimediafunktionen.**](../multimedia/multimedia-functions.md)

 

 
