---
title: WFP-Architektur
description: Dieser Abschnitt enthält eine kurze Übersicht über die Architektur der Windows-Filter Plattform.
ms.assetid: 17a90f5c-ef82-4b14-b7f1-dd025d5f7303
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8740fed254aca97ab77566e2a7f0ace9a6679d56
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104209178"
---
# <a name="wfp-architecture"></a><span data-ttu-id="70734-103">WFP-Architektur</span><span class="sxs-lookup"><span data-stu-id="70734-103">WFP Architecture</span></span>

<span data-ttu-id="70734-104">Die folgende Abbildung zeigt die grundlegende Architektur der Windows-Filter Plattform (WFP).</span><span class="sxs-lookup"><span data-stu-id="70734-104">The following figure shows the basic architecture of the Windows Filtering Platform (WFP).</span></span>

![grundlegende Architektur des Windows-Filter Platt Form Diagramms](images/wfp-architecture.png)

## <a name="filter-engine"></a><span data-ttu-id="70734-106">Filter-Engine</span><span class="sxs-lookup"><span data-stu-id="70734-106">Filter Engine</span></span>

<span data-ttu-id="70734-107">Die Filter-Engine enthält eine Benutzermoduskomponente und eine Kernelmoduskomponente, die alle Filter Vorgänge für Netzwerkdaten ausführt.</span><span class="sxs-lookup"><span data-stu-id="70734-107">The filter engine contains a user-mode component and a kernel-mode component, which together perform all of the filtering operations on network data.</span></span> <span data-ttu-id="70734-108">Die Filter-Engine enthält mehrere Filter Ebenen, die den Netzwerk Stapel Ebenen des Betriebssystems lose zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="70734-108">The filter engine contains multiple filtering layers that map loosely to the operating system's networking stack layers.</span></span> <span data-ttu-id="70734-109">Die Filter-Engine-Ebenen werden basierend auf der Filter-Engine-Komponente, die Sie besitzt, in benutzermodusebenen und Kernel Modus-Ebenen aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="70734-109">The filter engine layers are divided into user-mode layers and kernel-mode layers based on the filter engine component that owns them.</span></span>

<span data-ttu-id="70734-110">Die Benutzermoduskomponente führt RPC-und IPSec-Filterung aus.</span><span class="sxs-lookup"><span data-stu-id="70734-110">The user-mode component performs RPC and IPsec filtering.</span></span> <span data-ttu-id="70734-111">Die Filter-Engine enthält ungefähr 10 Benutzermodus-Filter Ebenen.</span><span class="sxs-lookup"><span data-stu-id="70734-111">The filter engine contains approximately 10 user-mode filtering layers.</span></span>

<span data-ttu-id="70734-112">Die Kernelmoduskomponente führt das Filtern auf der Netzwerk-und Transport Ebene des TC/IP-Stapels durch.</span><span class="sxs-lookup"><span data-stu-id="70734-112">The kernel-mode component performs filtering at the network and transport layers of the TC/IP stack.</span></span> <span data-ttu-id="70734-113">Diese Komponente ruft während des [Klassifizierungs](basic-operation.md) Prozesses auch die verfügbaren Legenden Funktionen auf.</span><span class="sxs-lookup"><span data-stu-id="70734-113">This component also calls the available callout functions during the [classification](basic-operation.md) process.</span></span> <span data-ttu-id="70734-114">Die Filter-Engine enthält ungefähr 50 Kernel Modus-Filter Ebenen.</span><span class="sxs-lookup"><span data-stu-id="70734-114">The filter engine contains approximately 50 kernel-mode filtering layers.</span></span>

<span data-ttu-id="70734-115">Unter [**Filtern von ebenenbezeichern**](management-filtering-layer-identifiers-.md) finden Sie eine Beschreibung der einzelnen Filter-Engine-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="70734-115">See [**Filtering Layer Identifiers**](management-filtering-layer-identifiers-.md) for a description of each of the filter engine layers.</span></span>

## <a name="base-filtering-engine"></a><span data-ttu-id="70734-116">Basisfiltermodul</span><span class="sxs-lookup"><span data-stu-id="70734-116">Base Filtering Engine</span></span>

