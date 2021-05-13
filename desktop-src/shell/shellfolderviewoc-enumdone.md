---
description: Gibt an, dass das ShellFolderView-Objekt das Aufzählen des Ordnerinhalts abgeschlossen hat.
title: ShellFolderViewOC.EnumDone-Ereignis (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumDone
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 7baa5f58-62c2-406e-a81e-4ca9c446a756
ms.openlocfilehash: 00b0e58ed18ab0da9c3fa362da4b8e3e066cdcc4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841051"
---
# <a name="shellfolderviewocenumdone-event"></a><span data-ttu-id="9d462-103">ShellFolderViewOC.EnumDone-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9d462-103">ShellFolderViewOC.EnumDone event</span></span>

<span data-ttu-id="9d462-104">Gibt an, [**dass das ShellFolderView-Objekt**](shellfolderview.md) das Aufzählen des Ordnerinhalts abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="9d462-104">Indicates that the [**ShellFolderView**](shellfolderview.md) object has finished enumerating the folder's contents.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d462-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d462-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.EnumDone = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="9d462-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d462-106">Parameters</span></span>

<span data-ttu-id="9d462-107">Dieser Ereignishandler verfügt über keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9d462-107">This event handler has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d462-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9d462-108">Remarks</span></span>

<span data-ttu-id="9d462-109">Das [**ShellFolderView-Objekt**](shellfolderview.md) muss den Inhalt eines Ordners aufzählen, bevor er angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9d462-109">The [**ShellFolderView**](shellfolderview.md) object must enumerate the contents of a folder before it can display it.</span></span> <span data-ttu-id="9d462-110">Bei ordnern, die groß sind oder sich auf einem Remotesystem befinden, kann dieser Vorgang bis zu mehrere Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="9d462-110">With folders that are large or located on a remote system, this process can take as much as several minutes.</span></span> <span data-ttu-id="9d462-111">Während dieser Zeit wird eine animierte Taschenlampengrafik angezeigt, um dem Benutzer anzuzeigen, dass die Verarbeitung in Bearbeitung ist.</span><span class="sxs-lookup"><span data-stu-id="9d462-111">During this time, an animated flashlight graphic is displayed to indicate to the user that processing is under way.</span></span> <span data-ttu-id="9d462-112">Sobald die Enumeration abgeschlossen ist, wird das **EnumDone-Ereignis** ausgelöst, und die Taschenlampengrafik wird durch den Inhalt des Ordners ersetzt.</span><span class="sxs-lookup"><span data-stu-id="9d462-112">Once the enumeration is complete, the **EnumDone** event is fired and the flashlight graphic is replaced by the contents of the folder.</span></span>

<span data-ttu-id="9d462-113">Geben Sie den Ereignisbehandlungscode für dieses Ereignis wie hier gezeigt an.</span><span class="sxs-lookup"><span data-stu-id="9d462-113">Provide event handling code for this event as shown here.</span></span>


```
 
Private Sub object_EnumDone()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a><span data-ttu-id="9d462-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d462-114">Requirements</span></span>



| <span data-ttu-id="9d462-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d462-115">Requirement</span></span> | <span data-ttu-id="9d462-116">Wert</span><span class="sxs-lookup"><span data-stu-id="9d462-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d462-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d462-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9d462-118">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d462-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9d462-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d462-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9d462-120">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d462-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9d462-121">Header</span><span class="sxs-lookup"><span data-stu-id="9d462-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d462-122"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="9d462-122"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="9d462-123">Idl</span><span class="sxs-lookup"><span data-stu-id="9d462-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9d462-124"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="9d462-124"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="9d462-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9d462-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d462-126"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="9d462-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d462-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d462-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d462-128">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="9d462-128">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)
</dt> </dl>

 

 




