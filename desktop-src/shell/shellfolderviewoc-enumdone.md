---
description: Gibt an, dass das shellfolderview-Objekt das Auflisten des Ordner Inhalts abgeschlossen hat.
title: Shellfolderviewoc. enumdone-Ereignis (Shldisp. h)
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
ms.openlocfilehash: 3ce02fd418a93ec5914c438fcad39d8dc73c5c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994990"
---
# <a name="shellfolderviewocenumdone-event"></a><span data-ttu-id="6d5b5-103">Shellfolderviewoc. enumdone-Ereignis</span><span class="sxs-lookup"><span data-stu-id="6d5b5-103">ShellFolderViewOC.EnumDone event</span></span>

<span data-ttu-id="6d5b5-104">Gibt an, dass das [**shellfolderview**](shellfolderview.md) -Objekt das Auflisten des Ordner Inhalts abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-104">Indicates that the [**ShellFolderView**](shellfolderview.md) object has finished enumerating the folder's contents.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d5b5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d5b5-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.EnumDone = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="6d5b5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d5b5-106">Parameters</span></span>

<span data-ttu-id="6d5b5-107">Dieser Ereignishandler verfügt über keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-107">This event handler has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d5b5-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d5b5-108">Remarks</span></span>

<span data-ttu-id="6d5b5-109">Das [**shellfolderview**](shellfolderview.md) -Objekt muss den Inhalt eines Ordners auflisten, bevor es angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-109">The [**ShellFolderView**](shellfolderview.md) object must enumerate the contents of a folder before it can display it.</span></span> <span data-ttu-id="6d5b5-110">Bei Ordnern, die groß sind oder sich auf einem Remote System befinden, kann dieser Vorgang einige Minuten in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-110">With folders that are large or located on a remote system, this process can take as much as several minutes.</span></span> <span data-ttu-id="6d5b5-111">Während dieser Zeit wird eine animierte Taschen Taschen Grafik angezeigt, um dem Benutzer mitzuteilen, dass die Verarbeitung unter dem Weg ist.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-111">During this time, an animated flashlight graphic is displayed to indicate to the user that processing is under way.</span></span> <span data-ttu-id="6d5b5-112">Sobald die Enumeration abgeschlossen ist, wird das Ereignis **enumdone** ausgelöst, und die Taschenlampen Grafik wird durch den Inhalt des Ordners ersetzt.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-112">Once the enumeration is complete, the **EnumDone** event is fired and the flashlight graphic is replaced by the contents of the folder.</span></span>

<span data-ttu-id="6d5b5-113">Geben Sie den Ereignis Behandlungs Code für dieses Ereignis an, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-113">Provide event handling code for this event as shown here.</span></span>


```
 
Private Sub object_EnumDone()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a><span data-ttu-id="6d5b5-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6d5b5-114">Requirements</span></span>



| <span data-ttu-id="6d5b5-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d5b5-115">Requirement</span></span> | <span data-ttu-id="6d5b5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6d5b5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d5b5-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d5b5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6d5b5-118">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d5b5-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6d5b5-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d5b5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6d5b5-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d5b5-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6d5b5-121">Header</span><span class="sxs-lookup"><span data-stu-id="6d5b5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d5b5-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d5b5-122"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="6d5b5-123">IDL</span><span class="sxs-lookup"><span data-stu-id="6d5b5-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6d5b5-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6d5b5-124"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="6d5b5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6d5b5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d5b5-126"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="6d5b5-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d5b5-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6d5b5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d5b5-128">**Shellfolderviewoc**</span><span class="sxs-lookup"><span data-stu-id="6d5b5-128">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)
</dt> </dl>

 

 




