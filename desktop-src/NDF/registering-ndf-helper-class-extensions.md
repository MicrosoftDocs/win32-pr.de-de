---
title: Registrieren von NDF-Hilfsklassen Erweiterungen
description: Jeder Hilfsklassen Erweiterung sind mehrere Registrierungsschlüssel zugeordnet. Einige Schlüssel sind für com erforderlich, und einige Schlüssel sind für die NDF erforderlich.
ms.assetid: 9ff3266d-5ffc-4a00-be24-2f85461c6ea6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f211517a975bdef61db7937fffa95f13beddc156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714670"
---
# <a name="registering-ndf-helper-class-extensions"></a><span data-ttu-id="4d288-104">Registrieren von NDF-Hilfsklassen Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="4d288-104">Registering NDF Helper Class Extensions</span></span>

<span data-ttu-id="4d288-105">Jeder Hilfsklassen Erweiterung sind mehrere Registrierungsschlüssel zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="4d288-105">Each helper class extension has a number of registry keys associated with it.</span></span> <span data-ttu-id="4d288-106">Einige Schlüssel sind für com erforderlich, und einige Schlüssel sind für die NDF erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4d288-106">Some keys are required by COM, and some keys are required by NDF.</span></span>

## <a name="com-registry-keys"></a><span data-ttu-id="4d288-107">COM-Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="4d288-107">COM Registry Keys</span></span>

<span data-ttu-id="4d288-108">Hilfsklassen Erweiterungen müssen als com-Server implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="4d288-108">Helper class extensions must be implemented as COM servers.</span></span> <span data-ttu-id="4d288-109">Die com-Registrierung muss für jede hilfsklassenerweiterung abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="4d288-109">COM registration must be completed for each helper class extension.</span></span> <span data-ttu-id="4d288-110">Die CLSID des Objekts, die [**inetdiaghelperinfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) -Schnittstelle und die [**inetdiaghelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) -Schnittstelle müssen registriert werden.</span><span class="sxs-lookup"><span data-stu-id="4d288-110">The object's CLSID, the [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) interface, and the [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) interface must be registered.</span></span> <span data-ttu-id="4d288-111">Bei der Registrierung wird eine Reihe von com-bezogenen Registrierungs Schlüsseln für die NDF-hilfsklassenerweiterung erstellt.</span><span class="sxs-lookup"><span data-stu-id="4d288-111">Registration creates a number of COM-related registry keys for the NDF helper class extension.</span></span>

## <a name="ndf-registry-keys"></a><span data-ttu-id="4d288-112">NDF-Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="4d288-112">NDF Registry Keys</span></span>

<span data-ttu-id="4d288-113">Hilfsklassen Erweiterungen müssen registriert werden, bevor Sie mit dem Netzwerk Diagnose Framework und mit anderen verwandten Hilfsklassen interagieren können.</span><span class="sxs-lookup"><span data-stu-id="4d288-113">Helper class extensions must be registered before interacting with the Network Diagnostics Framework and with other related helper classes.</span></span> <span data-ttu-id="4d288-114">Dies wird durch Auffüllen der Registrierung erreicht.</span><span class="sxs-lookup"><span data-stu-id="4d288-114">This is accomplished by populating the registry.</span></span>

<span data-ttu-id="4d288-115">Im folgenden Verfahren wird gezeigt, wie Sie der Registrierung Hilfsklassen Erweiterungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4d288-115">The following procedure shows how to add helper class extensions to the registry.</span></span>

