---
title: Übersicht über Windows-Touchgesten
description: In diesem Abschnitt werden die verschiedenen von Windows toucheingaben unterstützten Gesten beschrieben.
ms.assetid: b2fa11a7-9abb-4149-96e3-e8c663c29d4a
keywords:
- Windows-Toucheingabe, Gesten
- Gesten, Informationen
- Windows-Fingereingabe, Legacy Unterstützung
- Gesten, Legacy Unterstützung
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 2290477aa8b26e937fe6d5f300ed1fea32872f5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039280"
---
# <a name="windows-touch-gestures-overview"></a>Übersicht über Windows-Touchgesten

In diesem Abschnitt werden die verschiedenen von Windows toucheingaben unterstützten Gesten beschrieben.

## <a name="gestures-overview"></a>Gesten Übersicht

Windows-Toucheingabe ermöglicht mehrere Gesten, die einzelne und mehrere Kontakte unterstützen. In der folgenden Abbildung werden die verschiedenen Gesten veranschaulicht, die in Windows 7 unterstützt werden.

![Abbildung mit den Gesten, die Windows-Toucheingabe in Windows 7 unterstützt](images/gestures.png)

> [!Note]  
> Einige erkentungen sind zuverlässiger bei der Interpretation von Gesten mit mehreren Kontakten, wenn sich die Kontakte voneinander unterscheiden.

## <a name="legacy-support"></a>Legacy Unterstützung

Für Legacy Unterstützung ordnet der standardmäßige Gesten Handler einigen Gesten Windows-Meldungen zu, die in früheren Versionen von Windows verwendet wurden. In der folgenden Tabelle wird beschrieben, wie Gesten Legacy Nachrichten zugeordnet werden.

| Geste        | BESCHREIBUNG  | Meldung (en) generiert              |
|----------------|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| Schwenken            | Die Schwenkbewegung wird mit dem Mausrad dargestellt.                  | **WM_VSCROLL**<br/> **WM_HSCROLL**<br/>       |
| Halten Sie | Die Bewegung "drücken und halten" wird mit der rechten Maustaste angezeigt.     | **WM_RBUTTONDOWN**<br/> **WM_RBUTTONUP**<br/> |
| Zoom           | Die Zoom Bewegung löst Meldungen aus, die dem Drücken der STRG-Taste ähneln, und dreht das Mausrad, um einen Bildlauf durchzuführen. | **WM_MOUSEWHEEL** mit **MK_CONTROL** in *LPARAM* festgelegt |

## <a name="interpreting-windows-touch-gestures"></a>Interpretieren von Windows-Touchgesten

Windows-Touchgesten können von Anwendungsentwicklern interpretiert werden, indem die [**WM_GESTURE**](wm-gesture.md) Nachricht von der WndProc-Funktion einer Anwendung verarbeitet wird. Nachdem Sie diese Meldung verarbeitet haben, können Sie eine [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) -Struktur abrufen, in der die Geste beschrieben wird. Die **GESTUREINFO** -Struktur verfügt über sortierte Informationen, die von der Art der Bewegung abhängig sind.

Die [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) -Struktur wird durch Übergeben des Handles an die Gesten Informationsstruktur an die [**getgestureinfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) -Funktion abgerufen.

Die folgenden Flags geben die verschiedenen Zustände der Gesten an und werden in *dwFlags* gespeichert. 

| Name        | Wert      | BESCHREIBUNG                      |
|-------------|------------|----------------------------------|
| GF_BEGIN   | 0x00000001 | Eine Geste wird gestartet.           |
| GF_INERTIA | 0x00000002 | Eine Geste hat Trägheit ausgelöst. |
| GF_END     | 0x00000004 | Eine Geste ist abgeschlossen.          |

> [!Note]  
> Die meisten Anwendungen sollten die **GID_BEGIN** und **GID_END** ignorieren und an [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca)übergeben. Diese Nachrichten werden vom Standard Gesten Handler verwendet. Das Anwendungsverhalten ist nicht definiert, wenn die **GID_BEGIN** -und **GID_END** Nachrichten von einer Drittanbieter Anwendung genutzt werden.

In der folgenden Tabelle sind die verschiedenen Bezeichner für Gesten angegeben. 

| Name              | Wert | BESCHREIBUNG                 |
|-------------------|-------|-----------------------------|
| GID_BEGIN        | 1     | Eine Geste wird gestartet.      |
| GID_END          | 2     | Eine Geste wird beendet.        |
| GID_ZOOM         | 3     | Die Zoom Bewegung.           |
| GID_PAN          | 4     | Die Schwenkbewegung.            |
| GID_ROTATE       | 5     | Die Drehungs Bewegung.       |
| GID_TWOFINGERTAP | 6     | Die zwei-Finger-Tap-Geste. |
| GID_PRESSANDTAP  | 7     | Die Bewegung und tippen.  |

> [!Note]  
> Die **GID_PAN** Geste verfügt über eine integrierte Trägheit. Am Ende einer schwenken-Geste werden vom Betriebssystem weitere Meldungen der Schwenkbewegung erstellt.

Die [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) -Strukturmember **ptsLocation** und **ullarguments** geben einen Punkt (unter Verwendung der **Points** -Struktur) und zusätzliche Informationen zu Gesten abhängig von der Bewegung an. In der folgenden Tabelle sind die Werte aufgeführt, die den einzelnen Gesten Typen zugeordnet sind.

| Gesten-ID            | *ullarguments*                  | *ptsLocation*                       |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| **GID_ZOOM**         | Gibt den Abstand zwischen den beiden Punkten an.            | Gibt den Mittelpunkt des Zoom Punkts an.   |
| **GID_PAN**          | Gibt den Abstand zwischen den beiden Punkten an.            | Gibt die aktuelle Position der schwenken an.                    |
| **GID_ROTATE**       | Gibt den Drehwinkel an, wenn das **GF_BEGIN** -Flag festgelegt ist. Andernfalls ist dies die Winkel Änderung, seit die Drehung gestartet wurde. Dies wird signiert, um die Richtung der Drehung anzugeben. Verwenden Sie die Makros [**GID_ROTATE_ANGLE_FROM_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) und [**GID_ROTATE_ANGLE_TO_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) , um den Winkelwert zu erhalten und festzulegen. | Dies gibt den Mittelpunkt der Drehung an, bei dem es sich um den stationären Punkt handelt, um den das Zielobjekt gedreht wird. |
| **GID_TWOFINGERTAP** | Gibt den Abstand zwischen den beiden Fingern an.           | Gibt die Mitte der beiden Finger an.                      |
| **GID_PRESSANDTAP**  | Gibt das Delta zwischen dem ersten und dem zweiten Finger an. Dieser Wert wird in einer **Punkt** Struktur in den unteren 32 Bits des *ullarguments* -Members gespeichert.                        | Gibt die Position an, an der der erste Finger angezeigt wird.   |

## <a name="related-topics"></a>Zugehörige Themen

[Windows-Touchgesten](guide-multi-touch-gestures.md)