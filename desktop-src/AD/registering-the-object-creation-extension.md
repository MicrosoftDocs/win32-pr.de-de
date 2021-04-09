---
title: Die Objekt Erstellungs Erweiterung wird registriert.
description: Wenn eine Erweiterungs-DLL für die Objekt Erstellung in Active Directory Domain Services erstellt wird, muss Sie in der Windows-Registrierung registriert und Active Directory Domain Services werden, damit com und die Active Directory Verwaltungs-MMC-Snap-Ins die Erweiterung berücksichtigen.
ms.assetid: 6e950c6c-1a4f-4de0-9be1-004c31d4734c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27d8e2a50c2340d678fd43e546d68525afbc8a7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948550"
---
# <a name="registering-the-object-creation-extension"></a><span data-ttu-id="a44ca-103">Die Objekt Erstellungs Erweiterung wird registriert.</span><span class="sxs-lookup"><span data-stu-id="a44ca-103">Registering the Object Creation Extension</span></span>

<span data-ttu-id="a44ca-104">Wenn eine Erweiterungs-DLL für die Objekt Erstellung in Active Directory Domain Services erstellt wird, muss Sie in der Windows-Registrierung registriert und Active Directory Domain Services werden, damit com und die Active Directory Verwaltungs-MMC-Snap-Ins die Erweiterung berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="a44ca-104">When an object creation extension DLL in Active Directory Domain Services is created, it must be registered with the Windows registry and Active Directory Domain Services to make COM and the Active Directory administrative MMC snap-ins aware of the extension.</span></span>

## <a name="registering-in-the-windows-registry"></a><span data-ttu-id="a44ca-105">Registrieren in der Windows-Registrierung</span><span class="sxs-lookup"><span data-stu-id="a44ca-105">Registering in the Windows Registry</span></span>

<span data-ttu-id="a44ca-106">Wie alle com-Server muss eine Erweiterung zum Erstellen von Objekten in der Windows-Registrierung registriert werden.</span><span class="sxs-lookup"><span data-stu-id="a44ca-106">Like all COM servers, an object creation extension must be registered in the Windows registry.</span></span> <span data-ttu-id="a44ca-107">Die Erweiterung ist unter folgendem Schlüssel registriert:</span><span class="sxs-lookup"><span data-stu-id="a44ca-107">The extension is registered under the following key:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      <extension CLSID>
         InProcServer32
            (Default) = <extension path>
            ThreadingModel = Apartment
