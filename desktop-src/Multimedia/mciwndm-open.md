---
title: MCIWNDM_OPEN Meldung (VFW. h)
description: Die Meldung mciwndm \_ Open öffnet ein MCI-Gerät und ordnet es einem mciwnd-Fenster zu.
ms.assetid: ad1dfe0f-015b-45a9-ab88-cc0bdf0aa057
keywords:
- MCIWNDM_OPEN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2f232ea9076a1e0ff8c105d8c5cf94104e455c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103435"
---
# <a name="mciwndm_open-message"></a><span data-ttu-id="af3d1-104">Meldung zum Öffnen von mciwndm \_</span><span class="sxs-lookup"><span data-stu-id="af3d1-104">MCIWNDM\_OPEN message</span></span>

<span data-ttu-id="af3d1-105">Die Meldung **mciwndm \_ Open** öffnet ein MCI-Gerät und ordnet es einem mciwnd-Fenster zu.</span><span class="sxs-lookup"><span data-stu-id="af3d1-105">The **MCIWNDM\_OPEN** message opens an MCI device and associates it with an MCIWnd window.</span></span> <span data-ttu-id="af3d1-106">Bei MCI-Geräten, die Datendateien verwenden, kann dieses Makro auch eine bestimmte Datendatei öffnen, eine neue zu erstellende Datei benennen oder ein Dialogfeld anzeigen, in dem der Benutzer eine Datei auswählen kann, die geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="af3d1-106">For MCI devices that use data files, this macro can also open a specified data file, name a new file to be created, or display a dialog box to let the user select a file to open.</span></span> <span data-ttu-id="af3d1-107">Sie können diese Nachricht explizit oder mithilfe des [**mciwndopen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="af3d1-107">You can send this message explicitly or by using the [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) macro.</span></span>


```C++
MCIWNDM_OPEN 
wParam = (WPARAM) (UINT) wFlags; 
lParam = (LPARAM) (LPVOID) szFile; 
```



## <a name="parameters"></a><span data-ttu-id="af3d1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="af3d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af3d1-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span><span class="sxs-lookup"><span data-stu-id="af3d1-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span></span>
</dt> <dd>

<span data-ttu-id="af3d1-110">Flags, die dem zu öffnenden Gerät oder der Datei zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="af3d1-110">Flags associated with the device or file to open.</span></span> <span data-ttu-id="af3d1-111">Das neue mciwndopenf- \_ Flag gibt an, dass eine neue Datei mit dem Namen erstellt werden soll, der in **szFile** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="af3d1-111">The MCIWNDOPENF\_NEW flag specifies a new file is to be created with the name specified in **szFile**.</span></span>

</dd> <dt>

<span data-ttu-id="af3d1-112"><span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*</span><span class="sxs-lookup"><span data-stu-id="af3d1-112"><span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*</span></span>
</dt> <dd>

<span data-ttu-id="af3d1-113">Zeiger auf eine mit NULL endenden Zeichenfolge, die den zu öffnenden Dateinamen oder MCI-Gerätenamen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="af3d1-113">Pointer to a null-terminated string identifying the filename or MCI device name to open.</span></span> <span data-ttu-id="af3d1-114">Geben Sie 1 für diesen Parameter an, um das Dialogfeld Öffnen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="af3d1-114">Specify  1 for this parameter to display the Open dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af3d1-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af3d1-115">Return Value</span></span>

<span data-ttu-id="af3d1-116">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="af3d1-116">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="af3d1-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af3d1-117">Requirements</span></span>



| <span data-ttu-id="af3d1-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af3d1-118">Requirement</span></span> | <span data-ttu-id="af3d1-119">Wert</span><span class="sxs-lookup"><span data-stu-id="af3d1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="af3d1-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="af3d1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="af3d1-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af3d1-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="af3d1-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="af3d1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="af3d1-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af3d1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="af3d1-124">Header</span><span class="sxs-lookup"><span data-stu-id="af3d1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="af3d1-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="af3d1-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af3d1-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af3d1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af3d1-127">**Mciwndopen**</span><span class="sxs-lookup"><span data-stu-id="af3d1-127">**MCIWndOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)
</dt> </dl>

 

 





