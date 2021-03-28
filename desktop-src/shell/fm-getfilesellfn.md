---
description: Gesendet von einer Datei-Manager-Erweiterung zum Abrufen von Informationen über eine ausgewählte Datei aus dem aktiven Datei-Manager-Fenster (entweder im Verzeichnis Fenster oder im Fenster "Suchergebnisse"). Die ausgewählte Datei kann einen langen Dateinamen haben.
title: FM_GETFILESELLFN Meldung (WF. h)
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
ms.openlocfilehash: 847100f494772b3c59ad719d03d7bc2dbe28cc29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484046"
---
# <a name="fm_getfilesellfn-message"></a><span data-ttu-id="aca47-104">FM \_ getfilesellfn-Nachricht</span><span class="sxs-lookup"><span data-stu-id="aca47-104">FM\_GETFILESELLFN message</span></span>

<span data-ttu-id="aca47-105">Gesendet von einer Datei-Manager-Erweiterung zum Abrufen von Informationen über eine ausgewählte Datei aus dem aktiven Datei-Manager-Fenster (entweder im Verzeichnis Fenster oder im Fenster "Suchergebnisse").</span><span class="sxs-lookup"><span data-stu-id="aca47-105">Sent by a File Manager extension to retrieve information about a selected file from the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="aca47-106">Die ausgewählte Datei kann einen langen Dateinamen haben.</span><span class="sxs-lookup"><span data-stu-id="aca47-106">The selected file can have a long file name.</span></span>

## <a name="parameters"></a><span data-ttu-id="aca47-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="aca47-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aca47-108">*Index*</span><span class="sxs-lookup"><span data-stu-id="aca47-108">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="aca47-109">Der null basierte Index der ausgewählten Datei, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="aca47-109">The zero-based index of the selected file to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="aca47-110">*lpfmsgfs*</span><span class="sxs-lookup"><span data-stu-id="aca47-110">*lpfmsgfs*</span></span> 
</dt> <dd>

<span data-ttu-id="aca47-111">Die Adresse einer [**f- \_ getfilesel**](fms-getfilesel.md) -Struktur, die Informationen über die Auswahl empfängt.</span><span class="sxs-lookup"><span data-stu-id="aca47-111">The address of an [**FMS\_GETFILESEL**](fms-getfilesel.md) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aca47-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aca47-112">Return value</span></span>

<span data-ttu-id="aca47-113">Gibt den NULL basierten Index der ausgewählten Datei zurück, die abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="aca47-113">Returns the zero-based index of the selected file that was retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="aca47-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aca47-114">Remarks</span></span>

<span data-ttu-id="aca47-115">Diese Nachricht sollte nur von Erweiterungen verwendet werden, die lange Dateinamen unterstützen (z. b. Netzwerk abhängige Erweiterungen).</span><span class="sxs-lookup"><span data-stu-id="aca47-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

<span data-ttu-id="aca47-116">Eine Erweiterung kann die [**FM \_ getselzähltlfn**](fm-getselcountlfn.md) -Nachricht verwenden, um die Anzahl ausgewählter Dateien abzurufen.</span><span class="sxs-lookup"><span data-stu-id="aca47-116">An extension can use the [**FM\_GETSELCOUNTLFN**](fm-getselcountlfn.md) message to retrieve the count of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="aca47-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="aca47-117">Requirements</span></span>



| <span data-ttu-id="aca47-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aca47-118">Requirement</span></span> | <span data-ttu-id="aca47-119">Wert</span><span class="sxs-lookup"><span data-stu-id="aca47-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aca47-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aca47-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aca47-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aca47-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="aca47-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aca47-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aca47-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aca47-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="aca47-124">Header</span><span class="sxs-lookup"><span data-stu-id="aca47-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aca47-125"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="aca47-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aca47-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="aca47-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aca47-127">**"F"**</span><span class="sxs-lookup"><span data-stu-id="aca47-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="aca47-128">**FM \_ getfilesel**</span><span class="sxs-lookup"><span data-stu-id="aca47-128">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="aca47-129">**FM \_ getselcount**</span><span class="sxs-lookup"><span data-stu-id="aca47-129">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 




