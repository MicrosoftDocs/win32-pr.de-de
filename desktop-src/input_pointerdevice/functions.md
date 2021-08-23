---
description: Die Themen in diesem Abschnitt enthalten die Referenzspezifikationen für Pointer Device Input Stack-Funktionen.
ms.assetid: 44942954-3EA6-4C33-8CF1-E8BF72A914CB
title: Funktionen (Zeigergeräteeingabestapel)
ms.topic: article
ms.date: 02/05/2020
ms.openlocfilehash: 5101847d78f396edcb317986ab3d95d578dabdfe12197531787115f49c9a69a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611740"
---
# <a name="pointer-device-input-stack-functions"></a>Zeigergeräteeingabestapelfunktionen

Die Themen in diesem Abschnitt enthalten die Referenzspezifikationen für [Pointer Device Input Stack-Funktionen.](pointer-device-stack-portal.md)

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|---|---|
| [**CreateSyntheticPointerDevice**](/windows/win32/api/winuser/nf-winuser-createsyntheticpointerdevice)<br/> | Konfiguriert das Zeigerinjektionsgerät für die aufrufende Anwendung und initialisiert die maximale Anzahl gleichzeitiger Zeiger, die die App einfügen kann.<br/> |
| [**DestroySyntheticPointerDevice**](/windows/win32/api/winuser/nf-winuser-destroysyntheticpointerdevice)<br/> | Zerstört das angegebene Zeigerinjektionsgerät.<br/> |
| [**GetPointerDevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice)<br/> | Ruft Informationen zum Zeigergerät ab.<br/> |
| [**GetPointerDeviceCursors**](/windows/win32/api/winuser/nf-winuser-getpointerdevicecursors)<br/> | Ruft die Cursor-IDs ab, die den Cursorn zugeordnet sind, die einem Zeigergerät zugeordnet sind.<br/> |
| [**GetPointerDeviceProperties**](/windows/win32/api/winuser/nf-winuser-getpointerdeviceproperties)<br/> | Ruft Geräteeigenschaften ab, die nicht in der [**POINTER \_ DEVICE \_ INFO-Struktur**](/previous-versions/windows/desktop/api) enthalten sind. <br/> |
| [**GetPointerDeviceRects**](/windows/win32/api/winuser/nf-winuser-getpointerdevicerects)<br/> | Ruft den x- und y-Bereich für das Zeigergerät (in himetric) und den x- und y-Bereich (aktuelle Auflösung) für die Anzeige ab, der das Zeigergerät zugeordnet ist. <br/> |
| [**GetPointerDevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices)<br/> | Ruft Informationen zu den Zeigergeräten ab, die an das System angefügt sind.<br/> |
| [**GetRawPointerDeviceData**](/windows/win32/api/winuser/nf-winuser-getrawpointerdevicedata)<br/> | Ruft die rohen Eingabedaten vom Zeigergerät ab. <br/> |
| [**InjectSyntheticPointerInput**](/windows/win32/api/winuser/nf-winuser-injectsyntheticpointerinput)<br/> | Simuliert die Zeigereingabe (Stift oder Toucheingabe).<br/> |
| [**RegisterPointerDeviceNotifications**](/windows/win32/api/winuser/nf-winuser-registerpointerdevicenotifications)<br/> | Registriert ein Fenster, um die [**WM_POINTERDEVICECHANGE,**](../inputmsg/wm-pointerdevicechange.md) [**WM_POINTERDEVICEINRANGE**](../inputmsg/wm-pointerdeviceinrange.md)und [**WM_POINTERDEVICEOUTOFRANGE**](../inputmsg/wm-pointerdeviceoutofrange.md) Zeigergerätebenachrichtigungen zu verarbeiten.<br/> |

## <a name="related-topics"></a>Zugehörige Themen

[Zeigergeräteeingabestapelreferenz](unified-input-stack-reference.md)
