---
description: Ein Graphics-Objekt stellt Methoden wie DrawLine, DrawImage und DrawString zum Anzeigen von Vektorbildern, Rasterbildern und Text bereit.
ms.assetid: 721d0c1c-d105-4d9f-b5e9-6ca407b28c4e
title: Verwenden von Grafikcontainern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80570f3a45c8d67b36f677fc404dcd63581e7938
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978905"
---
# <a name="using-graphics-containers"></a>Verwenden von Grafikcontainern

Ein [**graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) -Objekt stellt Methoden wie [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))und [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) zum Anzeigen von Vektorbildern, Rasterbildern und Text bereit. Ein **Grafik** Objekt verfügt auch über mehrere Eigenschaften, die die Qualität und Ausrichtung der Elemente beeinflussen, die gezeichnet werden. Beispielsweise legt die Eigenschaft Glättungs Modus fest, ob Antialiasing auf Linien und Kurven angewendet wird, und die Welt Transformations Eigenschaft wirkt sich auf die Position und Drehung der Elemente aus, die gezeichnet werden.

Ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt ist oft einem bestimmten Anzeigegerät zugeordnet. Wenn Sie ein **Grafik** Objekt zum Zeichnen in einem Fenster verwenden, wird das **Grafik** Objekt auch diesem bestimmten Fenster zugeordnet.

Ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt kann als Container betrachtet werden, da es einen Satz von Eigenschaften enthält, die das Zeichnen beeinflussen und mit gerätespezifischen Informationen verknüpft sind. Sie können einen sekundären Container innerhalb eines vorhandenen **Grafik** Objekts erstellen, indem Sie die [BeginContainer](/previous-versions//ms535731(v=vs.85)) -Methode dieses **Grafik** Objekts aufrufen.

In den folgenden Themen werden [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekte und schsted-Container ausführlicher behandelt:

-   [Status eines Grafikobjekts](-gdiplus-the-state-of-a-graphics-object-use.md)
-   [Geschachtelte Grafikcontainer](-gdiplus-nested-graphics-containers-use.md)

 

 
