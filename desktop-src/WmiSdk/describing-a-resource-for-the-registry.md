---
description: Die Systemregistrierung enthält ressourcenbezogene Daten.
ms.assetid: e66f1db8-a5f3-41d3-9835-34b81b9da5ed
ms.tgt_platform: multiple
title: Beschreiben einer Ressource für die Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba175120b5abec238d1b9078010359effef8ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373207"
---
# <a name="describing-a-resource-for-the-registry"></a><span data-ttu-id="e833d-103">Beschreiben einer Ressource für die Registrierung</span><span class="sxs-lookup"><span data-stu-id="e833d-103">Describing a Resource for the Registry</span></span>

<span data-ttu-id="e833d-104">Die Systemregistrierung enthält ressourcenbezogene Daten.</span><span class="sxs-lookup"><span data-stu-id="e833d-104">The system registry contains resource-related data.</span></span> <span data-ttu-id="e833d-105">Diese Daten befinden sich unter dem folgenden Registrierungsschlüssel und werden in einem speziellen Registrierungs Datentyp namens " **reg \_ Resource \_ List**" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e833d-105">This data is located under the following registry key and is kept in a special registry data type named **REG\_RESOURCE\_LIST**.</span></span> <span data-ttu-id="e833d-106">Anwendungen können die ressourcenbezogenen Daten über den System Registrierungs Anbieter abrufen.</span><span class="sxs-lookup"><span data-stu-id="e833d-106">Applications can obtain the resource-related data through the System Registry provider.</span></span> <span data-ttu-id="e833d-107">Sie können Systemressourcen in der Registrierung hinzufügen und ändern.</span><span class="sxs-lookup"><span data-stu-id="e833d-107">You can add and modify system resources in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   Hardware
      ResourceMap
