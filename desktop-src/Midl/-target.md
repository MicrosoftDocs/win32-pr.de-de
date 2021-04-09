---
title: /target-Schalter
description: Der/Target-Schalter ermöglicht es dem Mittel-Compiler, Optimierungen zu aktivieren, die nur in neueren Versionen von Windows verfügbar sind. Der/Target-Schalter aktiviert automatisch weitere Switches.
ms.assetid: 8c5aa319-e6a6-4803-99f3-ed8751d565d5
keywords:
- /Target-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /target
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 43c17c6bb06eca94a1738ddc71255cd7cd441c5c
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "104050652"
---
# <a name="target-switch"></a><span data-ttu-id="7b097-105">/target-Schalter</span><span class="sxs-lookup"><span data-stu-id="7b097-105">/target switch</span></span>

<span data-ttu-id="7b097-106">Der **/target** -Schalter ermöglicht es dem Mittel-Compiler, Optimierungen zu aktivieren, die nur in neueren Versionen von Windows verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7b097-106">The **/target** switch enables the MIDL compiler to enable optimizations available only on recent versions of Windows.</span></span> <span data-ttu-id="7b097-107">Der **/target** -Schalter aktiviert automatisch weitere Switches.</span><span class="sxs-lookup"><span data-stu-id="7b097-107">The **/target** switch automatically activates additional switches.</span></span>

``` syntax
midl /target level
```

## <a name="switch-options"></a><span data-ttu-id="7b097-108">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="7b097-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="7b097-109">*level*</span><span class="sxs-lookup"><span data-stu-id="7b097-109">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="7b097-110">Gibt die Zielebene an, z. b. NT50, NT51, nt60, NT61, NT62 oder NT100.</span><span class="sxs-lookup"><span data-stu-id="7b097-110">Specifies the target level, such as NT50, NT51, NT60, NT61, NT62, or NT100.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b097-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b097-111">Remarks</span></span>

<span data-ttu-id="7b097-112">Der Schalter **/target** aktiviert basierend auf dem Betriebssystem automatisch weitere Switches, wie in der folgenden Tabelle angegeben:</span><span class="sxs-lookup"><span data-stu-id="7b097-112">The **/target** switch automatically activates additional switches, based on the operating system, as specified in the following table:</span></span>



| <span data-ttu-id="7b097-113">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="7b097-113">Operating system</span></span> | <span data-ttu-id="7b097-114">/Target-Ebene</span><span class="sxs-lookup"><span data-stu-id="7b097-114">/target level</span></span> | <span data-ttu-id="7b097-115">Aktivierte Switches</span><span class="sxs-lookup"><span data-stu-id="7b097-115">Switches Activated</span></span>                     |
|------------------|---------------|----------------------------------------|
| <span data-ttu-id="7b097-116">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7b097-116">Windows 2000</span></span>     | <span data-ttu-id="7b097-117">NT50</span><span class="sxs-lookup"><span data-stu-id="7b097-117">NT50</span></span>          | <span data-ttu-id="7b097-118">/Oicf/Error alle/robust</span><span class="sxs-lookup"><span data-stu-id="7b097-118">/Oicf /error all /robust</span></span>               |
| <span data-ttu-id="7b097-119">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7b097-119">Windows XP</span></span>       | <span data-ttu-id="7b097-120">NT51</span><span class="sxs-lookup"><span data-stu-id="7b097-120">NT51</span></span>          | <span data-ttu-id="7b097-121">/Oicf/Error alle/robust/Protocol alle</span><span class="sxs-lookup"><span data-stu-id="7b097-121">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="7b097-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b097-122">Windows Vista</span></span>    | <span data-ttu-id="7b097-123">NT60</span><span class="sxs-lookup"><span data-stu-id="7b097-123">NT60</span></span>          | <span data-ttu-id="7b097-124">/Oicf/Error alle/robust/Protocol alle</span><span class="sxs-lookup"><span data-stu-id="7b097-124">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="7b097-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7b097-125">Windows 7</span></span>        | <span data-ttu-id="7b097-126">NT61</span><span class="sxs-lookup"><span data-stu-id="7b097-126">NT61</span></span>          | <span data-ttu-id="7b097-127">/Oicf/Error alle/robust/Protocol alle</span><span class="sxs-lookup"><span data-stu-id="7b097-127">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="7b097-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7b097-128">Windows 8</span></span>        | <span data-ttu-id="7b097-129">NT62</span><span class="sxs-lookup"><span data-stu-id="7b097-129">NT62</span></span>          | <span data-ttu-id="7b097-130">/Oicf/Error alle/robust/Protocol alle</span><span class="sxs-lookup"><span data-stu-id="7b097-130">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="7b097-131">Windows 10</span><span class="sxs-lookup"><span data-stu-id="7b097-131">Windows 10</span></span>       | <span data-ttu-id="7b097-132">NT100</span><span class="sxs-lookup"><span data-stu-id="7b097-132">NT100</span></span>         | <span data-ttu-id="7b097-133">/Oicf/Error alle/robust/Protocol alle</span><span class="sxs-lookup"><span data-stu-id="7b097-133">/Oicf /error all /robust /protocol all</span></span> |
 

<span data-ttu-id="7b097-134">Um sicherzustellen, dass ein Stub auf dem System ausgeführt wird, das durch den **/target** -Schalter angegeben ist, gibt "Mittel l" einen Fehler aus, wenn ein Feature vorhanden ist, das nur auf einer neueren Version von Windows</span><span class="sxs-lookup"><span data-stu-id="7b097-134">To ensure a stub runs on the system specified by the **/target** switch, MIDL issues an error when a feature available only on a more recent version of Windows is present.</span></span> <span data-ttu-id="7b097-135">In der folgenden Tabelle wird die minimale **/target** -Ebene angegeben, die zum Aktivieren des Features erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7b097-135">The following table specifies the minimum **/target** level required to enable the feature.</span></span> <span data-ttu-id="7b097-136">Höhere Zielebenen umfassen alle Features von niedrigeren Zielebenen.</span><span class="sxs-lookup"><span data-stu-id="7b097-136">Higher target levels include all features from lower target levels.</span></span>



