---
description: Mit einigen geringfügigen Anpassungen an Ihrem Code können Sie Windows GDI+ Ausgabe an einen Drucker anstatt an einen Bildschirm senden.
ms.assetid: be6286e9-d125-40ad-b33e-b4e734ac2709
title: Drucken (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f5807c976ef3224bc4b66afc0bb8637d79d725f12cbdebd3199d9710ae529a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885081"
---
# <a name="printing-gdi"></a>Drucken (GDI+)

Mit einigen geringfügigen Anpassungen an Ihrem Code können Sie Windows GDI+ Ausgabe an einen Drucker anstatt an einen Bildschirm senden. Um auf einem Drucker zu zeichnen, erhalten Sie ein Gerätekontexthand handle für den Drucker, und übergeben Sie dieses Handle an einen [**Grafikkonstruktor.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Platzieren Sie ihre GDI+ Zeichenbefehle zwischen Aufrufen von [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) und [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc).

In den folgenden Themen wird das Senden GDI+ Ausgabe an Drucker ausführlicher behandelt:

-   [Senden von GDI+-Ausgabe an einen Drucker](-gdiplus-sending-gdi-output-to-a-printer-use.md)
-   [Anzeigen eines Druckdialogfelds](-gdiplus-displaying-a-print-dialog-box-use.md)
-   [Optimieren der Druckausgabe durch Bereitstellen eines Druckerhandles](-gdiplus-optimizing-printing-by-providing-a-printer-handle-use.md)

 

 