```

<span data-ttu-id="a44ca-108">" &lt; Extension CLSID &gt; " ist die Zeichen folgen Darstellung der CLSID, die von der [**stringfromclsid**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) -Funktion erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a44ca-108">"&lt;extension CLSID&gt;" is the string representation of the CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span> <span data-ttu-id="a44ca-109">" &lt; Erweiterungs Pfad &gt; " enthält den Pfad und den Dateinamen der Erweiterungs-DLL.</span><span class="sxs-lookup"><span data-stu-id="a44ca-109">"&lt;extension path&gt;" contains the path and file name of the extension DLL.</span></span> <span data-ttu-id="a44ca-110">Der **ThreadingModel** -Wert für alle Objekt Erstellungs Erweiterungen muss "Apartment" lauten.</span><span class="sxs-lookup"><span data-stu-id="a44ca-110">The **ThreadingModel** value for all object creation extensions must be "Apartment".</span></span>

## <a name="registering-with-active-directory-domain-services"></a><span data-ttu-id="a44ca-111">Registrieren bei Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="a44ca-111">Registering with Active Directory Domain Services</span></span>

<span data-ttu-id="a44ca-112">Die Registrierung der Objekt Erstellungs Erweiterung ist spezifisch für ein Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="a44ca-112">Object creation extension registration is specific to one locale.</span></span> <span data-ttu-id="a44ca-113">Wenn die Objekt Erstellungs Erweiterung auf alle Gebiets Schemas angewendet wird, muss Sie im **Display specifier** -Objekt der Objektklasse in allen Gebiets Schema-subcontainern im DisplaySpecifiers-Container registriert werden.</span><span class="sxs-lookup"><span data-stu-id="a44ca-113">If the object creation extension applies to all locales, it must be registered in the object class's **displaySpecifier** object in all of the locale subcontainers in the DisplaySpecifiers container.</span></span> <span data-ttu-id="a44ca-114">Wenn die Objekt Erstellungs Erweiterung für ein bestimmtes Gebiets Schema lokalisiert wird, registrieren Sie Sie im **displaySpecifier** -Objekt im unter Container dieses Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="a44ca-114">If the object creation extension is localized for a certain locale, register it in the **displaySpecifier** object in that locale's subcontainer.</span></span> <span data-ttu-id="a44ca-115">Weitere Informationen über den displayspecifieres-Container und die Gebiets Schemas finden Sie unter [anzeigen](display-specifiers.md) von Bezeichner und [displaySpecifier-Containern](displayspecifiers-container.md).</span><span class="sxs-lookup"><span data-stu-id="a44ca-115">For more information about the DisplaySpecifiers container and locales, see [Display Specifiers](display-specifiers.md) and [DisplaySpecifiers Container](displayspecifiers-container.md).</span></span>

<span data-ttu-id="a44ca-116">Es gibt zwei displaySpecifier-Attribute, unter denen eine Objekt Erstellungs Erweiterung registriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a44ca-116">There are two DisplaySpecifier attributes that an object creation extension can be registered under.</span></span> <span data-ttu-id="a44ca-117">Hierbei handelt es sich um den Ordner " **kreationwizard** **" und "**".</span><span class="sxs-lookup"><span data-stu-id="a44ca-117">These are **creationWizard** and **createWizardExt**.</span></span>

<span data-ttu-id="a44ca-118">Das Attribut " **kreationwizard** " identifiziert Erweiterungen der primären Objekt Erstellung, um den vorhandenen Assistenten oder den Assistenten zum Erstellen von systemeigenen Objekten in Active Directory administrativen Snap-Ins zu ersetzen Eine primäre Erstellungs Erweiterung stellt die erste Gruppe von Seiten bereit und wird auf die gleiche Weise wie Native Seiten gehostet.</span><span class="sxs-lookup"><span data-stu-id="a44ca-118">The **creationWizard** attribute identifies primary object creation extensions to replace the existing or native object creation wizard in Active Directory administrative snap-ins. A primary creation extension provides the first set of pages and is hosted in the same way as native pages.</span></span> <span data-ttu-id="a44ca-119">Dieses Attribut ist einwertig und erfordert das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="a44ca-119">This attribute is single-valued and requires the following format:</span></span>


```C++
<CLSID>
```



<span data-ttu-id="a44ca-120">Die " &lt; CLSID &gt; " ist die Zeichen folgen Darstellung der CLSID des COM-Objekts, die von der [**stringfromclsid**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) -Funktion erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a44ca-120">The "&lt;CLSID&gt;" is the string representation of the COM object's CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span>

<span data-ttu-id="a44ca-121">Das Attribut " **kreatewizardecoxt** " identifiziert Erweiterungen für die Erstellung sekundärer Objekte.</span><span class="sxs-lookup"><span data-stu-id="a44ca-121">The **createWizardExt** attribute identifies secondary object creation extensions.</span></span> <span data-ttu-id="a44ca-122">Eine sekundäre Erstellungs Erweiterung fügt der systemeigenen Seite oder der primären Erweiterung Assistenten Seiten hinzu.</span><span class="sxs-lookup"><span data-stu-id="a44ca-122">A secondary creation extension adds wizard pages to the native pages or primary extension.</span></span> <span data-ttu-id="a44ca-123">Dieses Attribut ist mehr wertig und erfordert folgendes Format:</span><span class="sxs-lookup"><span data-stu-id="a44ca-123">This attribute is multi-valued and requires the following format:</span></span>


```C++
<order number>,<CLSID>
```



<span data-ttu-id="a44ca-124">" &lt; Order Number &gt; " ist eine nicht signierte Zahl, die die Position der Seite im Assistenten darstellt.</span><span class="sxs-lookup"><span data-stu-id="a44ca-124">The "&lt;order number&gt;" is an unsigned number that represents the page's position in the wizard.</span></span> <span data-ttu-id="a44ca-125">Wenn ein Erstellungs-Assistent angezeigt wird, werden die Werte anhand eines Vergleichs der "Order Number"-Werte der einzelnen Werte sortiert &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="a44ca-125">When a creation wizard is displayed, the values are sorted using a comparison of each value's "&lt;order number&gt;".</span></span> <span data-ttu-id="a44ca-126">Wenn mehr als ein Wert dieselbe " &lt; Bestellnummer" aufweist &gt; , werden diese Seiten in der Reihenfolge geladen, in der Sie vom Active Directory Server gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="a44ca-126">If more than one value has the same "&lt;order number&gt;", those pages are loaded in the order they are read from the Active Directory server.</span></span> <span data-ttu-id="a44ca-127">Wenn möglich, sollten Sie eine nicht vorhandene " &lt; Bestellnummer" verwenden &gt; (d. h. eine, die nicht von anderen Werten in der-Eigenschaft verwendet wurde).</span><span class="sxs-lookup"><span data-stu-id="a44ca-127">If possible, you should use a non-existing "&lt;order number&gt;" (that is, one that has not been used by other values in the property).</span></span> <span data-ttu-id="a44ca-128">Es gibt keine vorgeschriebene Anfangsposition, und Lücken sind in der Sequenz " &lt; Order Number &gt; " zulässig.</span><span class="sxs-lookup"><span data-stu-id="a44ca-128">There is no prescribed starting position, and gaps are allowed in the "&lt;order number&gt;" sequence.</span></span>

<span data-ttu-id="a44ca-129">Die " &lt; CLSID &gt; " ist die Zeichen folgen Darstellung der CLSID des COM-Objekts, die von der [**stringfromclsid**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) -Funktion erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a44ca-129">The "&lt;CLSID&gt;" is the string representation of the COM object's CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span>

 

 