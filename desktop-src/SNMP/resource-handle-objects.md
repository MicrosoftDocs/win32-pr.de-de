---
title: Ressourcenhandle-Objekte
description: Die Struktur eines Ressourcen Objekts ist auf die Microsoft WinSNMP-Implementierung beschränkt. Eine WinSNMP-Anwendung kann mit einem Handle auf ein Ressourcen Objekt zugreifen.
ms.assetid: c70a03b1-afac-4f1a-81e7-7f31430f5655
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1afe5e6488190f95961bff7ce37f7b719d076d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713061"
---
# <a name="resource-handle-objects"></a><span data-ttu-id="f0f96-104">Ressourcenhandle-Objekte</span><span class="sxs-lookup"><span data-stu-id="f0f96-104">Resource Handle Objects</span></span>

<span data-ttu-id="f0f96-105">Die Struktur eines Ressourcen Objekts ist auf die Microsoft WinSNMP-Implementierung beschränkt.</span><span class="sxs-lookup"><span data-stu-id="f0f96-105">The structure of a resource object is restricted to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="f0f96-106">Eine WinSNMP-Anwendung kann mit einem Handle auf ein Ressourcen Objekt zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f0f96-106">A WinSNMP application can access a resource object with a handle.</span></span>

<span data-ttu-id="f0f96-107">Die-Implementierung kann einen der folgenden Typen von Ressourcen Handles für eine WinSNMP-Anwendung zuordnen.</span><span class="sxs-lookup"><span data-stu-id="f0f96-107">The implementation can allocate one of the following types of resource handles for a WinSNMP application.</span></span>

| <span data-ttu-id="f0f96-108">Handle-Typ</span><span class="sxs-lookup"><span data-stu-id="f0f96-108">Handle type</span></span>        | <span data-ttu-id="f0f96-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0f96-109">Description</span></span>                       |
|--------------------|-----------------------------------|
| <span data-ttu-id="f0f96-110">**hsnmp- \_ Sitzung**</span><span class="sxs-lookup"><span data-stu-id="f0f96-110">**HSNMP\_SESSION**</span></span> | <span data-ttu-id="f0f96-111">Handle für eine WinSNMP-Sitzung</span><span class="sxs-lookup"><span data-stu-id="f0f96-111">Handle to a WinSNMP session</span></span>       |
| <span data-ttu-id="f0f96-112">**hsnmp- \_ Entität**</span><span class="sxs-lookup"><span data-stu-id="f0f96-112">**HSNMP\_ENTITY**</span></span>  | <span data-ttu-id="f0f96-113">Handle für eine SNMP-Entität</span><span class="sxs-lookup"><span data-stu-id="f0f96-113">Handle to an SNMP entity</span></span>          |
| <span data-ttu-id="f0f96-114">**hsnmp- \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="f0f96-114">**HSNMP\_CONTEXT**</span></span> | <span data-ttu-id="f0f96-115">Handle für einen WinSNMP-Kontext</span><span class="sxs-lookup"><span data-stu-id="f0f96-115">Handle to a WinSNMP context</span></span>       |
| <span data-ttu-id="f0f96-116">**hsnmp- \_ PDU**</span><span class="sxs-lookup"><span data-stu-id="f0f96-116">**HSNMP\_PDU**</span></span>     | <span data-ttu-id="f0f96-117">Handle für eine Protokolldaten Einheit</span><span class="sxs-lookup"><span data-stu-id="f0f96-117">Handle to a protocol data unit</span></span>    |
| <span data-ttu-id="f0f96-118">**hsnmp- \_ VBL**</span><span class="sxs-lookup"><span data-stu-id="f0f96-118">**HSNMP\_VBL**</span></span>     | <span data-ttu-id="f0f96-119">Handle für eine Variablen Bindungs Liste</span><span class="sxs-lookup"><span data-stu-id="f0f96-119">Handle to a variable binding list</span></span> |



 

<span data-ttu-id="f0f96-120">Eine WinSNMP-Anwendung kann anfordern, dass die Implementierung Ressourcen Handles erstellt oder löscht, aber die Implementierung führt den Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="f0f96-120">A WinSNMP application can request that the implementation create or delete resource handles, but the implementation performs the operation.</span></span> <span data-ttu-id="f0f96-121">Weitere Informationen zum Freigeben einzelner Ressourcen finden Sie in den Funktionen " [**snmpfreedescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor)", " [**snmpfreevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)", " [**snmpfreepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)", " [**snmpfreeentity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)" und " [**snmpfreecontext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext) ".</span><span class="sxs-lookup"><span data-stu-id="f0f96-121">For additional information about freeing individual resources, see the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), and [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext) functions.</span></span>

 

 




