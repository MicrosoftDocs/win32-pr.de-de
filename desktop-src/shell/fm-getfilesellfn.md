---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um Informationen zu einer ausgewählten Datei aus dem aktiven Datei-Manager-Fenster abzurufen (entweder das Verzeichnisfenster oder das Fenster Suchergebnisse). Die ausgewählte Datei kann einen langen Dateinamen haben.
title: FM_GETFILESELLFN (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESELLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 461fd171-d47f-41d6-953e-8e497e023ab1
ms.openlocfilehash: e991d2705f74aa8822dcef89878e9762f22b08dc
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842391"
---
# <a name="fm_getfilesellfn-message"></a><span data-ttu-id="b5f79-104">FM \_ GETFILESELLFN-Nachricht</span><span class="sxs-lookup"><span data-stu-id="b5f79-104">FM\_GETFILESELLFN message</span></span>

<span data-ttu-id="b5f79-105">Wird von einer Datei-Manager-Erweiterung gesendet, um Informationen zu einer ausgewählten Datei aus dem aktiven Datei-Manager-Fenster abzurufen (entweder das Verzeichnisfenster oder das Fenster Suchergebnisse).</span><span class="sxs-lookup"><span data-stu-id="b5f79-105">Sent by a File Manager extension to retrieve information about a selected file from the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="b5f79-106">Die ausgewählte Datei kann einen langen Dateinamen haben.</span><span class="sxs-lookup"><span data-stu-id="b5f79-106">The selected file can have a long file name.</span></span>

## <a name="parameters"></a><span data-ttu-id="b5f79-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5f79-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5f79-108">*Index*</span><span class="sxs-lookup"><span data-stu-id="b5f79-108">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="b5f79-109">Der nullbasierte Index der abzurufenden ausgewählten Datei.</span><span class="sxs-lookup"><span data-stu-id="b5f79-109">The zero-based index of the selected file to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="b5f79-110">*lpfmsgfs*</span><span class="sxs-lookup"><span data-stu-id="b5f79-110">*lpfmsgfs*</span></span> 
</dt> <dd>

<span data-ttu-id="b5f79-111">Die Adresse einer [**FMS \_ GETFILESEL-Struktur,**](fms-getfilesel.md) die Informationen zur Auswahl empfängt.</span><span class="sxs-lookup"><span data-stu-id="b5f79-111">The address of an [**FMS\_GETFILESEL**](fms-getfilesel.md) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5f79-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5f79-112">Return value</span></span>

<span data-ttu-id="b5f79-113">Gibt den nullbasierten Index der ausgewählten Datei zurück, die abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f79-113">Returns the zero-based index of the selected file that was retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5f79-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b5f79-114">Remarks</span></span>

<span data-ttu-id="b5f79-115">Nur Erweiterungen, die lange Dateinamen unterstützen (z. B. netzwerkspezifische Erweiterungen), sollten diese Meldung verwenden.</span><span class="sxs-lookup"><span data-stu-id="b5f79-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

<span data-ttu-id="b5f79-116">Eine Erweiterung kann die [**FM \_ GETSELCOUNTLFN-Nachricht**](fm-getselcountlfn.md) verwenden, um die Anzahl der ausgewählten Dateien abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b5f79-116">An extension can use the [**FM\_GETSELCOUNTLFN**](fm-getselcountlfn.md) message to retrieve the count of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5f79-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5f79-117">Requirements</span></span>



| <span data-ttu-id="b5f79-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5f79-118">Requirement</span></span> | <span data-ttu-id="b5f79-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b5f79-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5f79-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5f79-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b5f79-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5f79-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b5f79-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5f79-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b5f79-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5f79-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b5f79-124">Header</span><span class="sxs-lookup"><span data-stu-id="b5f79-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5f79-125"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="b5f79-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5f79-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5f79-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5f79-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="b5f79-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="b5f79-128">**FM \_ GETFILESEL**</span><span class="sxs-lookup"><span data-stu-id="b5f79-128">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="b5f79-129">**FM \_ GETSELCOUNT**</span><span class="sxs-lookup"><span data-stu-id="b5f79-129">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 




