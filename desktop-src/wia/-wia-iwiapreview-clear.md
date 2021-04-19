---
description: 'Gibt das ungefilterte Bild frei, das von der iwiapreview:: getnewpreview-Methode zwischengespeichert wird. Außerdem wird der Bild Verarbeitungs Filter freigegeben.'
ms.assetid: af94d27f-9d93-40e1-8d1a-e5546531a176
title: 'Iwiapreview:: Clear-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.Clear
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1ac2cc1f12cf6fd59111d0159684459c2500a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348790"
---
# <a name="iwiapreviewclear-method"></a><span data-ttu-id="cf605-104">Iwiapreview:: Clear-Methode</span><span class="sxs-lookup"><span data-stu-id="cf605-104">IWiaPreview::Clear method</span></span>

<span data-ttu-id="cf605-105">Gibt das ungefilterte Bild frei, das von der [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md) -Methode zwischengespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="cf605-105">Releases the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="cf605-106">Außerdem wird der Bild Verarbeitungs Filter freigegeben.</span><span class="sxs-lookup"><span data-stu-id="cf605-106">It also releases the image processing filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf605-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf605-107">Syntax</span></span>


```C++
void Clear();
```



## <a name="parameters"></a><span data-ttu-id="cf605-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf605-108">Parameters</span></span>

<span data-ttu-id="cf605-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cf605-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cf605-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf605-110">Return value</span></span>

<span data-ttu-id="cf605-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cf605-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf605-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf605-112">Remarks</span></span>

<span data-ttu-id="cf605-113">Auf **iwiapreview:: Clear** die Windows-Abbild Übernahme (WIA) 2,0 Preview-Komponente gibt alle Schnittstellen Zeiger frei, die Sie speichert.</span><span class="sxs-lookup"><span data-stu-id="cf605-113">On **IWiaPreview::Clear** the Windows Image Acquisition (WIA) 2.0 Preview Component releases all interface pointers that it stores.</span></span> <span data-ttu-id="cf605-114">Die WIA 2,0-Vorschau Komponente behält Verweise auf *pWiaItem2* und *pwiatransfercallback* bei, die an [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md)übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="cf605-114">The WIA 2.0 Preview Component keeps references to *pWiaItem2* and *pWiaTransferCallback* passed into [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span> <span data-ttu-id="cf605-115">Um genau zu sein, behält die WIA 2,0-Vorschau Komponente einen Verweis auf *pWiaItem2* und den Bild Verarbeitungs Filter des Treibers bei, der wiederum einen Verweis auf *pwiatransfercallback* beibehält.</span><span class="sxs-lookup"><span data-stu-id="cf605-115">To be precise, the WIA 2.0 Preview Component keeps a reference to *pWiaItem2* and the driver's image processing filter, which in turn keeps a reference to *pWiaTransferCallback*.</span></span> <span data-ttu-id="cf605-116">Bei **iwiapreview:: Clear** gibt die WIA 2,0 Preview-Komponente auch Ihren Verweis auf *pWiaItem2* und den Bild Verarbeitungs Filter frei, der wiederum den Verweis auf *pwiatransfercallback* freigibt.</span><span class="sxs-lookup"><span data-stu-id="cf605-116">On **IWiaPreview::Clear**, the WIA 2.0 Preview Component also releases its reference to *pWiaItem2* and to the image processing filter, which in turn releases its reference to *pWiaTransferCallback*.</span></span> <span data-ttu-id="cf605-117">Die WIA 2,0-Vorschau Komponente löscht das zwischengespeicherte, ungefilterte Image, das intern gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="cf605-117">The WIA 2.0 Preview Component deletes the cached, unfiltered image that it stores internally.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf605-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf605-118">Requirements</span></span>



| <span data-ttu-id="cf605-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf605-119">Requirement</span></span> | <span data-ttu-id="cf605-120">Wert</span><span class="sxs-lookup"><span data-stu-id="cf605-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cf605-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf605-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cf605-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf605-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cf605-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf605-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cf605-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf605-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cf605-125">Header</span><span class="sxs-lookup"><span data-stu-id="cf605-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf605-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf605-126"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf605-127">IDL</span><span class="sxs-lookup"><span data-stu-id="cf605-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cf605-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cf605-128"><dt>Wia.idl</dt></span></span> </dl> |



 

 




