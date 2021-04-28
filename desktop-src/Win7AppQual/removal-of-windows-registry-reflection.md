---
description: Entfernen der Windows-Registrierungslektion
ms.assetid: 4b42d44d-cde8-4d96-96c5-24b7ab7e4cec
title: Entfernen der Windows-Registrierungslektion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeab0109cbbac988c89d6add91fa899cea9169ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116258"
---
# <a name="removal-of-windows-registry-reflection"></a><span data-ttu-id="ca2ab-103">Entfernen der Windows-Registrierungslektion</span><span class="sxs-lookup"><span data-stu-id="ca2ab-103">Removal of Windows Registry Reflection</span></span>

## <a name="platform"></a><span data-ttu-id="ca2ab-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="ca2ab-104">Platform</span></span>

<span data-ttu-id="ca2ab-105">**Clients** – Windows 7</span><span class="sxs-lookup"><span data-stu-id="ca2ab-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="ca2ab-106">**Server** – Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ca2ab-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="ca2ab-107">Auswirkung von Features</span><span class="sxs-lookup"><span data-stu-id="ca2ab-107">Feature Impact</span></span>

 <span data-ttu-id="ca2ab-108">**Schweregrad:** Niedrig</span><span class="sxs-lookup"><span data-stu-id="ca2ab-108">**Severity** - Low</span></span>  
<span data-ttu-id="ca2ab-109">**Häufigkeit** – Niedrig</span><span class="sxs-lookup"><span data-stu-id="ca2ab-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="ca2ab-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca2ab-110">Description</span></span>

<span data-ttu-id="ca2ab-111">Der Registrierungslektionsprozess kopiert Registrierungsschlüssel und -werte zwischen zwei Registrierungssichten, um sie synchron zu halten. In früheren 64-Bit-Installationen von Windows spiegelte der Prozess eine Teilmenge der umgeleiteten Registrierungsschlüssel zwischen den 32-Bit- und 64-Bit-Ansichten wider.</span><span class="sxs-lookup"><span data-stu-id="ca2ab-111">The registry reflection process copies registry keys and values between two registry views to keep them in synch. In previous 64-bit installations of Windows, the process reflected a subset of the redirected registry keys between the 32-bit and 64-bit views.</span></span> <span data-ttu-id="ca2ab-112">Die Implementierung von verursachte jedoch einige Inkonsistenzen im Zustand der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="ca2ab-112">However, the implementation of this caused some inconsistencies in the state of the registry.</span></span> <span data-ttu-id="ca2ab-113">(Weitere Informationen zur Reflektion von Registrierungen finden Sie im entsprechenden MSDN-Artikel im Abschnitt *Links zu anderen* Ressourcen weiter unten.)</span><span class="sxs-lookup"><span data-stu-id="ca2ab-113">(For details on Registry Reflection, please refer to the corresponding MSDN article in the *Links to Other Resources* section below.)</span></span>

<span data-ttu-id="ca2ab-114">Ab Windows 7 haben wir die Registrierungslektion vollständig entfernt und die Schlüssel zusammengeführt, die früher widergespiegelt wurden:</span><span class="sxs-lookup"><span data-stu-id="ca2ab-114">Starting with Windows 7, we have removed registry reflection completely and merged the keys that used to be reflected:</span></span>

-   <span data-ttu-id="ca2ab-115">HKEY \_ LOCAL \_ \\ MACHINE-Softwareklassen \\</span><span class="sxs-lookup"><span data-stu-id="ca2ab-115">HKEY\_LOCAL\_MACHINE\\Software\\Classes</span></span>
-   <span data-ttu-id="ca2ab-116">HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ COM3</span><span class="sxs-lookup"><span data-stu-id="ca2ab-116">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\COM3</span></span>
-   <span data-ttu-id="ca2ab-117">HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ EventSystem</span><span class="sxs-lookup"><span data-stu-id="ca2ab-117">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\EventSystem</span></span>
-   <span data-ttu-id="ca2ab-118">HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Ole</span><span class="sxs-lookup"><span data-stu-id="ca2ab-118">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Ole</span></span>
-   <span data-ttu-id="ca2ab-119">HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Rpc</span><span class="sxs-lookup"><span data-stu-id="ca2ab-119">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Rpc</span></span>
-   <span data-ttu-id="ca2ab-120">HKEY \_ \\ \* \\ \\ USERS-Softwareklassen</span><span class="sxs-lookup"><span data-stu-id="ca2ab-120">HKEY\_USERS\\\*\\Software\\Classes</span></span>
-   <span data-ttu-id="ca2ab-121">HKEY \_ \\ \* \_ USERS-Klassen</span><span class="sxs-lookup"><span data-stu-id="ca2ab-121">HKEY\_USERS\\\*\_Classes</span></span>

