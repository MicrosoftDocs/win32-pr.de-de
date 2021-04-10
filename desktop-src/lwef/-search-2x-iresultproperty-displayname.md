---
title: Iresultproperty DisplayName-Eigenschaft (wdssharedidl. h)
description: Lokalisierter Anzeige Name der Eigenschaft.
ms.assetid: 8f9e118a-9e92-4919-afe1-735c61af38f7
keywords:
- Display Name-Eigenschaft Legacy-Windows-Umgebungs Features
- Display Name-Eigenschaft Legacy-Windows-Umgebungs Funktionen, iresultproperty-Schnittstelle
- Iresultproperty-Schnittstelle Legacy Windows-Umgebungs Features, Display Name-Eigenschaft
topic_type:
- apiref
api_name:
- IResultProperty.DisplayName
- IResultProperty.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f36aa934d2ddf31d841478cef1cb9a33b0531224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104553"
---
# <a name="iresultpropertydisplayname-property"></a><span data-ttu-id="98dde-106">Iresultproperty::D isplayname-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="98dde-106">IResultProperty::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="98dde-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="98dde-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="98dde-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="98dde-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="98dde-109">Lokalisierter Anzeige Name der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="98dde-109">Localized display name of the property.</span></span>

<span data-ttu-id="98dde-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="98dde-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="98dde-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="98dde-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="98dde-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="98dde-112">Property value</span></span>

<span data-ttu-id="98dde-113">Gibt einen Zeiger auf den lokalisierten anzeigen Amen zurück.</span><span class="sxs-lookup"><span data-stu-id="98dde-113">returns a pointer to the localized display name.</span></span>

## <a name="requirements"></a><span data-ttu-id="98dde-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98dde-114">Requirements</span></span>



| <span data-ttu-id="98dde-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98dde-115">Requirement</span></span> | <span data-ttu-id="98dde-116">Wert</span><span class="sxs-lookup"><span data-stu-id="98dde-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="98dde-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98dde-117">Minimum supported client</span></span><br/> | <span data-ttu-id="98dde-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98dde-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="98dde-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98dde-119">Minimum supported server</span></span><br/> | <span data-ttu-id="98dde-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98dde-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="98dde-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="98dde-121">Redistributable</span></span><br/>          | <span data-ttu-id="98dde-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="98dde-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="98dde-123">Header</span><span class="sxs-lookup"><span data-stu-id="98dde-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="98dde-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="98dde-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





