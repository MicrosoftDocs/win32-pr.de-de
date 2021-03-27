---
description: Gesendet von einer Datei-Manager-Erweiterung zum Abrufen von Informationen über eine ausgewählte Datei aus dem aktiven Datei-Manager-Fenster (entweder im Verzeichnis Fenster oder im Fenster "Suchergebnisse").
title: FM_GETFILESEL Meldung (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c2b4aac6-165b-4eba-b012-ee7a20481cd3
ms.openlocfilehash: ec7d221e0c352c4b9284ae5fe2d6f80e50da85ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864947"
---
# <a name="fm_getfilesel-message"></a><span data-ttu-id="dcf5f-103">FM \_ getfilesel-Meldung</span><span class="sxs-lookup"><span data-stu-id="dcf5f-103">FM\_GETFILESEL message</span></span>

<span data-ttu-id="dcf5f-104">Gesendet von einer Datei-Manager-Erweiterung zum Abrufen von Informationen über eine ausgewählte Datei aus dem aktiven Datei-Manager-Fenster (entweder im Verzeichnis Fenster oder im Fenster "Suchergebnisse").</span><span class="sxs-lookup"><span data-stu-id="dcf5f-104">Sent by a File Manager extension to retrieve information about a selected file from the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="dcf5f-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="dcf5f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcf5f-106">*Index*</span><span class="sxs-lookup"><span data-stu-id="dcf5f-106">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="dcf5f-107">Der null basierte Index der ausgewählten Datei, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="dcf5f-107">The zero-based index of the selected file to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="dcf5f-108">*lpfmsgfs*</span><span class="sxs-lookup"><span data-stu-id="dcf5f-108">*lpfmsgfs*</span></span> 
</dt> <dd>

<span data-ttu-id="dcf5f-109">Die Adresse einer [**f- \_ getfilesel**](fms-getfilesel.md) -Struktur, die Informationen über die Auswahl empfängt.</span><span class="sxs-lookup"><span data-stu-id="dcf5f-109">The address of an [**FMS\_GETFILESEL**](fms-getfilesel.md) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcf5f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dcf5f-110">Return value</span></span>

<span data-ttu-id="dcf5f-111">Gibt den NULL basierten Index der ausgewählten Datei zurück, die abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="dcf5f-111">Returns the zero-based index of the selected file that was retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcf5f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dcf5f-112">Remarks</span></span>

<span data-ttu-id="dcf5f-113">Eine Erweiterung kann die [**FM \_ getselcount**](fm-getselcount.md) -Nachricht verwenden, um die Anzahl ausgewählter Dateien abzurufen.</span><span class="sxs-lookup"><span data-stu-id="dcf5f-113">An extension can use the [**FM\_GETSELCOUNT**](fm-getselcount.md) message to retrieve the count of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcf5f-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="dcf5f-114">Requirements</span></span>



| <span data-ttu-id="dcf5f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dcf5f-115">Requirement</span></span> | <span data-ttu-id="dcf5f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="dcf5f-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dcf5f-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dcf5f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dcf5f-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dcf5f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="dcf5f-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dcf5f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dcf5f-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dcf5f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dcf5f-121">Header</span><span class="sxs-lookup"><span data-stu-id="dcf5f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcf5f-122"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5f-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcf5f-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dcf5f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcf5f-124">**"F"**</span><span class="sxs-lookup"><span data-stu-id="dcf5f-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="dcf5f-125">**FM \_ getfilesellfn**</span><span class="sxs-lookup"><span data-stu-id="dcf5f-125">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="dcf5f-126">**FM \_ getselzähltlfn**</span><span class="sxs-lookup"><span data-stu-id="dcf5f-126">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




