---
title: Freenapcomponentregistrationinfoarray-Funktion (naputil. h)
description: Gibt eine angegebene Anzahl von napcomponentregistrationinfo-Datenstrukturen aus einem Array frei.
ms.assetid: 6fcb1394-04dd-4d8a-87f7-6b69b6ef29ff
keywords:
- Freenapcomponentregistrationinfoarray-Funktion NAP
topic_type:
- apiref
api_name:
- FreeNapComponentRegistrationInfoArray
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df823ad8086c57a6ee193bd0d58678786cfe325b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105417"
---
# <a name="freenapcomponentregistrationinfoarray-function"></a><span data-ttu-id="f2d28-104">Freenapcomponentregistrationinfoarray-Funktion</span><span class="sxs-lookup"><span data-stu-id="f2d28-104">FreeNapComponentRegistrationInfoArray function</span></span>

> [!Note]  
> <span data-ttu-id="f2d28-105">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f2d28-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f2d28-106">Die **freenapcomponentregistrationinfoarray** -Funktion gibt eine angegebene Anzahl von [**napcomponentregistrationinfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) -Datenstrukturen aus einem Array frei.</span><span class="sxs-lookup"><span data-stu-id="f2d28-106">The **FreeNapComponentRegistrationInfoArray** function frees a specified number of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) data structures from an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2d28-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2d28-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeNapComponentRegistrationInfoArray(
  _In_ UINT16                       count,
  _In_ NapComponentRegistrationInfo **info
);
```



## <a name="parameters"></a><span data-ttu-id="f2d28-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2d28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2d28-109">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2d28-109">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2d28-110">Die Anzahl der [**napcomponentregistrationinfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) -Strukturen in *Informationen* , die freigegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f2d28-110">The number of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structures in *info* to free.</span></span>

</dd> <dt>

<span data-ttu-id="f2d28-111">*Info* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2d28-111">*info* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2d28-112">Ein Zeiger auf ein Array von [**napcomponentregistrationinfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) -Datenstrukturen, die freigegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f2d28-112">A pointer to an array of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) data structures to be freed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2d28-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2d28-113">Remarks</span></span>

<span data-ttu-id="f2d28-114">Alle vom NAP-System unterstützten com-Schnittstellen verwenden Standard-com-Speicher Verwaltungsregeln und die com-Speicher Belegungs Funktion (**cotaskmembelegc** und **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="f2d28-114">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="f2d28-115">**In** -Parameter werden vom Aufrufer zugeordnet und freigegeben.</span><span class="sxs-lookup"><span data-stu-id="f2d28-115">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="f2d28-116">Out-Parameter werden vom **aufgerufenen** zugeordnet und vom Aufrufer mithilfe von **cotaskmem** freigegeben.</span><span class="sxs-lookup"><span data-stu-id="f2d28-116">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="f2d28-117">**In/out-** Parameter werden vom Aufrufer zugeordnet, vom aufgerufenen freigegeben und neu zugeordnet und schließlich mit **cotaskmem** vom Aufrufer freigegeben.</span><span class="sxs-lookup"><span data-stu-id="f2d28-117">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="f2d28-118">Alle NAP-Funktionen zum Freigeben von Speicher freigeben auch alle eingebetteten Zeiger.</span><span class="sxs-lookup"><span data-stu-id="f2d28-118">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2d28-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2d28-119">Requirements</span></span>



| <span data-ttu-id="f2d28-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2d28-120">Requirement</span></span> | <span data-ttu-id="f2d28-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f2d28-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f2d28-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2d28-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f2d28-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2d28-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f2d28-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2d28-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f2d28-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2d28-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f2d28-126">Header</span><span class="sxs-lookup"><span data-stu-id="f2d28-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2d28-127"><dt>Naputil. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2d28-127"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="f2d28-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f2d28-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2d28-129"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2d28-129"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