<span data-ttu-id="ca2ab-122">Effektiv bietet dies das gleiche Reflektionsverhalten, da Änderungen an diesen Schlüsseln sofort sowohl für 32-Bit- als auch für 64-Bit-Anwendungen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ca2ab-122">Effectively, this provides the same reflection behavior, since changes to these keys immediately are available for both 32-bit and 64-bit applications.</span></span>

<span data-ttu-id="ca2ab-123">Die Schlüssel, die bedingt widergespiegelt wurden, bleiben geteilt:</span><span class="sxs-lookup"><span data-stu-id="ca2ab-123">The keys that were reflected conditionally remain split:</span></span>

-   <span data-ttu-id="ca2ab-124">HKEY \_ LOCAL \_ MACHINE \\ Software \\ Classes \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="ca2ab-124">HKEY\_LOCAL\_MACHINE\\Software\\Classes\\CLSID</span></span>
-   <span data-ttu-id="ca2ab-125">HKEY \_ LOCAL \_ MACHINE \\ Software \\ Classes \\ Interface</span><span class="sxs-lookup"><span data-stu-id="ca2ab-125">HKEY\_LOCAL\_MACHINE\\Software\\Classes\\Interface</span></span>
-   <span data-ttu-id="ca2ab-126">HKEY \_ USERS \\ \* \\ Software \\ Classes \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="ca2ab-126">HKEY\_USERS\\\*\\Software\\Classes\\CLSID</span></span>
-   <span data-ttu-id="ca2ab-127">\_HKEY USERS \\ \* \\ Software Classes Interface (Schnittstelle für HKEY USERS-Softwareklassen) \\ \\</span><span class="sxs-lookup"><span data-stu-id="ca2ab-127">HKEY\_USERS\\\*\\Software\\Classes\\Interface</span></span>
-   <span data-ttu-id="ca2ab-128">HKEY \_ \\ \* \_ USERS-Klassen \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="ca2ab-128">HKEY\_USERS\\\*\_Classes\\CLSID</span></span>
-   <span data-ttu-id="ca2ab-129">HKEY \_ \\ \* \_ \\ USERS-Klassenschnittstelle</span><span class="sxs-lookup"><span data-stu-id="ca2ab-129">HKEY\_USERS\\\*\_Classes\\Interface</span></span>

<span data-ttu-id="ca2ab-130">Sie werden verwendet, um die Daten beizubehalten, die nicht von 32-Bit- und 64-Bit-Anwendungen gemeinsam genutzt werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="ca2ab-130">They are used to keep the data that should not be shared between 32-bit and 64-bit applications.</span></span>

## <a name="manifestation"></a><span data-ttu-id="ca2ab-131">Manifestation</span><span class="sxs-lookup"><span data-stu-id="ca2ab-131">Manifestation</span></span>

<span data-ttu-id="ca2ab-132">CLSID- und Schnittstellenschlüssel aus der obigen Liste werden nicht mehr widergespiegelt, während sie noch umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="ca2ab-132">CLSID and Interface keys from the list above are not reflected anymore while they are still redirected.</span></span> <span data-ttu-id="ca2ab-133">Obwohl dies in den meisten Fällen das gewünschte Verhalten ist, ist es möglich, dass Anwendungen von ihrem reflektierten Verhalten in Vista abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="ca2ab-133">While this is the desired behavior in most of cases, it is possible that applications could take a dependency on their reflected behavior in Vista.</span></span>

<span data-ttu-id="ca2ab-134">Die Funktionen, mit denen Anwendungen reflektion (RegDisableReflectionKey und RegEnableReflectionKey) steuern können, sind in Windows 7 keine Ops.</span><span class="sxs-lookup"><span data-stu-id="ca2ab-134">The functions allowing applications to control reflection (RegDisableReflectionKey and RegEnableReflectionKey) are no-ops in Windows 7.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="ca2ab-135">Entschärfung der Auswirkungen</span><span class="sxs-lookup"><span data-stu-id="ca2ab-135">Mitigation of Impact</span></span>

