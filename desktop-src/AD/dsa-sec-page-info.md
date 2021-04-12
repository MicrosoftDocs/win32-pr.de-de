---
title: DSA_SEC_PAGE_INFO Struktur
description: Wird mit dem Blatt "WM \_ adsprop \_ Sheet \_ Create" und "WM- \_ DSA" \_ \_ Erstellen \_ von Benachrichtigungs Meldungen zum Definieren eines sekundären Eigenschaften Blatts in einem Active Directory MMC-Snap-in verwendet.
ms.assetid: 422d84dc-6b5e-43bf-ac4f-3b99cb59f9df
ms.tgt_platform: multiple
keywords:
- DSA_SEC_PAGE_INFO Struktur Active Directory
- PDSA_SEC_PAGE_INFO Struktur Zeiger Active Directory
topic_type:
- apiref
api_name:
- DSA_SEC_PAGE_INFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e4c8602a958c50c72942d89657a812d24f64571d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956732"
---
# <a name="dsa_sec_page_info-structure"></a><span data-ttu-id="215fb-105">DSA \_ sec- \_ Seite \_ Info-Struktur</span><span class="sxs-lookup"><span data-stu-id="215fb-105">DSA\_SEC\_PAGE\_INFO structure</span></span>

<span data-ttu-id="215fb-106">Die **Informationen Struktur der DSA \_ sec- \_ Seite \_** wird mit dem Blatt " [**WM \_ adsprop \_ Sheet \_ Create**](wm-adsprop-sheet-create.md) " und " [**WM-DSA" Erstellen von \_ \_ \_ \_ Benachrichtigungs**](wm-dsa-sheet-create-notify.md) Meldungen zum Definieren eines sekundären Eigenschaften Blatts in einem Active Directory MMC-Snap-in verwendet.</span><span class="sxs-lookup"><span data-stu-id="215fb-106">The **DSA\_SEC\_PAGE\_INFO** structure is used with the [**WM\_ADSPROP\_SHEET\_CREATE**](wm-adsprop-sheet-create.md) and [**WM\_DSA\_SHEET\_CREATE\_NOTIFY**](wm-dsa-sheet-create-notify.md) messages to define a secondary property sheet in an Active Directory MMC snap-in.</span></span>

> [!Note]  
> <span data-ttu-id="215fb-107">Diese Struktur ist nicht in einer veröffentlichten Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="215fb-107">This structure is not defined in a published header file.</span></span> <span data-ttu-id="215fb-108">Um diese Struktur zu verwenden, definieren Sie Sie im exakten Format.</span><span class="sxs-lookup"><span data-stu-id="215fb-108">To use this structure, define it in the exact format shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="215fb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="215fb-109">Syntax</span></span>


```C++
typedef struct _DSA_SEC_PAGE_INFO {
  HWND          hwndParentSheet;
  DWORD         offsetTitle;
  DSOBJECTNAMES dsObjectNames;
} DSA_SEC_PAGE_INFO, *PDSA_SEC_PAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="215fb-110">Member</span><span class="sxs-lookup"><span data-stu-id="215fb-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="215fb-111">**hwndparametrisheet**</span><span class="sxs-lookup"><span data-stu-id="215fb-111">**hwndParentSheet**</span></span>
</dt> <dd>

<span data-ttu-id="215fb-112">Enthält das Fenster Handle des übergeordneten Elements des sekundären Eigenschaften Blatts.</span><span class="sxs-lookup"><span data-stu-id="215fb-112">Contains the window handle of the parent of the secondary property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="215fb-113">**offsettitle**</span><span class="sxs-lookup"><span data-stu-id="215fb-113">**offsetTitle**</span></span>
</dt> <dd>

<span data-ttu-id="215fb-114">Enthält den Offset in Bytes vom Anfang der **DSA- \_ \_ Seiten \_ Info** Struktur zu einer auf NULL endenden Unicode-Zeichenfolge, die den Titel des sekundären Eigenschaften Blatts enthält.</span><span class="sxs-lookup"><span data-stu-id="215fb-114">Contains the offset, in bytes, from the start of the **DSA\_SEC\_PAGE\_INFO** structure to a NULL-terminated, Unicode string that contains the title of the secondary property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="215fb-115">**dsobjectnames**</span><span class="sxs-lookup"><span data-stu-id="215fb-115">**dsObjectNames**</span></span>
</dt> <dd>

<span data-ttu-id="215fb-116">Enthält eine [**dsobjectnames**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) -Struktur, die das sekundäre Eigenschaften Blatt definiert.</span><span class="sxs-lookup"><span data-stu-id="215fb-116">Contains a [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) structure that defines the secondary property sheet.</span></span> <span data-ttu-id="215fb-117">Es kann immer nur ein sekundäres Eigenschaften Blatt erstellt werden. Daher kann die **dsobjectnames** -Struktur nur eine [**dsobject**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) -Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="215fb-117">Only one secondary property sheet can be created at a time, so the **DSOBJECTNAMES** structure can only contain one [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="215fb-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="215fb-118">Requirements</span></span>



| <span data-ttu-id="215fb-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="215fb-119">Requirement</span></span> | <span data-ttu-id="215fb-120">Wert</span><span class="sxs-lookup"><span data-stu-id="215fb-120">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="215fb-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="215fb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="215fb-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="215fb-122">Windows Vista</span></span><br/>       |
| <span data-ttu-id="215fb-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="215fb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="215fb-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="215fb-124">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="215fb-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="215fb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="215fb-126">**WM- \_ adsprop- \_ Blatt \_ Erstellen**</span><span class="sxs-lookup"><span data-stu-id="215fb-126">**WM\_ADSPROP\_SHEET\_CREATE**</span></span>](wm-adsprop-sheet-create.md)
</dt> <dt>

[<span data-ttu-id="215fb-127">**WM \_ - \_ Blatt "DSA \_ Erstellen \_ "**</span><span class="sxs-lookup"><span data-stu-id="215fb-127">**WM\_DSA\_SHEET\_CREATE\_NOTIFY**</span></span>](wm-dsa-sheet-create-notify.md)
</dt> <dt>

[<span data-ttu-id="215fb-128">**Dsobjectnames**</span><span class="sxs-lookup"><span data-stu-id="215fb-128">**DSOBJECTNAMES**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[<span data-ttu-id="215fb-129">**Dsobject**</span><span class="sxs-lookup"><span data-stu-id="215fb-129">**DSOBJECT**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> </dl>

 

 





