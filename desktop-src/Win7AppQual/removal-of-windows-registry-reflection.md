---
description: .
ms.assetid: 4b42d44d-cde8-4d96-96c5-24b7ab7e4cec
title: Entfernen der Windows-Registrierungs Reflektion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c610cb0b6ce446e3105fd61cb940028f478892ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364215"
---
# <a name="removal-of-windows-registry-reflection"></a><span data-ttu-id="7ea56-103">Entfernen der Windows-Registrierungs Reflektion</span><span class="sxs-lookup"><span data-stu-id="7ea56-103">Removal of Windows Registry Reflection</span></span>

## <a name="platform"></a><span data-ttu-id="7ea56-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="7ea56-104">Platform</span></span>

<span data-ttu-id="7ea56-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="7ea56-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="7ea56-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7ea56-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="7ea56-107">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="7ea56-107">Feature Impact</span></span>

 <span data-ttu-id="7ea56-108">**Schweregrad** -niedrig</span><span class="sxs-lookup"><span data-stu-id="7ea56-108">**Severity** - Low</span></span>  
<span data-ttu-id="7ea56-109">**Häufigkeit** -niedrig</span><span class="sxs-lookup"><span data-stu-id="7ea56-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="7ea56-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ea56-110">Description</span></span>

<span data-ttu-id="7ea56-111">Der Registrierungs Reflektionsprozess kopiert Registrierungsschlüssel und-Werte zwischen zwei Registrierungs Sichten, um sie synchron zu halten. In früheren 64-Bit-Installationen von Windows hat der Prozess eine Teilmenge der umgeleiteten Registrierungsschlüssel zwischen den 32-Bit-und 64-Bit-Sichten reflektiert.</span><span class="sxs-lookup"><span data-stu-id="7ea56-111">The registry reflection process copies registry keys and values between two registry views to keep them in synch. In previous 64-bit installations of Windows, the process reflected a subset of the redirected registry keys between the 32-bit and 64-bit views.</span></span> <span data-ttu-id="7ea56-112">Die Implementierung dieser Ursache hat jedoch einige Inkonsistenzen im Zustand der Registrierung verursacht.</span><span class="sxs-lookup"><span data-stu-id="7ea56-112">However, the implementation of this caused some inconsistencies in the state of the registry.</span></span> <span data-ttu-id="7ea56-113">(Ausführliche Informationen zur Registrierungs Reflektion finden Sie im entsprechenden MSDN-Artikel im Abschnitt *Links zu anderen Ressourcen* weiter unten.)</span><span class="sxs-lookup"><span data-stu-id="7ea56-113">(For details on Registry Reflection, please refer to the corresponding MSDN article in the *Links to Other Resources* section below.)</span></span>

<span data-ttu-id="7ea56-114">Ab Windows 7 haben wir die Registrierungs Reflektion vollständig entfernt und die Schlüssel zusammengeführt, die für die Wiederverwendung verwendet wurden:</span><span class="sxs-lookup"><span data-stu-id="7ea56-114">Starting with Windows 7, we have removed registry reflection completely and merged the keys that used to be reflected:</span></span>

-   <span data-ttu-id="7ea56-115">HKEY \_ - \_ \\ Software \\ Klassen für lokale Computer</span><span class="sxs-lookup"><span data-stu-id="7ea56-115">HKEY\_LOCAL\_MACHINE\\Software\\Classes</span></span>
-   <span data-ttu-id="7ea56-116">HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ COM3</span><span class="sxs-lookup"><span data-stu-id="7ea56-116">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\COM3</span></span>
-   <span data-ttu-id="7ea56-117">HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ EventSystem</span><span class="sxs-lookup"><span data-stu-id="7ea56-117">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\EventSystem</span></span>
-   <span data-ttu-id="7ea56-118">HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ OLE</span><span class="sxs-lookup"><span data-stu-id="7ea56-118">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Ole</span></span>
-   <span data-ttu-id="7ea56-119">HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ RPC</span><span class="sxs-lookup"><span data-stu-id="7ea56-119">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Rpc</span></span>
-   <span data-ttu-id="7ea56-120">\_ \\ \* \\ Software \\ Klassen für HKEY-Benutzer</span><span class="sxs-lookup"><span data-stu-id="7ea56-120">HKEY\_USERS\\\*\\Software\\Classes</span></span>
-   <span data-ttu-id="7ea56-121">HKEY- \_ Benutzer \\ \* \_ Klassen</span><span class="sxs-lookup"><span data-stu-id="7ea56-121">HKEY\_USERS\\\*\_Classes</span></span>

