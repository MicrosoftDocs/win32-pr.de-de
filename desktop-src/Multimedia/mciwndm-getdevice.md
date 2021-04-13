---
title: MCIWNDM_GETDEVICE Meldung (VFW. h)
description: Die mciwndm \_ getdevice-Nachricht Ruft den Namen des aktuell geöffneten MCI-Geräts ab. Sie können diese Nachricht explizit oder mit dem mciwndgetdevice-Makro senden.
ms.assetid: e69a73a6-a927-4536-98c7-ee7d5b16668a
keywords:
- MCIWNDM_GETDEVICE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32664508a577db9d5a077e3cb4fd00aab34fbdf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475534"
---
# <a name="mciwndm_getdevice-message"></a><span data-ttu-id="69b50-105">Mciwndm \_ getdevice-Meldung</span><span class="sxs-lookup"><span data-stu-id="69b50-105">MCIWNDM\_GETDEVICE message</span></span>

<span data-ttu-id="69b50-106">Die **mciwndm \_ getdevice** -Nachricht Ruft den Namen des aktuell geöffneten MCI-Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="69b50-106">The **MCIWNDM\_GETDEVICE** message retrieves the name of the currently open MCI device.</span></span> <span data-ttu-id="69b50-107">Sie können diese Nachricht explizit oder mit dem [**mciwndgetdevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="69b50-107">You can send this message explicitly or by using the [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) macro.</span></span>


```C++
MCIWNDM_GETDEVICE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="69b50-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="69b50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69b50-109"><span id="len"></span><span id="LEN"></span>*Nest*</span><span class="sxs-lookup"><span data-stu-id="69b50-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="69b50-110">Größe (in Bytes) des Puffers.</span><span class="sxs-lookup"><span data-stu-id="69b50-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="69b50-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="69b50-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="69b50-112">Zeiger auf einen Anwendungs definierten Puffer, um den Gerätenamen zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="69b50-112">Pointer to an application-defined buffer to return the device name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69b50-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69b50-113">Return Value</span></span>

<span data-ttu-id="69b50-114">Gibt NULL zurück, wenn erfolgreich, andernfalls ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="69b50-114">Returns zero if successful or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="69b50-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69b50-115">Remarks</span></span>

<span data-ttu-id="69b50-116">Wenn die mit NULL endenden Zeichenfolge, die den Gerätenamen enthält, länger ist als der Puffer, wird Sie von mciwnd abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="69b50-116">If the null-terminated string containing the device name is longer than the buffer, MCIWnd truncates it.</span></span>

## <a name="requirements"></a><span data-ttu-id="69b50-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69b50-117">Requirements</span></span>



| <span data-ttu-id="69b50-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69b50-118">Requirement</span></span> | <span data-ttu-id="69b50-119">Wert</span><span class="sxs-lookup"><span data-stu-id="69b50-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="69b50-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69b50-120">Minimum supported client</span></span><br/> | <span data-ttu-id="69b50-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69b50-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="69b50-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69b50-122">Minimum supported server</span></span><br/> | <span data-ttu-id="69b50-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69b50-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="69b50-124">Header</span><span class="sxs-lookup"><span data-stu-id="69b50-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="69b50-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="69b50-125"><dt>Vfw.h</dt></span></span> </dl> |



 

 





