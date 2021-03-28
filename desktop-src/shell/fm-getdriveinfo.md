---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um Laufwerks Informationen aus dem aktiven Datei-Manager-Fenster abzurufen.
title: FM_GETDRIVEINFO Meldung (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 142fff71-3a1b-4197-8c06-2e981cce4e4f
ms.openlocfilehash: 7accd78b36e82abbf56b02b133c79e92dd40d37c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993703"
---
# <a name="fm_getdriveinfo-message"></a><span data-ttu-id="e2bcd-103">FM \_ GetDriveInfo-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e2bcd-103">FM\_GETDRIVEINFO message</span></span>

<span data-ttu-id="e2bcd-104">Wird von einer Datei-Manager-Erweiterung gesendet, um Laufwerks Informationen aus dem aktiven Datei-Manager-Fenster abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e2bcd-104">Sent by a File Manager extension to retrieve drive information from the active File Manager window.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2bcd-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2bcd-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2bcd-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2bcd-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e2bcd-107">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e2bcd-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e2bcd-108">*lpfmsgdi*</span><span class="sxs-lookup"><span data-stu-id="e2bcd-108">*lpfmsgdi*</span></span> 
</dt> <dd>

<span data-ttu-id="e2bcd-109">Die Adresse einer [**FMS \_ GetDriveInfo**](fms-getdriveinfo.md) -Struktur, die Laufwerk Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="e2bcd-109">The address of an [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure that receives drive information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2bcd-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2bcd-110">Return value</span></span>

<span data-ttu-id="e2bcd-111">Gibt einen Wert ungleich 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="e2bcd-111">Returns nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2bcd-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2bcd-112">Remarks</span></span>

<span data-ttu-id="e2bcd-113">Wenn 0xFFFFFFFF im **dwtotalspace** -oder **dwfreespace** -Member der [**FMS \_ GetDriveInfo**](fms-getdriveinfo.md) -Struktur zurückgegeben wird, muss die Erweiterungs Bibliothek den Wert oder die Werte berechnen.</span><span class="sxs-lookup"><span data-stu-id="e2bcd-113">If 0xFFFFFFFF is returned in the **dwTotalSpace** or **dwFreeSpace** member of the [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure, the extension library must compute the value or values.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2bcd-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e2bcd-114">Requirements</span></span>



| <span data-ttu-id="e2bcd-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2bcd-115">Requirement</span></span> | <span data-ttu-id="e2bcd-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e2bcd-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e2bcd-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2bcd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e2bcd-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2bcd-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e2bcd-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2bcd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e2bcd-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2bcd-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e2bcd-121">Header</span><span class="sxs-lookup"><span data-stu-id="e2bcd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2bcd-122"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2bcd-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2bcd-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e2bcd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2bcd-124">**"F"**</span><span class="sxs-lookup"><span data-stu-id="e2bcd-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




