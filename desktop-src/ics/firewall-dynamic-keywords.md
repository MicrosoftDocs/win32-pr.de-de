---
title: Dynamische Firewallschlüsselwörter
description: Sie verwenden die APIs für dynamische Firewallschlüsselwörter, um dynamische Schlüsselwortadressen in Windows Defender Firewall zu verwalten.
keywords:
- Dynamische Firewallschlüsselwörter
ms.topic: article
ms.date: 05/17/2021
ms.localizationpriority: low
ms.openlocfilehash: e60526d8a7889af3173913774790bdd209121040
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2021
ms.locfileid: "112681166"
---
# <a name="firewall-dynamic-keywords"></a><span data-ttu-id="a90a6-104">Dynamische Firewallschlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a90a6-104">Firewall dynamic keywords</span></span>

<span data-ttu-id="a90a6-105">Sie verwenden die APIs für dynamische Schlüsselwörter der Firewall, um *dynamische Schlüsselwortadressen* in [Windows Defender Firewall](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security)zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="a90a6-105">You use the firewall dynamic keywords APIs to manage *dynamic keyword addresses* in [Windows Defender Firewall](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security).</span></span> <span data-ttu-id="a90a6-106">Eine dynamische Schlüsselwortadresse wird verwendet, um einen Satz von IP-Adressen zu erstellen, auf die eine oder mehrere Firewallregeln verweisen können.</span><span class="sxs-lookup"><span data-stu-id="a90a6-106">A dynamic keyword address is used to create a set of IP addresses to which one or more firewall rules can refer.</span></span> <span data-ttu-id="a90a6-107">Dynamische Schlüsselwortadressen unterstützen sowohl IPv4 als auch IPv6.</span><span class="sxs-lookup"><span data-stu-id="a90a6-107">Dynamic keyword addresses support both IPv4 and IPv6.</span></span>

> [!NOTE]
> <span data-ttu-id="a90a6-108">Api-Referenzinhalte für die in diesem Thema eingeführten APIs finden Sie unter Referenz zu [dynamischen Firewallschlüsselwörtern.](firewall-dynamic-keywords-reference.md)</span><span class="sxs-lookup"><span data-stu-id="a90a6-108">For API reference content for the APIs introduced in this topic, see [Firewall dynamic keywords reference](firewall-dynamic-keywords-reference.md).</span></span>

## <a name="operations-on-dynamic-keyword-addresses"></a><span data-ttu-id="a90a6-109">Vorgänge für dynamische Schlüsselwortadressen</span><span class="sxs-lookup"><span data-stu-id="a90a6-109">Operations on dynamic keyword addresses</span></span>

<span data-ttu-id="a90a6-110">Mit den APIs für dynamische Firewallschlüsselwörter können Sie die folgenden Vorgänge ausführen.</span><span class="sxs-lookup"><span data-stu-id="a90a6-110">With the Firewall dynamic keywords APIs, you can perform the following operations.</span></span>

* <span data-ttu-id="a90a6-111">Hinzufügen dynamischer Schlüsselwortadressen</span><span class="sxs-lookup"><span data-stu-id="a90a6-111">Add dynamic keyword addresses</span></span>
* <span data-ttu-id="a90a6-112">Löschen dynamischer Schlüsselwortadressen</span><span class="sxs-lookup"><span data-stu-id="a90a6-112">Delete dynamic keyword addresses</span></span>
* <span data-ttu-id="a90a6-113">Aufzählen dynamischer Schlüsselwortadressen nach ID oder Typ</span><span class="sxs-lookup"><span data-stu-id="a90a6-113">Enumerate dynamic keyword addresses by ID, or by type</span></span>
* <span data-ttu-id="a90a6-114">Aktualisieren dynamischer Schlüsselwortadressen</span><span class="sxs-lookup"><span data-stu-id="a90a6-114">Update dynamic keyword addresses</span></span>
* <span data-ttu-id="a90a6-115">Abonnieren und Behandeln von Benachrichtigungen über Dynamische Schlüsselwortadressänderungen</span><span class="sxs-lookup"><span data-stu-id="a90a6-115">Subscribe to, and handle, dynamic keyword address change notifications</span></span>

