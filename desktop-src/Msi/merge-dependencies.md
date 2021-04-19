---
description: Die Eigenschaft schreibgeschützte Abhängigkeiten des Merge-Objekts gibt eine Auflistung von Abhängigkeits Objekten zurück, die einen Satz von nicht erfüllten Abhängigkeiten für die aktuelle Datenbank auflistet.
ms.assetid: d7081ffe-3d9e-486e-84b6-b45e92fff5f0
title: Merge. Abhängigkeiten-Eigenschaft (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Dependencies
- IMsmMerge.get_Dependencies
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4c92d24ac2172b0d14de8e0609a407f2a0808494
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369690"
---
# <a name="mergedependencies-property"></a><span data-ttu-id="75b23-103">Merge. Abhängigkeiten (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="75b23-103">Merge.Dependencies property</span></span>

<span data-ttu-id="75b23-104">Die Eigenschaft schreibgeschützte **Abhängigkeiten** des [**Merge**](merge-object.md) -Objekts gibt eine Auflistung von [**Abhängigkeits**](dependency-object.md) Objekten zurück, die einen Satz von nicht erfüllten Abhängigkeiten für die aktuelle Datenbank auflistet.</span><span class="sxs-lookup"><span data-stu-id="75b23-104">The read-only **Dependencies** property of the [**Merge**](merge-object.md) object returns a collection of [**Dependency**](dependency-object.md) objects that enumerates a set of unsatisfied dependencies for the current database.</span></span>

<span data-ttu-id="75b23-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="75b23-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="75b23-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="75b23-106">Syntax</span></span>


```JScript
propVal = Merge.Dependencies
```



## <a name="property-value"></a><span data-ttu-id="75b23-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="75b23-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="75b23-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75b23-108">Remarks</span></span>

<span data-ttu-id="75b23-109">Ein Modul muss nicht geöffnet sein, um Abhängigkeitsinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="75b23-109">A module does not need to be open to retrieve dependency information.</span></span>

### <a name="c"></a><span data-ttu-id="75b23-110">C++</span><span class="sxs-lookup"><span data-stu-id="75b23-110">C++</span></span>

<span data-ttu-id="75b23-111">Weitere Informationen finden [**Sie unter Get- \_ Abhängigkeiten**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_dependencies)</span><span class="sxs-lookup"><span data-stu-id="75b23-111">See [**get\_Dependencies**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_dependencies) Function.</span></span>

## <a name="requirements"></a><span data-ttu-id="75b23-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75b23-112">Requirements</span></span>



| <span data-ttu-id="75b23-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75b23-113">Requirement</span></span> | <span data-ttu-id="75b23-114">Wert</span><span class="sxs-lookup"><span data-stu-id="75b23-114">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75b23-115">Version</span><span class="sxs-lookup"><span data-stu-id="75b23-115">Version</span></span><br/> | <span data-ttu-id="75b23-116">Mergemod.dll 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="75b23-116">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="75b23-117">Header</span><span class="sxs-lookup"><span data-stu-id="75b23-117">Header</span></span><br/>  | <dl> <span data-ttu-id="75b23-118"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="75b23-118"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="75b23-119">DLL</span><span class="sxs-lookup"><span data-stu-id="75b23-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="75b23-120"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75b23-120"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
