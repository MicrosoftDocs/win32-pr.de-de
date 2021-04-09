---
title: Freesohattributevalue-Funktion (naputil. h)
description: Gibt eine sohattributevalue-Datenstruktur frei.
ms.assetid: 21647ee6-2ea2-45fd-b1f2-fb1836196f94
keywords:
- Freesohattributevalue-Funktion NAP
topic_type:
- apiref
api_name:
- FreeSoHAttributeValue
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bd56049eb727554227bd5eb509969f6795670a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040936"
---
# <a name="freesohattributevalue-function"></a><span data-ttu-id="29947-104">Freesohattributevalue-Funktion</span><span class="sxs-lookup"><span data-stu-id="29947-104">FreeSoHAttributeValue function</span></span>

> [!Note]  
> <span data-ttu-id="29947-105">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="29947-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="29947-106">Die **freesohattributevalue** -Funktion gibt eine [**sohattributevalue**](sohattributevalue-union.md) -Datenstruktur frei.</span><span class="sxs-lookup"><span data-stu-id="29947-106">The **FreeSoHAttributeValue** function frees an [**SoHAttributeValue**](sohattributevalue-union.md) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="29947-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="29947-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeSoHAttributeValue(
  _In_ SoHAttributeType  type,
  _In_ SoHAttributeValue *value
);
```



## <a name="parameters"></a><span data-ttu-id="29947-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="29947-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29947-109">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29947-109">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29947-110">Ein [**sohattributetype**](sohattributetype-enum.md) -Wert, der den Typ des SoH-Attribut Werts angibt, der freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="29947-110">A [**SoHAttributeType**](sohattributetype-enum.md) value that specifies the type of SoH attribute value to free.</span></span>

</dd> <dt>

<span data-ttu-id="29947-111">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29947-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29947-112">Ein Zeiger auf den freien [**sohattributevalue-Wert**](sohattributevalue-union.md) .</span><span class="sxs-lookup"><span data-stu-id="29947-112">A pointer to the [**SoHAttributeValue**](sohattributevalue-union.md) to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29947-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29947-113">Remarks</span></span>

<span data-ttu-id="29947-114">Alle vom NAP-System unterstützten com-Schnittstellen verwenden Standard-com-Speicher Verwaltungsregeln und die com-Speicher Belegungs Funktion (**cotaskmembelegc** und **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="29947-114">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="29947-115">**In** -Parameter werden vom Aufrufer zugeordnet und freigegeben.</span><span class="sxs-lookup"><span data-stu-id="29947-115">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="29947-116">Out-Parameter werden vom **aufgerufenen** zugeordnet und vom Aufrufer mithilfe von **cotaskmem** freigegeben.</span><span class="sxs-lookup"><span data-stu-id="29947-116">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="29947-117">**In/out-** Parameter werden vom Aufrufer zugeordnet, vom aufgerufenen freigegeben und neu zugeordnet und schließlich mit **cotaskmem** vom Aufrufer freigegeben.</span><span class="sxs-lookup"><span data-stu-id="29947-117">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="29947-118">Alle NAP-Funktionen zum Freigeben von Speicher freigeben auch alle eingebetteten Zeiger.</span><span class="sxs-lookup"><span data-stu-id="29947-118">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="29947-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29947-119">Requirements</span></span>



| <span data-ttu-id="29947-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29947-120">Requirement</span></span> | <span data-ttu-id="29947-121">Wert</span><span class="sxs-lookup"><span data-stu-id="29947-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="29947-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29947-122">Minimum supported client</span></span><br/> | <span data-ttu-id="29947-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29947-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="29947-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29947-124">Minimum supported server</span></span><br/> | <span data-ttu-id="29947-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29947-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="29947-126">Header</span><span class="sxs-lookup"><span data-stu-id="29947-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="29947-127"><dt>Naputil. h</dt></span><span class="sxs-lookup"><span data-stu-id="29947-127"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="29947-128">DLL</span><span class="sxs-lookup"><span data-stu-id="29947-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29947-129"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29947-129"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





