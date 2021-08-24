---
title: WMPCD-Protokoll
description: WMPCD-Protokoll
ms.assetid: 385cfb03-88cc-400c-a2b9-174008ebd854
keywords:
- Windows Media Player,Protokolle
- Windows Media Player Objektmodell,Protokolle
- Objektmodell, Protokolle
- Windows Media Player ActiveX,Protokolle für objektmodell
- ActiveX-Steuerelement,Protokolle für das Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement,Protokolle für objektmodell
- Windows Media Player Mobil,Protokolle für Objektmodell
- protocols,Windows Media Player-Objektmodell
- Protocols,WMPCD
- WMPCD-Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181b1359d22b792587f7cceeb46f0f9e621585dfba296422a227e9012077df7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900140"
---
# <a name="wmpcd-protocol"></a>WMPCD-Protokoll

Mit dem WMPCD-Protokoll können Sie mithilfe der URL-Syntax Spuren auf einem Datenträger angeben. Dies ist die allgemeine Syntax des Protokolls:


```C++
wmpcd://drive/track
```



Das *Laufwerksegment* ist der Index des CD-Laufwerks. Das *Tracksegment* ist die Nummer der Spur. Im folgenden Beispiel wird die Verwendung des WMPCD-Protokolls veranschaulicht.


```C++
player.url = "wmpcd://0/4";
```



Im Beispiel wird die vierte Spur auf dem Datenträger im ersten CD-Laufwerk (das Laufwerk mit dem Index 0) abgespielt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Unterstützte Protokolle und Dateitypen**](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




