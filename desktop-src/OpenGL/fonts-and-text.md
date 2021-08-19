---
title: Schriftarten und Text (OpenGL)
description: Die Microsoft-Implementierung von OpenGL in Windows unterstützt GDI-Grafiken in einem einzelnen gepufferten OpenGL-Fenster.
ms.assetid: 25a45e1a-6c1e-416b-8993-daeefc1100f3
keywords:
- OpenGL für Windows,Schriftarten
- OpenGL auf Windows,Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966298b6a8d8e5584e761570205a5d3e7be58be3a8dfeb488db2a6f523fc9a25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082430"
---
# <a name="fonts-and-text-opengl"></a>Schriftarten und Text (OpenGL)

Die Microsoft-Implementierung von OpenGL in Windows unterstützt GDI-Grafiken in einem einzelnen gepufferten OpenGL-Fenster. GDI-Grafiken in einem doppelt gepufferten OpenGL-Fenster werden nicht unterstützt. Daher können Sie nur die GDI-Standardschriftarten und -textfunktionen aufrufen, um Text in einem einzelnen gepufferten OpenGL-Fenster zu zeichnen. Sie können diese Funktionen nicht aufrufen, um Text in einem doppelt gepufferten OpenGL-Fenster zu zeichnen.

Es gibt eine Problemumgehung für diese Einschränkung für Text in doppelt gepufferten Fenstern: Erstellen Sie OpenGL-Anzeigelisten für Bitmapbilder von Zeichen, und führen Sie diese Anzeigelisten dann aus, um Zeichen zu zeichnen. Dieser Prozess besteht aus drei Hauptschritten:

1.  Wählen Sie eine Schriftart für einen Gerätekontext aus, und legen Sie die Eigenschaften der Schriftart wie gewünscht fest.
2.  Erstellen Sie eine Reihe von Bitmapanzeigelisten basierend auf den Symbolen in der Schriftart des Gerätekontexts, eine Anzeigeliste für jedes Symbol, das von der Anwendung gezeichnet wird.
3.  Zeichnen Sie jedes Symbol in einer Zeichenfolge mithilfe dieser Bitmapanzeigelisten.

Um die Anzeigelisten zu erstellen, rufen Sie die Funktionen [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) und [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) auf. Um Zeichen in einer Zeichenfolge mithilfe dieser Anzeigelisten zu zeichnen, rufen Sie [**glCallLists auf.**](glcalllists.md)

Um Anwendungen zu erstellen, die einfach zu lokalisieren sind und ressourcensparend verwendet werden, müssen die Erstellung und Speicherung dieser Symbolbildanzeigelisten sorgfältig verwaltet werden. Viele Sprachen verfügen im Gegensatz zu Englisch über Alphabete, deren Zeichencodes über einen relativ großen Satz von Werten liegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schriftart- und Textfunktionen](font-and-text-functions.md)
</dt> </dl>

 

 




