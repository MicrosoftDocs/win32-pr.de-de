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
# <a name="touch-input-support-in-windows-vista"></a><span data-ttu-id="1c1a1-104">Unterstützung für Berührungs Eingaben in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c1a1-104">Touch Input Support in Windows Vista</span></span>

<span data-ttu-id="1c1a1-105">Ab Windows Vista bietet die Tablet PC-Technologie Unterstützung für Fingereingabe auf Tablet PCs mit Touchscreen-fähigen Digitalisierern.</span><span class="sxs-lookup"><span data-stu-id="1c1a1-105">Starting with Windows Vista, Tablet PC Technology has support for touch input on Tablet PC's with touch capable digitizers.</span></span> <span data-ttu-id="1c1a1-106">Diese Unterstützung umfasst eine erweiterte Benutzeroberfläche, um die Ziel-und Befehlsfenster zu unterstützen, wenn Sie einen Finger für die Eingabe verwenden.</span><span class="sxs-lookup"><span data-stu-id="1c1a1-106">This support includes an enhanced user interface to aid in targeting and commanding Windows when using a finger for input.</span></span>

## <a name="touch-digitizer-support"></a><span data-ttu-id="1c1a1-107">Unterstützung für Fingerabdruck Unterstützung</span><span class="sxs-lookup"><span data-stu-id="1c1a1-107">Touch Digitizer Support</span></span>

### <a name="pen-and-touch-input-not-exclusive"></a><span data-ttu-id="1c1a1-108">Stift-und Berührungs Eingabe nicht exklusiv</span><span class="sxs-lookup"><span data-stu-id="1c1a1-108">Pen and Touch Input Not Exclusive</span></span>

<span data-ttu-id="1c1a1-109">Gehen Sie nicht davon aus, dass sich Stift-und Berührungs Eingaben in den Anwendungen [**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)und [**RealTimeStylus**](realtimestylus-class.md) gegenseitig ausschließen.</span><span class="sxs-lookup"><span data-stu-id="1c1a1-109">Do not assume pen and touch input are mutually exclusive in [**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md), and [**RealTimeStylus**](realtimestylus-class.md) applications.</span></span>

<span data-ttu-id="1c1a1-110">Wenn das System in Windows Vista einen Stift erkennt, werden Berührungs Eingaben ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1c1a1-110">In Windows Vista, when the system recognizes a pen it ignores touch input.</span></span> <span data-ttu-id="1c1a1-111">Das heißt, der Fingerabdruck wird beendet, und der Stift Strich beginnt.</span><span class="sxs-lookup"><span data-stu-id="1c1a1-111">That is, the touch stroke ends and the pen stroke begins.</span></span> <span data-ttu-id="1c1a1-112">Da sich dies möglicherweise in der Zukunft ändern kann, sollte der Code nicht annehmen, dass der Stift und die Berührungs Eingabe sich gegenseitig ausschließen.</span><span class="sxs-lookup"><span data-stu-id="1c1a1-112">Because this could possibly change in the future, your code should not assume pen and touch input are mutually exclusive.</span></span>

### <a name="other-mouse-message-sources"></a><span data-ttu-id="1c1a1-113">Andere Maus Nachrichtenquellen</span><span class="sxs-lookup"><span data-stu-id="1c1a1-113">Other Mouse Message Sources</span></span>

<span data-ttu-id="1c1a1-114">Es gibt auch andere Quellen für Maus Meldungen, auch wenn der Benutzer nur mit Finger oder Pen interagiert.</span><span class="sxs-lookup"><span data-stu-id="1c1a1-114">There are other sources of mouse messages even when the user is only interacting using finger or pen.</span></span> <span data-ttu-id="1c1a1-115">Zu den Quellen gehören Touchpads sowie eine Bewegung, mit der eine Anwendung hinter einem geschichteten Fenster erkennen kann, dass der Mauszeiger über der Anwendung bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="1c1a1-115">Sources include touchpads, as well as movement intended to let an application behind a layered window be aware that the mouse is moving above the application.</span></span>

### <a name="enabling-and-disabling-the-touch-input-user-interface"></a><span data-ttu-id="1c1a1-116">Aktivieren und Deaktivieren der Benutzeroberfläche für Berührungs Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c1a1-116">Enabling and Disabling the Touch Input User Interface</span></span>

<span data-ttu-id="1c1a1-117">Abhängig von den Anforderungen Ihrer Anwendung möchten Sie möglicherweise die Benutzeroberfläche für die Berührungs Eingabe aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="1c1a1-117">You may wish to enable or disable the touch input user interface depending on the requirements of your application.</span></span> <span data-ttu-id="1c1a1-118">Um dies zu erreichen, fangen Sie die Meldungen des Betriebssystem Fensters in einer Fenster Prozedur ab, und ändern Sie die Windows-Meldung.</span><span class="sxs-lookup"><span data-stu-id="1c1a1-118">To accomplish this, intercept operating system window messages in a window procedure and modify the Windows message.</span></span> <span data-ttu-id="1c1a1-119">Überschreiben Sie [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) in Ihrer Anwendung, um diese Meldungen abzufangen.</span><span class="sxs-lookup"><span data-stu-id="1c1a1-119">Override [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) in your application to intercept these messages.</span></span> <span data-ttu-id="1c1a1-120">Der folgende C \# -Pseudo Code zeigt, wie Sie die Benutzeroberfläche für die Berührungs Eingabe aktivieren und deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="1c1a1-120">The following C\# pseudo-code shows how to enable and disable the touch input user interface.</span></span> <span data-ttu-id="1c1a1-121">Der Code zeigt auch die Verwendung desselben Verfahrens zum Deaktivieren der Press-und-Halt-Geste.</span><span class="sxs-lookup"><span data-stu-id="1c1a1-121">The code also shows using the same technique to disable the press-and-hold gesture.</span></span> <span data-ttu-id="1c1a1-122">Diese Methode kann auch zum Deaktivieren des Tablettstifts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c1a1-122">This method also works for disabling the stylus.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1c1a1-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1c1a1-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c1a1-124">Windows-Fingereingabe</span><span class="sxs-lookup"><span data-stu-id="1c1a1-124">Windows Touch</span></span>](../wintouch/windows-touch-portal.md)
</dt> </dl>

 

 