| <span data-ttu-id="7b097-137">Mindestens erforderliche/Target-Ebene</span><span class="sxs-lookup"><span data-stu-id="7b097-137">Minimum required /target level</span></span> | <span data-ttu-id="7b097-138">Features</span><span class="sxs-lookup"><span data-stu-id="7b097-138">Features</span></span>                                                                                                                                                                                          |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b097-139">NT50</span><span class="sxs-lookup"><span data-stu-id="7b097-139">NT50</span></span>                           | <span data-ttu-id="7b097-140">/robust</span><span class="sxs-lookup"><span data-stu-id="7b097-140">/robust</span></span><br/> <span data-ttu-id="7b097-141">\[Nachricht\]</span><span class="sxs-lookup"><span data-stu-id="7b097-141">\[message\]</span></span><br/> <span data-ttu-id="7b097-142">\[async\]</span><span class="sxs-lookup"><span data-stu-id="7b097-142">\[async\]</span></span><br/> <span data-ttu-id="7b097-143">\[Async- \_ UUID\]</span><span class="sxs-lookup"><span data-stu-id="7b097-143">\[async\_uuid\]</span></span><br/> <span data-ttu-id="7b097-144">\[Benachrichtigen \] im/Oicf-Modus</span><span class="sxs-lookup"><span data-stu-id="7b097-144">\[notify\] in /Oicf mode</span></span><br/> <span data-ttu-id="7b097-145">\[Codieren \] oder \[ decodieren \] im/Oicf-Modus</span><span class="sxs-lookup"><span data-stu-id="7b097-145">\[encode\] or \[decode\] in /Oicf mode</span></span><br/>                   |
| <span data-ttu-id="7b097-146">NT51</span><span class="sxs-lookup"><span data-stu-id="7b097-146">NT51</span></span>                           | <span data-ttu-id="7b097-147">/Protocol 64-Bit-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="7b097-147">/protocol 64-bit support</span></span><br/> <span data-ttu-id="7b097-148">\[teilweise \_ ignorieren\]</span><span class="sxs-lookup"><span data-stu-id="7b097-148">\[partial\_ignore\]</span></span><br/> <span data-ttu-id="7b097-149">\[\_zuordnen erzwingen\]</span><span class="sxs-lookup"><span data-stu-id="7b097-149">\[force\_allocate\]</span></span><br/>                                                                                                 |
| <span data-ttu-id="7b097-150">NT60</span><span class="sxs-lookup"><span data-stu-id="7b097-150">NT60</span></span>                           | <span data-ttu-id="7b097-151">Erzwungene komplexe Struktur Marshalling</span><span class="sxs-lookup"><span data-stu-id="7b097-151">Forced complex structure marshalling</span></span><br/> <span data-ttu-id="7b097-152">Kontext Handles in einem Array oder einer Struktur</span><span class="sxs-lookup"><span data-stu-id="7b097-152">Context handles in an array or structure</span></span><br/> <span data-ttu-id="7b097-153">\[Bereichs \] Unterstützung für Zeichen folgen ohne Größenanpassung</span><span class="sxs-lookup"><span data-stu-id="7b097-153">\[range\] support for unsized strings</span></span><br/> <span data-ttu-id="7b097-154">\[Typ \_ Strict- \_ Kontext \_ handle\]</span><span class="sxs-lookup"><span data-stu-id="7b097-154">\[type\_strict\_context\_handle\]</span></span><br/> |
| <span data-ttu-id="7b097-155">NT61</span><span class="sxs-lookup"><span data-stu-id="7b097-155">NT61</span></span>                           | <span data-ttu-id="7b097-156">Direkte com-Stub-Aufrufe für Schnittstellen mit weniger als 32 Methoden erfordern das Verknüpfen von com-Stubs mit **OLE32.DLL**.</span><span class="sxs-lookup"><span data-stu-id="7b097-156">Direct COM stub calls for interfaces with less than 32 methods requires linking COM stubs with **OLE32.DLL**.</span></span><br/>                                                                          |
| <span data-ttu-id="7b097-157">NT62</span><span class="sxs-lookup"><span data-stu-id="7b097-157">NT62</span></span>                           | <span data-ttu-id="7b097-158">Arm-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="7b097-158">ARM support</span></span><br/> <span data-ttu-id="7b097-159">WinRT-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="7b097-159">WinRT support</span></span><br/>                                                                                                                                                   |
| <span data-ttu-id="7b097-160">NT100</span><span class="sxs-lookup"><span data-stu-id="7b097-160">NT100</span></span>                          | <span data-ttu-id="7b097-161">\[system_handle \] Unterstützung</span><span class="sxs-lookup"><span data-stu-id="7b097-161">\[system_handle\] support</span></span><br /> |


 

## <a name="examples"></a><span data-ttu-id="7b097-162">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b097-162">Examples</span></span>

<span data-ttu-id="7b097-163">**Mittel l/Target NT50**</span><span class="sxs-lookup"><span data-stu-id="7b097-163">**midl /target NT50**</span></span>

## <a name="see-also"></a><span data-ttu-id="7b097-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b097-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b097-165">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="7b097-165">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="7b097-166">**/osf**</span><span class="sxs-lookup"><span data-stu-id="7b097-166">**/osf**</span></span>](-osf.md)
</dt> </dl>
