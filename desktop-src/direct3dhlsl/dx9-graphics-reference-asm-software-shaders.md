---
title: Software-Shader
description: Software-Shader werden implementiert, um die Entwicklung von Shadern ohne zugrunde liegende Hardwareunterstützung zu ermöglichen. Sie unterstützen den vollständigen Featuresatz. Da Sie in Software implementiert werden, erzielen Sie nicht die beste Leistung.
ms.assetid: 0153732d-a487-473b-ad77-32ab457979f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df101edd0362321847fb9c0baf7feb3cc865e2da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037634"
---
# <a name="software-shaders"></a><span data-ttu-id="9f88f-105">Software-Shader</span><span class="sxs-lookup"><span data-stu-id="9f88f-105">Software Shaders</span></span>

<span data-ttu-id="9f88f-106">Software-Shader werden implementiert, um die Entwicklung von Shadern ohne zugrunde liegende Hardwareunterstützung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="9f88f-106">Software shaders are implemented to allow development of shaders without underlying hardware support.</span></span> <span data-ttu-id="9f88f-107">Sie unterstützen den vollständigen Featuresatz.</span><span class="sxs-lookup"><span data-stu-id="9f88f-107">They support the full feature set.</span></span> <span data-ttu-id="9f88f-108">Da Sie in Software implementiert werden, erzielen Sie nicht die beste Leistung.</span><span class="sxs-lookup"><span data-stu-id="9f88f-108">Because they are implemented in software, they will not produce the best performance.</span></span>



| <span data-ttu-id="9f88f-109">Version</span><span class="sxs-lookup"><span data-stu-id="9f88f-109">Version</span></span>   | <span data-ttu-id="9f88f-110">Funktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="9f88f-110">Feature Set</span></span>                  | <span data-ttu-id="9f88f-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9f88f-111">Requirements</span></span>                                                         |
|-----------|------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="9f88f-112">vs \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9f88f-112">vs\_2\_sw</span></span> | <span data-ttu-id="9f88f-113">Alle Features von vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9f88f-113">All the features of vs\_2\_x</span></span> | <span data-ttu-id="9f88f-114">Wird nur von der Verarbeitung von Software Scheitel Punkten und einem Referenzgerät unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f88f-114">Only supported by software vertex processing and a reference device.</span></span> |
| <span data-ttu-id="9f88f-115">vs \_ 3- \_ SW</span><span class="sxs-lookup"><span data-stu-id="9f88f-115">vs\_3\_sw</span></span> | <span data-ttu-id="9f88f-116">Alle Features von vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9f88f-116">All the features of vs\_3\_0</span></span> | <span data-ttu-id="9f88f-117">Wird nur von der Verarbeitung von Software Scheitel Punkten und einem Referenzgerät unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f88f-117">Only supported by software vertex processing and a reference device.</span></span> |
| <span data-ttu-id="9f88f-118">PS \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9f88f-118">ps\_2\_sw</span></span> | <span data-ttu-id="9f88f-119">Alle Features von PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9f88f-119">All the features of ps\_2\_x</span></span> | <span data-ttu-id="9f88f-120">Wird nur von einem Referenzgerät unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f88f-120">Only supported by a reference device.</span></span>                                |
| <span data-ttu-id="9f88f-121">PS \_ 3 ( \_ SW)</span><span class="sxs-lookup"><span data-stu-id="9f88f-121">ps\_3\_sw</span></span> | <span data-ttu-id="9f88f-122">Alle Features von PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9f88f-122">All the features of ps\_3\_0</span></span> | <span data-ttu-id="9f88f-123">Wird nur von einem Referenzgerät unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f88f-123">Only supported by a reference device.</span></span>                                |



 

<span data-ttu-id="9f88f-124">Einige Überprüfungen werden für Software-Shader gelockert.</span><span class="sxs-lookup"><span data-stu-id="9f88f-124">Some validations are relaxed for software shaders.</span></span> <span data-ttu-id="9f88f-125">Dies ist nützlich für das Debuggen und das Prototypen.</span><span class="sxs-lookup"><span data-stu-id="9f88f-125">This is useful for debugging and prototyping purposes.</span></span> <span data-ttu-id="9f88f-126">Die folgenden Überprüfungen werden gelockert: (alle anderen Überprüfungen bleiben unverändert)</span><span class="sxs-lookup"><span data-stu-id="9f88f-126">The following validations are relaxed: (all other validations remain the same)</span></span>



