---
title: MCIWNDM_NOTIFYMEDIA Meldung (VFW. h)
description: Die mciwndm \_ notifymedia-Meldung benachrichtigt das übergeordnete Fenster einer Anwendung, dass das Medium geändert wurde.
ms.assetid: cc31502d-09a9-4580-9ff8-9c2be51c8e35
keywords:
- MCIWNDM_NOTIFYMEDIA-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7026bd984e1d79775aac52caad56c87be6e8098e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741152"
---
# <a name="mciwndm_notifymedia-message"></a><span data-ttu-id="87928-104">Mciwndm \_ notifymedia-Meldung</span><span class="sxs-lookup"><span data-stu-id="87928-104">MCIWNDM\_NOTIFYMEDIA message</span></span>

<span data-ttu-id="87928-105">Die **mciwndm \_ notifymedia** -Meldung benachrichtigt das übergeordnete Fenster einer Anwendung, dass das Medium geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="87928-105">The **MCIWNDM\_NOTIFYMEDIA** message notifies the parent window of an application that the media has changed.</span></span>


```C++
MCIWNDM_NOTIFYMEDIA 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="87928-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="87928-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87928-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="87928-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="87928-108">Handle für das mciwnd-Fenster.</span><span class="sxs-lookup"><span data-stu-id="87928-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="87928-109"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="87928-109"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="87928-110">Zeiger auf eine mit NULL endenden Zeichenfolge, die den neuen Dateinamen enthält.</span><span class="sxs-lookup"><span data-stu-id="87928-110">Pointer to a null-terminated string containing the new filename.</span></span> <span data-ttu-id="87928-111">Wenn das Medium geschlossen wird, gibt es eine NULL-Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="87928-111">If the media is closing, it specifies a null string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87928-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87928-112">Remarks</span></span>

<span data-ttu-id="87928-113">Sie können die Benachrichtigung über Medien Änderungen aktivieren, indem Sie den Fenster Stil mciwndf \_ notifymedia angeben.</span><span class="sxs-lookup"><span data-stu-id="87928-113">You can enable notification of media changes by specifying the MCIWNDF\_NOTIFYMEDIA window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="87928-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87928-114">Requirements</span></span>



| <span data-ttu-id="87928-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87928-115">Requirement</span></span> | <span data-ttu-id="87928-116">Wert</span><span class="sxs-lookup"><span data-stu-id="87928-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="87928-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="87928-117">Minimum supported client</span></span><br/> | <span data-ttu-id="87928-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87928-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="87928-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="87928-119">Minimum supported server</span></span><br/> | <span data-ttu-id="87928-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87928-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="87928-121">Header</span><span class="sxs-lookup"><span data-stu-id="87928-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="87928-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="87928-122"><dt>Vfw.h</dt></span></span> </dl> |



 

 





