---
title: Normale tertiäre Image Quelle
description: Normale tertiäre Image Quelle
ms.assetid: ce0b009a-b008-4e8b-875b-b2ff3c1c0b81
keywords:
- Windows Media Player Mobile Skins, Schaltflächen Bildquelle
- Skins, Schaltflächen Bildquelle
- Verweis für Skins, Schaltflächen
- Schaltflächen in Skins, Bildquelle
- Bildquelle für Skins, Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109509914c498e950f148caf7c260ef814c1074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388602"
---
# <a name="normal-tertiary-image-source"></a>Normale tertiäre Image Quelle

Die Funktion "playpautsplay" erfordert, dass Sie die Position des normalen Bilds für den tertiären Zustand der Schaltfläche definieren. Dies ist das Bild, das Benutzern angezeigt wird, nachdem Sie die playpausestopschtaste gedrückt haben, um mit dem Streamen einer Liveübertragung zu beginnen.

Um dieses Bild zu definieren, müssen Sie den Bildtyp gefolgt von einem Leerzeichen und dem @-Symbol und einem weiteren Leerzeichen eingeben. Sie müssen dann zwei positive ganze Zahlen eingeben, die die oberen linken Koordinaten (in Pixel) des Bilds definieren, das Sie in den zu zeichnenden Bitmaptyp verwenden möchten.

Wenn Sie z. b. das normale Bild für eine tertiäre Image Quelle definieren möchten, geben Sie Folgendes ein, wenn sich Ihr Image in der über drückten Bitmap befindet:


```C++
Pushed @ 286,0

```



Tertiäre Zustände dürfen kein deaktiviertes Image aufweisen. Es wird davon ausgegangen, dass es sich um die gleiche Breite und Höhe wie die primären und sekundären Images handelt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schaltflächen**](buttons.md)
</dt> </dl>

 

 