<span data-ttu-id="7ea56-122">Dadurch wird das gleiche Reflektionsverhalten bereitgestellt, da Änderungen an diesen Schlüsseln sofort für 32-Bit-und 64-Bit-Anwendungen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7ea56-122">Effectively, this provides the same reflection behavior, since changes to these keys immediately are available for both 32-bit and 64-bit applications.</span></span>

<span data-ttu-id="7ea56-123">Die Schlüssel, die bedingt reflektiert wurden, bleiben getrennt:</span><span class="sxs-lookup"><span data-stu-id="7ea56-123">The keys that were reflected conditionally remain split:</span></span>

-   <span data-ttu-id="7ea56-124">HKEY \_ - \_ \\ Software \\ Klassen- \\ CLSID für lokale Computer</span><span class="sxs-lookup"><span data-stu-id="7ea56-124">HKEY\_LOCAL\_MACHINE\\Software\\Classes\\CLSID</span></span>
-   <span data-ttu-id="7ea56-125">Schnittstelle für HKEY- \_ \_ \\ Software \\ Klassen \\ für lokale Computer</span><span class="sxs-lookup"><span data-stu-id="7ea56-125">HKEY\_LOCAL\_MACHINE\\Software\\Classes\\Interface</span></span>
-   <span data-ttu-id="7ea56-126">HKEY- \_ Benutzer- \\ \* \\ Software \\ Klassen \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="7ea56-126">HKEY\_USERS\\\*\\Software\\Classes\\CLSID</span></span>
-   <span data-ttu-id="7ea56-127">Schnittstelle für HKEY- \_ Benutzer- \\ \* \\ Software \\ Klassen \\</span><span class="sxs-lookup"><span data-stu-id="7ea56-127">HKEY\_USERS\\\*\\Software\\Classes\\Interface</span></span>
-   <span data-ttu-id="7ea56-128">HKEY- \_ Benutzer \\ \* \_ Klassen \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="7ea56-128">HKEY\_USERS\\\*\_Classes\\CLSID</span></span>
-   <span data-ttu-id="7ea56-129">\_ \\ \* \_ Klassen \\ Schnittstelle für HKEY-Benutzer</span><span class="sxs-lookup"><span data-stu-id="7ea56-129">HKEY\_USERS\\\*\_Classes\\Interface</span></span>

<span data-ttu-id="7ea56-130">Sie werden verwendet, um die Daten beizubehalten, die von 32-Bit-und 64-Bit-Anwendungen nicht gemeinsam verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7ea56-130">They are used to keep the data that should not be shared between 32-bit and 64-bit applications.</span></span>

## <a name="manifestation"></a><span data-ttu-id="7ea56-131">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="7ea56-131">Manifestation</span></span>

<span data-ttu-id="7ea56-132">CLSID-und Schnittstellen Schlüssel aus der obigen Liste werden nicht mehr angezeigt, wenn Sie noch umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="7ea56-132">CLSID and Interface keys from the list above are not reflected anymore while they are still redirected.</span></span> <span data-ttu-id="7ea56-133">Obwohl dies das gewünschte Verhalten in den meisten Fällen ist, kann es vorkommen, dass Anwendungen eine Abhängigkeit von Ihrem reflektierten Verhalten in Vista annehmen können.</span><span class="sxs-lookup"><span data-stu-id="7ea56-133">While this is the desired behavior in most of cases, it is possible that applications could take a dependency on their reflected behavior in Vista.</span></span>

<span data-ttu-id="7ea56-134">Die Funktionen, mit denen Anwendungen die Reflektion steuern können (regdisablereflectionkey und regenablereflectionkey), sind in Windows 7 nicht funktionsfähig.</span><span class="sxs-lookup"><span data-stu-id="7ea56-134">The functions allowing applications to control reflection (RegDisableReflectionKey and RegEnableReflectionKey) are no-ops in Windows 7.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="7ea56-135">Minderung der Auswirkung</span><span class="sxs-lookup"><span data-stu-id="7ea56-135">Mitigation of Impact</span></span>

