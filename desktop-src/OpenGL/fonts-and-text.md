---
title: Schriftarten und Text (OpenGL)
description: Die Microsoft-Implementierung von OpenGL in Windows unterstützt GDI-Grafiken in einem Single-Buffered OpenGL-Fenster.
ms.assetid: 25a45e1a-6c1e-416b-8993-daeefc1100f3
keywords:
- OpenGL unter Windows, Schriftarten
- OpenGL unter Windows, Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fba4ffe996bd88a6285f615ddacb31e57fc311
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391415"
---
# <a name="fonts-and-text-opengl"></a>Schriftarten und Text (OpenGL)

Die Microsoft-Implementierung von OpenGL in Windows unterstützt GDI-Grafiken in einem Single-Buffered OpenGL-Fenster. GDI-Grafiken in einem doppelt gepufferten OpenGL-Fenster werden nicht unterstützt. Daher können Sie nur die Standardfunktionen für GDI-Schriftart und-Text aufrufen, um Text in einem Single-Buffered OpenGL-Fenster zu zeichnen. Sie können diese Funktionen nicht aufrufen, um Text in einem doppelt gepufferten OpenGL-Fenster zu zeichnen.

Es gibt eine Problem Umgehung für diese Einschränkung bei Text in doppelt gepufferten Fenstern: Build OpenGL-Anzeigelisten für Bitmap-Bilder von Zeichen und führen dann diese anzeigen Listen aus, um Zeichen zu zeichnen. Dieser Prozess umfasst drei Hauptschritte:

1.  Wählen Sie eine Schriftart für einen Gerätekontext aus, und legen Sie die Eigenschaften der Schriftart wie gewünscht fest.
2.  Erstellen Sie eine Reihe von Bitmap-Anzeigelisten basierend auf den Symbolen in der Schriftart des Geräte Kontexts, einer Anzeigeliste für jedes Symbol, das von der Anwendung gezeichnet wird.
3.  Zeichnen Sie jedes Symbol mithilfe dieser Bitmap-Anzeigelisten in einer Zeichenfolge.

Um die Anzeigelisten zu erstellen, rufen Sie die Funktionen [**wgluseefontbitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) und [**wglusetfontgliederungen**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) auf. Rufen Sie zum Zeichnen von Zeichen in einer Zeichenfolge mithilfe dieser Anzeigelisten die " [**glcalllists**](glcalllists.md)" auf.

Zum Erstellen von Anwendungen, die leicht lokalisiert werden können und die Ressourcen sparsam verwenden, müssen die Erstellung und Speicherung dieser Symbol Listen der Symbol Anzeige sorgfältig verwaltet werden. Im Gegensatz zu Englisch verfügen viele Sprachen über Alphabete, deren Zeichen Codes über einen relativ großen Satz von Werten reichen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schriftart-und Text Funktionen](font-and-text-functions.md)
</dt> </dl>

 

 




