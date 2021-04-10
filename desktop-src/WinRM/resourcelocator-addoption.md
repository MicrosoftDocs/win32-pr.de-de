---
title: ResourceLocator. AddOption-Methode (WSManDisp. h)
description: Fügt zusätzliche Daten hinzu, die für die Verarbeitung der Anforderung erforderlich sind. Einige WMI-Anbieter benötigen beispielsweise ein IWbemContext-oder ein Swap-Objekt mit anbieterspezifischen Informationen.
ms.assetid: c85949fc-41e7-47eb-8aab-9b456490bc81
ms.tgt_platform: multiple
keywords:
- AddOption-Methode Windows-Remoteverwaltung
- AddOption-Methode Windows-Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows-Remoteverwaltung, AddOption-Methode
topic_type:
- apiref
api_name:
- ResourceLocator.AddOption
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 882f400dd2c59d2395dd2755846245f4e4ad385e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040257"
---
# <a name="resourcelocatoraddoption-method"></a><span data-ttu-id="7312e-107">ResourceLocator. AddOption-Methode</span><span class="sxs-lookup"><span data-stu-id="7312e-107">ResourceLocator.AddOption method</span></span>

<span data-ttu-id="7312e-108">Fügt zusätzliche Daten hinzu, die für die Verarbeitung der Anforderung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7312e-108">Adds additional data required to process the request.</span></span> <span data-ttu-id="7312e-109">Einige WMI-Anbieter benötigen beispielsweise ein [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) -oder ein [**Swap**](/windows/desktop/WmiSdk/swbemnamedvalueset) -Objekt mit anbieterspezifischen Informationen.</span><span class="sxs-lookup"><span data-stu-id="7312e-109">For example, some WMI providers may require an [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) or [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) object with provider-specific information.</span></span> <span data-ttu-id="7312e-110">Sie können ein [**ResourceLocator**](resourcelocator.md) -Objekt bereitstellen, anstatt einen Ressourcen-URI in [**Sitzungs**](session.md) Objekt Vorgängen wie " [**Session. Get**](session-get.md)", " [**Session. Put**](session-put.md)" oder " [**Session. Enumerate**](session-enumerate.md)" anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7312e-110">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7312e-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="7312e-111">Syntax</span></span>


```VB
ResourceLocator.AddOption( _
  ByVal OptionName, _
  ByVal OptionValue, _
  ByVal mustComply _
)
```



## <a name="parameters"></a><span data-ttu-id="7312e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7312e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7312e-113">*OptionName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7312e-113">*OptionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7312e-114">Der Name (Schlüssel) des optionalen Datenobjekts.</span><span class="sxs-lookup"><span data-stu-id="7312e-114">The name (key) of the optional data object.</span></span>

</dd> <dt>

<span data-ttu-id="7312e-115">*OptionValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7312e-115">*OptionValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7312e-116">Ein Wert, der für das optionale Datenobjekt angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7312e-116">A value supplied for the optional data object.</span></span>

</dd> <dt>

<span data-ttu-id="7312e-117">*mustcompliance* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7312e-117">*mustComply* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7312e-118">Ein Flag, das angibt, dass die Option verarbeitet werden muss.</span><span class="sxs-lookup"><span data-stu-id="7312e-118">A flag that indicates the option must be processed.</span></span> <span data-ttu-id="7312e-119">Der Standardwert ist **false** (0).</span><span class="sxs-lookup"><span data-stu-id="7312e-119">The default is **False** (0).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7312e-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7312e-120">Return value</span></span>

<span data-ttu-id="7312e-121">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7312e-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7312e-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7312e-122">Remarks</span></span>

<span data-ttu-id="7312e-123">**Iwsmanresourcelocator:: AddOption** ist die entsprechende C++-Methode.</span><span class="sxs-lookup"><span data-stu-id="7312e-123">**IWSManResourceLocator::AddOption** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7312e-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7312e-124">Requirements</span></span>



| <span data-ttu-id="7312e-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7312e-125">Requirement</span></span> | <span data-ttu-id="7312e-126">Wert</span><span class="sxs-lookup"><span data-stu-id="7312e-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7312e-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7312e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7312e-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7312e-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="7312e-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7312e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7312e-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7312e-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="7312e-131">Header</span><span class="sxs-lookup"><span data-stu-id="7312e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7312e-132"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7312e-132"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7312e-133">IDL</span><span class="sxs-lookup"><span data-stu-id="7312e-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7312e-134"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7312e-134"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="7312e-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7312e-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="7312e-136"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7312e-136"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7312e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7312e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7312e-138"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7312e-138"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7312e-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7312e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7312e-140">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="7312e-140">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

