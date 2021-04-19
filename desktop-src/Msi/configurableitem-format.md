---
description: Die Format-Eigenschaft des configurableitem-Objekts gibt den Wert aus der Spalte Format der Tabelle ModuleConfiguration zurück.
ms.assetid: e75ed650-7309-4e24-9c35-82ebf27d011b
title: Configurableitem. Format-Eigenschaft (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem.Format
- IMsmConfigurableItem.get_Format
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 20db09126e9b10aac5c31a3748c4f1606f3f3bab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366691"
---
# <a name="configurableitemformat-property"></a><span data-ttu-id="3acdb-103">Configurableitem. Format (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3acdb-103">ConfigurableItem.Format property</span></span>

<span data-ttu-id="3acdb-104">Die **Format** -Eigenschaft des [**configurableitem**](configurableitem-object.md) -Objekts gibt den Wert aus der Spalte Format der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="3acdb-104">The **Format** property of the [**ConfigurableItem**](configurableitem-object.md) object returns the value from the Format column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="3acdb-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3acdb-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3acdb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3acdb-106">Syntax</span></span>


```JScript
propVal = ConfigurableItem.Format
```



## <a name="property-value"></a><span data-ttu-id="3acdb-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3acdb-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="3acdb-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3acdb-108">Remarks</span></span>

<span data-ttu-id="3acdb-109">Diese Eigenschaft kann nur die folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3acdb-109">This property can only have the following values.</span></span>



| <span data-ttu-id="3acdb-110">Konstante</span><span class="sxs-lookup"><span data-stu-id="3acdb-110">Constant</span></span>                        | <span data-ttu-id="3acdb-111">Wert</span><span class="sxs-lookup"><span data-stu-id="3acdb-111">Value</span></span> |
|---------------------------------|-------|
| <span data-ttu-id="3acdb-112">**msmconfigurableitemtext**</span><span class="sxs-lookup"><span data-stu-id="3acdb-112">**msmConfigurableItemText**</span></span>     | <span data-ttu-id="3acdb-113">0</span><span class="sxs-lookup"><span data-stu-id="3acdb-113">0</span></span>     |
| <span data-ttu-id="3acdb-114">**msmconfigurableitemkey**</span><span class="sxs-lookup"><span data-stu-id="3acdb-114">**msmConfigurableItemKey**</span></span>      | <span data-ttu-id="3acdb-115">1</span><span class="sxs-lookup"><span data-stu-id="3acdb-115">1</span></span>     |
| <span data-ttu-id="3acdb-116">**msmconfigurableiteminteger**</span><span class="sxs-lookup"><span data-stu-id="3acdb-116">**msmConfigurableItemInteger**</span></span>  | <span data-ttu-id="3acdb-117">2</span><span class="sxs-lookup"><span data-stu-id="3acdb-117">2</span></span>     |
| <span data-ttu-id="3acdb-118">**msmconfigurableitembitfield**</span><span class="sxs-lookup"><span data-stu-id="3acdb-118">**msmConfigurableItemBitfield**</span></span> | <span data-ttu-id="3acdb-119">3</span><span class="sxs-lookup"><span data-stu-id="3acdb-119">3</span></span>     |



 

### <a name="c"></a><span data-ttu-id="3acdb-120">C++</span><span class="sxs-lookup"><span data-stu-id="3acdb-120">C++</span></span>

<span data-ttu-id="3acdb-121">Siehe [**get \_ Format**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) function.</span><span class="sxs-lookup"><span data-stu-id="3acdb-121">See [**get\_Format**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3acdb-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3acdb-122">Requirements</span></span>



| <span data-ttu-id="3acdb-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3acdb-123">Requirement</span></span> | <span data-ttu-id="3acdb-124">Wert</span><span class="sxs-lookup"><span data-stu-id="3acdb-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3acdb-125">Version</span><span class="sxs-lookup"><span data-stu-id="3acdb-125">Version</span></span><br/> | <span data-ttu-id="3acdb-126">Mergemod.dll 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="3acdb-126">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="3acdb-127">Header</span><span class="sxs-lookup"><span data-stu-id="3acdb-127">Header</span></span><br/>  | <dl> <span data-ttu-id="3acdb-128"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="3acdb-128"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="3acdb-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3acdb-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="3acdb-130"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3acdb-130"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




