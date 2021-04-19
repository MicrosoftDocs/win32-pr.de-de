---
description: Leitet die Arbeit zum Auflösen von verzögert geladenen Importen aus der übergeordneten Binärdatei in eine Ziel Binärdatei weiter.
ms.assetid: 65629d7b-36b0-426b-a20d-ec736b8461dc
title: Resolvedelta-loadsfromdll-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadsFromDll
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: a0fb517de7384a964c21c9e1a0a3e695a0d6e6cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370816"
---
# <a name="resolvedelayloadsfromdll-function"></a><span data-ttu-id="2f409-103">Resolvedelta-loadsfromdll-Funktion</span><span class="sxs-lookup"><span data-stu-id="2f409-103">ResolveDelayLoadsFromDll function</span></span>

<span data-ttu-id="2f409-104">Leitet die Arbeit zum Auflösen von verzögert geladenen Importen aus der übergeordneten Binärdatei in eine Ziel Binärdatei weiter.</span><span class="sxs-lookup"><span data-stu-id="2f409-104">Forwards the work in resolving delay-loaded imports from the parent binary to a target binary.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f409-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f409-105">Syntax</span></span>


```C++
NTSTATUS WINAPI ResolveDelayLoadsFromDll(
  _In_       PVOID  ParentBase,
  _In_       LPCSTR TargetDllName,
  _Reserved_ ULONG  Flags
);
```



## <a name="parameters"></a><span data-ttu-id="2f409-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f409-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f409-107">*Parametribase* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f409-107">*ParentBase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f409-108">Die Basisadresse des Moduls, das verzögert eine andere Binärdatei lädt.</span><span class="sxs-lookup"><span data-stu-id="2f409-108">The base address of the module that delay loads another binary.</span></span>

</dd> <dt>

<span data-ttu-id="2f409-109">*Targetdllname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f409-109">*TargetDllName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f409-110">Der Name der Ziel-dll.</span><span class="sxs-lookup"><span data-stu-id="2f409-110">The name of the target DLL.</span></span>

</dd> <dt>

<span data-ttu-id="2f409-111">*Flags*</span><span class="sxs-lookup"><span data-stu-id="2f409-111">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="2f409-112">Bleiben muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="2f409-112">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f409-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f409-113">Return value</span></span>

<span data-ttu-id="2f409-114">Die Adresse des Deskriptors für verzögertes Laden, wenn Sie gefunden wird. andernfalls **null**.</span><span class="sxs-lookup"><span data-stu-id="2f409-114">The address of the delay-load descriptor, if it is found; otherwise, **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f409-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f409-115">Requirements</span></span>



| <span data-ttu-id="2f409-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f409-116">Requirement</span></span> | <span data-ttu-id="2f409-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2f409-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f409-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2f409-118">Library</span></span><br/> | <dl> <span data-ttu-id="2f409-119"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f409-119"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2f409-120">DLL</span><span class="sxs-lookup"><span data-stu-id="2f409-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="2f409-121"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f409-121"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f409-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f409-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="2f409-123">[Linker-Unterstützung für Delay-Loaded DLLs](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="2f409-123">[Linker Support for Delay-Loaded DLLs](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span></span>
</dt> </dl>

 

 




