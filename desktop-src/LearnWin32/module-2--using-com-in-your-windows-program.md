---
title: Verwenden von com in Ihrer Windows-App
description: In Modul 1 dieser Reihe wurde gezeigt, wie ein Fenster erstellt und auf Fenster Meldungen wie WM \_ Paint und WM close reagiert wird \_ . In Modul 2 wird der Component Object Model (com) eingeführt.
ms.assetid: 6e867618-4d02-4c17-b7ea-dc7290507689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c03f16937846c4479a70e16141f1b50bde3efc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726952"
---
# <a name="module-2-using-com-in-your-windows-based-program"></a>Modul 2. Verwenden von com in Ihrem Windows-Based Programm

In [Modul 1](your-first-windows-program.md) dieser Reihe wurde gezeigt, wie ein Fenster erstellt und auf Fenster Meldungen wie [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) und [**WM \_ Close**](/windows/desktop/winmsg/wm-close)reagiert wird. In Modul 2 wird der Component Object Model (com) eingeführt.

COM ist eine Spezifikation zum Erstellen wiederverwendbarer Softwarekomponenten. Viele der Features, die Sie in einem modernen Windows-basierten Programm verwenden werden, basieren auf com, wie z. b. folgendem:

-   Grafiken (Direct2D)
-   Text (DirectWrite)
-   Die Windows-Shell
-   Menüband-Steuerelement
-   UI-Animation

(Einige Technologien in dieser Liste verwenden eine Teilmenge von com und sind daher nicht "Pure" com.)

COM hat den Ruf, schwer zu erlernen. Und es ist richtig, dass das Schreiben eines neuen Software Moduls zur Unterstützung von com schwierig sein kann. Wenn Ihr Programm jedoch nur ein com- *Consumer* ist, kann es sein, dass com leichter zu verstehen ist als erwartet.

Dieses Modul zeigt, wie COM-basierte APIs in Ihrem Programm aufgerufen werden. Außerdem werden einige der Argumente hinter dem Design von com beschrieben. Wenn Sie verstehen, warum com genauso konzipiert ist, können Sie mit dem com-Programm effektiver programmieren. Der zweite Teil des Moduls beschreibt einige empfohlene Programmiermethoden für com.

COM wurde in 1993 eingeführt, um das Verknüpfen und Einbetten von Objekten (OLE) 2,0 zu unterstützen. Manchmal ist es wichtig, dass com und OLE identisch sind. Dies kann ein weiterer Grund dafür sein, dass com schwer zu erlernen ist. OLE 2,0 basiert auf com, aber Sie müssen OLE nicht kennen, um com zu verstehen.

COM ist ein *binärer Standard* und kein Sprachstandard: er definiert die binäre Schnittstelle zwischen einer Anwendung und einer Softwarekomponente. Als binärer Standard ist com sprachneutral, obwohl es sich auf natürliche Weise bestimmten C++-Konstrukten zuordnet. Dieses Modul konzentriert sich auf drei Hauptziele von com:

-   Trennen der Implementierung eines Objekts von der-Schnittstelle.
-   Verwalten der Lebensdauer eines Objekts.
-   Ermitteln der Funktionen eines Objekts zur Laufzeit.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Was ist eine COM-Schnittstelle?](what-is-a-com-interface-.md)
-   [Initialisieren der com-Bibliothek](initializing-the-com-library.md)
-   [Fehler Codes in com](error-codes-in-com.md)
-   [Erstellen eines Objekts in com](creating-an-object-in-com.md)
-   [Beispiel: das Dialog Feld "Öffnen"](example--the-open-dialog-box.md)
-   [Verwalten der Lebensdauer eines Objekts](managing-the-lifetime-of-an-object.md)
-   [Anfordern eines Objekts für eine Schnittstelle](asking-an-object-for-an-interface.md)
-   [Speicher Belegung in com](memory-allocation-in-com.md)
-   [COM-Codierungs Methoden](com-coding-practices.md)
-   [Fehlerbehandlung in com](error-handling-in-com.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erlernen Sie das Program mieren für Windows in C++](learn-to-program-for-windows.md)
</dt> </dl>

 

 