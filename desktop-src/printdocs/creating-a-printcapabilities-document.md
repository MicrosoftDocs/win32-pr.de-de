---
description: Nachdem ein PrintTicket überprüft wurde, kann es verwendet werden, um eine Momentaufnahme der PrintCapabilities zu erstellen.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Erstellen eines PrintCapabilities-Dokuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96ea51cef9dfd0f351704b3b71a7f6163737736
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409513"
---
# <a name="creating-a-printcapabilities-document"></a><span data-ttu-id="f2627-103">Erstellen eines PrintCapabilities-Dokuments</span><span class="sxs-lookup"><span data-stu-id="f2627-103">Creating a PrintCapabilities Document</span></span>

<span data-ttu-id="f2627-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="f2627-104">This topic is not current.</span></span> <span data-ttu-id="f2627-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="f2627-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f2627-106">Nachdem ein PrintTicket überprüft wurde, kann es verwendet werden, um eine Momentaufnahme der PrintCapabilities zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f2627-106">After a PrintTicket is validated, it can be used to create a snapshot of the PrintCapabilities.</span></span> <span data-ttu-id="f2627-107">Der Anbieter muss über eine interne Darstellung für jede Eigenschaft verfügen, deren Wert von der Gerätekonfiguration abhängt.</span><span class="sxs-lookup"><span data-stu-id="f2627-107">The provider must have an internal representation for any Property whose Value is dependent on the device configuration.</span></span> <span data-ttu-id="f2627-108">Wenn SpotDiameter beispielsweise eine Eigenschaft ist, die sowohl von den Auflösungs- als auch von mediaType-Features abhängig ist, kann eine interne Darstellung von SpotDiameter in Bezug auf die verschiedenen Werte für Auflösung und MediaType wie in der folgenden Tabelle angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="f2627-108">For example, if SpotDiameter is a Property that is dependent on both the Resolution and MediaType Features, an internal representation of SpotDiameter as it relates to the various values for Resolution and MediaType might appear as in the following table:</span></span>



| <span data-ttu-id="f2627-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="f2627-109">Resolution</span></span>      | <span data-ttu-id="f2627-110">MediaType</span><span class="sxs-lookup"><span data-stu-id="f2627-110">MediaType</span></span>         | <span data-ttu-id="f2627-111">SpotDiameter</span><span class="sxs-lookup"><span data-stu-id="f2627-111">SpotDiameter</span></span>   |
|-----------------|-------------------|----------------|
| <span data-ttu-id="f2627-112">300</span><span class="sxs-lookup"><span data-stu-id="f2627-112">300</span></span><br/>  | <span data-ttu-id="f2627-113">Bindung</span><span class="sxs-lookup"><span data-stu-id="f2627-113">Bond</span></span><br/>   | <span data-ttu-id="f2627-114">520</span><span class="sxs-lookup"><span data-stu-id="f2627-114">520</span></span><br/> |
| <span data-ttu-id="f2627-115">300</span><span class="sxs-lookup"><span data-stu-id="f2627-115">300</span></span><br/>  | <span data-ttu-id="f2627-116">Glänzend</span><span class="sxs-lookup"><span data-stu-id="f2627-116">Glossy</span></span><br/> | <span data-ttu-id="f2627-117">350</span><span class="sxs-lookup"><span data-stu-id="f2627-117">350</span></span><br/> |
| <span data-ttu-id="f2627-118">600</span><span class="sxs-lookup"><span data-stu-id="f2627-118">600</span></span><br/>  | <span data-ttu-id="f2627-119">Bindung</span><span class="sxs-lookup"><span data-stu-id="f2627-119">Bond</span></span><br/>   | <span data-ttu-id="f2627-120">330</span><span class="sxs-lookup"><span data-stu-id="f2627-120">330</span></span><br/> |
| <span data-ttu-id="f2627-121">600</span><span class="sxs-lookup"><span data-stu-id="f2627-121">600</span></span><br/>  | <span data-ttu-id="f2627-122">Glänzend</span><span class="sxs-lookup"><span data-stu-id="f2627-122">Glossy</span></span><br/> | <span data-ttu-id="f2627-123">180</span><span class="sxs-lookup"><span data-stu-id="f2627-123">180</span></span><br/> |
| <span data-ttu-id="f2627-124">1200</span><span class="sxs-lookup"><span data-stu-id="f2627-124">1200</span></span><br/> | <span data-ttu-id="f2627-125">Bindung</span><span class="sxs-lookup"><span data-stu-id="f2627-125">Bond</span></span><br/>   | <span data-ttu-id="f2627-126">250</span><span class="sxs-lookup"><span data-stu-id="f2627-126">250</span></span><br/> |
| <span data-ttu-id="f2627-127">1200</span><span class="sxs-lookup"><span data-stu-id="f2627-127">1200</span></span><br/> | <span data-ttu-id="f2627-128">Glänzend</span><span class="sxs-lookup"><span data-stu-id="f2627-128">Glossy</span></span><br/> | <span data-ttu-id="f2627-129">100</span><span class="sxs-lookup"><span data-stu-id="f2627-129">100</span></span><br/> |



 

<span data-ttu-id="f2627-130">In diesem Beispiel muss der PrintCapabilities-Anbieter das bereitgestellte PrintTicket verwenden, um den richtigen Eintrag aus der internen Tabelle auszuwählen und diesen als Wert für die SpotDiameter-Eigenschaft zu melden.</span><span class="sxs-lookup"><span data-stu-id="f2627-130">For this example, the PrintCapabilities provider must use the provided PrintTicket to select the proper entry from the internal table and report that as the Value for the SpotDiameter Property.</span></span> <span data-ttu-id="f2627-131">Dieser Prozess wird für jede mehrwertige Eigenschaft wiederholt (für jede Eigenschaft, deren Wert von der Konfiguration abhängig ist).</span><span class="sxs-lookup"><span data-stu-id="f2627-131">This process is repeated for every multi-valued Property (for every Property whose Value is dependent on the configuration).</span></span> <span data-ttu-id="f2627-132">Im Abschnitt [PrintCapabilities Schema and Document Construction (PrintCapabilities-Schema und Dokumenterstellung)](printcapabilities-schema-and-document-construction.md) werden die anderen Schritte beschrieben, die beim Erstellen einer Momentaufnahme von PrintCapabilities erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f2627-132">The [PrintCapabilities Schema and Document Construction](printcapabilities-schema-and-document-construction.md) section describes the other steps involved in creating a snapshot of the PrintCapabilities.</span></span>

<span data-ttu-id="f2627-133">Um eine Momentaufnahme des PrintCapabilities-Standarddokuments zu erstellen, geben Sie für die Methode, die PrintCapabilities-Dokumente erstellt, ein PrintTicket -Standardticket (anstelle eines beliebigen PrintTickets) an.</span><span class="sxs-lookup"><span data-stu-id="f2627-133">To create a snapshot of the default PrintCapabilities document, provide a default PrintTicket (rather than an arbitrary PrintTicket) to the method that creates PrintCapabilities documents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2627-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f2627-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2627-135">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="f2627-135">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




