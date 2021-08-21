---
description: Ein Grafikobjekt stellt Methoden wie DrawLine, DrawImage und DrawString zum Anzeigen von Vektorbildern, Rasterbildern und Text zur Auswahl.
ms.assetid: 721d0c1c-d105-4d9f-b5e9-6ca407b28c4e
title: Verwenden von Grafikcontainern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96292395113b80ec79f8b59d4ac7f203c3d1f2d892c2da62ce4957e49b81860d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036288"
---
# <a name="using-graphics-containers"></a>Verwenden von Grafikcontainern

Ein [**Grafikobjekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) stellt Methoden wie [DrawLine,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))und [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) zum Anzeigen von Vektorbildern, Rasterbildern und Text zur Auswahl. Ein **Grafikobjekt** verfügt auch über mehrere Eigenschaften, die die Qualität und Ausrichtung der gezeichneten Elemente beeinflussen. Beispielsweise bestimmt die Eigenschaft des Glättungsmodus, ob Antialiasing auf Linien und Kurven angewendet wird, und die Transformationseigenschaft der Welt beeinflusst die Position und Drehung der gezeichneten Elemente.

Ein [**Grafikobjekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) ist häufig einem bestimmten Anzeigegerät zugeordnet. Wenn Sie ein **Graphics-Objekt** verwenden, um in einem Fenster zu zeichnen, wird das **Grafikobjekt** auch diesem bestimmten Fenster zugeordnet.

Ein [**Grafikobjekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) kann als Container bezeichnet werden, da es eine Reihe von Eigenschaften enthält, die das Zeichnen beeinflussen, und es ist mit gerätespezifischen Informationen verknüpft. Sie können einen sekundären Container innerhalb eines vorhandenen **Graphics-Objekts** erstellen, indem Sie die [BeginContainer-Methode](/previous-versions//ms535731(v=vs.85)) dieses **Graphics-Objekts** aufrufen.

In den folgenden Themen werden [**Grafikobjekte**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) und geschachtelte Container ausführlicher behandelt:

-   [Status eines Grafikobjekts](-gdiplus-the-state-of-a-graphics-object-use.md)
-   [Geschachtelte Grafikcontainer](-gdiplus-nested-graphics-containers-use.md)

 

 