1.  <span data-ttu-id="4d288-116">Veröffentlichen Sie die Namen der von der dll implementierten Hilfsklassen und ihrer Abhängigkeiten, indem Sie einen Schlüssel für die dll unter erstellen.</span><span class="sxs-lookup"><span data-stu-id="4d288-116">Publish the names of helper classes implemented by the DLL and their dependencies by creating a key for the DLL under</span></span>

    <span data-ttu-id="4d288-117">**HKLM \\ System \\ CurrentControlSet- \\ Steuerelement \\ netdiagfx** \\ *VendorName* \\ **hostdlls** \\ *Hilfsklasse dll* \\ **helperclasses** \\ *Hilfsklassenname*</span><span class="sxs-lookup"><span data-stu-id="4d288-117">**HKLM\\System\\CurrentControlSet\\Control\\NetDiagFx**\\*VendorName*\\**HostDLLs**\\*Helper Class DLL*\\**HelperClasses**\\*Helper Class Name*</span></span>

    <span data-ttu-id="4d288-118">Ersetzen Sie *VendorName*, *Helper Class dll* und *Helper Class Name* durch benutzerdefinierte Werte, wie unten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4d288-118">Replace *VendorName*, *Helper Class DLL*, and *Helper Class Name* with user-defined values as described below.</span></span>

    | <span data-ttu-id="4d288-119">Wert</span><span class="sxs-lookup"><span data-stu-id="4d288-119">Value</span></span>               | <span data-ttu-id="4d288-120">type</span><span class="sxs-lookup"><span data-stu-id="4d288-120">Type</span></span>    | <span data-ttu-id="4d288-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4d288-121">Meaning</span></span>                                                                      |
    |---------------------|---------|------------------------------------------------------------------------------|
    | <span data-ttu-id="4d288-122">*VendorName*</span><span class="sxs-lookup"><span data-stu-id="4d288-122">*VendorName*</span></span>        | <span data-ttu-id="4d288-123">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="4d288-123">REG\_SZ</span></span> | <span data-ttu-id="4d288-124">Der Name des Herstellers.</span><span class="sxs-lookup"><span data-stu-id="4d288-124">The name of the vendor.</span></span>                                                      |
    | <span data-ttu-id="4d288-125">*Hilfsklassen-dll*</span><span class="sxs-lookup"><span data-stu-id="4d288-125">*Helper Class DLL*</span></span>  | <span data-ttu-id="4d288-126">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="4d288-126">REG\_SZ</span></span> | <span data-ttu-id="4d288-127">Der Name der DLL ohne Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="4d288-127">Name of the DLL, without extension.</span></span>                                          |
    | <span data-ttu-id="4d288-128">*Name der Hilfsklasse*</span><span class="sxs-lookup"><span data-stu-id="4d288-128">*Helper Class Name*</span></span> | <span data-ttu-id="4d288-129">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="4d288-129">REG\_SZ</span></span> | <span data-ttu-id="4d288-130">Der Name der Hilfsklasse, von der die aktuelle Hilfsklasse abhängt.</span><span class="sxs-lookup"><span data-stu-id="4d288-130">The name of the helper class on which the current helper class is dependent.</span></span> |

    

     

