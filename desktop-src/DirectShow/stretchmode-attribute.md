---
description: Das stretchmode-Attribut gibt an, wie ein Bild gestreckt wird, das nicht den Ausgabe Dimensionen entspricht.
ms.assetid: 9a26bb8b-2b1c-424a-ae30-e175c60c76a1
title: stretchmode-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a629a34dc1875a7f1d3669e32c53d0e8d3d29c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867084"
---
# <a name="stretchmode-attribute"></a>stretchmode-Attribut

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Das- `stretchmode` Attribut gibt an, wie ein Bild gestreckt wird, das nicht den Ausgabe Dimensionen entspricht.

## <a name="possible-values"></a>Mögliche Werte

Muss einen der folgenden Werte aufweisen.

-   "Stretch": das Bild wird so gestreckt, dass es der Ausgabe Frame Größe entspricht, ohne das Seitenverhältnis beizubehalten. (Standardwert)
-   "Zuschneiden": das Bild wird an die Ausgabe Frame Größe angepasst.
-   "preserveaspectratio": das ursprüngliche Seitenverhältnis wird beibehalten, wobei ein schwarzes buchfeld entlang der kürzeren Dimension liegt.
-   "preserveaspectrationoletterbox": die Größe des Bilds wird geändert, um den gesamten Zielframe auszufüllen und gleichzeitig das Seitenverhältnis beizubehalten.

## <a name="applies-to"></a>Gilt für

[**Techno**](clip-element.md)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XTL-Attribute](xtl-attributes.md)
</dt> <dt>

[**Iamtimelinesrc:: setstretchmode**](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 



