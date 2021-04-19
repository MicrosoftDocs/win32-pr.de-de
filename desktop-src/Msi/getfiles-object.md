---
description: Das GetFiles-Objekt ruft die erforderlichen Dateien in einer bestimmten Sprache des Moduls ab. Erfordert, dass bestimmte Aktionen über das Merge-Objekt durchgeführt werden, bevor alle Teile dieser Schnittstelle gültige Ergebnisse zurückgeben.
ms.assetid: f3bf64ec-75f7-43a6-bbd8-a51508c57002
title: GetFiles-Objekt (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles
- IMsmGetFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8a26bb072b0b4a1f048ded76fbd52ffc6d42de62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369260"
---
# <a name="getfiles-object"></a><span data-ttu-id="7716a-104">GetFiles-Objekt</span><span class="sxs-lookup"><span data-stu-id="7716a-104">GetFiles object</span></span>

<span data-ttu-id="7716a-105">Das **GetFiles** -Objekt ruft die erforderlichen Dateien in einer bestimmten Sprache des Moduls ab.</span><span class="sxs-lookup"><span data-stu-id="7716a-105">The **GetFiles** object retrieves the files needed in a particular language of the module.</span></span> <span data-ttu-id="7716a-106">Erfordert, dass bestimmte Aktionen über das [Merge-Objekt](merge-object.md) durchgeführt werden, bevor alle Teile dieser Schnittstelle gültige Ergebnisse zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7716a-106">Requires certain actions be performed through the [Merge object](merge-object.md) before all parts of this interface returns valid results.</span></span>

## <a name="members"></a><span data-ttu-id="7716a-107">Member</span><span class="sxs-lookup"><span data-stu-id="7716a-107">Members</span></span>

<span data-ttu-id="7716a-108">Das **GetFiles** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7716a-108">The **GetFiles** object has these types of members:</span></span>

-   [<span data-ttu-id="7716a-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7716a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7716a-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7716a-110">Properties</span></span>

<span data-ttu-id="7716a-111">Das **GetFiles** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7716a-111">The **GetFiles** object has these properties.</span></span>



| <span data-ttu-id="7716a-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7716a-112">Property</span></span>                                               | <span data-ttu-id="7716a-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7716a-113">Description</span></span>                                                                                                                                                     |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7716a-114">**Modulefiles**</span><span class="sxs-lookup"><span data-stu-id="7716a-114">**ModuleFiles**</span></span>](getfiles-modulefiles.md)<br/> | <span data-ttu-id="7716a-115">Die [**Modulefiles**](getfiles-modulefiles.md) -Eigenschaft gibt alle Primärschlüssel der [Dateitabelle](file-table.md) für das aktuell geöffnete Modul zurück.</span><span class="sxs-lookup"><span data-stu-id="7716a-115">[**ModuleFiles**](getfiles-modulefiles.md) property returns all the primary keys of the [File table](file-table.md) for the currently open module.</span></span><br/> |



 

## <a name="c"></a><span data-ttu-id="7716a-116">C++</span><span class="sxs-lookup"><span data-stu-id="7716a-116">C++</span></span>

<span data-ttu-id="7716a-117">Schnittstelle **imsmgetfiles: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="7716a-117">interface **IMsmGetFiles : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="7716a-118">Schnittstellen-ID</span><span class="sxs-lookup"><span data-stu-id="7716a-118">Interface ID</span></span>



| <span data-ttu-id="7716a-119">Konstante</span><span class="sxs-lookup"><span data-stu-id="7716a-119">Constant</span></span>              | <span data-ttu-id="7716a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7716a-120">Value</span></span>                                  |
|-----------------------|----------------------------------------|
| <span data-ttu-id="7716a-121">**IID \_ imsmgetfiles**</span><span class="sxs-lookup"><span data-stu-id="7716a-121">**IID\_IMsmGetFiles**</span></span> | <span data-ttu-id="7716a-122">{7041ae26-2d78-11d2-888a-00a0c981b015}</span><span class="sxs-lookup"><span data-stu-id="7716a-122">{7041AE26-2D78-11D2-888A-00A0C981B015}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="7716a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7716a-123">Requirements</span></span>



| <span data-ttu-id="7716a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7716a-124">Requirement</span></span> | <span data-ttu-id="7716a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7716a-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7716a-126">Version</span><span class="sxs-lookup"><span data-stu-id="7716a-126">Version</span></span><br/> | <span data-ttu-id="7716a-127">Mergemod.dll 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="7716a-127">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="7716a-128">Header</span><span class="sxs-lookup"><span data-stu-id="7716a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7716a-129"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="7716a-129"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="7716a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7716a-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="7716a-131"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7716a-131"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




