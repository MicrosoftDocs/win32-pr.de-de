---
title: Verwenden von COM in Ihrer Windows-App
description: In Modul 1 dieser Reihe wurde gezeigt, wie Sie ein Fenster erstellen und auf Fenstermeldungen wie WM \_ PAINT und WM CLOSE \_ reagieren. In Modul 2 wird die Component Object Model (COM) vorgestellt.
ms.assetid: 6e867618-4d02-4c17-b7ea-dc7290507689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2180d47bd0dd12c0184a2f9241ec5656c7fe711150e1d5163ca2fec9e0b28fd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068030"
---
# <a name="module-2-using-com-in-your-windows-based-program"></a>Modul 2. Verwenden von COM in Ihrem Windows-Based-Programm

[In Modul 1](your-first-windows-program.md) dieser Reihe wurde gezeigt, wie Sie ein Fenster erstellen und auf Fenstermeldungen wie [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint) und [**WM \_ CLOSE**](/windows/desktop/winmsg/wm-close)reagieren. In Modul 2 wird die Component Object Model (COM) vorgestellt.

COM ist eine Spezifikation zum Erstellen wiederverwendbarer Softwarekomponenten. Viele der Features, die Sie in einem modernen Windows-basierten Programm verwenden, basieren auf COM, z. B.:

-   Grafiken (Direct2D)
-   Text (DirectWrite)
-   Die Windows Shell
-   Das Menüband-Steuerelement
-   Benutzeroberflächenanimation

(Einige Technologien in dieser Liste verwenden eine Teilmenge von COM und sind daher nicht "reines" COM.)

COM hat den Ruf, schwierig zu lernen. Und es ist richtig, dass das Schreiben eines neuen Softwaremoduls zur Unterstützung von COM schwierig sein kann. Wenn Ihr Programm jedoch ausschließlich ein *Com-Consumer* ist, stellen Sie möglicherweise fest, dass COM einfacher zu verstehen ist, als Sie erwarten.

In diesem Modul wird gezeigt, wie COM-basierte APIs in Ihrem Programm aufgerufen werden. Außerdem werden einige der Gründe für den Entwurf von COM beschrieben. Wenn Sie verstehen, warum COM so entworfen wurde, wie es ist, können Sie damit effektiver programmieren. Im zweiten Teil des Moduls werden einige empfohlene Programmiermethoden für COM beschrieben.

COM wurde 1993 eingeführt, um Die Objektverknüpfung und -einbettung (OLE) 2.0 zu unterstützen. Manchmal denken Benutzer, dass COM und OLE dasselbe sind. Dies kann ein weiterer Grund für die Wahrnehmung sein, dass COM schwer zu erlernen ist. OLE 2.0 basiert auf COM, aber Sie müssen OLE nicht kennen, um COM zu verstehen.

COM ist ein *binärer Standard,* kein Sprachstandard: Es definiert die binäre Schnittstelle zwischen einer Anwendung und einer Softwarekomponente. Als binärer Standard ist COM sprachneutral, obwohl es natürlich bestimmten C++-Konstrukten zugeordnet ist. Dieses Modul konzentriert sich auf drei wichtige Ziele von COM:

-   Trennen der Implementierung eines Objekts von seiner Schnittstelle.
-   Verwalten der Lebensdauer eines Objekts.
-   Ermitteln der Funktionen eines Objekts zur Laufzeit.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Was ist eine COM-Schnittstelle?](what-is-a-com-interface-.md)
-   [Initialisieren der COM-Bibliothek](initializing-the-com-library.md)
-   [Fehlercodes in COM](error-codes-in-com.md)
-   [Erstellen eines Objekts in COM](creating-an-object-in-com.md)
-   [Beispiel: Das Dialogfeld "Öffnen"](example--the-open-dialog-box.md)
-   [Verwalten der Lebensdauer eines Objekts](managing-the-lifetime-of-an-object.md)
-   [Fragen eines Objekts nach einer Schnittstelle](asking-an-object-for-an-interface.md)
-   [Speicherbelegung in COM](memory-allocation-in-com.md)
-   [COM-Codierungsmethoden](com-coding-practices.md)
-   [Fehlerbehandlung in COM](error-handling-in-com.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieren für Windows in C++](learn-to-program-for-windows.md)
</dt> </dl>

 

 