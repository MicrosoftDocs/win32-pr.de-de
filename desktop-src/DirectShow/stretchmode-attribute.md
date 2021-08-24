---
description: Das Stretchmode-Attribut gibt an, wie ein Bild gestreckt wird, das nicht mit den Ausgabedimensionen übereinstimmt.
ms.assetid: 9a26bb8b-2b1c-424a-ae30-e175c60c76a1
title: stretchmode-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed398fbe193ef262bdfc9a28cf66bef3a5b11f759d90c460cc99342ec7cd66b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903870"
---
# <a name="stretchmode-attribute"></a>stretchmode-Attribut

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Das `stretchmode` -Attribut gibt an, wie ein Bild gestreckt wird, das nicht mit den Ausgabedimensionen übereinstimmt.

## <a name="possible-values"></a>Mögliche Werte

Muss einen der folgenden Werte aufweisen.

-   "stretch": Das Bild wird gestreckt, um die Größe des Ausgaberahmens anzupassen, ohne das Seitenverhältnis zu erhalten. (Standardwert)
-   "zuschneiden": Das Bild wird an die Größe des Ausgaberahmens angepasst.
-   "preserveaspectratio": Das ursprüngliche Seitenverhältnis wird mit einem schwarzen Letterbox entlang der kürzeren Dimension beibehalten.
-   "preserveaspectrationoletterbox": Die Größe des Bilds wird geändert, um den gesamten Zielrahmen zu füllen, während das Seitenverhältnis beibehalten wird.

## <a name="applies-to"></a>Gilt für

[**clip**](clip-element.md)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XTL-Attribute](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetStretchMode**](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 



