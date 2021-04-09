---
title: Iagentcharakteriex
description: Iagentcharakteriex
ms.assetid: d4d42122-3d27-40c4-8770-0de105e5d933
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674fc8dcca3bca2f44c0928474d8684e77fc6e9b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101498"
---
# <a name="iagentcharacterexsethelpmodeon"></a><span data-ttu-id="407de-103">Iagentcharakteriex:: Setup</span><span class="sxs-lookup"><span data-stu-id="407de-103">IAgentCharacterEx::SetHelpModeOn</span></span>

<span data-ttu-id="407de-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="407de-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpModeOn(
   long bHelpModeOn  // help mode setting
);
```

<span data-ttu-id="407de-105">Legt den kontextbezogenen Hilfe Modus für das Zeichen fest.</span><span class="sxs-lookup"><span data-stu-id="407de-105">Sets context-sensitive Help mode on for the character.</span></span>

-   <span data-ttu-id="407de-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="407de-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="407de-107"><span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*bhelpmudeon*</span><span class="sxs-lookup"><span data-stu-id="407de-107"><span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*bHelpModeOn*</span></span>
</dt> <dd>

<span data-ttu-id="407de-108">Hilfe Modus-Flag.</span><span class="sxs-lookup"><span data-stu-id="407de-108">Help mode flag.</span></span> <span data-ttu-id="407de-109">Wenn dieser Parameter den Wert **true** hat, schaltet der Microsoft-Agent den Hilfe Modus für das Zeichen ein.</span><span class="sxs-lookup"><span data-stu-id="407de-109">If this parameter is **True**, Microsoft Agent turns on Help mode for the character.</span></span>

</dd> </dl>

<span data-ttu-id="407de-110">Wenn Sie diese Eigenschaft auf **true** festlegen, ändert sich der Mauszeiger in das kontextabhängige Hilfe Bild, wenn es über das Zeichen oder über das Popup Menü für das Zeichen verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="407de-110">When you set this property to **True**, the mouse pointer changes to the context-sensitive Help image when moved over the character or over the pop-up menu for the character.</span></span> <span data-ttu-id="407de-111">Wenn der Benutzer auf das Zeichen klickt oder zieht oder auf ein Element im Popup Menü des Zeichens klickt, löst der Server das [**iagentnotifysinkex:: helpcomplete**](iagentnotifysinkex--helpcomplete.md) -Ereignis aus und beendet den Hilfe Modus.</span><span class="sxs-lookup"><span data-stu-id="407de-111">When the user clicks or drags the character or clicks an item in the character's pop-up menu, the server triggers the [**IAgentNotifySinkEx::HelpComplete**](iagentnotifysinkex--helpcomplete.md) event and exits Help mode.</span></span>

<span data-ttu-id="407de-112">Im Hilfe Modus sendet der Server das [**Click**](click-event.md)-, [**DragStart**](/windows/desktop/lwef/dragstart-event)-, [**dragcomplete**](https://www.bing.com/search?q=**DragComplete**)-und [**Command**](command-event.md) -Ereignis nicht, es sei denn, die [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md) -Eigenschaft gibt **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="407de-112">In Help mode, the server does not send the [**Click**](click-event.md), [**DragStart**](/windows/desktop/lwef/dragstart-event), [**DragComplete**](https://www.bing.com/search?q=**DragComplete**), and [**Command**](command-event.md) events, unless the [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md) property returns **True**.</span></span> <span data-ttu-id="407de-113">In diesem Fall sendet der Server das **Click** -Ereignis (der Hilfe Modus wird nicht beendet), sondern nur für die Rechte Maustaste, sodass Sie das Popup Menü anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="407de-113">In that case, the server will send the **Click** event (does not exit Help mode), but only for the right mouse button so you can display the pop-up menu.</span></span>

<span data-ttu-id="407de-114">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="407de-114">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="407de-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="407de-115">See Also</span></span>

<span data-ttu-id="407de-116">[**Iagentcharakteriex:: gethelpmudeon**](iagentcharacterex--gethelpmodeon.md), [ **iagentnotifysinkex:: helpcomplete**](iagentnotifysinkex--helpcomplete.md)</span><span class="sxs-lookup"><span data-stu-id="407de-116">[**IAgentCharacterEx::GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md), [**IAgentNotifySinkEx::HelpComplete**](iagentnotifysinkex--helpcomplete.md)</span></span>


 

 