---
title: SeekThumb-Datei
description: SeekThumb-Datei
ms.assetid: 757aeb93-ebf0-4659-8cb0-686e54485ac4
keywords:
- Windows Media Player Mobile Skins, Grafikdateien
- Skins, Art-Dateien
- Dateien für Skins, Art
- Grafikdateien für Skins, SeekThumbd-Dateien
- Windows Media Player Mobile Skins, SeekThumb-Dateien
- Skins, SeekThumb-Dateien
- SeekThumb-Dateien in Skins
- thumb,SeekThumb-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de49bf3a93b5dd3a538fc98c824e274547bf97a883c4255322336c2ba23b54cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117933725"
---
# <a name="seekthumb-file"></a>SeekThumb-Datei

Die SeekThumb-Datei definiert das Bild, das die Wiedergabeposition innerhalb des Medienelements für eine Seek-Trackleiste angibt. Sie können eine Datei verwenden und für die Verwendung durch SeekThumb und VolumeThumb definieren. Im Gegensatz zu den anderen Grafikdateien werden die Thumb-Dateien im Abschnitt Trackbars der Skindefinitionsdatei definiert.

Die folgende Abbildung ist eine typische SeekThumb-Datei.

![seekthumb-Datei](images/cesdksee.gif)

Diese beiden Schaltflächendateien sehen gleich aus, unterscheiden sich jedoch geringfügig. Das linke Bild ist die normale Ansicht, die dem Benutzer angezeigt wird, und das rechte Bild ist das Per Push übertragene Bild, das dem Benutzer angezeigt wird, wenn er auf die Schaltfläche tippt.

> [!Note]  
> SeekThumb-Grafikdateien, die für Skins erstellt wurden, die in Windows Media Player 10 Mobile oder höher verwendet werden, müssen die folgenden drei Bilder (von links nach rechts) aufweisen: normal, pushed und disabled.

 

Möglicherweise möchten Sie bestimmte Bereiche der Daumenbilder transparent machen. Dadurch können Sie Thumb-Bilder in anderen Formen als rechteckig erstellen. Jeder Bereich eines Fingerabdruckbilds, den Sie mit der durch den RGB-Wert 255, 0, 255 angegebenen Farbe füllen, wird in Ihrer Skin transparent angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Art Files**](art-files-mobile.md)
</dt> </dl>

 

 




