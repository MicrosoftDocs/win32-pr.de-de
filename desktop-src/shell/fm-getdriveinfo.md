---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um Laufwerksinformationen aus dem aktiven Datei-Manager-Fenster abzurufen.
title: FM_GETDRIVEINFO (Wfext.h)
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
ms.openlocfilehash: 0abac794ed23eca30676a839a6eb5ad7c1079c3c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842411"
---
# <a name="fm_getdriveinfo-message"></a><span data-ttu-id="91938-103">FM \_ GETDRIVEINFO-Nachricht</span><span class="sxs-lookup"><span data-stu-id="91938-103">FM\_GETDRIVEINFO message</span></span>

<span data-ttu-id="91938-104">Wird von einer Datei-Manager-Erweiterung gesendet, um Laufwerksinformationen aus dem aktiven Datei-Manager-Fenster abzurufen.</span><span class="sxs-lookup"><span data-stu-id="91938-104">Sent by a File Manager extension to retrieve drive information from the active File Manager window.</span></span>

## <a name="parameters"></a><span data-ttu-id="91938-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="91938-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91938-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91938-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="91938-107">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="91938-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="91938-108">*lpfmsgdi*</span><span class="sxs-lookup"><span data-stu-id="91938-108">*lpfmsgdi*</span></span> 
</dt> <dd>

<span data-ttu-id="91938-109">Die Adresse einer [**FMS \_ GETDRIVEINFO-Struktur,**](fms-getdriveinfo.md) die Laufwerkinformationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="91938-109">The address of an [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure that receives drive information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91938-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91938-110">Return value</span></span>

<span data-ttu-id="91938-111">Gibt einen Wert ungleich 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="91938-111">Returns nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="91938-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="91938-112">Remarks</span></span>

<span data-ttu-id="91938-113">Wenn 0xFFFFFFFF **dwTotalSpace-** oder **dwFreeSpace-Member** der [**FMS \_ GETDRIVEINFO-Struktur**](fms-getdriveinfo.md) zurückgegeben wird, muss die Erweiterungsbibliothek den Wert oder die Werte berechnen.</span><span class="sxs-lookup"><span data-stu-id="91938-113">If 0xFFFFFFFF is returned in the **dwTotalSpace** or **dwFreeSpace** member of the [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure, the extension library must compute the value or values.</span></span>

## <a name="requirements"></a><span data-ttu-id="91938-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91938-114">Requirements</span></span>



| <span data-ttu-id="91938-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91938-115">Requirement</span></span> | <span data-ttu-id="91938-116">Wert</span><span class="sxs-lookup"><span data-stu-id="91938-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="91938-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91938-117">Minimum supported client</span></span><br/> | <span data-ttu-id="91938-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91938-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="91938-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91938-119">Minimum supported server</span></span><br/> | <span data-ttu-id="91938-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91938-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="91938-121">Header</span><span class="sxs-lookup"><span data-stu-id="91938-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="91938-122"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="91938-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91938-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91938-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91938-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="91938-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




