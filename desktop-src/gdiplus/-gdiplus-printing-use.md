---
description: Mit einigen geringfügigen Anpassungen an Ihrem Code können Sie die Windows GDI+-Ausgabe an einen Drucker anstatt an einen Bildschirm senden.
ms.assetid: be6286e9-d125-40ad-b33e-b4e734ac2709
title: Drucken (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3b60010bcb63c553a96c5d70826f3fe0d3d4aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978953"
---
# <a name="printing-gdi"></a>Drucken (GDI+)

Mit einigen geringfügigen Anpassungen an Ihrem Code können Sie die Windows GDI+-Ausgabe an einen Drucker anstatt an einen Bildschirm senden. Um auf einem Drucker zu zeichnen, rufen Sie ein Gerätekontext Handle für den Drucker ab, und übergeben [](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Sie dieses Handle an einen grafikkonstruktor. Platzieren Sie die GDI+-Zeichnungs Befehle zwischen Aufrufen von [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) und [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc).

In den folgenden Themen wird das Senden der GDI+-Ausgabe an Drucker ausführlicher behandelt:

-   [Senden von GDI+-Ausgabe an einen Drucker](-gdiplus-sending-gdi-output-to-a-printer-use.md)
-   [Anzeigen eines Druck Dialogfelds](-gdiplus-displaying-a-print-dialog-box-use.md)
-   [Optimieren der Druckausgabe durch Bereitstellen eines Druckerhandles](-gdiplus-optimizing-printing-by-providing-a-printer-handle-use.md)

 

 



