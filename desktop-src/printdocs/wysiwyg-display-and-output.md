---
description: Die meisten Anwendungen versuchen, WYSIWYG (was Sie sehen, was Sie erhalten) zu unterstützen.
ms.assetid: 34a1f37c-0fbf-451b-bb55-80ad85bcd4de
title: WYSIWYG-Anzeige und-Ausgabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c03e4fa653c0d8e891cb079a7a7e7a003f9ad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351487"
---
# <a name="wysiwyg-display-and-output"></a>WYSIWYG-Anzeige und-Ausgabe

Die meisten Anwendungen versuchen, WYSIWYG (was Sie sehen, was Sie erhalten) zu unterstützen. Dies bedeutet, dass der Text, der im Anwendungsfenster mit einer 10-stufigen, im Anwendungsfenster gezeichneten 10-Punkt-Schriftart gezeichnet wird, beim Drucken eine ähnliche Darstellung aufweisen sollte. Das Abrufen der tatsächlichen WYSIWYG-Ausgabe ist praktisch unmöglich und in den meisten Fällen sogar unerwünscht. Dies ist teilweise auf die Unterschiede in Video-und Drucker Technologien zurückzuführen. ein Pixel auf einem Bildschirm ist in der Regel größer als ein Punkt auf einem gängigen Laserdrucker. Die Anzeige von Entfernungen unterscheidet sich ebenfalls. ein Computerbenutzer befindet sich in der Regel ungefähr zwei Meter vom Bildschirm, aber die Augen eines Readers sind in der Regel ein oder weniger von der gedruckten Seite.

Um die Unterschiede bei der Lesbarkeit zwischen Bildschirmen und der gedruckten Seite auszugleichen, unterstützt das System eine Einheit, die als logischer Zoll bezeichnet wird und immer in Pixel angegeben wird. Bei einer Videoanzeige ist der logische Zoll immer größer als der physische Zoll, um die längere Anzeige Entfernung und die (im allgemeinen) koarser Auflösung auszugleichen. Bei Druckern ist der logische Zoll immer gleich dem physischen Zoll.

Zum Abrufen eines WYSIWYG-Effekts beim Zeichnen von Text sind zwei verwandte Probleme aufgetreten: das Aussehen einzelner Zeichen und das geräteunabhängige Seitenlayout. Um das erste Problem zu beheben, kann eine Anwendung mithilfe [**der Funktion "" die Funktion**](/windows/desktop/api/wingdi/nf-wingdi-createfonta) "-Funktion" den Schriftart Namen und die Größe einer idealen (oder logischen) Schriftart angeben und dann die [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) -Funktion aufrufen, um den Anzeige-oder Drucker Gerätekontext zu identifizieren. Wenn die Anwendung **SelectObject** aufruft, wählt das System eine physische Schriftart aus, die der angegebenen logischen Schriftart am ehesten entspricht. Wenn das System die Anzeige Schriftart auswählt, wählt es eine physische Schriftart aus, die größer als die tatsächliche Größe ist. Dies tritt auf, weil der größere logische Zoll auf der Anzeige angezeigt wird. Aus Sicht des Benutzers ist es jedoch anscheinend sehr nahe an der richtigen Höhe. Wenn das System die Schriftart für den Drucker auswählt, wählt es eine physische Schriftart aus, die tatsächlich die angeforderte Größe ist. Weitere Informationen zu Schriftarten und Textausgaben finden Sie unter [Schriftarten und Text](/windows/desktop/gdi/fonts-and-text).

Das zweite Problem, das geräteunabhängige Seitenlayout, kann durch die Verwendung von TrueType-Metriken behoben werden. Dies gilt auch, wenn die Kompatibilität mit 16-Bit-Versionen von Windows gewahrt bleibt. Weitere Informationen finden Sie unter [Verwenden von portablen TrueType-Metriken](/windows/desktop/gdi/using-portable-truetype-metrics).

Um beim Zeichnen von Bitmapgrafiken einen WYSIWYG-Effekt zu erhalten, kann eine Anwendung die Breite und Höhe des Bildschirms und der gedruckten Seite in logischen Zoll abrufen. Mit diesen Werten kann die Anwendung horizontale und vertikale Skalierungsfaktoren erstellen, um den Anteil von Bitmapbildern beizubehalten, wenn Sie auf einem Drucker gezeichnet werden. Weitere Informationen zu Bitmaps und zur bitmapausgabe finden Sie unter [Bitmaps](/windows/desktop/gdi/bitmaps).

 

 