<span data-ttu-id="70734-117">Die Basis Filter-Engine (Basis Filter-Engine, BFE) ist ein Dienst im Benutzermodus (bfe.dll in einem svchost.exe Prozess ausgeführt), der die WFP-Komponenten koordiniert.</span><span class="sxs-lookup"><span data-stu-id="70734-117">The Base Filtering Engine (BFE) is a user-mode service (bfe.dll running in a svchost.exe process) that coordinates the WFP components.</span></span> <span data-ttu-id="70734-118">Die Prinzipal Aufgaben, die von BFE durchgeführt werden, sind das Hinzufügen und Entfernen von Filtern aus dem System, das Speichern der Filter Konfiguration und das Erzwingen der WFP</span><span class="sxs-lookup"><span data-stu-id="70734-118">The principal tasks performed by BFE are adding and removing filters from the system, storing filter configuration, and enforcing WFP configuration security.</span></span> <span data-ttu-id="70734-119">Anwendungen kommunizieren über die [WFP-Verwaltungsfunktionen](fwp-mgmt-functions.md)mit BFE.</span><span class="sxs-lookup"><span data-stu-id="70734-119">Applications communicate with BFE through the [WFP management functions](fwp-mgmt-functions.md).</span></span>

## <a name="callout-drivers"></a><span data-ttu-id="70734-120">Callout-Treiber</span><span class="sxs-lookup"><span data-stu-id="70734-120">Callout Drivers</span></span>

<span data-ttu-id="70734-121">Legenden-Treiber bieten zusätzliche Filter Funktionalität durch Hinzufügen von benutzerdefinierten Legenden Funktionen zur Filter-Engine auf einer oder mehreren kernelmodusfilterungs-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="70734-121">Callout drivers provide additional filtering functionality by adding custom callout functions to the filter engine at one or more of the kernel-mode filtering layers.</span></span> <span data-ttu-id="70734-122">Callouts unterstützen tiefgreifende Überprüfungen und Pakete sowie Datenstrom Änderungen.</span><span class="sxs-lookup"><span data-stu-id="70734-122">Callouts support deep inspection and packet as well as stream modification.</span></span> <span data-ttu-id="70734-123">Nachdem ein Legenden Treiber seine Legenden Funktionen zur Filter-Engine hinzugefügt hat, können Filter, die die Legenden-Funktion eines bestimmten Treibers angeben, dem Filter Vorgang hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="70734-123">After a callout driver has added its callout functions to the filter engine, filters that specify a given driver's callout function can be added to the filtering process.</span></span> <span data-ttu-id="70734-124">Solche Filter können entweder von einer Verwaltungs Anwendung im Benutzermodus oder vom Legenden Treiber selbst hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="70734-124">Such filters can be added by either a user-mode management application or by the callout driver itself.</span></span> <span data-ttu-id="70734-125">Die im Windows Development Kit gelieferte kernelmodusschnittstelle sollte nur bei Bedarf verwendet und nicht als Ersatz für die benutzermodusapi verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70734-125">The kernel-mode interface, delivered in the Windows Development Kit, should only be used where needed and not as a substitute for the user-mode API.</span></span>

> [!Note]  
> <span data-ttu-id="70734-126">Weitere Informationen zu Legenden Treibern finden Sie im Abschnitt Windows-Filter Plattform des [Windows Development Kits](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2).</span><span class="sxs-lookup"><span data-stu-id="70734-126">For more information on callout drivers, see the Windows Filtering Platform section of the [Windows Development Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2).</span></span>

 

<span data-ttu-id="70734-127">Die Windows-Filter Plattform enthält eine Reihe integrierter Legenden Funktionen, die für die sichere IPSec-Datenkommunikation, Zustands behaftete Filtereinstellungen und das Filtern im verborgenen Modus verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="70734-127">The Windows Filtering Platform includes a number of built-in callout functions that can be used for IPsec secure data communication, stateful filtering settings, and stealth-mode filtering.</span></span> <span data-ttu-id="70734-128">Eine komplette Liste der integrierten Legenden Funktionen finden Sie unter [**integrierte**](built-in-callout-identifiers.md) Legenden Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="70734-128">See [**Built-in Callout Identifiers**](built-in-callout-identifiers.md) for a complete list of built-in callout functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70734-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="70734-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70734-130">Objektmodell</span><span class="sxs-lookup"><span data-stu-id="70734-130">Object Model</span></span>](object-model.md)
</dt> <dt>

[<span data-ttu-id="70734-131">WFP-Vorgang</span><span class="sxs-lookup"><span data-stu-id="70734-131">WFP Operation</span></span>](basic-operation.md)
</dt> <dt>

[<span data-ttu-id="70734-132">Windows-Filter Plattform-Callout-Treiber-Entwurfs Handbuch</span><span class="sxs-lookup"><span data-stu-id="70734-132">Windows Filtering Platform Callout Drivers - Design Guide</span></span>](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[<span data-ttu-id="70734-133">Windows-Filter Plattform-Callout-Treiber-Referenz</span><span class="sxs-lookup"><span data-stu-id="70734-133">Windows Filtering Platform Callout Drivers - Reference</span></span>](/windows-hardware/drivers/ddi/_netvista/)
</dt> </dl>

 

 