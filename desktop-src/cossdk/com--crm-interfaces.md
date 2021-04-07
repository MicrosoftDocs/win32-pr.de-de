---
description: Die CRM-Schnittstellen sind erforderlich, um die Unterstützung für CRM-Worker und CRM-kompenatoren zu bieten, die mit Visual Basic und Visual C++
ms.assetid: 68a75da7-1f35-41a4-8872-e3f4ad1fc30d
title: Com+ CRM-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ba3235b1cd2a82fc913dd676bbb78324f340cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749008"
---
# <a name="com-crm-interfaces"></a><span data-ttu-id="0b320-103">Com+ CRM-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0b320-103">COM+ CRM Interfaces</span></span>

<span data-ttu-id="0b320-104">Die CRM-Schnittstellen sind erforderlich, um die Unterstützung für CRM-Worker und CRM-kompenatoren zu bieten, die mit Visual Basic und Visual C++</span><span class="sxs-lookup"><span data-stu-id="0b320-104">The CRM interfaces are required to provide support for CRM Workers and CRM Compensators developed using Visual Basic and Visual C++.</span></span>

<span data-ttu-id="0b320-105">Sie können das com+-kompensierende Ressourcen-Manager (CRM) verwenden, um Anwendungs Ressourcen schnell und einfach in Microsoft Distributed Transaction Coordinator (DTC)-Transaktionen zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="0b320-105">You can use the COM+ Compensating Resource Manager (CRM) to quickly and easily integrate application resources with Microsoft Distributed Transaction Coordinator (DTC) transactions.</span></span>

<span data-ttu-id="0b320-106">Bei Komponenten, die mit Visual Basic geschrieben wurden, ist es einfacher, einen Protokolldaten Satz als eine Sammlung von Varianten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0b320-106">It is easier for components written with Visual Basic to build up a log record as a collection of Variants.</span></span> <span data-ttu-id="0b320-107">Außerdem sind Visual Basic Komponenten Apartment Thread, was bedeutet, dass es möglich sein muss, die Schnittstellen aus dem Multithread-Apartment in ein Single Thread-Apartment zu Mars Hallen.</span><span class="sxs-lookup"><span data-stu-id="0b320-107">Also, Visual Basic components are apartment threaded, which implies that it must be possible to marshal the interfaces from the multithreaded apartment to a single-threaded apartment.</span></span> <span data-ttu-id="0b320-108">Bei CRM-Komponenten, die mit Visual C++ entwickelt wurden, könnte auch das Apartment Threading Modell verwendet werden. es wird jedoch empfohlen, stattdessen das beide Threading Modell zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0b320-108">CRM components developed with Visual C++ could also use the Apartment threading model, although it is recommended that these use the Both threading model instead.</span></span>

<span data-ttu-id="0b320-109">Die in der folgenden Tabelle beschriebenen Schnittstellen enthalten ausführliche Referenzinformationen für Entwickler von com+-CRMs.</span><span class="sxs-lookup"><span data-stu-id="0b320-109">The interfaces described in the following table provide detailed reference information for developers of COM+ CRMs.</span></span>



| <span data-ttu-id="0b320-110">CRM-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0b320-110">CRM interfaces</span></span>                                             | <span data-ttu-id="0b320-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b320-111">Description</span></span>                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b320-112">**Icrmcompensator**</span><span class="sxs-lookup"><span data-stu-id="0b320-112">**ICrmCompensator**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator)                 | <span data-ttu-id="0b320-113">Diese Schnittstelle stellt unstrukturierte Protokolldaten Sätze in Visual C++ bereit.</span><span class="sxs-lookup"><span data-stu-id="0b320-113">This interface delivers unstructured log records in Visual C++.</span></span>                                                           |
| [<span data-ttu-id="0b320-114">**Icrmcompensatorvarianten**</span><span class="sxs-lookup"><span data-stu-id="0b320-114">**ICrmCompensatorVariants**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) | <span data-ttu-id="0b320-115">Diese Schnittstelle stellt beim Verwenden von Visual Basic strukturierte Protokolldaten Sätze an den CRM-kompenerer bereit.</span><span class="sxs-lookup"><span data-stu-id="0b320-115">This interface delivers structured log records to the CRM Compensator when using Visual Basic.</span></span>                            |
| [<span data-ttu-id="0b320-116">**Icrmformatlogrecords**</span><span class="sxs-lookup"><span data-stu-id="0b320-116">**ICrmFormatLogRecords**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmformatlogrecords)       | <span data-ttu-id="0b320-117">Diese Schnittstelle konvertiert die Protokolldaten Sätze in das Anzeige Format, sodass Sie mit einem generischen Überwachungs Tool angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="0b320-117">This interface converts the log records to viewable format so that they can be presented using a generic monitoring tool.</span></span> |
| [<span data-ttu-id="0b320-118">**Icrmlogcontrol**</span><span class="sxs-lookup"><span data-stu-id="0b320-118">**ICrmLogControl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)                   | <span data-ttu-id="0b320-119">Diese Schnittstelle wird vom CRM-Worker und CRM-kompenator verwendet, um Datensätze in das Protokoll zu schreiben und Sie dauerhaft zu machen.</span><span class="sxs-lookup"><span data-stu-id="0b320-119">This interface is used by the CRM Worker and CRM Compensator to write records to the log and make them durable.</span></span>           |
| [<span data-ttu-id="0b320-120">**Icrmmonitor**</span><span class="sxs-lookup"><span data-stu-id="0b320-120">**ICrmMonitor**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitor)                         | <span data-ttu-id="0b320-121">Diese Schnittstelle erfasst eine Momentaufnahme des aktuellen Status eines CRM und enthält einen bestimmten CRM-Clerk.</span><span class="sxs-lookup"><span data-stu-id="0b320-121">This interface captures a snapshot of the current state of a CRM and holds a specific CRM clerk.</span></span>                          |
| [<span data-ttu-id="0b320-122">**Icrmmonitorclerchs**</span><span class="sxs-lookup"><span data-stu-id="0b320-122">**ICrmMonitorClerks**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorclerks)             | <span data-ttu-id="0b320-123">Diese Schnittstelle erhält Informationen über den Zustand von clerchs.</span><span class="sxs-lookup"><span data-stu-id="0b320-123">This interface obtains information about the state of clerks.</span></span>                                                             |
| [<span data-ttu-id="0b320-124">**Icrmmonitorlogrecords**</span><span class="sxs-lookup"><span data-stu-id="0b320-124">**ICrmMonitorLogRecords**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)     | <span data-ttu-id="0b320-125">Diese Schnittstelle überwacht die einzelnen Protokolldaten Sätze, die von einem bestimmten CRM-Clerk für eine bestimmte Transaktion verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="0b320-125">This interface monitors the individual log records maintained by a specific CRM clerk for a given transaction.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="0b320-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b320-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b320-127">Kompensierende com+-Ressourcen-Manager Konzepte</span><span class="sxs-lookup"><span data-stu-id="0b320-127">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



