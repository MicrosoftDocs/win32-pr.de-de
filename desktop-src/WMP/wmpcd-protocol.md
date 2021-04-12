---
title: Wmpcd-Protokoll
description: Wmpcd-Protokoll
ms.assetid: 385cfb03-88cc-400c-a2b9-174008ebd854
keywords:
- Windows-Media Player, Protokolle
- Windows Media Player-Objektmodell, Protokolle
- Objektmodell, Protokolle
- Windows Media Player ActiveX-Steuerelement, Protokolle für das Objektmodell
- ActiveX-Steuerelement, Protokolle für Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Protokolle für das Objektmodell
- Windows Media Player Mobile, Protokolle für das Objektmodell
- Protokolle, Windows Media Player-Objektmodell
- Protokolle, wmpcd
- Wmpcd-Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa78c591d0ba9605f1f63e3e152b974d112548d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206708"
---
# <a name="wmpcd-protocol"></a>Wmpcd-Protokoll

Mit dem wmpcd-Protokoll können Sie mithilfe der URL-Syntax Spuren auf einer Compact Disk angeben. Dies ist die allgemeine Syntax des Protokolls:


```C++
wmpcd://drive/track
```



Das *Laufwerk* Segment ist der Index des CD-Laufwerks. Das *Track* -Segment ist die Nummer des Titels. Im folgenden Beispiel wird die Verwendung des wmpcd-Protokolls veranschaulicht.


```C++
player.url = "wmpcd://0/4";
```



Im Beispiel wird der vierte Titel auf der Festplatte auf dem ersten CD-Laufwerk (dem Laufwerk mit dem Index 0) wiedergegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Unterstützte Protokolle und Dateitypen**](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




