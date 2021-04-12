---
title: Iagentcharakteriex gethelpmudeon
description: Iagentcharakteriex gethelpmudeon
ms.assetid: 848c9e75-6e4c-487c-b01c-36ec6314d0c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 072f657ba5ac93d057474f062f73101f2559aed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207269"
---
# <a name="iagentcharacterexgethelpmodeon"></a><span data-ttu-id="85eb9-103">Iagentcharakteriex:: gethelpmudeon</span><span class="sxs-lookup"><span data-stu-id="85eb9-103">IAgentCharacterEx::GetHelpModeOn</span></span>

<span data-ttu-id="85eb9-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="85eb9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpModeOn(
   long * pbHelpModeOn  // address of help mode setting
);
```

<span data-ttu-id="85eb9-105">Ruft ab, ob der kontextabhängige Hilfe Modus für das Zeichen on ist.</span><span class="sxs-lookup"><span data-stu-id="85eb9-105">Retrieves whether context-sensitive Help mode is on for the character.</span></span>

-   <span data-ttu-id="85eb9-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="85eb9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="85eb9-107"><span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbhelpmudeon*</span><span class="sxs-lookup"><span data-stu-id="85eb9-107"><span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbHelpModeOn*</span></span>
</dt> <dd>

<span data-ttu-id="85eb9-108">Adresse einer Variablen, die **true** empfängt, wenn der Hilfe Modus für das Zeichen on ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="85eb9-108">Address of a variable that receives **True** if Help mode is on for the character and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="85eb9-109">Wenn diese Eigenschaft auf **true** festgelegt ist, ändert sich der Mauszeiger in das kontextabhängige Hilfe Bild, wenn er über das Zeichen oder über das Popupmenü für das Zeichen verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="85eb9-109">When this property is set to **True**, the mouse pointer changes to the context-sensitive Help image when moved over the character or over the pop-up menu for the character.</span></span> <span data-ttu-id="85eb9-110">Wenn der Benutzer auf das Zeichen klickt oder zieht oder auf ein Element im Popup Menü des Zeichens klickt, löst der Server das [**iagentnotifysinkex:: helpcomplete**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) -Ereignis aus und beendet den Hilfe Modus.</span><span class="sxs-lookup"><span data-stu-id="85eb9-110">When the user clicks or drags the character or clicks an item in the character's pop-up menu, the server triggers the [**IAgentNotifySinkEx::HelpComplete**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) event and exits Help mode.</span></span>

<span data-ttu-id="85eb9-111">Im Hilfe Modus sendet der Server die Ereignisse " [**iagentnotifysink:: Click**](iagentnotifysink--click.md)", " [**iagentnotifysink::D ragstart**](iagentnotifysink--dragstart.md)", " [**iagentnotifysink::D ragcomplete**](iagentnotifysink--dragcomplete.md)" und " [**iagentnotifysink:: Command**](iagentnotifysink--command.md) " nicht, es sei denn, die [**GetAutoPopupMenu**](https://www.bing.com/search?q=**GetAutoPopupMenu**) -Eigenschaft gibt " **true**" zurück.</span><span class="sxs-lookup"><span data-stu-id="85eb9-111">In Help mode, the server does not send the [**IAgentNotifySink::Click**](iagentnotifysink--click.md), [**IAgentNotifySink::DragStart**](iagentnotifysink--dragstart.md), [**IAgentNotifySink::DragComplete**](iagentnotifysink--dragcomplete.md), and [**IAgentNotifySink::Command**](iagentnotifysink--command.md) events, unless [**GetAutoPopupMenu**](https://www.bing.com/search?q=**GetAutoPopupMenu**) property returns **True**.</span></span> <span data-ttu-id="85eb9-112">In diesem Fall sendet der Server das **iagentnotifysink:: Click** -Ereignis (der Hilfe Modus wird nicht beendet), sondern nur für die Rechte Maustaste, damit Sie das Popup Menü anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="85eb9-112">In that case, the server will send the **IAgentNotifySink::Click** event (does not exit Help mode), but only for the right mouse button to enable you to display the pop-up menu.</span></span>

<span data-ttu-id="85eb9-113">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="85eb9-113">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="85eb9-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="85eb9-114">See Also</span></span>

[<span data-ttu-id="85eb9-115">**Iagentcharakteriex:: Setup**</span><span class="sxs-lookup"><span data-stu-id="85eb9-115">**IAgentCharacterEx::SetHelpModeOn**</span></span>](iagentcharacterex--sethelpmodeon.md)


 

 




