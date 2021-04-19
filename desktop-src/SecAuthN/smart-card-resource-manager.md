---
description: Smartcard-Ressourcen-Manager
ms.assetid: 96434996-88fa-47d3-bb44-3ebb23610b27
title: Smartcard-Ressourcen-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3ee8e0bf311539863502d3e789544717e6dff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373229"
---
# <a name="smart-card-resource-manager"></a><span data-ttu-id="4b00f-103">Smartcard-Ressourcen-Manager</span><span class="sxs-lookup"><span data-stu-id="4b00f-103">Smart Card Resource Manager</span></span>

<span data-ttu-id="4b00f-104">Der [*Smartcard*](../secgloss/s-gly.md) - [*Ressourcen-Manager*](../secgloss/r-gly.md) verwaltet den Zugriff auf [*Reader*](../secgloss/r-gly.md) und *Smartcards*.</span><span class="sxs-lookup"><span data-stu-id="4b00f-104">The [*smart card*](../secgloss/s-gly.md) [*resource manager*](../secgloss/r-gly.md) manages access to [*readers*](../secgloss/r-gly.md) and to *smart cards*.</span></span> <span data-ttu-id="4b00f-105">Um diese Ressourcen zu verwalten, führt Sie die folgenden Funktionen aus.</span><span class="sxs-lookup"><span data-stu-id="4b00f-105">To manage these resources, it performs the following functions.</span></span>

-   <span data-ttu-id="4b00f-106">Identifiziert und verfolgt Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="4b00f-106">Identifies and tracks resources.</span></span>
-   <span data-ttu-id="4b00f-107">Ordnet Leser und Ressourcen über mehrere Anwendungen zu.</span><span class="sxs-lookup"><span data-stu-id="4b00f-107">Allocates readers and resources across multiple applications.</span></span>
-   <span data-ttu-id="4b00f-108">Unterstützt [*Transaktions*](../secgloss/t-gly.md) primitive für den Zugriff auf Dienste, die auf einer bestimmten Karte verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="4b00f-108">Supports [*transaction*](../secgloss/t-gly.md) primitives for accessing services available on a given card.</span></span>
    > [!Note]  
    > <span data-ttu-id="4b00f-109">Dies ist ein wichtiger Punkt, da es sich bei den aktuellen Karten um Single Thread Geräte handelt, die oft die Ausführung mehrerer Befehle erfordern, um eine einzelne Funktion abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="4b00f-109">This is an important point because current cards are single-threaded devices that often require the execution of multiple commands to complete a single function.</span></span> <span data-ttu-id="4b00f-110">[*Transaktionen*](../secgloss/t-gly.md) ermöglichen die Ausführung mehrerer Befehle ohne Unterbrechung. Dadurch wird sichergestellt, dass die zwischen [*Zustands*](../secgloss/s-gly.md) Informationen nicht beschädigt sind.</span><span class="sxs-lookup"><span data-stu-id="4b00f-110">[*Transactions*](../secgloss/t-gly.md) allow multiple commands to be executed without interruption, ensuring that intermediate [*state*](../secgloss/s-gly.md) information is not corrupted.</span></span>

     

<span data-ttu-id="4b00f-111">Auf den Ressourcen-Manager kann direkt über die Resource Manager-API oder indirekt über einen beliebigen [*smartcarddienstanbieter*](../secgloss/s-gly.md)zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="4b00f-111">The resource manager can be accessed directly by way of the resource manager API or indirectly through any smart card [*service provider*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="4b00f-112">Die Resource Manager-API ist eine Reihe von Windows-Funktionen, die einen direkten Zugriff auf die Dienste des Ressourcen-Managers bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4b00f-112">The resource manager API is a set of Windows functions that provide direct access to the resource manager's services.</span></span> <span data-ttu-id="4b00f-113">Eine Übersicht über die von der API bereitgestellten Windows-Funktionen finden Sie unter [Smartcard-Ressourcen-Manager-API](smart-card-resource-manager-api.md).</span><span class="sxs-lookup"><span data-stu-id="4b00f-113">For an overview of the Windows functions provided by the API, see [Smart Card Resource Manager API](smart-card-resource-manager-api.md).</span></span> <span data-ttu-id="4b00f-114">Im Vergleich dazu verwenden smartcarddienstanbieter com-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="4b00f-114">In comparison, smart card service providers use COM interfaces.</span></span>

<span data-ttu-id="4b00f-115">Viele der Windows-Funktionen in der Resource Manager-API verfügen über äquivalente in den Eigenschaften und Methoden der COM-Schnittstellen des Smartcard-Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="4b00f-115">Many of the Windows functions in the resource manager API have equivalents in the properties and methods of the smart card service providers' COM interfaces.</span></span> <span data-ttu-id="4b00f-116">Obwohl die meisten Anwendungsentwickler die Arbeit mit com vereinfachen, müssen einige Anwendungen weiterhin die Windows-Funktionen verwenden, um bestimmte Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4b00f-116">And although most application developers will find COM easier to work with, some applications will still need to use the Windows functions to perform certain tasks.</span></span> <span data-ttu-id="4b00f-117">Beispielsweise müssen Anwendungen, die die Liste der Leser oder Lesergruppen in der [*Smartcard-Datenbank*](../secgloss/s-gly.md)bearbeiten müssen, und diejenigen, die eine direkte Steuerung eines Readers benötigen, die Resource Manager-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b00f-117">For example, applications that need to manipulate the list of readers or reader groups in the [*smart card database*](../secgloss/s-gly.md), and those that need direct control of a reader, must use the resource manager API.</span></span> <span data-ttu-id="4b00f-118">Die Dienste, die diese Funktionen bereitstellen, sind nur in den Windows-Funktionen verfügbar, nicht im com, das von den Dienstanbietern bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4b00f-118">The services that provide these capabilities are available only in the Windows functions, not in the COM provided by the service providers.</span></span>

<span data-ttu-id="4b00f-119">Informationen dazu, wie der [*Ressourcen-Manager*](../secgloss/r-gly.md) in Windows implementiert wird, finden Sie unter [Ressourcen-Manager-Implementierung](resource-manager-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="4b00f-119">For information about how the [*resource manager*](../secgloss/r-gly.md) is implemented in Windows, see [Resource Manager Implementation](resource-manager-implementation.md).</span></span>

 

 