<span data-ttu-id="ca2ab-136">COM ist der Hauptverbraucher der Registrierungsreflektion.</span><span class="sxs-lookup"><span data-stu-id="ca2ab-136">COM is the major consumer of registry reflection.</span></span> <span data-ttu-id="ca2ab-137">COM und andere Consumer wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="ca2ab-137">COM and other consumers were updated to accommodate this change.</span></span> <span data-ttu-id="ca2ab-138">Diese Änderung wirkt sich nicht auf Anwendungen aus, die COM-Standard-APIs verwenden.</span><span class="sxs-lookup"><span data-stu-id="ca2ab-138">This change does not affect applications that use standard COM APIs..</span></span>

## <a name="solution"></a><span data-ttu-id="ca2ab-139">Lösung</span><span class="sxs-lookup"><span data-stu-id="ca2ab-139">Solution</span></span>

<span data-ttu-id="ca2ab-140">Wenden Sie eine der folgenden Optionen an, wenn Sie sich auf die Registrierungsreflektion verlassen, um 32-Bit- und 64-Bit-Ansichten zu synchronisieren:</span><span class="sxs-lookup"><span data-stu-id="ca2ab-140">Apply one of the following options if you are relying on registry reflection to synchronize 32bit and 64bit views:</span></span>

-   <span data-ttu-id="ca2ab-141">Explizites Erstellen von Schlüsseln in beiden Ansichten während der Installation</span><span class="sxs-lookup"><span data-stu-id="ca2ab-141">Create keys in both views explicitly during installation</span></span>
-   <span data-ttu-id="ca2ab-142">Verschieben der Schlüssel aus dem Bereich der reflektierten Schlüssel</span><span class="sxs-lookup"><span data-stu-id="ca2ab-142">Move the keys out of the scope of reflected keys</span></span>
-   <span data-ttu-id="ca2ab-143">Überprüfen beider Ansichten der Registrierung beim Abfragen eines reflektierten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="ca2ab-143">Check both views of the registry when querying for a reflected key</span></span>

    <span data-ttu-id="ca2ab-144">**Hinweis:** KEY \_ WOW64 \_ 32KEY- und KEY \_ WOW64 \_ 64KEY-Flags können nicht kombiniert werden</span><span class="sxs-lookup"><span data-stu-id="ca2ab-144">**Note:** KEY\_WOW64\_32KEY and KEY\_WOW64\_64KEY flags cannot be combined</span></span>

<span data-ttu-id="ca2ab-145">Wenden Sie eine der folgenden Optionen an, wenn Sie regDisableReflectionKey-Funktionen verwenden, um die Reflektion der Registrierung zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="ca2ab-145">Apply one of the following options if you are relying on RegDisableReflectionKey functions to disable registry reflection:</span></span>

-   <span data-ttu-id="ca2ab-146">Explizites Erstellen von Schlüsseln in beiden Ansichten während der Installation</span><span class="sxs-lookup"><span data-stu-id="ca2ab-146">Create keys in both views explicitly during installation</span></span>
-   <span data-ttu-id="ca2ab-147">Verschieben der Schlüssel aus dem Bereich der reflektierten Schlüssel</span><span class="sxs-lookup"><span data-stu-id="ca2ab-147">Move the keys out of the scope of reflected keys</span></span>
-   <span data-ttu-id="ca2ab-148">Verwenden Sie plattformspezifische Unterschlüssel (wie x86, amd64 und ia64), um bitspezifische Daten zu trennen.</span><span class="sxs-lookup"><span data-stu-id="ca2ab-148">Use platform-specific subkeys (like x86, amd64 and ia64) to separate bitness-specific data</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="ca2ab-149">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ca2ab-149">Links to Other Resources</span></span>

-   [<span data-ttu-id="ca2ab-150">Artikel zur Registrierungslektion</span><span class="sxs-lookup"><span data-stu-id="ca2ab-150">Registry Reflection article</span></span>](../winprog64/registry-reflection.md)
-   [<span data-ttu-id="ca2ab-151">Liste der umgeleiteten Schlüssel im Artikel "Registrierungsumleitung"</span><span class="sxs-lookup"><span data-stu-id="ca2ab-151">Redirected keys list within Registry Redirector article</span></span>](../winprog64/registry-redirector.md)
-   [<span data-ttu-id="ca2ab-152">Bewährte Methoden für Wow64</span><span class="sxs-lookup"><span data-stu-id="ca2ab-152">Best Practices for Wow64</span></span>](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)

> [!Note]  
> <span data-ttu-id="ca2ab-153">Diese Ressourcen sind in einigen Sprachen und Ländern/Regionen möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ca2ab-153">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
