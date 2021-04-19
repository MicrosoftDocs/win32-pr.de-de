---
description: Gibt die Zielfunktion des angegebenen Imports an und ersetzt den Funktionszeiger im Import Thunk durch das Ziel der Funktions Implementierung.
ms.assetid: 4ab79b7c-81d1-40bf-a76b-217d93567e40
title: Resolvedelta-loadedapi-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadedAPI
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: 019729cacb45cce87de2cc4015c661c494125108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370184"
---
# <a name="resolvedelayloadedapi-function"></a><span data-ttu-id="e37dc-103">Resolvedelta-loadedapi-Funktion</span><span class="sxs-lookup"><span data-stu-id="e37dc-103">ResolveDelayLoadedAPI function</span></span>

<span data-ttu-id="e37dc-104">Gibt die Zielfunktion des angegebenen Imports an und ersetzt den Funktionszeiger im Import Thunk durch das Ziel der Funktions Implementierung.</span><span class="sxs-lookup"><span data-stu-id="e37dc-104">Locates the target function of the specified import and replaces the function pointer in the import thunk with the target of the function implementation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e37dc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e37dc-105">Syntax</span></span>


```C++
PVOID WINAPI ResolveDelayLoadedAPI(
  _In_       PVOID                             ParentModuleBase,
  _In_       PCIMAGE_DELAYLOAD_DESCRIPTOR      DelayloadDescriptor,
  _In_opt_   PDELAYLOAD_FAILURE_DLL_CALLBACK   FailureDllHook,
  _In_opt_   PDELAYLOAD_FAILURE_SYSTEM_ROUTINE FailureSystemHook,
  _Out_      PIMAGE_THUNK_DATA                 ThunkAddress,
  _Reserved_ ULONG                             Flags
);
```



## <a name="parameters"></a><span data-ttu-id="e37dc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e37dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e37dc-107">" *Parametrimodulebase* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="e37dc-107">*ParentModuleBase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e37dc-108">Die Adresse der Basis des Moduls, das eine verzögert geladene Funktion importiert.</span><span class="sxs-lookup"><span data-stu-id="e37dc-108">The address of the base of the module importing a delay-loaded function.</span></span>

</dd> <dt>

<span data-ttu-id="e37dc-109">*Delta-loaddescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e37dc-109">*DelayloadDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e37dc-110">Der Deskriptor für das Modul, das geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e37dc-110">The descriptor for the module to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="e37dc-111">*Failuredllhook* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="e37dc-111">*FailureDllHook* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e37dc-112">Die Adresse des fehlerhaften Hooks.</span><span class="sxs-lookup"><span data-stu-id="e37dc-112">The address of the failure hook.</span></span> <span data-ttu-id="e37dc-113">Siehe " [**Delta-loadfailurehook**](delayloadfailurehook.md)".</span><span class="sxs-lookup"><span data-stu-id="e37dc-113">See [**DelayLoadFailureHook**](delayloadfailurehook.md).</span></span>

</dd> <dt>

<span data-ttu-id="e37dc-114">*Failuresystemhook* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="e37dc-114">*FailureSystemHook* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e37dc-115">Die Adresse des Systemfehler-Hooks.</span><span class="sxs-lookup"><span data-stu-id="e37dc-115">The address of the system failure hook.</span></span>

</dd> <dt>

<span data-ttu-id="e37dc-116">*Thunkaddress* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e37dc-116">*ThunkAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e37dc-117">Die Thunk-Daten für die Zielfunktion.</span><span class="sxs-lookup"><span data-stu-id="e37dc-117">The thunk data for the target function.</span></span> <span data-ttu-id="e37dc-118">Wird verwendet, um den Namen der jeweiligen namens Tabelle der Funktion zu suchen.</span><span class="sxs-lookup"><span data-stu-id="e37dc-118">Used to find the specific name table entry of the function.</span></span>

</dd> <dt>

<span data-ttu-id="e37dc-119">*Flags*</span><span class="sxs-lookup"><span data-stu-id="e37dc-119">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="e37dc-120">Bleiben muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="e37dc-120">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e37dc-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e37dc-121">Return value</span></span>

<span data-ttu-id="e37dc-122">Die Adresse des Imports oder der fehlerstub für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e37dc-122">The address of the import, or the failure stub for it.</span></span>

## <a name="requirements"></a><span data-ttu-id="e37dc-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e37dc-123">Requirements</span></span>



| <span data-ttu-id="e37dc-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e37dc-124">Requirement</span></span> | <span data-ttu-id="e37dc-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e37dc-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e37dc-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e37dc-126">Library</span></span><br/> | <dl> <span data-ttu-id="e37dc-127"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e37dc-127"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e37dc-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e37dc-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="e37dc-129"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e37dc-129"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e37dc-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e37dc-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="e37dc-131">[Linker-Unterstützung für Delay-Loaded DLLs](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="e37dc-131">[Linker Support for Delay-Loaded DLLs](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span></span>
</dt> </dl>

 

 




