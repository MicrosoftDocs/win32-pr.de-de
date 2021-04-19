---
description: Ruft Hilfsfunktionen für die IDispatch-Schnittstelle auf.
ms.assetid: ccef47af-d9dd-48c3-93d3-ee997dacf7a8
title: Invokeidispatch-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InvokeIDispatch
api_type:
- LibDef
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: e4989e3ec23a1ffa97ba317831143ecf0920ef9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349929"
---
# <a name="invokeidispatch-function"></a><span data-ttu-id="26906-103">Invokeidispatch-Funktion</span><span class="sxs-lookup"><span data-stu-id="26906-103">InvokeIDispatch function</span></span>

<span data-ttu-id="26906-104">Ruft Hilfsfunktionen für die IDispatch-Schnittstelle auf.</span><span class="sxs-lookup"><span data-stu-id="26906-104">Invokes helper functionality for the IDispatch interface.</span></span>

<span data-ttu-id="26906-105">Diese Funktion ist nicht für die Verwendung durch den Anwendungscode vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="26906-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="26906-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="26906-106">Syntax</span></span>


```C++
HRESULT WINAPI InvokeIDispatch(
        IDispatch  *pDispatch,
        DISPID     dispid,
        DISPPARAMS *pDisp,
  _Out_ VARIANT    *pVarResult
);
```



## <a name="parameters"></a><span data-ttu-id="26906-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="26906-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26906-108">*pdispatch*</span><span class="sxs-lookup"><span data-stu-id="26906-108">*pDispatch*</span></span> 
</dt> <dd>

<span data-ttu-id="26906-109">Die Instanz der IDispatch-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="26906-109">The instance of the IDispatch interface.</span></span>

</dd> <dt>

<span data-ttu-id="26906-110">*DISPID*</span><span class="sxs-lookup"><span data-stu-id="26906-110">*dispid*</span></span> 
</dt> <dd>

<span data-ttu-id="26906-111">Die Methode, die Eigenschaft oder das Argument, das übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="26906-111">The method, property, or argument to pass in.</span></span>

</dd> <dt>

<span data-ttu-id="26906-112">*pDisp*</span><span class="sxs-lookup"><span data-stu-id="26906-112">*pDisp*</span></span> 
</dt> <dd>

<span data-ttu-id="26906-113">Die Parameter, die übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="26906-113">The parameters to pass in.</span></span>

</dd> <dt>

<span data-ttu-id="26906-114">*pVarResult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="26906-114">*pVarResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26906-115">Eine-Struktur, die die abgerufenen Werte empfängt.</span><span class="sxs-lookup"><span data-stu-id="26906-115">A structure that receives the retrieved values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26906-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26906-116">Return value</span></span>

<span data-ttu-id="26906-117">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="26906-117">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="26906-118">Wenn ein Fehler auftritt, enthalten mögliche Rückgabecodes die in der folgenden Tabelle aufgeführten Werte, sind jedoch nicht darauf beschränkt.</span><span class="sxs-lookup"><span data-stu-id="26906-118">If it fails, possible return codes include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="26906-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="26906-119">Return code</span></span>                                                                                  | <span data-ttu-id="26906-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26906-120">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="26906-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="26906-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="26906-122">Der Wert für *pdispatch* ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="26906-122">The value for *pDispatch* is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="26906-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26906-123">Requirements</span></span>



| <span data-ttu-id="26906-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26906-124">Requirement</span></span> | <span data-ttu-id="26906-125">Wert</span><span class="sxs-lookup"><span data-stu-id="26906-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26906-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26906-126">Minimum supported client</span></span><br/> | <span data-ttu-id="26906-127">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26906-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="26906-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26906-128">Minimum supported server</span></span><br/> | <span data-ttu-id="26906-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="26906-129">None supported</span></span><br/>                                                             |
| <span data-ttu-id="26906-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="26906-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="26906-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26906-131"><dt>InkObj.dll</dt></span></span> </dl> |



 

 