| <span data-ttu-id="9f88f-127">Überprüfungstyp</span><span class="sxs-lookup"><span data-stu-id="9f88f-127">Validation type</span></span>                                 | <span data-ttu-id="9f88f-128">Suchende</span><span class="sxs-lookup"><span data-stu-id="9f88f-128">Relaxation</span></span>                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f88f-129">Anweisungs Anzahl:</span><span class="sxs-lookup"><span data-stu-id="9f88f-129">Instruction Counts:</span></span>                             | <span data-ttu-id="9f88f-130">Dies wird für vs \_ 2 \_ SW, vs \_ 3 \_ SW und PS \_ 2 \_ SW, PS \_ 3 SW, gelockert \_ .</span><span class="sxs-lookup"><span data-stu-id="9f88f-130">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="9f88f-131">Es sind unbegrenzte Anweisungen zulässig.</span><span class="sxs-lookup"><span data-stu-id="9f88f-131">Unlimited instructions are allowed.</span></span>                                                                                                              |
| <span data-ttu-id="9f88f-132">Konstante Anzahl von Gleit Komma Werten:</span><span class="sxs-lookup"><span data-stu-id="9f88f-132">Float Constant Counts:</span></span>                          | <span data-ttu-id="9f88f-133">Dies wird für vs \_ 2 \_ SW, vs \_ 3 \_ SW und PS \_ 2 \_ SW, PS \_ 3 SW, gelockert \_ .</span><span class="sxs-lookup"><span data-stu-id="9f88f-133">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="9f88f-134">Bis zu 8192 Konstanten sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="9f88f-134">Up to 8192 constants are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="9f88f-135">Ganzzahlige Konstante Anzahl:</span><span class="sxs-lookup"><span data-stu-id="9f88f-135">Integer Constant Counts:</span></span>                        | <span data-ttu-id="9f88f-136">Dies wird für vs \_ 2 \_ SW, vs \_ 3 \_ SW und PS \_ 2 \_ SW, PS \_ 3 SW, gelockert \_ .</span><span class="sxs-lookup"><span data-stu-id="9f88f-136">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="9f88f-137">Bis zu 2048 Konstanten sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="9f88f-137">Up to 2048 constants are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="9f88f-138">Anzahl von booleschen Konstanten:</span><span class="sxs-lookup"><span data-stu-id="9f88f-138">Boolean Constant Counts:</span></span>                        | <span data-ttu-id="9f88f-139">Dies wird für vs \_ 2 \_ SW, vs \_ 3 \_ SW und PS \_ 2 \_ SW, PS \_ 3 SW, gelockert \_ .</span><span class="sxs-lookup"><span data-stu-id="9f88f-139">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="9f88f-140">Bis zu 2048 Konstanten sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="9f88f-140">Up to 2048 constants are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="9f88f-141">Abhängige Lese Tiefe:</span><span class="sxs-lookup"><span data-stu-id="9f88f-141">Dependent-read depth:</span></span>                           | <span data-ttu-id="9f88f-142">Dies wird für PS \_ 2 \_ SW gelockert.</span><span class="sxs-lookup"><span data-stu-id="9f88f-142">This is relaxed for ps\_2\_sw.</span></span> <span data-ttu-id="9f88f-143">Wie in vs \_ 3 \_ 0 und PS \_ 3 \_ 0 sind unbegrenzte abhängige Lesevorgänge zulässig.</span><span class="sxs-lookup"><span data-stu-id="9f88f-143">Like in vs\_3\_0 and ps\_3\_0, unlimited dependent reads are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="9f88f-144">Anzahl der Anweisungen und Bezeichnungen der Fluss Steuerung:</span><span class="sxs-lookup"><span data-stu-id="9f88f-144">Number of flow control instructions and labels:</span></span> | <span data-ttu-id="9f88f-145">Dies wird für vs \_ 2 \_ SW gelockert.</span><span class="sxs-lookup"><span data-stu-id="9f88f-145">This is relaxed for vs\_2\_sw.</span></span> <span data-ttu-id="9f88f-146">Es sind unbegrenzte Anweisungen zur Fluss Steuerung und bis zu 2048 Bezeichnungen zulässig.</span><span class="sxs-lookup"><span data-stu-id="9f88f-146">Unlimited flow control instructions and upto 2048 labels are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="9f88f-147">Schleifen Anzahl/Start/Schritt:</span><span class="sxs-lookup"><span data-stu-id="9f88f-147">Loop count/start/step:</span></span>                          | <span data-ttu-id="9f88f-148">Diese werden für vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW und PS \_ 3 SW gelockert \_ .</span><span class="sxs-lookup"><span data-stu-id="9f88f-148">These are relaxed for vs\_2\_sw, vs\_3\_sw, ps\_2\_sw and ps\_3\_sw.</span></span> <span data-ttu-id="9f88f-149">Die Schrittgröße der Iterations-und Interpunktions Schritte für rep-und Loop-Anweisungen sind 32-Bit-interkte mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="9f88f-149">Iteration start and interation step size for rep and loop instructions are 32-bit signed intergers.</span></span> <span data-ttu-id="9f88f-150">Die Anzahl der interationen kann maximal \_ int/64 betragen.</span><span class="sxs-lookup"><span data-stu-id="9f88f-150">Interation count can be up to MAX\_INT/64.</span></span> |
| <span data-ttu-id="9f88f-151">Grenzwerte für den Lesezugriff:</span><span class="sxs-lookup"><span data-stu-id="9f88f-151">Read-port limits:</span></span>                               | <span data-ttu-id="9f88f-152">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW und PS \_ 3 \_ SW haben keinen Grenzwert für Lesevorgänge.</span><span class="sxs-lookup"><span data-stu-id="9f88f-152">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw and ps\_3\_sw have no read-port limit.</span></span>                                                                                                                                              |
| <span data-ttu-id="9f88f-153">Anzahl der Interpolatoren:</span><span class="sxs-lookup"><span data-stu-id="9f88f-153">Number of interpolators:</span></span>                        | <span data-ttu-id="9f88f-154">Es gibt 16 [Register-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# ) in vs \_ 3 \_ SW und 10 [PS \_ 3 \_ 0 Registern](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# ) für PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="9f88f-154">There are 16 [Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o\#) in vs\_3\_sw and 10 [ps\_3\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v\#) for ps\_3\_sw.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="9f88f-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9f88f-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f88f-156">ASM-Shader-Referenz</span><span class="sxs-lookup"><span data-stu-id="9f88f-156">Asm Shader Reference</span></span>](dx9-graphics-reference-asm.md)
</dt> </dl>

 

 