```

<span data-ttu-id="e833d-108">Im folgenden Verfahren wird beschrieben, wie ressourcenbezogene Informationen in der Systemregistrierung gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e833d-108">The following procedure describes how to store resource-related information in the system registry.</span></span>

<span data-ttu-id="e833d-109">**So speichern Sie ressourcenbezogene Informationen in der Systemregistrierung**</span><span class="sxs-lookup"><span data-stu-id="e833d-109">**To store resource-related information in the system registry**</span></span>

1.  <span data-ttu-id="e833d-110">Erstellen Sie eine Zeichenfolge, die die folgenden Felder enthält.</span><span class="sxs-lookup"><span data-stu-id="e833d-110">Create a string that contains the following fields.</span></span>

    

    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="e833d-111">Feld</span><span class="sxs-lookup"><span data-stu-id="e833d-111">Field</span></span></th>
    <th><span data-ttu-id="e833d-112">Enthält</span><span class="sxs-lookup"><span data-stu-id="e833d-112">Contains</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="e833d-113">Schnittstellentyp</span><span class="sxs-lookup"><span data-stu-id="e833d-113">Interface type</span></span></td>
    <td><span data-ttu-id="e833d-114">Einer der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="e833d-114">One of the following values:</span></span><br/> <dl> <span data-ttu-id="e833d-115">Intern</span><span class="sxs-lookup"><span data-stu-id="e833d-115">Internal</span></span><br />
    <span data-ttu-id="e833d-116">ISA</span><span class="sxs-lookup"><span data-stu-id="e833d-116">Isa</span></span><br />
    <span data-ttu-id="e833d-117">EISA</span><span class="sxs-lookup"><span data-stu-id="e833d-117">Eisa</span></span><br />
    <span data-ttu-id="e833d-118">Mikrochannel</span><span class="sxs-lookup"><span data-stu-id="e833d-118">MicroChannel</span></span><br />
    <span data-ttu-id="e833d-119">TURBOchannel</span><span class="sxs-lookup"><span data-stu-id="e833d-119">TurboChannel</span></span><br />
    <span data-ttu-id="e833d-120">PCIBus</span><span class="sxs-lookup"><span data-stu-id="e833d-120">PCIBus</span></span><br />
    <span data-ttu-id="e833d-121">VMEbus</span><span class="sxs-lookup"><span data-stu-id="e833d-121">VMEBus</span></span><br />
    <span data-ttu-id="e833d-122">NuBus</span><span class="sxs-lookup"><span data-stu-id="e833d-122">NuBus</span></span><br />
    <span data-ttu-id="e833d-123">PCMCIABus</span><span class="sxs-lookup"><span data-stu-id="e833d-123">PCMCIABus</span></span><br />
    <span data-ttu-id="e833d-124">CBUS</span><span class="sxs-lookup"><span data-stu-id="e833d-124">CBus</span></span><br />
    <span data-ttu-id="e833d-125">Mpibus</span><span class="sxs-lookup"><span data-stu-id="e833d-125">MPIBus</span></span><br />
    <span data-ttu-id="e833d-126">Mpsabus</span><span class="sxs-lookup"><span data-stu-id="e833d-126">MPSABus</span></span><br />
    </dl></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="e833d-127">Busnummer</span><span class="sxs-lookup"><span data-stu-id="e833d-127">Bus number</span></span></td>
    <td><span data-ttu-id="e833d-128">Eine ganze Zahl, die die Busnummer angibt.</span><span class="sxs-lookup"><span data-stu-id="e833d-128">Integer specifying the bus number.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="e833d-129">Partielle deskriptornummer</span><span class="sxs-lookup"><span data-stu-id="e833d-129">Partial descriptor number</span></span></td>
    <td><span data-ttu-id="e833d-130">Eine ganze Zahl, die die deskriptornummer angibt.</span><span class="sxs-lookup"><span data-stu-id="e833d-130">Integer specifying the descriptor number.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="e833d-131">Offset-oder Union-Typ</span><span class="sxs-lookup"><span data-stu-id="e833d-131">Offset or union type</span></span></td>
    <td><span data-ttu-id="e833d-132">Einer der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="e833d-132">One of the following values:</span></span><br/> <dl> <span data-ttu-id="e833d-133">Port. Start</span><span class="sxs-lookup"><span data-stu-id="e833d-133">Port.Start</span></span><br />
    <span data-ttu-id="e833d-134">Port. PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="e833d-134">Port.PhysicalAddress</span></span><br />
    <span data-ttu-id="e833d-135">Port. length</span><span class="sxs-lookup"><span data-stu-id="e833d-135">Port.Length</span></span><br />
    <span data-ttu-id="e833d-136">Interrupt. Level</span><span class="sxs-lookup"><span data-stu-id="e833d-136">Interrupt.Level</span></span><br />
    <span data-ttu-id="e833d-137">Interrupt. Vector</span><span class="sxs-lookup"><span data-stu-id="e833d-137">Interrupt.Vector</span></span><br />
    <span data-ttu-id="e833d-138">Interrupt. Affinität</span><span class="sxs-lookup"><span data-stu-id="e833d-138">Interrupt.Affinity</span></span><br />
    <span data-ttu-id="e833d-139">Arbeitsspeicher. Start</span><span class="sxs-lookup"><span data-stu-id="e833d-139">Memory.Start</span></span><br />
    <span data-ttu-id="e833d-140">"Memory. PhysicalAddress"</span><span class="sxs-lookup"><span data-stu-id="e833d-140">Memory.PhysicalAddress</span></span><br />
    <span data-ttu-id="e833d-141">Arbeitsspeicher. Länge</span><span class="sxs-lookup"><span data-stu-id="e833d-141">Memory.Length</span></span><br />
    <span data-ttu-id="e833d-142">DMA. Channel</span><span class="sxs-lookup"><span data-stu-id="e833d-142">Dma.Channel</span></span><br />
    <span data-ttu-id="e833d-143">DMA. Port</span><span class="sxs-lookup"><span data-stu-id="e833d-143">Dma.Port</span></span><br />
    <span data-ttu-id="e833d-144">DMA. "reserved1"</span><span class="sxs-lookup"><span data-stu-id="e833d-144">Dma.Reserved1</span></span><br />
    <span data-ttu-id="e833d-145">"De vicespecificdata. DataSize"</span><span class="sxs-lookup"><span data-stu-id="e833d-145">DeviceSpecificData.DataSize</span></span><br />
    <span data-ttu-id="e833d-146">"De vicespecificdata." reserved1 ""</span><span class="sxs-lookup"><span data-stu-id="e833d-146">DeviceSpecificData.Reserved1</span></span><br />
    <span data-ttu-id="e833d-147">"De vicespecificdata." reserved2 ""</span><span class="sxs-lookup"><span data-stu-id="e833d-147">DeviceSpecificData.Reserved2</span></span><br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="e833d-148">Platzieren Sie die Zeichenfolge im entsprechenden Schlüssel unter dem Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="e833d-148">Place the string in the appropriate key under the registry key.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Hardware
          ResourceMap
    ```

<span data-ttu-id="e833d-149">Im folgenden Codebeispiel wird ein gültiger Ressourcen Deskriptor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e833d-149">The following code example describes a valid resource descriptor.</span></span>

``` syntax
local|hkey_local_machine\hardware\resourcemap\
  hardware abstraction layer\
  pc compatible eisa/isa HAL|.raw("eisa",0,0,"interrupt.affinity")
```

<span data-ttu-id="e833d-150">Das folgende Codebeispiel zeigt die gültige MOF-Syntax zum Abrufen eines Ressourcen Deskriptors.</span><span class="sxs-lookup"><span data-stu-id="e833d-150">The following code example shows valid MOF syntax for retrieving a resource descriptor.</span></span>

``` syntax
[DYNPROPS] 
class MyRegProp
{    
   [KEY]  
   STRING MyKey; 
   STRING MyReservedTranslated;
};

[DYNPROPS] 
instance of MyRegProp
{
   MyKey = "1";
   [PropertyContext("local|hkey_local_Machine\\hardware\\ResourceMap\\
                   System Resources\\Reserved|.Translated
                   (\"Internal\")(0)(1)(\"Memory.PhysicalAddress\")"),
   Dynamic, Provider("RegPropProv")] 
   MyReservedTranslated;
};
```

 

 




