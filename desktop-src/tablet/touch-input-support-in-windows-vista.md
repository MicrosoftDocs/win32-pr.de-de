---
description: Ab Windows Vista bietet Tablet PC Technology Unterstützung für Toucheingaben auf Tablet-PCs mit touchfähigen Digitizern. Diese Unterstützung umfasst eine erweiterte Benutzeroberfläche, die bei der Ausrichtung und Befehlssteuerung Windows beim Verwenden eines Fingers für die Eingabe hilft.
ms.assetid: 63f1d71f-03d8-4d83-a174-e3dc7c57bad0
title: Toucheingabeunterstützung in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81b22130a7c731d49556db263d5c1d5565ef51aa103925969b35c98548a32d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119335070"
---
# <a name="touch-input-support-in-windows-vista"></a>Toucheingabeunterstützung in Windows Vista

Ab Windows Vista bietet Tablet PC Technology Unterstützung für Toucheingaben auf Tablet-PCs mit touchfähigen Digitizern. Diese Unterstützung umfasst eine erweiterte Benutzeroberfläche, die bei der Ausrichtung und Befehlssteuerung Windows beim Verwenden eines Fingers für die Eingabe hilft.

## <a name="touch-digitizer-support"></a>Touch Digitizer-Unterstützung

### <a name="pen-and-touch-input-not-exclusive"></a>Stift und Toucheingabe nicht exklusiv

Gehen Sie nicht davon aus, dass Stift- und Toucheingaben sich in [**InkCollector-,**](inkcollector-class.md) [**InkOverlay-**](inkoverlay-class.md)und [**RealTimeStylus-Anwendungen**](realtimestylus-class.md) gegenseitig ausschließen.

Wenn das System in Windows Vista einen Stift erkennt, ignoriert es Toucheingaben. Das heißt, der Touchstrich endet, und der Stiftstrich beginnt. Da sich dies in Zukunft möglicherweise ändern könnte, sollte Ihr Code nicht davon ausgehen, dass Stift- und Toucheingaben sich gegenseitig ausschließen.

### <a name="other-mouse-message-sources"></a>Andere Mausnachrichtenquellen

Es gibt auch andere Quellen für Mausnachrichten, auch wenn der Benutzer nur mit dem Finger oder Stift interagiert. Zu den Quellen gehören Touchpads sowie Bewegung, mit der eine Anwendung hinter einem mehrstufigen Fenster darauf achten kann, dass sich die Maus über der Anwendung bewegt.

### <a name="enabling-and-disabling-the-touch-input-user-interface"></a>Aktivieren und Deaktivieren der Toucheingabe-Benutzeroberfläche

Abhängig von den Anforderungen Ihrer Anwendung können Sie die Toucheingabe-Benutzeroberfläche aktivieren oder deaktivieren. Um dies zu erreichen, fangen Sie Betriebssystemfenstermeldungen in einer Fensterprozedur ab, und ändern Sie die Windows Meldung. Überschreiben Sie [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) in Ihrer Anwendung, um diese Nachrichten abzufangen. Der folgende \# C-Pseudocode zeigt, wie die Benutzeroberfläche für die Toucheingabe aktiviert und deaktiviert wird. Der Code zeigt auch die Verwendung der gleichen Technik zum Deaktivieren der Gedrückt halten-Geste. Diese Methode funktioniert auch zum Deaktivieren des Stifts.


```C++
const int WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS = 716;

const uint SYSTEM_GESTURE_STATUS_NOHOLD           = 0x00000001;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON  = 0x00000100;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF = 0x00000200;

protected override void WndProc(ref Message msg)
{
    switch (msg.Msg)
    {
        case WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS:
        {
            uint result = 0;
            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_NOHOLD;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF;
            }

            msg.Result = (IntPtr)result;
        }
        break;

        default:
            base.WndProc(ref msg);
            break;
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Touch](../wintouch/windows-touch-portal.md)
</dt> </dl>

 

 
