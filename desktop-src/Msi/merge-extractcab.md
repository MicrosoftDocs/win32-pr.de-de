---
description: Die ExtractCab-Methode des Merge-Objekts extrahiert die eingebettete CAB-Datei aus einem Modul und speichert Sie als die angegebene Datei. Das Installationsprogramm erstellt diese Datei, wenn Sie noch nicht vorhanden ist, und wird überschrieben, wenn Sie vorhanden ist.
ms.assetid: a6fe8b69-8f4a-45f7-b7e6-7620a00500bb
title: Merge. ExtractCab-Methode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractCAB
- IMsmMerge.ExtractCAB
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d0bdc79fb0087456d035bf732faca384b35b2a9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359231"
---
# <a name="mergeextractcab-method"></a><span data-ttu-id="6c6a0-104">Merge. ExtractCab-Methode</span><span class="sxs-lookup"><span data-stu-id="6c6a0-104">Merge.ExtractCAB method</span></span>

<span data-ttu-id="6c6a0-105">Die **ExtractCab** -Methode des [**Merge**](merge-object.md) -Objekts extrahiert die eingebettete CAB-Datei aus einem Modul und speichert Sie als die angegebene Datei.</span><span class="sxs-lookup"><span data-stu-id="6c6a0-105">The **ExtractCAB** method of the [**Merge**](merge-object.md) object extracts the embedded .cab file from a module and saves it as the specified file.</span></span> <span data-ttu-id="6c6a0-106">Das Installationsprogramm erstellt diese Datei, wenn Sie noch nicht vorhanden ist, und wird überschrieben, wenn Sie vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6c6a0-106">The installer creates this file if it does not already exist and overwritten if it does exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c6a0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c6a0-107">Syntax</span></span>


```JScript
Merge.ExtractCAB(
  FileName
)
```



## <a name="parameters"></a><span data-ttu-id="6c6a0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c6a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c6a0-109">*FileName*</span><span class="sxs-lookup"><span data-stu-id="6c6a0-109">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="6c6a0-110">Die voll qualifizierte Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="6c6a0-110">The fully qualified destination file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c6a0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c6a0-111">Return value</span></span>

<span data-ttu-id="6c6a0-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6c6a0-112">This method does not return a value.</span></span>

## <a name="c"></a><span data-ttu-id="6c6a0-113">C++</span><span class="sxs-lookup"><span data-stu-id="6c6a0-113">C++</span></span>

<span data-ttu-id="6c6a0-114">Siehe [**ExtractCab**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="6c6a0-114">See [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c6a0-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c6a0-115">Requirements</span></span>



| <span data-ttu-id="6c6a0-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c6a0-116">Requirement</span></span> | <span data-ttu-id="6c6a0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6c6a0-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c6a0-118">Version</span><span class="sxs-lookup"><span data-stu-id="6c6a0-118">Version</span></span><br/> | <span data-ttu-id="6c6a0-119">Mergemod.dll 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="6c6a0-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="6c6a0-120">Header</span><span class="sxs-lookup"><span data-stu-id="6c6a0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="6c6a0-121"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c6a0-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c6a0-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6c6a0-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="6c6a0-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c6a0-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
