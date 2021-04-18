---
description: Die Eigenschaft Schreib geschützter Fehler des Merge-Objekts gibt eine Auflistung von Fehler Objekten zurück, die den aktuellen Satz von Fehlern ist.
ms.assetid: 619f17cc-131a-4262-ad48-9ab1318142aa
title: Merge. Errors-Eigenschaft (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Errors
- IMsmMerge.get_Errors
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9f07bdbba9fecf48001aed1fbcd42e02abb5c5c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351309"
---
# <a name="mergeerrors-property"></a><span data-ttu-id="718af-103">Merge. Errors-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="718af-103">Merge.Errors property</span></span>

<span data-ttu-id="718af-104">Die Eigenschaft Schreib geschützter **Fehler** des [**Merge**](merge-object.md) -Objekts gibt eine Auflistung von [**Fehler**](error-object.md) Objekten zurück, die den aktuellen Satz von Fehlern ist.</span><span class="sxs-lookup"><span data-stu-id="718af-104">The read-only **Errors** property of the [**Merge**](merge-object.md) object returns a collection of [**Error**](error-object.md) objects that is the current set of errors.</span></span>

<span data-ttu-id="718af-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="718af-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="718af-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="718af-106">Syntax</span></span>


```JScript
propVal = Merge.Errors
```



## <a name="property-value"></a><span data-ttu-id="718af-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="718af-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="718af-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="718af-108">Remarks</span></span>

<span data-ttu-id="718af-109">Der Abruf ist nicht destruktiv.</span><span class="sxs-lookup"><span data-stu-id="718af-109">The retrieval is non-destructive.</span></span> <span data-ttu-id="718af-110">Mehrere Instanzen der Fehlersammlung können durch wiederholtes Aufrufen dieser Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="718af-110">Multiple instances of the error collection may be retrieved by repeatedly calling this method.</span></span>

### <a name="c"></a><span data-ttu-id="718af-111">C++</span><span class="sxs-lookup"><span data-stu-id="718af-111">C++</span></span>

<span data-ttu-id="718af-112">Siehe [**get \_ Errors**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) function.</span><span class="sxs-lookup"><span data-stu-id="718af-112">See [**get\_Errors**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) Function.</span></span>

## <a name="requirements"></a><span data-ttu-id="718af-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="718af-113">Requirements</span></span>



| <span data-ttu-id="718af-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="718af-114">Requirement</span></span> | <span data-ttu-id="718af-115">Wert</span><span class="sxs-lookup"><span data-stu-id="718af-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="718af-116">Version</span><span class="sxs-lookup"><span data-stu-id="718af-116">Version</span></span><br/> | <span data-ttu-id="718af-117">Mergemod.dll 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="718af-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="718af-118">Header</span><span class="sxs-lookup"><span data-stu-id="718af-118">Header</span></span><br/>  | <dl> <span data-ttu-id="718af-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="718af-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="718af-120">DLL</span><span class="sxs-lookup"><span data-stu-id="718af-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="718af-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="718af-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