<span data-ttu-id="a90a6-116">Es gibt Codebeispiele für alle diese Vorgänge weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="a90a6-116">There are code examples for all of those operations later in this topic.</span></span>

<span data-ttu-id="a90a6-117">Nachdem Sie eine dynamische Schlüsselwortadresse hinzugefügt haben, wird sie bei Neustarts beibehalten.</span><span class="sxs-lookup"><span data-stu-id="a90a6-117">Once you've added a dynamic keyword address, it persists across reboots.</span></span> <span data-ttu-id="a90a6-118">Sie müssen eine dynamische Schlüsselwortadresse löschen, sobald Sie mit dem -Objekt fertig sind.</span><span class="sxs-lookup"><span data-stu-id="a90a6-118">You must delete a dynamic keyword address once you're done with the object.</span></span>

<span data-ttu-id="a90a6-119">Es gibt zwei Klassen dynamischer Schlüsselwortadressen, wie in den nächsten beiden Abschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a90a6-119">There are two classes of dynamic keyword addresses, as described in the next two sections.</span></span>

## <a name="autoresolve-dynamic-keyword-addresses"></a><span data-ttu-id="a90a6-120">Dynamische Schlüsselwortadressen automatisch auflösen</span><span class="sxs-lookup"><span data-stu-id="a90a6-120">AutoResolve dynamic keyword addresses</span></span>

<span data-ttu-id="a90a6-121">Der erste Typ ist *AutoResolve,* wobei das *Schlüsselwortfeld* einen auflösbaren Namen darstellt und die IP-Adressen bei der Erstellung nicht definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a90a6-121">The first type is *AutoResolve*, where the *keyword* field represents a resolvable name, and the IP addresses aren't defined upon creation.</span></span>

<span data-ttu-id="a90a6-122">Diese Objekte sollen ihre IP-Adressen automatisch auflösen.</span><span class="sxs-lookup"><span data-stu-id="a90a6-122">These objects are intended to have their IP addresses resolved automatically.</span></span> <span data-ttu-id="a90a6-123">Das heißt, nicht über einen Administrator zum Zeitpunkt der Objekterstellung; auch nicht über das Betriebssystem selbst.</span><span class="sxs-lookup"><span data-stu-id="a90a6-123">That is, not through an admin at object creation time; nor through the operating system (OS) itself.</span></span> <span data-ttu-id="a90a6-124">Eine Komponente außerhalb des Firewalldiensts muss die IP-Adressauflösung für diese Objekte durchführen und sie entsprechend aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a90a6-124">A component outside of the firewall service must do the IP address resolution for these objects, and update them appropriately.</span></span> <span data-ttu-id="a90a6-125">Die Implementierung einer solchen Komponente liegt außerhalb des Bereichs dieses Inhalts.</span><span class="sxs-lookup"><span data-stu-id="a90a6-125">The implementation of such a component is outside the scope of this content.</span></span>

