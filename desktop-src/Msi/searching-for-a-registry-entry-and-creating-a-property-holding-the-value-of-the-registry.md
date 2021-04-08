---
description: Während einer Windows Installer Installation kann das Installationsprogramm nach einem Registrierungs Eintrag suchen und eine Eigenschaft erstellen, die den Wert der Registrierung enthält.
ms.assetid: 3a663fc7-cdcf-4ac3-8251-836ba0d3cc11
title: Suchen nach einem Registrierungs Eintrag und Erstellen einer Eigenschaft mit dem Wert der Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82bd7572c0176f4870eed199800715190d9bbbf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862039"
---
# <a name="searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry"></a><span data-ttu-id="ec3b9-103">Suchen nach einem Registrierungs Eintrag und Erstellen einer Eigenschaft mit dem Wert der Registrierung</span><span class="sxs-lookup"><span data-stu-id="ec3b9-103">Searching for a Registry Entry and Creating a Property Holding the Value of the Registry</span></span>

<span data-ttu-id="ec3b9-104">**So suchen Sie nach einem Registrierungs Eintrag und erstellen eine Eigenschaft, die den Wert dieser Datei enthält**</span><span class="sxs-lookup"><span data-stu-id="ec3b9-104">**To search for a registry entry and create a property holding the value of that file**</span></span>

1.  <span data-ttu-id="ec3b9-105">Fügen Sie die Signatur der [Signatur Tabelle](signature-table.md) oder der Tabelle " [complocator](complocator-table.md)" nicht hinzu.</span><span class="sxs-lookup"><span data-stu-id="ec3b9-105">Do not add the signature to the [Signature Table](signature-table.md) or the [CompLocator Table](complocator-table.md).</span></span> <span data-ttu-id="ec3b9-106">Wenn eine Datei Signatur in der Tabelle " [AppSearch](appsearch-table.md) " aufgeführt ist und nicht in den Tabellen "Signature" oder "complocator" aufgeführt ist, sucht das Installationsprogramm in der [Tabelle "reglocator](reglocator-table.md)".</span><span class="sxs-lookup"><span data-stu-id="ec3b9-106">If a file signature is listed in the [AppSearch Table](appsearch-table.md) and is not listed in the Signature or CompLocator tables, the Installer looks in the [RegLocator Table](reglocator-table.md).</span></span>

2.  <span data-ttu-id="ec3b9-107">Geben Sie den Registrierungs Eintrag an, nach dem in der [reglocator-Tabelle](reglocator-table.md)gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec3b9-107">Specify the registry entry to be searched for in the [RegLocator Table](reglocator-table.md).</span></span> <span data-ttu-id="ec3b9-108">Wenn die Signatur in der [Signatur Tabelle](signature-table.md) nicht vorhanden ist und der Wert der Type-Spalte **msidblocatortyperawvalue** ist, wird angenommen, dass die Suche für den spezifischen Registrierungsschlüssel Namen erfolgt, auf den die reglocator-Tabelle verweist.</span><span class="sxs-lookup"><span data-stu-id="ec3b9-108">If the signature is absent from the [Signature Table](signature-table.md) and the value of the Type column is **msidbLocatorTypeRawValue**, then the search is assumed to be for the specific registry key name pointed to by the RegLocator Table.</span></span>

    <span data-ttu-id="ec3b9-109">[Reglocator-Tabelle](reglocator-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="ec3b9-109">[RegLocator Table](reglocator-table.md) (partial)</span></span>

    

    | <span data-ttu-id="ec3b9-110">Signatur\_</span><span class="sxs-lookup"><span data-stu-id="ec3b9-110">Signature\_</span></span>         | <span data-ttu-id="ec3b9-111">Root</span><span class="sxs-lookup"><span data-stu-id="ec3b9-111">Root</span></span>         | <span data-ttu-id="ec3b9-112">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="ec3b9-112">Key</span></span>                                                           | <span data-ttu-id="ec3b9-113">Name</span><span class="sxs-lookup"><span data-stu-id="ec3b9-113">Name</span></span>                  | <span data-ttu-id="ec3b9-114">type</span><span class="sxs-lookup"><span data-stu-id="ec3b9-114">Type</span></span>                                    |
    |---------------------|--------------|---------------------------------------------------------------|-----------------------|-----------------------------------------|
    | <span data-ttu-id="ec3b9-115">Appvalue</span><span class="sxs-lookup"><span data-stu-id="ec3b9-115">AppValue</span></span><br/> | <span data-ttu-id="ec3b9-116">2</span><span class="sxs-lookup"><span data-stu-id="ec3b9-116">2</span></span><br/> | <span data-ttu-id="ec3b9-117">**Software** \\ **Microsoft** \\ **Myapp**</span><span class="sxs-lookup"><span data-stu-id="ec3b9-117">**SOFTWARE**\\**Microsoft**\\**MyApp**</span></span><br/> <br/> | <span data-ttu-id="ec3b9-118">**"Myname"**</span><span class="sxs-lookup"><span data-stu-id="ec3b9-118">**Myname**</span></span><br/> | <span data-ttu-id="ec3b9-119">**msidbloserortyperawvalue**</span><span class="sxs-lookup"><span data-stu-id="ec3b9-119">**msidbLocatorTypeRawValue**</span></span><br/> |

    

     

3.  <span data-ttu-id="ec3b9-120">Füllen Sie schließlich die [AppSearch-Tabelle](appsearch-table.md) auf, damit die [AppSearch-Aktion](appsearch-action.md) den Wert von appvalue zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ec3b9-120">Finally, populate the [AppSearch Table](appsearch-table.md) so that the [AppSearch Action](appsearch-action.md) returns the value of AppValue.</span></span> <span data-ttu-id="ec3b9-121">Nachdem das Installationsprogramm die AppSearch-Aktion ausgeführt hat, ist der Wert von myregval der Wert von appvalue.</span><span class="sxs-lookup"><span data-stu-id="ec3b9-121">After the Installer executes the AppSearch Action, the value of MYREGVAL is the value of AppValue.</span></span>

    <span data-ttu-id="ec3b9-122">[AppSearch-Tabelle](appsearch-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="ec3b9-122">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="ec3b9-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ec3b9-123">Property</span></span>            | <span data-ttu-id="ec3b9-124">Signatur</span><span class="sxs-lookup"><span data-stu-id="ec3b9-124">Signature</span></span>           |
    |---------------------|---------------------|
    | <span data-ttu-id="ec3b9-125">Myregval</span><span class="sxs-lookup"><span data-stu-id="ec3b9-125">MYREGVAL</span></span><br/> | <span data-ttu-id="ec3b9-126">Appvalue</span><span class="sxs-lookup"><span data-stu-id="ec3b9-126">AppValue</span></span><br/> |

    

     

 

 