<span data-ttu-id="7ea56-136">COM ist der größte Consumer der Registrierungs Reflektion.</span><span class="sxs-lookup"><span data-stu-id="7ea56-136">COM is the major consumer of registry reflection.</span></span> <span data-ttu-id="7ea56-137">COM und andere Consumer wurden aktualisiert, um dieser Änderung Rechnung zu tragen.</span><span class="sxs-lookup"><span data-stu-id="7ea56-137">COM and other consumers were updated to accommodate this change.</span></span> <span data-ttu-id="7ea56-138">Diese Änderung wirkt sich nicht auf Anwendungen aus, die com-Standard-APIs verwenden.</span><span class="sxs-lookup"><span data-stu-id="7ea56-138">This change does not affect applications that use standard COM APIs..</span></span>

## <a name="solution"></a><span data-ttu-id="7ea56-139">Lösung</span><span class="sxs-lookup"><span data-stu-id="7ea56-139">Solution</span></span>

<span data-ttu-id="7ea56-140">Wenden Sie eine der folgenden Optionen an, wenn Sie sich für die Synchronisierung von 32-Bit-und 64-Bit-Ansichten auf die Registrierung der</span><span class="sxs-lookup"><span data-stu-id="7ea56-140">Apply one of the following options if you are relying on registry reflection to synchronize 32bit and 64bit views:</span></span>

-   <span data-ttu-id="7ea56-141">Erstellen Sie während der Installation explizit Schlüssel in beiden Ansichten.</span><span class="sxs-lookup"><span data-stu-id="7ea56-141">Create keys in both views explicitly during installation</span></span>
-   <span data-ttu-id="7ea56-142">Verschieben der Schlüssel aus dem Bereich der reflektierten Schlüssel</span><span class="sxs-lookup"><span data-stu-id="7ea56-142">Move the keys out of the scope of reflected keys</span></span>
-   <span data-ttu-id="7ea56-143">Überprüfen Sie beim Abfragen eines reflektierten Schlüssels beide Sichten der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="7ea56-143">Check both views of the registry when querying for a reflected key</span></span>

    <span data-ttu-id="7ea56-144">**Hinweis:** Key \_ WOW64 \_ 32key und Key \_ WOW64 \_ 64 Schlüsselflags können nicht kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="7ea56-144">**Note:** KEY\_WOW64\_32KEY and KEY\_WOW64\_64KEY flags cannot be combined</span></span>

<span data-ttu-id="7ea56-145">Wenden Sie eine der folgenden Optionen an, wenn Sie sich auf regdisablereflectionkey-Funktionen verlassen, um die Registrierungs Reflektion zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="7ea56-145">Apply one of the following options if you are relying on RegDisableReflectionKey functions to disable registry reflection:</span></span>

-   <span data-ttu-id="7ea56-146">Erstellen Sie während der Installation explizit Schlüssel in beiden Ansichten.</span><span class="sxs-lookup"><span data-stu-id="7ea56-146">Create keys in both views explicitly during installation</span></span>
-   <span data-ttu-id="7ea56-147">Verschieben der Schlüssel aus dem Bereich der reflektierten Schlüssel</span><span class="sxs-lookup"><span data-stu-id="7ea56-147">Move the keys out of the scope of reflected keys</span></span>
-   <span data-ttu-id="7ea56-148">Verwenden Sie plattformspezifische Unterschlüssel (z. b. x86, amd64 und ia64), um Bitness spezifische Daten zu trennen.</span><span class="sxs-lookup"><span data-stu-id="7ea56-148">Use platform-specific subkeys (like x86, amd64 and ia64) to separate bitness-specific data</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="7ea56-149">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7ea56-149">Links to Other Resources</span></span>

-   [<span data-ttu-id="7ea56-150">Artikel zur Registrierungs Reflektion</span><span class="sxs-lookup"><span data-stu-id="7ea56-150">Registry Reflection article</span></span>](../winprog64/registry-reflection.md)
-   [<span data-ttu-id="7ea56-151">Liste mit umgeleiteten Schlüsseln im Artikel zum Registrierungs Redirector</span><span class="sxs-lookup"><span data-stu-id="7ea56-151">Redirected keys list within Registry Redirector article</span></span>](../winprog64/registry-redirector.md)
-   [<span data-ttu-id="7ea56-152">Bewährte Methoden für WOW64</span><span class="sxs-lookup"><span data-stu-id="7ea56-152">Best Practices for Wow64</span></span>](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)

> [!Note]  
> <span data-ttu-id="7ea56-153">Diese Ressourcen sind in einigen Sprachen und Ländern bzw. Regionen möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7ea56-153">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
