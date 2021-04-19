---
description: Mit der Connect-Methode des Merge-Objekts wird ein Modul mit einer zusätzlichen Funktion verbunden. Das Modul muss bereits in der Datenbank zusammengeführt worden sein oder in der Datenbank zusammengeführt werden. Die Funktion muss vorhanden sein, bevor diese Funktion aufgerufen wird.
ms.assetid: 1c1ef664-792c-4cdc-b468-1ffe0b7810a5
title: Merge. Connect-Methode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Connect
- IMsmMerge.Connect
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: da66f7dfe4203e80d4778ae9b39c665a66164384
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358369"
---
# <a name="mergeconnect-method"></a><span data-ttu-id="d6a9c-105">Merge. Connect-Methode</span><span class="sxs-lookup"><span data-stu-id="d6a9c-105">Merge.Connect method</span></span>

<span data-ttu-id="d6a9c-106">Mit der **Connect** -Methode des [**Merge**](merge-object.md) -Objekts wird ein Modul mit einer zusätzlichen Funktion verbunden.</span><span class="sxs-lookup"><span data-stu-id="d6a9c-106">The **Connect** method of the [**Merge**](merge-object.md) object connects a module to an additional feature.</span></span> <span data-ttu-id="d6a9c-107">Das Modul muss bereits in der Datenbank zusammengeführt worden sein oder in der Datenbank zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d6a9c-107">The module must have already been merged into the database or will be merged into the database.</span></span> <span data-ttu-id="d6a9c-108">Die Funktion muss vorhanden sein, bevor diese Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d6a9c-108">The feature must exist before calling this function.</span></span>

<span data-ttu-id="d6a9c-109">An der Datenbank vorgenommene Änderungen werden nicht auf dem Datenträger gespeichert, es sei denn, die [**CloseDatabase**](merge-closedatabase.md) -Methode wird aufgerufen, wenn *bcommit* auf **true** festgelegt</span><span class="sxs-lookup"><span data-stu-id="d6a9c-109">Changes made to the database are not saved to disk unless the [**CloseDatabase**](merge-closedatabase.md) method is called with *bCommit* set to **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6a9c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6a9c-110">Syntax</span></span>


```JScript
Merge.Connect(
  Feature
)
```



## <a name="parameters"></a><span data-ttu-id="d6a9c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6a9c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6a9c-112">*Feature*</span><span class="sxs-lookup"><span data-stu-id="d6a9c-112">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="d6a9c-113">Der Name eines Features, das bereits in der Datenbank vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d6a9c-113">The name of a feature already existing in the database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6a9c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6a9c-114">Return value</span></span>

<span data-ttu-id="d6a9c-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d6a9c-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6a9c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6a9c-116">Remarks</span></span>

<span data-ttu-id="d6a9c-117">Fehler können mithilfe der [**Errors**](merge-errors.md) -Eigenschaft abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d6a9c-117">Errors may be retrieved through the [**Errors**](merge-errors.md) property.</span></span> <span data-ttu-id="d6a9c-118">Fehler und Informationsmeldungen werden in der aktuellen Protokolldatei gepostet.</span><span class="sxs-lookup"><span data-stu-id="d6a9c-118">Errors and informational messages are posted to the current log file.</span></span>

### <a name="c"></a><span data-ttu-id="d6a9c-119">C++</span><span class="sxs-lookup"><span data-stu-id="d6a9c-119">C++</span></span>

<span data-ttu-id="d6a9c-120">Siehe [**Connect**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="d6a9c-120">See [**Connect**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6a9c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6a9c-121">Requirements</span></span>



| <span data-ttu-id="d6a9c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6a9c-122">Requirement</span></span> | <span data-ttu-id="d6a9c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d6a9c-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6a9c-124">Version</span><span class="sxs-lookup"><span data-stu-id="d6a9c-124">Version</span></span><br/> | <span data-ttu-id="d6a9c-125">Mergemod.dll 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="d6a9c-125">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="d6a9c-126">Header</span><span class="sxs-lookup"><span data-stu-id="d6a9c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d6a9c-127"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6a9c-127"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6a9c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d6a9c-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="d6a9c-129"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6a9c-129"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
