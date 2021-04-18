---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Erstellen eines printfunktionalitäten-Dokuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ccb1adf4626254ba9f71c706ad7d4556a23aeb6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106354919"
---
# <a name="creating-a-printcapabilities-document"></a><span data-ttu-id="8c359-104">Erstellen eines printfunktionalitäten-Dokuments</span><span class="sxs-lookup"><span data-stu-id="8c359-104">Creating a PrintCapabilities Document</span></span>

<span data-ttu-id="8c359-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="8c359-105">This topic is not current.</span></span> <span data-ttu-id="8c359-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8c359-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8c359-107">Nachdem ein Print Ticket überprüft wurde, kann es verwendet werden, um eine Momentaufnahme der Print-Funktionen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8c359-107">After a PrintTicket is validated, it can be used to create a snapshot of the PrintCapabilities.</span></span> <span data-ttu-id="8c359-108">Der Anbieter muss über eine interne Darstellung für jede Eigenschaft verfügen, deren Wert von der Gerätekonfiguration abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="8c359-108">The provider must have an internal representation for any Property whose Value is dependent on the device configuration.</span></span> <span data-ttu-id="8c359-109">Wenn z. b. "spotpulse" eine Eigenschaft ist, die sowohl von der Auflösung als auch von den MediaType-Features abhängig ist, wird eine interne Darstellung von "spotpulse", die sich auf die verschiedenen Werte für "Resolution" und "MediaType" bezieht, in der folgenden Tabelle</span><span class="sxs-lookup"><span data-stu-id="8c359-109">For example, if SpotDiameter is a Property that is dependent on both the Resolution and MediaType Features, an internal representation of SpotDiameter as it relates to the various values for Resolution and MediaType might appear as in the following table:</span></span>



| <span data-ttu-id="8c359-110">Lösung</span><span class="sxs-lookup"><span data-stu-id="8c359-110">Resolution</span></span>      | <span data-ttu-id="8c359-111">MediaType</span><span class="sxs-lookup"><span data-stu-id="8c359-111">MediaType</span></span>         | <span data-ttu-id="8c359-112">Spot-Durchmesser</span><span class="sxs-lookup"><span data-stu-id="8c359-112">SpotDiameter</span></span>   |
|-----------------|-------------------|----------------|
| <span data-ttu-id="8c359-113">300</span><span class="sxs-lookup"><span data-stu-id="8c359-113">300</span></span><br/>  | <span data-ttu-id="8c359-114">Kauf</span><span class="sxs-lookup"><span data-stu-id="8c359-114">Bond</span></span><br/>   | <span data-ttu-id="8c359-115">520</span><span class="sxs-lookup"><span data-stu-id="8c359-115">520</span></span><br/> |
| <span data-ttu-id="8c359-116">300</span><span class="sxs-lookup"><span data-stu-id="8c359-116">300</span></span><br/>  | <span data-ttu-id="8c359-117">Glanz</span><span class="sxs-lookup"><span data-stu-id="8c359-117">Glossy</span></span><br/> | <span data-ttu-id="8c359-118">350</span><span class="sxs-lookup"><span data-stu-id="8c359-118">350</span></span><br/> |
| <span data-ttu-id="8c359-119">600</span><span class="sxs-lookup"><span data-stu-id="8c359-119">600</span></span><br/>  | <span data-ttu-id="8c359-120">Kauf</span><span class="sxs-lookup"><span data-stu-id="8c359-120">Bond</span></span><br/>   | <span data-ttu-id="8c359-121">330</span><span class="sxs-lookup"><span data-stu-id="8c359-121">330</span></span><br/> |
| <span data-ttu-id="8c359-122">600</span><span class="sxs-lookup"><span data-stu-id="8c359-122">600</span></span><br/>  | <span data-ttu-id="8c359-123">Glanz</span><span class="sxs-lookup"><span data-stu-id="8c359-123">Glossy</span></span><br/> | <span data-ttu-id="8c359-124">180</span><span class="sxs-lookup"><span data-stu-id="8c359-124">180</span></span><br/> |
| <span data-ttu-id="8c359-125">1200</span><span class="sxs-lookup"><span data-stu-id="8c359-125">1200</span></span><br/> | <span data-ttu-id="8c359-126">Kauf</span><span class="sxs-lookup"><span data-stu-id="8c359-126">Bond</span></span><br/>   | <span data-ttu-id="8c359-127">250</span><span class="sxs-lookup"><span data-stu-id="8c359-127">250</span></span><br/> |
| <span data-ttu-id="8c359-128">1200</span><span class="sxs-lookup"><span data-stu-id="8c359-128">1200</span></span><br/> | <span data-ttu-id="8c359-129">Glanz</span><span class="sxs-lookup"><span data-stu-id="8c359-129">Glossy</span></span><br/> | <span data-ttu-id="8c359-130">100</span><span class="sxs-lookup"><span data-stu-id="8c359-130">100</span></span><br/> |



 

<span data-ttu-id="8c359-131">In diesem Beispiel muss der printfunktionalitäten-Anbieter das angegebene PrintTicket verwenden, um den richtigen Eintrag aus der internen Tabelle auszuwählen und diesen als Wert für die Eigenschaft "Spot-Durchmesser" zu melden.</span><span class="sxs-lookup"><span data-stu-id="8c359-131">For this example, the PrintCapabilities provider must use the provided PrintTicket to select the proper entry from the internal table and report that as the Value for the SpotDiameter Property.</span></span> <span data-ttu-id="8c359-132">Dieser Vorgang wird für jede mehrwertige Eigenschaft (für jede Eigenschaft, deren Wert abhängig von der Konfiguration ist) wiederholt.</span><span class="sxs-lookup"><span data-stu-id="8c359-132">This process is repeated for every multi-valued Property (for every Property whose Value is dependent on the configuration).</span></span> <span data-ttu-id="8c359-133">Im Abschnitt [printfunktionalitäten-Schema und Dokument](printcapabilities-schema-and-document-construction.md) Erstellung werden die anderen Schritte beschrieben, die zum Erstellen einer Momentaufnahme der Print-Funktionen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8c359-133">The [PrintCapabilities Schema and Document Construction](printcapabilities-schema-and-document-construction.md) section describes the other steps involved in creating a snapshot of the PrintCapabilities.</span></span>

<span data-ttu-id="8c359-134">Um eine Momentaufnahme des Standard Dokuments printfunktionalitäten zu erstellen, geben Sie der Methode, mit der printfunktionalitäten-Dokumente erstellt werden, ein Standardmäßiges Print Ticket (anstelle eines beliebigen PrintTicket).</span><span class="sxs-lookup"><span data-stu-id="8c359-134">To create a snapshot of the default PrintCapabilities document, provide a default PrintTicket (rather than an arbitrary PrintTicket) to the method that creates PrintCapabilities documents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c359-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8c359-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c359-136">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="8c359-136">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




