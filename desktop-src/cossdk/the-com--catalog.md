---
description: Der com+-Katalog speichert com+-Anwendungs Attribute, Klassenattribute und Attribute auf Computer Ebene. Sie gewährleistet die Konsistenz zwischen diesen Attributen und bietet allgemeine Vorgänge oberhalb dieser Attribute.
ms.assetid: 1838757c-aa8e-4678-8042-207498fb0bbc
title: Der com+-Katalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad869a6df6a61fc338fe07002512a1de27002788
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345427"
---
# <a name="the-com-catalog"></a><span data-ttu-id="2aed3-104">Der com+-Katalog</span><span class="sxs-lookup"><span data-stu-id="2aed3-104">The COM+ Catalog</span></span>

<span data-ttu-id="2aed3-105">Der com+-Katalog speichert com+-Anwendungs Attribute, Klassenattribute und Attribute auf Computer Ebene.</span><span class="sxs-lookup"><span data-stu-id="2aed3-105">The COM+ catalog stores COM+ application attributes, class attributes, and computer-level attributes.</span></span> <span data-ttu-id="2aed3-106">Sie gewährleistet die Konsistenz zwischen diesen Attributen und bietet allgemeine Vorgänge oberhalb dieser Attribute.</span><span class="sxs-lookup"><span data-stu-id="2aed3-106">It guarantees consistency among these attributes and provides common operations on top of these attributes.</span></span>

<span data-ttu-id="2aed3-107">Der com+-Katalog verwendet zwei verschiedene Speicher wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2aed3-107">The COM+ catalog uses two different stores, as follows:</span></span>

-   <span data-ttu-id="2aed3-108">Die COM+-Registrierungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="2aed3-108">The COM+ registration database</span></span>
-   <span data-ttu-id="2aed3-109">Die Windows-Registrierung (**HKEY \_ Classes \_ root**)</span><span class="sxs-lookup"><span data-stu-id="2aed3-109">The Windows registry (**HKEY\_CLASSES\_ROOT**)</span></span>

<span data-ttu-id="2aed3-110">Der Katalog stellt eine einheitliche logische Ansicht dieser beiden Speicher bereit und macht Sie über die com+-Verwaltungs Bibliothek verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2aed3-110">The catalog presents a unified, logical view of these two stores and exposes them through the COM+ Administration Library.</span></span> <span data-ttu-id="2aed3-111">Diese Bibliothek bietet über eine Skriptsprache sämtliche Funktionen des Verwaltungs Programms Komponenten Dienste.</span><span class="sxs-lookup"><span data-stu-id="2aed3-111">This library provides, through a scripting language, all the functionality of the Component Services administrative tool.</span></span>

<span data-ttu-id="2aed3-112">Für vorhandene COM-Komponenten, für die keine neuen com+-Dienste erforderlich sind, erfolgt die Suche in der vorhandenen Windows-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="2aed3-112">For existing COM components that do not require any new COM+ services, lookup occurs in the existing Windows registry.</span></span> <span data-ttu-id="2aed3-113">Der com+-Katalog verwendet auch die Windows-Registrierung für die Typbibliothek und die Schnittstellen Proxy-/stubregistrierung.</span><span class="sxs-lookup"><span data-stu-id="2aed3-113">The COM+ catalog also uses the Windows registry for type library and interface proxy/stub registration.</span></span>

## <a name="split-registration"></a><span data-ttu-id="2aed3-114">Geteilte Registrierung</span><span class="sxs-lookup"><span data-stu-id="2aed3-114">Split Registration</span></span>

<span data-ttu-id="2aed3-115">Bei neuen Komponenten, die tatsächlich bereits vorhandene COM-Komponenten verwenden, die in der Dienst Umgebung verwendet werden (z. b. MTS-Komponenten), wird der grundlegende com-Aspekt der Registrierung in der Windows-Registrierung gespeichert, und neue Dienste und Attribute (z. b. in der Warteschlange befindliche Komponenten) werden in der COM+-Registrierungsdatenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2aed3-115">For new components that are actually already existing COM components that are used in the services environment (for example, MTS components), the basic COM aspect of the registration is stored in the Windows registry and new services and attributes (for example, queued components) are stored in the COM+ registration database.</span></span> <span data-ttu-id="2aed3-116">Dies wird als *geteilte Registrierung* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2aed3-116">This is known as a *split registration*.</span></span>

<span data-ttu-id="2aed3-117">Jedes Attribut wird nur an einem Speicherort gespeichert: entweder in der Windows-Registrierung oder in der COM+-Registrierungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="2aed3-117">Each attribute is stored in only one location: either the Windows registry or the COM+ registration database.</span></span> <span data-ttu-id="2aed3-118">Neue COM-Komponenten werden ausschließlich in der COM+-Registrierungsdatenbank registriert, wobei eine Duplizierung in der Windows-Registrierung möglich ist, damit vorhandene Tools Sie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="2aed3-118">New COM components are registered exclusively in the COM+ registration database, with some duplication in the Windows registry so that existing tools can use them.</span></span>

## <a name="transactional-updates-to-the-catalog"></a><span data-ttu-id="2aed3-119">Transaktionale Aktualisierungen des Katalogs</span><span class="sxs-lookup"><span data-stu-id="2aed3-119">Transactional Updates to the Catalog</span></span>

<span data-ttu-id="2aed3-120">Einige Vorgänge im Katalog werden auf transaktionale Weise ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2aed3-120">Some operations on the catalog are performed in a transactional manner.</span></span> <span data-ttu-id="2aed3-121">Wenn Sie die com+-Verwaltungs Bibliothek über eine transaktionale Komponente aufrufen, werden die Aktualisierungen der COM+-Registrierungsdatenbank innerhalb der Transaktionsgrenze der aufrufenden Komponente durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="2aed3-121">When you invoke the COM+ Administration Library from a transactional component, the updates to the COM+ registration database will take place within the calling component's transaction boundary.</span></span>

<span data-ttu-id="2aed3-122">Updates, die Änderungen an anderen speichern (z. b. Dateisystem und Windows-Registrierung) betreffen, sind jedoch nicht unbedingt vollständig transaktional.</span><span class="sxs-lookup"><span data-stu-id="2aed3-122">However, updates that involve changes to other stores (such as the file system and Windows registry) are not guaranteed to be fully transactional.</span></span> <span data-ttu-id="2aed3-123">Eine abgebrochene Transaktion kann diese Speicher in einem Zustand belassen, der nicht mit vorgenommenen Änderungen oder der COM+-Registrierungsdatenbank konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="2aed3-123">An aborted transaction can leave these stores in a state that is inconsistent with any changes made to one another or to the COM+ registration database.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2aed3-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2aed3-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2aed3-125">Installationspakete für COM+-Anwendungen werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="2aed3-125">Creating Installation Packages for COM+ Applications</span></span>](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[<span data-ttu-id="2aed3-126">Anwendungs Proxys</span><span class="sxs-lookup"><span data-stu-id="2aed3-126">Deploying Application Proxies</span></span>](deploying-application-proxies.md)
</dt> <dt>

[<span data-ttu-id="2aed3-127">Das Hilfsprogramm zur Comrepl-Replikation</span><span class="sxs-lookup"><span data-stu-id="2aed3-127">The COMREPL Replication Utility</span></span>](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