2.  <span data-ttu-id="4d288-131">Veröffentlichen Sie unter jedem Namen Schlüssel der *Hilfsprogrammklasse* die folgenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="4d288-131">Under each *Helper Class Name* key, publish the following information.</span></span>

    

    | <span data-ttu-id="4d288-132">Wert</span><span class="sxs-lookup"><span data-stu-id="4d288-132">Value</span></span>         | <span data-ttu-id="4d288-133">type</span><span class="sxs-lookup"><span data-stu-id="4d288-133">Type</span></span>       | <span data-ttu-id="4d288-134">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4d288-134">Meaning</span></span>                                                                                                                                                                 |
    |---------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="4d288-135">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="4d288-135">**CLSID**</span></span>     | <span data-ttu-id="4d288-136">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="4d288-136">REG\_SZ</span></span>    | <span data-ttu-id="4d288-137">Eine Zeichenfolge, die die com-Klassen-ID der Hilfsklasse enthält.</span><span class="sxs-lookup"><span data-stu-id="4d288-137">A string that contains the COM class ID of the helper class.</span></span>                                                                                                            |
    | <span data-ttu-id="4d288-138">**Version**</span><span class="sxs-lookup"><span data-stu-id="4d288-138">**Version**</span></span>   | <span data-ttu-id="4d288-139">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="4d288-139">REG\_SZ</span></span>    | <span data-ttu-id="4d288-140">Eine Zeichenfolge, die die Haupt-und neben Versionen der Hilfsklasse im-Format enthält <major> <minor> .</span><span class="sxs-lookup"><span data-stu-id="4d288-140">A string the contains the major and minor versions of the helper class in the format <major><minor>.</span></span>                                                        |
    | <span data-ttu-id="4d288-141">**Enes**</span><span class="sxs-lookup"><span data-stu-id="4d288-141">**Published**</span></span> | <span data-ttu-id="4d288-142">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="4d288-142">REG\_DWORD</span></span> | <span data-ttu-id="4d288-143">Der Wert 1 bedeutet, dass diese Hilfsklasse direkt vom Diagnose Client aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d288-143">A value of 1 means that this helper class is expected to be directly invoked from the Diagnostics client.</span></span> <span data-ttu-id="4d288-144">der Wert 0 bedeutet, dass er nur von einer anderen Hilfsklasse aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="4d288-144">0 means that it can be called only from another helper class.</span></span> |
    | <span data-ttu-id="4d288-145">**Parent**</span><span class="sxs-lookup"><span data-stu-id="4d288-145">**Parent**</span></span>    | <span data-ttu-id="4d288-146">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="4d288-146">REG\_SZ</span></span>    | <span data-ttu-id="4d288-147">Eine Zeichenfolge, die die Microsoft Extensible Helper-Klasse benennt, die erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="4d288-147">A string that names the Microsoft extensible helper class that is being extended.</span></span>                                                                                       |

    

     

3.  <span data-ttu-id="4d288-148">Veröffentlichen Sie für jede Hilfsklasse die Liste der übereinstimmenden Attribute, indem Sie einen Schlüssel unter</span><span class="sxs-lookup"><span data-stu-id="4d288-148">For each helper class, publish the list of matching attributes by creating a key under</span></span>

    <span data-ttu-id="4d288-149">**HKLM \\ System \\ CurrentControlSet \\ Control \\ netdiagfx** \\ *VendorName* \\ **hostdlls** \\ *Hilfsklasse dll* \\ **helperclasses** \\ *Hilfsklassen Name* \\ **MatchAttribute**</span><span class="sxs-lookup"><span data-stu-id="4d288-149">**HKLM\\System\\CurrentControlSet\\Control\\NetDiagFx**\\*VendorName*\\**HostDLLs**\\*Helper Class DLL*\\**HelperClasses**\\*Helper Class Name*\\**MatchAttributes**</span></span>

    <span data-ttu-id="4d288-150">Der Schlüssel muss mindestens einen Wert (einen pro Attribut) des folgenden Typs enthalten.</span><span class="sxs-lookup"><span data-stu-id="4d288-150">They key must contain one or more values (one per attribute) of the following type.</span></span>

    | <span data-ttu-id="4d288-151">Wert</span><span class="sxs-lookup"><span data-stu-id="4d288-151">Value</span></span>             | <span data-ttu-id="4d288-152">type</span><span class="sxs-lookup"><span data-stu-id="4d288-152">Type</span></span>                             | <span data-ttu-id="4d288-153">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4d288-153">Meaning</span></span>                                                                    |
    |-------------------|----------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="4d288-154">**AttributeName**</span><span class="sxs-lookup"><span data-stu-id="4d288-154">**AttributeName**</span></span> | <span data-ttu-id="4d288-155">reg \_ SZ \| reg \_ DWORD \| reg \_ Binär</span><span class="sxs-lookup"><span data-stu-id="4d288-155">REG\_SZ\|REG\_DWORD\|REG\_BINARY</span></span> | <span data-ttu-id="4d288-156">Ein-Wert, der das Name-Wert-Paar für ein bestimmtes Attribut abschließt.</span><span class="sxs-lookup"><span data-stu-id="4d288-156">A value that completes the name and value pair for a particular attribute.</span></span> |

    

     

 

 




