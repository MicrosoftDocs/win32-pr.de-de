---
description: Erfahren Sie mehr über die IAMFilterData-Schnittstelle, die Filterinformationen in gepackte Binärdaten konvertiert. Diese Schnittstelle ist veraltet.
ms.assetid: d9800850-b0ee-44f7-bcb4-f2bac8d17693
title: IAMFilterData-Schnittstelle (Fil \_ data.h)
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
ms.openlocfilehash: 1e43e0f16ddfdee596f0dc6bd736ed86fc6fa37d
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989435"
---
# <a name="iamfilterdata-interface"></a><span data-ttu-id="d429a-104">IAMFilterData-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d429a-104">IAMFilterData interface</span></span>

> [!Note]  
> <span data-ttu-id="d429a-105">Diese Schnittstelle ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="d429a-105">This interface has been deprecated.</span></span> <span data-ttu-id="d429a-106">Neue Anwendungen sollten stattdessen die [**IFilterMapper2-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) verwenden.</span><span class="sxs-lookup"><span data-stu-id="d429a-106">New applications should use the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface instead.</span></span>

 

<span data-ttu-id="d429a-107">Die `IAMFilterData` -Schnittstelle konvertiert Filterinformationen in gepackte Binärdaten, die in der Registrierung gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="d429a-107">The `IAMFilterData` interface converts filter information to packed binary data, which can be stored in the registry.</span></span> <span data-ttu-id="d429a-108">Das Filterzuordnungsobjekt macht diese Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d429a-108">The Filter Mapper object exposes this interface.</span></span>

## <a name="members"></a><span data-ttu-id="d429a-109">Member</span><span class="sxs-lookup"><span data-stu-id="d429a-109">Members</span></span>

<span data-ttu-id="d429a-110">Die **IAMFilterData-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="d429a-110">The **IAMFilterData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d429a-111">**IAMFilterData** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d429a-111">**IAMFilterData** also has these types of members:</span></span>

-   [<span data-ttu-id="d429a-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="d429a-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d429a-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="d429a-113">Methods</span></span>

<span data-ttu-id="d429a-114">Die **IAMFilterData-Schnittstelle** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d429a-114">The **IAMFilterData** interface has these methods.</span></span>



| <span data-ttu-id="d429a-115">Methode</span><span class="sxs-lookup"><span data-stu-id="d429a-115">Method</span></span>                                                     | <span data-ttu-id="d429a-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d429a-116">Description</span></span>                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [<span data-ttu-id="d429a-117">**CreateFilterData**</span><span class="sxs-lookup"><span data-stu-id="d429a-117">**CreateFilterData**</span></span>](iamfilterdata-createfilterdata.md) | <span data-ttu-id="d429a-118">Erstellt binäre Registrierungsdaten für einen Filter.</span><span class="sxs-lookup"><span data-stu-id="d429a-118">Creates binary registry data for a filter.</span></span><br/>     |
| [<span data-ttu-id="d429a-119">**ParseFilterData**</span><span class="sxs-lookup"><span data-stu-id="d429a-119">**ParseFilterData**</span></span>](iamfilterdata-parsefilterdata.md)   | <span data-ttu-id="d429a-120">Entpackt die binären Registrierungsdaten für einen Filter.</span><span class="sxs-lookup"><span data-stu-id="d429a-120">Unpacks the binary registry data for a filter.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d429a-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d429a-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d429a-122">Der Header Fil \_ data.h befindet sich im Verzeichnis [Mapper Sample](mapper-sample.md) im Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d429a-122">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d429a-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d429a-123">Requirements</span></span>



| <span data-ttu-id="d429a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d429a-124">Requirement</span></span> | <span data-ttu-id="d429a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="d429a-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d429a-126">Header</span><span class="sxs-lookup"><span data-stu-id="d429a-126">Header</span></span><br/> | <dl> <span data-ttu-id="d429a-127"><dt>Fil \_ data.h</dt></span><span class="sxs-lookup"><span data-stu-id="d429a-127"><dt>Fil\_data.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d429a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d429a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d429a-129">Veraltete Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d429a-129">Deprecated Interfaces</span></span>](deprecated-interfaces.md)
</dt> </dl>

 

 
