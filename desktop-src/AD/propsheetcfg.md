---
title: Propsheetcfg-Struktur
description: Wird verwendet, um Eigenschaften Blatt-Konfigurationsdaten zu enthalten.
ms.assetid: d3bde744-9d85-4506-894f-f8be3463721f
ms.tgt_platform: multiple
keywords:
- Propsheetcfg-Struktur Active Directory
- Ppropsheetcfg-Struktur Zeiger Active Directory
topic_type:
- apiref
api_name:
- PROPSHEETCFG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33f4a1186cc756435cc49ed7c81592385faaee60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040644"
---
# <a name="propsheetcfg-structure"></a><span data-ttu-id="381a3-105">Propsheetcfg-Struktur</span><span class="sxs-lookup"><span data-stu-id="381a3-105">PROPSHEETCFG structure</span></span>

<span data-ttu-id="381a3-106">Die **propsheetcfg** -Struktur wird verwendet, um Eigenschaften Blatt-Konfigurationsdaten zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="381a3-106">The **PROPSHEETCFG** structure is used to contain property sheet configuration data.</span></span> <span data-ttu-id="381a3-107">Diese Struktur ist im " [**cfstr \_ DS \_ propsheetconfig**](cfstr-ds-propsheetconfig.md) "-Zwischenablage Format enthalten.</span><span class="sxs-lookup"><span data-stu-id="381a3-107">This structure is contained in the [**CFSTR\_DS\_PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md) clipboard format.</span></span>

> [!Note]  
> <span data-ttu-id="381a3-108">Diese Struktur ist nicht in einer veröffentlichten Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="381a3-108">This structure is not defined in a published header file.</span></span> <span data-ttu-id="381a3-109">Um diese Struktur verwenden zu können, müssen Sie Sie im exakten Format definieren.</span><span class="sxs-lookup"><span data-stu-id="381a3-109">To use this structure, you must define it yourself in the exact format shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="381a3-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="381a3-110">Syntax</span></span>


```C++
typedef struct {
  LONG_PTR lNotifyHandle;
  HWND     hwndParentSheet;
  HWND     hwndHidden;
  WPARAM   wParamSheetClose;
} PROPSHEETCFG, *PPROPSHEETCFG;
```



## <a name="members"></a><span data-ttu-id="381a3-111">Member</span><span class="sxs-lookup"><span data-stu-id="381a3-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="381a3-112">**lnotifyhandle**</span><span class="sxs-lookup"><span data-stu-id="381a3-112">**lNotifyHandle**</span></span>
</dt> <dd>

<span data-ttu-id="381a3-113">Enthält das Benachrichtigungs handle.</span><span class="sxs-lookup"><span data-stu-id="381a3-113">Contains the notification handle.</span></span> <span data-ttu-id="381a3-114">Dies ist identisch mit dem Handle, das für den *handle* -Parameter in der [**IExtendPropertySheet2:: deatepropertypages**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)) -Methode übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="381a3-114">This is identical to the handle passed for the *handle* parameter in the [**IExtendPropertySheet2::CreatePropertyPages**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)) method.</span></span>

</dd> <dt>

<span data-ttu-id="381a3-115">**hwndparametrisheet**</span><span class="sxs-lookup"><span data-stu-id="381a3-115">**hwndParentSheet**</span></span>
</dt> <dd>

<span data-ttu-id="381a3-116">Enthält das Fenster Handle des übergeordneten Eigenschaften Blatts.</span><span class="sxs-lookup"><span data-stu-id="381a3-116">Contains the window handle of the parent property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="381a3-117">**hwndhidden**</span><span class="sxs-lookup"><span data-stu-id="381a3-117">**hwndHidden**</span></span>
</dt> <dd>

<span data-ttu-id="381a3-118">Enthält das Handle des ausgeblendeten Fensters.</span><span class="sxs-lookup"><span data-stu-id="381a3-118">Contains the handle of the hidden window.</span></span>

</dd> <dt>

<span data-ttu-id="381a3-119">**wparamsheetclose**</span><span class="sxs-lookup"><span data-stu-id="381a3-119">**wParamSheetClose**</span></span>
</dt> <dd>

<span data-ttu-id="381a3-120">Enthält einen von der Anwendung definierten 32-Bit-Wert.</span><span class="sxs-lookup"><span data-stu-id="381a3-120">Contains an application-defined 32-bit value.</span></span> <span data-ttu-id="381a3-121">Dieser Wert wird an die Anwendung in der *wParam* des [**WM-DSA- \_ Blatts \_ " \_ Close \_ Notify**](wm-dsa-sheet-close-notify.md) Message" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="381a3-121">This value is passed back to the application in the *wParam* of the [**WM\_DSA\_SHEET\_CLOSE\_NOTIFY**](wm-dsa-sheet-close-notify.md) message.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="381a3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="381a3-122">Requirements</span></span>



| <span data-ttu-id="381a3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="381a3-123">Requirement</span></span> | <span data-ttu-id="381a3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="381a3-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="381a3-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="381a3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="381a3-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="381a3-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="381a3-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="381a3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="381a3-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="381a3-128">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="381a3-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="381a3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="381a3-130">**cfstr \_ DS \_ propsheetconfig**</span><span class="sxs-lookup"><span data-stu-id="381a3-130">**CFSTR\_DS\_PROPSHEETCONFIG**</span></span>](cfstr-ds-propsheetconfig.md)
</dt> <dt>

[<span data-ttu-id="381a3-131">**WM- \_ DSA- \_ Blatt " \_ Schließen \_ "**</span><span class="sxs-lookup"><span data-stu-id="381a3-131">**WM\_DSA\_SHEET\_CLOSE\_NOTIFY**</span></span>](wm-dsa-sheet-close-notify.md)
</dt> </dl>

 

