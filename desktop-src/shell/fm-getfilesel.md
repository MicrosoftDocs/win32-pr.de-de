---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um Informationen zu einer ausgewählten Datei aus dem aktiven Datei-Manager-Fenster abzurufen (entweder das Verzeichnisfenster oder das Fenster Suchergebnisse).
title: FM_GETFILESEL Nachricht (Wfext.h)
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
ms.openlocfilehash: 2da95a39f8e84215640e926ae21a043865223665
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841421"
---
# <a name="fm_getfilesel-message"></a><span data-ttu-id="003b5-103">FM \_ GETFILESEL-Nachricht</span><span class="sxs-lookup"><span data-stu-id="003b5-103">FM\_GETFILESEL message</span></span>

<span data-ttu-id="003b5-104">Wird von einer Datei-Manager-Erweiterung gesendet, um Informationen zu einer ausgewählten Datei aus dem aktiven Datei-Manager-Fenster abzurufen (entweder das Verzeichnisfenster oder das Fenster Suchergebnisse).</span><span class="sxs-lookup"><span data-stu-id="003b5-104">Sent by a File Manager extension to retrieve information about a selected file from the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="003b5-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="003b5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="003b5-106">*Index*</span><span class="sxs-lookup"><span data-stu-id="003b5-106">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="003b5-107">Der nullbasierte Index der ausgewählten abzurufenden Datei.</span><span class="sxs-lookup"><span data-stu-id="003b5-107">The zero-based index of the selected file to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="003b5-108">*lpfmsgfs*</span><span class="sxs-lookup"><span data-stu-id="003b5-108">*lpfmsgfs*</span></span> 
</dt> <dd>

<span data-ttu-id="003b5-109">Die Adresse einer [**FMS \_ GETFILESEL-Struktur,**](fms-getfilesel.md) die Informationen zur Auswahl empfängt.</span><span class="sxs-lookup"><span data-stu-id="003b5-109">The address of an [**FMS\_GETFILESEL**](fms-getfilesel.md) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="003b5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="003b5-110">Return value</span></span>

<span data-ttu-id="003b5-111">Gibt den nullbasierten Index der ausgewählten Datei zurück, die abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="003b5-111">Returns the zero-based index of the selected file that was retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="003b5-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="003b5-112">Remarks</span></span>

<span data-ttu-id="003b5-113">Eine Erweiterung kann die [**FM \_ GETSELCOUNT-Nachricht**](fm-getselcount.md) verwenden, um die Anzahl der ausgewählten Dateien abzurufen.</span><span class="sxs-lookup"><span data-stu-id="003b5-113">An extension can use the [**FM\_GETSELCOUNT**](fm-getselcount.md) message to retrieve the count of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="003b5-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="003b5-114">Requirements</span></span>



| <span data-ttu-id="003b5-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="003b5-115">Requirement</span></span> | <span data-ttu-id="003b5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="003b5-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="003b5-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="003b5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="003b5-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="003b5-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="003b5-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="003b5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="003b5-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="003b5-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="003b5-121">Header</span><span class="sxs-lookup"><span data-stu-id="003b5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="003b5-122"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="003b5-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="003b5-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="003b5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="003b5-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="003b5-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="003b5-125">**FM \_ GETFILESELLFN**</span><span class="sxs-lookup"><span data-stu-id="003b5-125">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="003b5-126">**FM \_ GETSELCOUNTLFN**</span><span class="sxs-lookup"><span data-stu-id="003b5-126">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