<span data-ttu-id="a90a6-126">Eine dynamische Schlüsselwortadresse wird als *AutoResolve* angegeben, indem das **FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE-Flag** im -Objekt festgelegt wird, wenn die [**FWAddDynamicKeywordAddress0-Funktion**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a90a6-126">A dynamic keyword address is indicated as being *AutoResolve* by setting the **FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE** flag in the object when calling the [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) function.</span></span> <span data-ttu-id="a90a6-127">Das *Schlüsselwortfeld* sollte verwendet werden, um den aufgelösten Wert &mdash; darzustellen, d. h. einen vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) oder einen Hostnamen.</span><span class="sxs-lookup"><span data-stu-id="a90a6-127">The *keyword* field should be used to represent the value being resolved&mdash;that is, a fully qualified domain name (FQDN) or hostname.</span></span> <span data-ttu-id="a90a6-128">Das  Adressfeld muss für diese Objekte anfänglich NULL sein.</span><span class="sxs-lookup"><span data-stu-id="a90a6-128">The *addresses* field must initially be NULL for these objects.</span></span> <span data-ttu-id="a90a6-129">Bei diesen Objekten werden ihre IP-Adressen nicht über Startzyklen hinweg beibehalten, und Sie sollten ihre Adressen während des nächsten Startzyklus neu auswerten/erneut auffüllen.</span><span class="sxs-lookup"><span data-stu-id="a90a6-129">These objects won't have their IP addresses persisted across boot cycles, and you should re-evaluate/re-populate their addresses during the next boot cycle.</span></span>

> [!NOTE]
> <span data-ttu-id="a90a6-130">AutoResolve dynamic keyword address objects trigger notifications on [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) and [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0), but not [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span><span class="sxs-lookup"><span data-stu-id="a90a6-130">AutoResolve dynamic keyword address objects trigger notifications on [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) and [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0), but not [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span></span>

## <a name="non-autoresolve-dynamic-keyword-addresses"></a><span data-ttu-id="a90a6-131">Dynamische Schlüsselwortadressen, die nicht automatisch aufgelöst werden</span><span class="sxs-lookup"><span data-stu-id="a90a6-131">Non-AutoResolve dynamic keyword addresses</span></span>

<span data-ttu-id="a90a6-132">Der zweite Typ ist *nicht AutoResolve,* wobei das *Schlüsselwortfeld* eine beliebige Zeichenfolge ist und die Adressen zum Zeitpunkt der Erstellung definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a90a6-132">The second type is *non-AutoResolve*, where the *keyword* field is any string, and the addresses are defined at creation time.</span></span>

<span data-ttu-id="a90a6-133">Diese Objekte werden verwendet, um einen Satz von IP-Adressen, Subnetzen oder Bereichen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a90a6-133">These objects are used to store a set of IP address, subnets, or ranges.</span></span> <span data-ttu-id="a90a6-134">Das *Schlüsselwortfeld* wird hier zur Vereinfachung der Verwaltung verwendet und kann auf eine beliebige Zeichenfolge festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a90a6-134">The *keyword* field here is used for management convenience, and it can be set to any string.</span></span> <span data-ttu-id="a90a6-135">Das  Adressfeld muss bei der Erstellung ungleich NULL sein.</span><span class="sxs-lookup"><span data-stu-id="a90a6-135">The *addresses* field must be non-NULL upon creation.</span></span> <span data-ttu-id="a90a6-136">Adressen für diese Objekte werden bei Neustarts beibehalten.</span><span class="sxs-lookup"><span data-stu-id="a90a6-136">Addresses for these objects are persisted across reboots.</span></span>

> [!NOTE]
> <span data-ttu-id="a90a6-137">Nicht automatisch auflösende dynamische Schlüsselwortadressobjekte lösen Benachrichtigungen für [**FWAddDynamicKeywordAddress0,**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)und auch [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0)aus.</span><span class="sxs-lookup"><span data-stu-id="a90a6-137">Non-AutoResolve dynamic keyword address objects trigger notifications on [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0), [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0), and also [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span></span>

## <a name="more-about-dynamic-keyword-addresses"></a><span data-ttu-id="a90a6-138">Weitere Informationen zu dynamischen Schlüsselwortadressen</span><span class="sxs-lookup"><span data-stu-id="a90a6-138">More about dynamic keyword addresses</span></span> 

<span data-ttu-id="a90a6-139">Alle dynamischen Schlüsselwortadressen müssen über einen eindeutigen [**GUID-Bezeichner**](/windows/win32/api/guiddef/ns-guiddef-guid) verfügen, um sie darzustellen.</span><span class="sxs-lookup"><span data-stu-id="a90a6-139">All dynamic keyword addresses must have a unique [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) identifier to represent them.</span></span>

<span data-ttu-id="a90a6-140">Die [**FwpmDynamicKeywordSubscribe0-API**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) übermittelt Benachrichtigungen an einen Client, wenn sich dynamische Schlüsselwortadressen ändern.</span><span class="sxs-lookup"><span data-stu-id="a90a6-140">The [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) API delivers notifications to a client when dynamic keyword addresses change.</span></span> <span data-ttu-id="a90a6-141">Es wird keine Nutzlast an den Client übermittelt, die genau beschreibt, was sich auf dem System geändert hat.</span><span class="sxs-lookup"><span data-stu-id="a90a6-141">There's no payload delivered to the client describing exactly what changed on the system.</span></span> <span data-ttu-id="a90a6-142">Wenn Sie wissen müssen, welche Objekte sich geändert haben, sollten Sie den aktuellen Zustand von Objekten im System mithilfe der [**APIs FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) oder [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) abfragen.</span><span class="sxs-lookup"><span data-stu-id="a90a6-142">If you need to know what objects changed, then you should query the current state of objects on the system using the [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) or [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) APIs.</span></span> <span data-ttu-id="a90a6-143">Sie können die verschiedenen Flags verwenden, um Benachrichtigungen nur für eine Teilmenge von -Objekten anzufordern.</span><span class="sxs-lookup"><span data-stu-id="a90a6-143">You can use the various flags to request notifications for only a subset of objects.</span></span> <span data-ttu-id="a90a6-144">Wenn Sie keine Flags verwenden, werden Änderungsbenachrichtigungen für alle Objekte übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a90a6-144">If you use no flags, then change notifications will be delivered for all objects.</span></span>

<span data-ttu-id="a90a6-145">Eine Firewallregel kann dynamische Schlüsselwortadressen verwenden, anstatt IP-Adressen explizit für die Remoteadressenbedingung zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a90a6-145">A firewall rule can use dynamic keyword addresses instead of explicitly defining IP addresses for its remote address condition.</span></span> <span data-ttu-id="a90a6-146">Eine Firewallregel kann sowohl dynamische Schlüsselwortadressen als auch statisch definierte Remoteadressbereiche verwenden.</span><span class="sxs-lookup"><span data-stu-id="a90a6-146">A firewall rule can use both dynamic keyword addresses and statically defined remote address ranges.</span></span> <span data-ttu-id="a90a6-147">Ein einzelnes dynamisches Schlüsselwortadressobjekt kann über mehrere Firewallregeln hinweg wiederverwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a90a6-147">A single dynamic keyword address object can be re-used across multiple firewall rules.</span></span> <span data-ttu-id="a90a6-148">Wenn eine Firewallregel über keine konfigurierten Remoteadressen verfügt (d. h. nur mit AutoResolve-Objekten konfiguriert, die noch nicht aufgelöst wurden), wird die Regel nicht erzwungen.</span><span class="sxs-lookup"><span data-stu-id="a90a6-148">If a firewall rule doesn't have any configured remote addresses (that is, configured with only AutoResolve objects which have not yet been resolved), then the rule won't be enforced.</span></span> <span data-ttu-id="a90a6-149">Wenn eine Regel mehrere dynamische Schlüsselwortadressen verwendet, wird die Regel außerdem für alle Adressen erzwungen, die derzeit aufgelöst werden, auch wenn es andere Objekte gibt, die noch nicht aufgelöst wurden.</span><span class="sxs-lookup"><span data-stu-id="a90a6-149">Furthermore, if a rule uses multiple dynamic keyword addresses, then the rule will be enforced for all addresses that are currently resolved, even if there are other objects that are not yet resolved.</span></span> <span data-ttu-id="a90a6-150">Wenn eine dynamische Schlüsselwortadresse aktualisiert wird, werden auch die Remoteadressen aller zugeordneten Regelobjekte aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a90a6-150">When a dynamic keyword address is updated, all associated rule objects will have their remote addresses updated as well.</span></span>

<span data-ttu-id="a90a6-151">Das Betriebssystem selbst erzwingt keine Abhängigkeiten zwischen einer Regel und einer dynamischen Schlüsselwortadresse.</span><span class="sxs-lookup"><span data-stu-id="a90a6-151">The operating system (OS) itself doesn't enforce any dependencies between a rule and a dynamic keyword address.</span></span> <span data-ttu-id="a90a6-152">Dies bedeutet, dass beide Objekte zuerst erstellt werden können, &mdash; sodass die Regel auf dynamische Schlüsselwortadressen-IDs verweisen kann, die noch nicht vorhanden sind (in diesem Fall wird die Regel nicht erzwungen).</span><span class="sxs-lookup"><span data-stu-id="a90a6-152">This means that either object can be created first&mdash;the rule can reference dynamic keyword address IDs that don't yet exist (in which case, the rule won't be enforced).</span></span> <span data-ttu-id="a90a6-153">Darüber hinaus können Sie eine dynamische Schlüsselwortadresse auch dann löschen, wenn sie von einer Firewallregel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a90a6-153">Furthermore, you can delete a dynamic keyword address even if it's in use by a firewall rule.</span></span> <span data-ttu-id="a90a6-154">In diesem Thema wird beschrieben, wie ein Administrator Regeln für die Verwendung der dynamischen Schlüsselwortadresse konfigurieren kann.</span><span class="sxs-lookup"><span data-stu-id="a90a6-154">This topic outlines how an admin can configure rules to use dynamic keyword address.</span></span>

## <a name="code-examples"></a><span data-ttu-id="a90a6-155">Codebeispiele</span><span class="sxs-lookup"><span data-stu-id="a90a6-155">Code examples</span></span>

<span data-ttu-id="a90a6-156">Um jedes dieser Codebeispiele auszuprobieren, starten Sie zuerst Visual Studio und erstellen ein neues Projekt basierend auf der **Projektvorlage Konsolen-App.**</span><span class="sxs-lookup"><span data-stu-id="a90a6-156">To try out each of these code examples, first launch Visual Studio and create a new project based on the **Console App** project template.</span></span> <span data-ttu-id="a90a6-157">Sie können einfach den Inhalt von `main.cpp` durch die Codeauflistung ersetzen.</span><span class="sxs-lookup"><span data-stu-id="a90a6-157">You can just replace the contents of `main.cpp` with the code listing.</span></span>

<span data-ttu-id="a90a6-158">In den meisten Codebeispielen werden die [Windows-Implementierungsbibliotheken (WINDOWS Implementation Libraries, WILL)](https://github.com/Microsoft/wil)verwendet.</span><span class="sxs-lookup"><span data-stu-id="a90a6-158">Most of the code examples use the [Windows Implementation Libraries (WIL)](https://github.com/Microsoft/wil).</span></span> <span data-ttu-id="a90a6-159">Eine bequeme Möglichkeit zum Installieren vonWILL besteht darin, zu Visual Studio zu wechseln, auf **Projekt** \> **NuGet-Pakete verwalten...** Durchsuchen zu \> klicken, **Microsoft.Windows.ImplementationLibrary** in das Suchfeld einzugeben, das Element in den Suchergebnissen auszuwählen und dann auf **Installieren** zu klicken, um das Paket für dieses Projekt zu installieren.</span><span class="sxs-lookup"><span data-stu-id="a90a6-159">A convenient way to install WIL is to go to Visual Studio, click **Project** \> **Manage NuGet Packages...** \> **Browse**, type or paste **Microsoft.Windows.ImplementationLibrary** in the search box, select the item in search results, and then click **Install** to install the package for that project.</span></span>

> [!NOTE]
> <span data-ttu-id="a90a6-160">Zeigertypen für die freien NetFw-Funktionen werden über `NetFw.h` veröffentlicht, aber es wird keine statische Linkbibliothek veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="a90a6-160">Pointer types for the NetFw free functions are published via `NetFw.h`, but a static-link library isn't published.</span></span> <span data-ttu-id="a90a6-161">Verwenden [](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw)Sie das / [GetProcAddress-Muster](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) LoadLibraryExW zum Aufrufen dieser Funktionen, wie in diesen Codebeispielen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a90a6-161">Use the [LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw)/[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pattern for calling these functions, as shown in these code examples.</span></span>

### <a name="add-a-dynamic-keyword-address"></a><span data-ttu-id="a90a6-162">Hinzufügen einer dynamischen Schlüsselwortadresse</span><span class="sxs-lookup"><span data-stu-id="a90a6-162">Add a dynamic keyword address</span></span>

<span data-ttu-id="a90a6-163">In diesem Beispiel wird die Verwendung der [**FWAddDynamicKeywordAddress0-Funktion**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="a90a6-163">This example shows how to use the [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) function.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWADDDYNAMICKEYWORDADDRESS0 addDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;
    FW_DYNAMIC_KEYWORD_ADDRESS0 autoResolveKeywordAddress = { 0 };
    FW_DYNAMIC_KEYWORD_ADDRESS0 nonAutoResolveKeywordAddress = { 0 };

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        addDynamicKeywordAddressFn = (PFN_FWADDDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWAddDynamicKeywordAddress0"
        );
    }

    if (addDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Ensure the ID is unique. If not, the add operation will fail with ERROR_ALREADY_EXISTS
    // and you should invoke the API with a new ID.

    // Initialize and add an auto-resolve dynamic keyword address
    autoResolveKeywordAddress.id = DYNAMIC_KEYWORD_ADDRESS_ID_1;
    autoResolveKeywordAddress.keyword = L"bing.com";
    autoResolveKeywordAddress.flags = FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE;
    // must be NULL as we have set the auto resolve flag
    autoResolveKeywordAddress.addresses = NULL;

    error = addDynamicKeywordAddressFn(&autoResolveKeywordAddress);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    // Initialize and add a non auto-resolve dynamic keyword address
    nonAutoResolveKeywordAddress.id = DYNAMIC_KEYWORD_ADDRESS_ID_2;
    nonAutoResolveKeywordAddress.keyword = L"myServerIPs";
    nonAutoResolveKeywordAddress.flags = 0;
    nonAutoResolveKeywordAddress.addresses = L"10.0.0.5,20.0.0.0/24,30.0.0.0-40.0.0.0";

    error = addDynamicKeywordAddressFn(&nonAutoResolveKeywordAddress);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }
    return error;
}
```

### <a name="delete-a-dynamic-keyword-address"></a><span data-ttu-id="a90a6-164">Löschen einer dynamischen Schlüsselwortadresse</span><span class="sxs-lookup"><span data-stu-id="a90a6-164">Delete a dynamic keyword address</span></span>

<span data-ttu-id="a90a6-165">In diesem Beispiel wird die Verwendung der [**FWDeleteDynamicKeywordAddress0-Funktion**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="a90a6-165">This example shows how to use the [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) function.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};


// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWDELETEDYNAMICKEYWORDADDRESS0 deleteDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });


    if (moduleHandle != NULL)
    {
        deleteDynamicKeywordAddressFn = (PFN_FWDELETEDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWDeleteDynamicKeywordAddress0"
        );
    }

    if (deleteDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke the functions
    error = deleteDynamicKeywordAddressFn(DYNAMIC_KEYWORD_ADDRESS_ID_1);
    if (error != ERROR_SUCCESS)
    {
        wprintf(L"Failed to delete object with ID 1, err=[%d]", error);
    }

    error = deleteDynamicKeywordAddressFn(DYNAMIC_KEYWORD_ADDRESS_ID_2);
    if (error != ERROR_SUCCESS)
    {
        wprintf(L"Failed to delete object with ID 2, err=[%d]", error);
    }

    return error;
}
```

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-id"></a><span data-ttu-id="a90a6-166">Aufzählen und Freigeben dynamischer Schlüsselwortadressen nach ID</span><span class="sxs-lookup"><span data-stu-id="a90a6-166">Enumerate and free dynamic keyword addresses by ID</span></span>

<span data-ttu-id="a90a6-167">In diesem Beispiel wird gezeigt, wie die Funktionen [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) und [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a90a6-167">This example shows how to use the [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) and [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) functions.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0 enumDynamicKeywordAddressByIdFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressByIdFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressById0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressByIdFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    error = enumDynamicKeywordAddressByIdFn(
        DYNAMIC_KEYWORD_ADDRESS_ID_1,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    if (dynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address
    }

    // Free the dynamic keyword address
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);
    return error;
}
```

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-type"></a><span data-ttu-id="a90a6-168">Aufzählen und Freigeben dynamischer Schlüsselwortadressen nach Typ</span><span class="sxs-lookup"><span data-stu-id="a90a6-168">Enumerate and free dynamic keyword addresses by type</span></span>

<span data-ttu-id="a90a6-169">In diesem Beispiel wird gezeigt, wie die Funktionen [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) und [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a90a6-169">This example shows how to use the [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) and [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) functions.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0 enumDynamicKeywordAddressesByTypeFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;

    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 currDynamicKeywordAddressData = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressesByTypeFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressesByType0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressesByTypeFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke enum for ALL dynamic keyword addresses
    error = enumDynamicKeywordAddressesByTypeFn(
        FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_ALL,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    currDynamicKeywordAddressData = dynamicKeywordAddressData;
    while (currDynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address

        // iterate to the next one in the list
        currDynamicKeywordAddressData = currDynamicKeywordAddressData->next;
    }

    // Free the dynamic keyword addresses
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);

    return error;
}
```

### <a name="update-dynamic-keyword-addresses"></a><span data-ttu-id="a90a6-170">Aktualisieren dynamischer Schlüsselwortadressen</span><span class="sxs-lookup"><span data-stu-id="a90a6-170">Update dynamic keyword addresses</span></span>

<span data-ttu-id="a90a6-171">In diesem Beispiel wird die Verwendung der [**FWUpdateDynamicKeywordAddress0-Funktion**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="a90a6-171">This example shows how to use the [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) function.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWUPDATEDYNAMICKEYWORDADDRESS0 updateDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;
    BOOL appendToCurrentAddresses = TRUE;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        updateDynamicKeywordAddressFn = (PFN_FWUPDATEDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWUpdateDynamicKeywordAddress0"
        );
    }

    if (updateDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke the function
    error = updateDynamicKeywordAddressFn(
        DYNAMIC_KEYWORD_ADDRESS_ID_1,
        L"20.0.0.5",
        appendToCurrentAddresses);
    return error;
}
```

### <a name="subscribe-to-and-handle-dynamic-keyword-address-change-notifications"></a><span data-ttu-id="a90a6-172">Abonnieren und Behandeln von Benachrichtigungen über Dynamische Schlüsselwortadressänderungen</span><span class="sxs-lookup"><span data-stu-id="a90a6-172">Subscribe to, and handle, dynamic keyword address change notifications</span></span>

<span data-ttu-id="a90a6-173">In diesem Beispiel wird gezeigt, wie die Funktionen [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) und [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordunsubscribe0) sowie der [**FWPM_DYNAMIC_KEYWORD_CALLBACK0-Rückruf**](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_dynamic_keyword_callback0) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a90a6-173">This example shows how to use the [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) and [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordunsubscribe0) functions, and the [**FWPM_DYNAMIC_KEYWORD_CALLBACK0**](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_dynamic_keyword_callback0) callback.</span></span>

```cppwinrt
// main.cpp in a Console App project.
#include <windows.h>
#include <netfw.h>
#include <fwpmu.h>
#pragma comment(lib, "Fwpuclnt")

void CALLBACK TestCallback(_Inout_ VOID* /*pNotification*/, _Inout_ VOID* pContext)
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0 enumDynamicKeywordAddressesByTypeFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;

    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 currDynamicKeywordAddressData = NULL;
    HANDLE* waitHandle = (HANDLE*)pContext;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryW(L"firewallapi.dll");
    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressesByTypeFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressesByType0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressesByTypeFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        return;
    }

    // Invoke enum for ALL AutoResolve dynamic keyword addresses
    error = enumDynamicKeywordAddressesByTypeFn(
        FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_AUTO_RESOLVE,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return;
    }

    currDynamicKeywordAddressData = dynamicKeywordAddressData;
    while (currDynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address

        currDynamicKeywordAddressData = currDynamicKeywordAddressData->next;
    }

    // Free the dynamic keyword addresses
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);

    SetEvent(*waitHandle);
}

int main()
{
    DWORD error = ERROR_SUCCESS;
    HANDLE notifyHandle;
    HANDLE waitHandle;

    waitHandle = CreateEventW(
        NULL,
        TRUE,
        FALSE,
        L"subscriptionWaitEvent"
    );


    // Subscribe for change notifications
    error = FwpmDynamicKeywordSubscribe0(
        FWPM_NOTIFY_ADDRESSES_AUTO_RESOLVE,
        TestCallback,
        &waitHandle,
        &notifyHandle);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    WaitForSingleObject(waitHandle, INFINITE);

    // When client is ready to unsubscribe
    error = FwpmDynamicKeywordUnsubscribe0(notifyHandle);

    return error;
}
```

## <a name="related-topics"></a><span data-ttu-id="a90a6-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a90a6-174">Related topics</span></span>

* [<span data-ttu-id="a90a6-175">Referenz zu dynamischen Firewallschlüsselwörtern</span><span class="sxs-lookup"><span data-stu-id="a90a6-175">Firewall dynamic keywords reference</span></span>](firewall-dynamic-keywords-reference.md)
