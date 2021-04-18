---
description: Beachten Sie, dass diese Schnittstelle veraltet ist.
ms.assetid: d9800850-b0ee-44f7-bcb4-f2bac8d17693
title: Iamfilterdata-Schnittstelle (fil \_ Data. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData
api_type:
- COM
api_location:
- fil_data.h
ms.openlocfilehash: 1ab5ea8e9c90c043c33cca4d9f8138dd7d9937ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368368"
---
# <a name="iamfilterdata-interface"></a><span data-ttu-id="e908c-103">Iamfilterdata-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e908c-103">IAMFilterData interface</span></span>

> [!Note]  
> <span data-ttu-id="e908c-104">Diese Schnittstelle ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="e908c-104">This interface has been deprecated.</span></span> <span data-ttu-id="e908c-105">Neue Anwendungen sollten stattdessen die [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) -Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="e908c-105">New applications should use the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface instead.</span></span>

 

<span data-ttu-id="e908c-106">Die- `IAMFilterData` Schnittstelle konvertiert Filter Informationen in gepackte Binärdaten, die in der Registrierung gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="e908c-106">The `IAMFilterData` interface converts filter information to packed binary data, which can be stored in the registry.</span></span> <span data-ttu-id="e908c-107">Diese Schnittstelle wird vom filtermapper-Objekt verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="e908c-107">The Filter Mapper object exposes this interface.</span></span>

## <a name="members"></a><span data-ttu-id="e908c-108">Member</span><span class="sxs-lookup"><span data-stu-id="e908c-108">Members</span></span>

<span data-ttu-id="e908c-109">Die **iamfilterdata** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e908c-109">The **IAMFilterData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e908c-110">**Iamfilterdata** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e908c-110">**IAMFilterData** also has these types of members:</span></span>

-   [<span data-ttu-id="e908c-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="e908c-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e908c-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="e908c-112">Methods</span></span>

<span data-ttu-id="e908c-113">Die **iamfilterdata** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e908c-113">The **IAMFilterData** interface has these methods.</span></span>



| <span data-ttu-id="e908c-114">Methode</span><span class="sxs-lookup"><span data-stu-id="e908c-114">Method</span></span>                                                     | <span data-ttu-id="e908c-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e908c-115">Description</span></span>                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [<span data-ttu-id="e908c-116">**"Kreatefilterdata"**</span><span class="sxs-lookup"><span data-stu-id="e908c-116">**CreateFilterData**</span></span>](iamfilterdata-createfilterdata.md) | <span data-ttu-id="e908c-117">Erstellt binäre Registrierungsdaten für einen Filter.</span><span class="sxs-lookup"><span data-stu-id="e908c-117">Creates binary registry data for a filter.</span></span><br/>     |
| [<span data-ttu-id="e908c-118">**"Parameterfilterdata"**</span><span class="sxs-lookup"><span data-stu-id="e908c-118">**ParseFilterData**</span></span>](iamfilterdata-parsefilterdata.md)   | <span data-ttu-id="e908c-119">Entpackt die binären Registrierungsdaten für einen Filter.</span><span class="sxs-lookup"><span data-stu-id="e908c-119">Unpacks the binary registry data for a filter.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e908c-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e908c-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e908c-121">Der Header "fil \_ Data. h" befindet sich im Verzeichnis " [Mapper Sample](mapper-sample.md) " in der Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e908c-121">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e908c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e908c-122">Requirements</span></span>



| <span data-ttu-id="e908c-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e908c-123">Requirement</span></span> | <span data-ttu-id="e908c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e908c-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e908c-125">Header</span><span class="sxs-lookup"><span data-stu-id="e908c-125">Header</span></span><br/> | <dl> <span data-ttu-id="e908c-126"><dt>Fil- \_ Daten. h</dt></span><span class="sxs-lookup"><span data-stu-id="e908c-126"><dt>Fil\_data.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e908c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e908c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e908c-128">Veraltete Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="e908c-128">Deprecated Interfaces</span></span>](deprecated-interfaces.md)
</dt> </dl>

 

 
