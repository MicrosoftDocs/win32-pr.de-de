---
title: Windows Übersicht über Touchgesten
description: In diesem Abschnitt werden die verschiedenen Gesten beschrieben, die von Windows Touch unterstützt werden.
ms.assetid: b2fa11a7-9abb-4149-96e3-e8c663c29d4a
keywords:
- Windows Toucheingabe, Gesten
- Gesten, Informationen
- Windows Toucheingabe, Legacyunterstützung
- Gesten, Legacyunterstützung
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: f2a0f6229afe4ad0d894a1cc2d40489f5d8371de3d7c42cefdccde619119df75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587254"
---
# <a name="windows-touch-gestures-overview"></a>Windows Übersicht über Touchgesten

In diesem Abschnitt werden die verschiedenen Gesten beschrieben, die von Windows Touch unterstützt werden.

## <a name="gestures-overview"></a>Übersicht über Gesten

Windows Touch ermöglicht mehrere Gesten, die einzelne und mehrere Kontakte unterstützen. Die folgende Abbildung veranschaulicht die verschiedenen Gesten, die in Windows 7 unterstützt werden.

![Abbildung der Gesten, die die Windows-Toucheingabe in Windows 7 unterstützt](images/gestures.png)

> [!Note]  
> Einige Erkennungen sind zuverlässiger beim Interpretieren von Gesten mit mehreren Kontakten, wenn die Kontakte weiter voneinander entfernt sind.

## <a name="legacy-support"></a>Legacyunterstützung

Für die Legacyunterstützung ordnet der Standardgestenhandler einige Gesten Windows Nachrichten zu, die in früheren Versionen von Windows verwendet wurden. In der folgenden Tabelle wird beschrieben, wie Gesten Legacynachrichten zugeordnet werden.

| Geste        | BESCHREIBUNG  | Generierte Nachrichten              |
|----------------|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| Schwenken            | Die Schwenkgeste wird mithilfe des Scrollrads zugeordnet.                  | **WM_VSCROLL**<br/> **WM_HSCROLL**<br/>       |
| Drücken und halten | Die Geste gedrückt halten wird zugeordnet, um mit der rechten Maustaste zu klicken.     | **WM_RBUTTONDOWN**<br/> **WM_RBUTTONUP**<br/> |
| Zoom           | Die Zoomgeste löst Meldungen aus, die dem Halten der STRG-TASTE und dem Drehen des Mausrads zum Scrollen ähneln. | **WM_MOUSEWHEEL** mit **festgelegter MK_CONTROL** in *der lParam* |

## <a name="interpreting-windows-touch-gestures"></a>Interpretieren von Windows Touchgesten

Windows Touchgesten können von Anwendungsentwicklern interpretiert werden, indem die [**WM_GESTURE**](wm-gesture.md) Nachricht aus der WndProc-Funktion einer Anwendung verarbeitet wird. Nachdem Sie diese Meldung verarbeitet haben, können Sie eine [**GESTUREINFO-Struktur**](/windows/win32/api/winuser/ns-winuser-gestureinfo) abrufen, die die Geste beschreibt. Die **GESTUREINFO-Struktur** weist verschiedene Informationen auf, die vom Typ der Geste abhängen.

Die [**GESTUREINFO-Struktur**](/windows/win32/api/winuser/ns-winuser-gestureinfo) wird abgerufen, indem das Handle an die Gesteninformationsstruktur an die [**GetGestureInfo-Funktion**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) übergeben wird.

Die folgenden Flags geben die verschiedenen Zustände der Gesten an und werden in *dwFlags* gespeichert. 

| Name        | Wert      | Beschreibung                      |
|-------------|------------|----------------------------------|
| GF_BEGIN   | 0x00000001 | Eine Geste wird gestartet.           |
| GF_INERTIA | 0x00000002 | Eine Geste hat Trägheit ausgelöst. |
| GF_END     | 0x00000004 | Eine Geste wurde abgeschlossen.          |

> [!Note]  
> Die meisten Anwendungen sollten die **GID_BEGIN** und **GID_END** ignorieren und an [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)übergeben. Diese Meldungen werden vom Standardgestenhandler verwendet. Das Anwendungsverhalten ist nicht definiert, wenn die **GID_BEGIN** und **GID_END** Nachrichten von einer Drittanbieteranwendung genutzt werden.

Die folgende Tabelle gibt die verschiedenen Bezeichner für Gesten an. 

| Name              | Wert | Beschreibung                 |
|-------------------|-------|-----------------------------|
| GID_BEGIN        | 1     | Eine Geste wird gestartet.      |
| GID_END          | 2     | Eine Geste endet.        |
| GID_ZOOM         | 3     | Die Zoomgeste.           |
| GID_PAN          | 4     | Die Schwenkbewegung.            |
| GID_ROTATE       | 5     | Die Drehbewegung.       |
| GID_TWOFINGERTAP | 6     | Die Tippbewegung mit zwei Fingern. |
| GID_PRESSANDTAP  | 7     | Die Geste zum Drücken und Tippen.  |

> [!Note]  
> Die **GID_PAN** Geste weist integrierte Trägheit auf. Am Ende einer Schwenkbewegung werden zusätzliche Schwenkgestenmeldungen vom Betriebssystem erstellt.

Die [**GESTINFO-Strukturmember**](/windows/win32/api/winuser/ns-winuser-gestureinfo) **ptsLocation** und **ullArguments** geben je nach Geste einen Punkt (mithilfe der **POINTS-Struktur)** und zusätzliche Informationen zu Gesten an. In der folgenden Tabelle sind die Werte aufgeführt, die den einzelnen Gestentypen zugeordnet sind.

| Gesten-ID            | *ullArguments*                  | *ptsLocation*                       |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| **GID_ZOOM**         | Gibt den Abstand zwischen den beiden Punkten an.            | Gibt die Mitte des Zooms an.   |
| **GID_PAN**          | Gibt den Abstand zwischen den beiden Punkten an.            | Gibt die aktuelle Position des Schwenkens an.                    |
| **GID_ROTATE**       | Gibt den Drehwinkel an, wenn das **flag GF_BEGIN** festgelegt ist. Andernfalls ist dies die Winkeländerung seit Beginn der Drehung. Dies wird signiert, um die Drehrichtung anzugeben. Verwenden Sie die [**Makros GID_ROTATE_ANGLE_FROM_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) und [**GID_ROTATE_ANGLE_TO_ARGUMENT,**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) um den Winkelwert abzurufen und festzulegen. | Dies gibt den Mittelpunkt der Drehung an, bei dem es sich um den stationären Punkt handelt, um den das Zielobjekt gedreht wird. |
| **GID_TWOFINGERTAP** | Gibt den Abstand zwischen den beiden Fingern an.           | Gibt die Mitte der beiden Finger an.                      |
| **GID_PRESSANDTAP**  | Gibt das Delta zwischen dem ersten und dem zweiten Finger an. Dieser Wert wird in einer **POINT-Struktur** in den unteren 32 Bits des *ullArguments-Members* gespeichert.                        | Gibt die Position an, an der der erste Finger herunterkommt.   |

## <a name="related-topics"></a>Zugehörige Themen

[Windows Touchgesten](guide-multi-touch-gestures.md)