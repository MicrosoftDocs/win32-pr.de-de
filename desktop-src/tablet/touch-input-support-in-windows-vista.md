---
description: Ab Windows Vista bietet die Tablet PC-Technologie Unterstützung für Fingereingabe auf Tablet PCs mit Touchscreen-fähigen Digitalisierern. Diese Unterstützung umfasst eine erweiterte Benutzeroberfläche, um die Ziel-und Befehlsfenster zu unterstützen, wenn Sie einen Finger für die Eingabe verwenden.
ms.assetid: 63f1d71f-03d8-4d83-a174-e3dc7c57bad0
title: Unterstützung für Berührungs Eingaben in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b623630c93c33b846ab1bb491fc56fe46dfe825
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348686"
---
# <a name="touch-input-support-in-windows-vista"></a>Unterstützung für Berührungs Eingaben in Windows Vista

Ab Windows Vista bietet die Tablet PC-Technologie Unterstützung für Fingereingabe auf Tablet PCs mit Touchscreen-fähigen Digitalisierern. Diese Unterstützung umfasst eine erweiterte Benutzeroberfläche, um die Ziel-und Befehlsfenster zu unterstützen, wenn Sie einen Finger für die Eingabe verwenden.

## <a name="touch-digitizer-support"></a>Unterstützung für Fingerabdruck Unterstützung

### <a name="pen-and-touch-input-not-exclusive"></a>Stift-und Berührungs Eingabe nicht exklusiv

Gehen Sie nicht davon aus, dass sich Stift-und Berührungs Eingaben in den Anwendungen [**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)und [**RealTimeStylus**](realtimestylus-class.md) gegenseitig ausschließen.

Wenn das System in Windows Vista einen Stift erkennt, werden Berührungs Eingaben ignoriert. Das heißt, der Fingerabdruck wird beendet, und der Stift Strich beginnt. Da sich dies möglicherweise in der Zukunft ändern kann, sollte der Code nicht annehmen, dass der Stift und die Berührungs Eingabe sich gegenseitig ausschließen.

### <a name="other-mouse-message-sources"></a>Andere Maus Nachrichtenquellen

Es gibt auch andere Quellen für Maus Meldungen, auch wenn der Benutzer nur mit Finger oder Pen interagiert. Zu den Quellen gehören Touchpads sowie eine Bewegung, mit der eine Anwendung hinter einem geschichteten Fenster erkennen kann, dass der Mauszeiger über der Anwendung bewegt wird.

### <a name="enabling-and-disabling-the-touch-input-user-interface"></a>Aktivieren und Deaktivieren der Benutzeroberfläche für Berührungs Eingaben

Abhängig von den Anforderungen Ihrer Anwendung möchten Sie möglicherweise die Benutzeroberfläche für die Berührungs Eingabe aktivieren oder deaktivieren. Um dies zu erreichen, fangen Sie die Meldungen des Betriebssystem Fensters in einer Fenster Prozedur ab, und ändern Sie die Windows-Meldung. Überschreiben Sie [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) in Ihrer Anwendung, um diese Meldungen abzufangen. Der folgende C \# -Pseudo Code zeigt, wie Sie die Benutzeroberfläche für die Berührungs Eingabe aktivieren und deaktivieren. Der Code zeigt auch die Verwendung desselben Verfahrens zum Deaktivieren der Press-und-Halt-Geste. Diese Methode kann auch zum Deaktivieren des Tablettstifts verwendet werden.


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

[Windows-Fingereingabe](../wintouch/windows-touch-portal.md)
</dt> </dl>

 

 
