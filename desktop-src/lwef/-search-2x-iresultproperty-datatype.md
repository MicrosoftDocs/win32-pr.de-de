---
title: Iresultproperty DataType-Eigenschaft (wdssharedidl. h)
description: Ein Properties-Datentyp.
ms.assetid: 2bf83256-0d69-48f2-aa7d-d34dcba17050
keywords:
- DataType-Eigenschaft Legacy-Windows-Umgebungs Features
- DataType-Eigenschaft Legacy-Windows-Umgebungs Funktionen, iresultproperty-Schnittstelle
- Iresultproperty-Schnittstelle Legacy Windows-Umgebungs Features, DataType-Eigenschaft
topic_type:
- apiref
api_name:
- IResultProperty.DataType
- IResultProperty.get_DataType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d887642594ed5ac7f78de1d4eac76fb4709f0dfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345906"
---
# <a name="iresultpropertydatatype-property"></a><span data-ttu-id="05197-106">Iresultproperty::D atatype-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="05197-106">IResultProperty::DataType property</span></span>

> [!NOTE]
> <span data-ttu-id="05197-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="05197-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="05197-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="05197-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="05197-109">Ein Properties-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="05197-109">A properties data type.</span></span>

<span data-ttu-id="05197-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="05197-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="05197-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="05197-111">Syntax</span></span>


```C++
HRESULT get_DataType(
  [out, retval] VARTYPE *vt
);
```



## <a name="property-value"></a><span data-ttu-id="05197-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="05197-112">Property value</span></span>

<span data-ttu-id="05197-113">Gibt einen Zeiger auf den Properties-Datentyp zurück.</span><span class="sxs-lookup"><span data-stu-id="05197-113">returns a pointer to the properties data type.</span></span>

## <a name="requirements"></a><span data-ttu-id="05197-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05197-114">Requirements</span></span>



| <span data-ttu-id="05197-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05197-115">Requirement</span></span> | <span data-ttu-id="05197-116">Wert</span><span class="sxs-lookup"><span data-stu-id="05197-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="05197-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05197-117">Minimum supported client</span></span><br/> | <span data-ttu-id="05197-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05197-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="05197-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05197-119">Minimum supported server</span></span><br/> | <span data-ttu-id="05197-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05197-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="05197-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="05197-121">Redistributable</span></span><br/>          | <span data-ttu-id="05197-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="05197-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="05197-123">Header</span><span class="sxs-lookup"><span data-stu-id="05197-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="05197-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="05197-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





