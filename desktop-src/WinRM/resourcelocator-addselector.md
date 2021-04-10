---
title: ResourceLocator. addselector-Methode (WSManDisp. h)
description: Fügt dem ResourceLocator-Objekt einen Selektor hinzu. Der Selektor gibt eine bestimmte Instanz einer Ressource an.
ms.assetid: 4b513d39-a377-487f-a03b-f3c5ab0f0b5a
ms.tgt_platform: multiple
keywords:
- Addselector-Methode Windows-Remoteverwaltung
- Addselector-Methode Windows-Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows-Remoteverwaltung, addselector-Methode
topic_type:
- apiref
api_name:
- ResourceLocator.AddSelector
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 064108f535c9f46dc074d1b37754e626dc3f1d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956516"
---
# <a name="resourcelocatoraddselector-method"></a><span data-ttu-id="876c5-107">ResourceLocator. addselector-Methode</span><span class="sxs-lookup"><span data-stu-id="876c5-107">ResourceLocator.AddSelector method</span></span>

<span data-ttu-id="876c5-108">Fügt dem [**ResourceLocator**](resourcelocator.md) -Objekt einen [*Selektor*](windows-remote-management-glossary.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="876c5-108">Adds a [*selector*](windows-remote-management-glossary.md) to the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="876c5-109">Der Selektor gibt eine bestimmte Instanz einer *Ressource* an.</span><span class="sxs-lookup"><span data-stu-id="876c5-109">The selector specifies a particular instance of a *resource*.</span></span> <span data-ttu-id="876c5-110">Sie können ein [**ResourceLocator**](resourcelocator.md) -Objekt bereitstellen, anstatt einen Ressourcen-URI in [**Sitzungs**](session.md) Objekt Vorgängen wie " [**Session. Get**](session-get.md)", " [**Session. Put**](session-put.md)" oder " [**Session. Enumerate**](session-enumerate.md)" anzugeben.</span><span class="sxs-lookup"><span data-stu-id="876c5-110">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="876c5-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="876c5-111">Syntax</span></span>


```VB
ResourceLocator.AddSelector( _
  ByVal resourceSelName, _
  ByVal selValue _
)
```



## <a name="parameters"></a><span data-ttu-id="876c5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="876c5-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="876c5-113">*resourceselname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="876c5-113">*resourceSelName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="876c5-114">Der Name der Auswahl.</span><span class="sxs-lookup"><span data-stu-id="876c5-114">The selector name.</span></span> <span data-ttu-id="876c5-115">Wenn z. b. WMI-Daten angefordert werden, handelt es sich bei diesem Parameter um die Schlüsseleigenschaft für eine WMI-Klasse.</span><span class="sxs-lookup"><span data-stu-id="876c5-115">For example, when requesting WMI data, this parameter is the key property for a WMI class.</span></span>

</dd> <dt>

<span data-ttu-id="876c5-116">*selvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="876c5-116">*selValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="876c5-117">Der Auswahl Wert.</span><span class="sxs-lookup"><span data-stu-id="876c5-117">The selector value.</span></span> <span data-ttu-id="876c5-118">Für WMI-Daten enthält dieser Parameter z. b. einen Wert für eine Schlüsseleigenschaft, die eine bestimmte Instanz identifiziert.</span><span class="sxs-lookup"><span data-stu-id="876c5-118">For example, for WMI data, this parameter contains a value for a key property that identifies a specific instance.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="876c5-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="876c5-119">Remarks</span></span>

<span data-ttu-id="876c5-120">**Iwsmanresourcelocator:: addselector** ist die entsprechende C++-Methode.</span><span class="sxs-lookup"><span data-stu-id="876c5-120">**IWSManResourceLocator::AddSelector** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="876c5-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="876c5-121">Requirements</span></span>



| <span data-ttu-id="876c5-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="876c5-122">Requirement</span></span> | <span data-ttu-id="876c5-123">Wert</span><span class="sxs-lookup"><span data-stu-id="876c5-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="876c5-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="876c5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="876c5-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="876c5-125">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="876c5-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="876c5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="876c5-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="876c5-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="876c5-128">Header</span><span class="sxs-lookup"><span data-stu-id="876c5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="876c5-129"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="876c5-129"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="876c5-130">IDL</span><span class="sxs-lookup"><span data-stu-id="876c5-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="876c5-131"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="876c5-131"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="876c5-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="876c5-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="876c5-133"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="876c5-133"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="876c5-134">DLL</span><span class="sxs-lookup"><span data-stu-id="876c5-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="876c5-135"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="876c5-135"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="876c5-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="876c5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="876c5-137">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="876c5-137">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





