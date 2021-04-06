---
description: Arbeiten mit Effekten und Übergängen
ms.assetid: 00e97d02-ff43-4e1f-9806-abaeb9288058
title: Arbeiten mit Effekten und Übergängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99029269ac86e17246fd641341b071654582bc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960936"
---
# <a name="working-with-effects-and-transitions"></a>Arbeiten mit Effekten und Übergängen

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Auswirkungen Ändern eines einzelnen Clips, nach Titels oder einer Komposition. Mithilfe von Übergängen werden sequenen aus einer Spur erstellt, oder es wird eine andere erstellt.

[DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) verwenden DirectX-Transformations Objekte für Video Übergänge und Video Effekte. Verwenden Sie für Video Übergänge ein beliebiges 2-D-DirectX-Transformations Objekt mit zwei Eingaben. Verwenden Sie für Video Effekte ein beliebiges 2D-Einzel Eingabe-DirectX-Transformations Objekt. Microsoft unterstützt die Entwicklung von DirectX-Transformations Objekten von Drittanbietern nicht mehr. Mit DirectShow werden jedoch mehrere bereitgestellt, und andere werden mit Microsoft Internet Explorer bereitgestellt. Weitere Informationen zu den Übergängen, die mit Internet Explorer bereitgestellt werden, finden Sie unter [visuelle Filter und Übergänge-Referenz](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms532853(v=vs.85)).

Für Audioeffekte können Sie einen beliebigen DirectShow-Audioeffekt-Filter verwenden. Der stellt außerdem einen [volumeumschlags Effekt](volume-envelope-effect.md) für das Festlegen des Volumes auf einem Track-oder Clip-Wert bereit. DES unterstützt keine audioübergänge.

Dieser Abschnitt enthält die folgenden Themen:

-   [Hinzufügen von Effekt-und Übergangs Objekten](adding-effect-and-transition-objects.md)
-   [Vorschau von Effekten und Übergängen](previewing-effects-and-transitions.md)
-   [Aufzählen von Effekten und Übergängen](enumerating-effects-and-transitions.md)
-   [Festlegen von Eigenschaften für Effekte und Übergänge](setting-properties-on-effects-and-transitions.md)
-   [Übergangs Richtung](transition-direction.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DirectShow-Bearbeitungs Diensten](using-directshow-editing-services.md)
</dt> </dl>

 

 
