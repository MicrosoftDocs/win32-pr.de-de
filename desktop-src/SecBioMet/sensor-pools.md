---
title: Sensor Pools
description: Beschreibt drei mögliche Sensor Pools System, private und nicht zugewiesene.
ms.assetid: d7fd3c39-d719-4cfd-9af0-a87837f3f328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263275af5c7decff37ef70ad3a5396ec562562f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390553"
---
# <a name="sensor-pools"></a><span data-ttu-id="620a7-103">Sensor Pools</span><span class="sxs-lookup"><span data-stu-id="620a7-103">Sensor Pools</span></span>

<span data-ttu-id="620a7-104">Zur Unterstützung von Windows-Authentifizierungs Szenarien und Hersteller definierter Authentifizierung organisiert der Windows-biometrische Dienst biometrische Einheiten in drei mögliche Sensor Pools:</span><span class="sxs-lookup"><span data-stu-id="620a7-104">To support both Windows authentication scenarios and vendor defined authentication, the Windows Biometric service organizes biometric units into three possible sensor pools:</span></span>

-   <span data-ttu-id="620a7-105">**Privater Pool** eine Sammlung von biometrischen Einheiten, die für die ausschließliche Verwendung durch eine Client Anwendung reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="620a7-105">**Private pool** a collection of biometric units allocated for exclusive use by a client application.</span></span> <span data-ttu-id="620a7-106">Private Pools können Authentifizierungs Szenarien unterstützen, die nicht auf Windows basieren, und eine Anwendung können auf die Hardware einer biometrischen Einheit auf Hersteller definierte Weise zugreifen.</span><span class="sxs-lookup"><span data-stu-id="620a7-106">Private pools can support authentication scenarios that are not Windows-based, and they make it possible for an application to access the hardware of a biometric unit in a vendor-defined fashion.</span></span> <span data-ttu-id="620a7-107">Es können beliebig viele private Sensor Pools auf dem System vorhanden sein, da biometrische Einheiten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="620a7-107">There can be as many private sensor pools on the system as there are biometric units.</span></span>
-   <span data-ttu-id="620a7-108">**System Sensor Pool** : eine Sammlung von shardbaren biometrischen Einheiten, die Zugriff auf die Windows-Authentifizierungsdienste bieten.</span><span class="sxs-lookup"><span data-stu-id="620a7-108">**System sensor pool** a collection of sharable biometric units that provide access to Windows authentication services.</span></span> <span data-ttu-id="620a7-109">Dieser Pool wird von Winlogon, UAC und einem beliebigen anderen Client verwendet, der einer bestimmten biometrischen Vorlage eine SID zuordnet.</span><span class="sxs-lookup"><span data-stu-id="620a7-109">This pool is used by Winlogon, UAC, and any other client that associates a SID with a specific biometric template.</span></span> <span data-ttu-id="620a7-110">Jeder biometrische Dienstanbieter verfügt über einen System Sensor Pool.</span><span class="sxs-lookup"><span data-stu-id="620a7-110">Each biometric service provider has one system sensor pool.</span></span>
-   <span data-ttu-id="620a7-111">**Nicht zugewiesener Pool** enthält eine (möglicherweise leere) Auflistung von biometrischen Einheiten, die weder dem System Pool noch dem privaten Pool zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="620a7-111">**Unassigned pool** contains a (possibly empty) collection of biometric units that are not assigned to either the system pool or the private pool.</span></span>

<span data-ttu-id="620a7-112">Anwendungen können den freigegebenen System Pool verwenden, oder Sie können einen privaten Pool erstellen, der aus biometrischen Einheiten besteht, die aus dem System oder aus nicht zugewiesenen Pools entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="620a7-112">Applications can use the shared system pool or they can create a private pool made up of biometric units removed from the system or unassigned pools.</span></span> <span data-ttu-id="620a7-113">Wenn eine Anwendung Ihren privaten Pool freigibt, werden die biometrischen Einheiten neu konfiguriert und an Ihre ursprünglichen Pools zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="620a7-113">When an application releases its private pool, the biometric units are reconfigured and returned to their original pools.</span></span> <span data-ttu-id="620a7-114">Um Denial-of-Service-Angriffe zu verhindern, dürfen nur privilegierte Benutzer den letzten Sensor aus dem System Pool entfernen.</span><span class="sxs-lookup"><span data-stu-id="620a7-114">To prevent denial of service attacks, only privileged users are permitted to remove the last sensor from the system pool.</span></span> <span data-ttu-id="620a7-115">Weitere Informationen finden Sie in den nachfolgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="620a7-115">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="620a7-116">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="620a7-116">In this section</span></span>



| <span data-ttu-id="620a7-117">Thema</span><span class="sxs-lookup"><span data-stu-id="620a7-117">Topic</span></span>                                                       | <span data-ttu-id="620a7-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="620a7-118">Description</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="620a7-119">Privater Sensor Pool</span><span class="sxs-lookup"><span data-stu-id="620a7-119">Private Sensor Pool</span></span>](private-sensor-pool.md)<br/>   | <span data-ttu-id="620a7-120">Eine Sammlung biometrischer Einheiten, die für die ausschließliche Verwendung durch eine Client Anwendung reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="620a7-120">A collection of biometric units reserved for exclusive use by a client application.</span></span> <span data-ttu-id="620a7-121">Private Pools unterstützen proprietäre Authentifizierungsmethoden und ermöglichen es einer Client Anwendung, mithilfe von vom Hersteller angegebenen Steuerungs Befehlen auf eine biometrische Einheit zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="620a7-121">Private pools support proprietary authentication methods and enable a client application to access a biometric unit by using vendor-specified control commands.</span></span><br/> |
| [<span data-ttu-id="620a7-122">System Sensor Pool</span><span class="sxs-lookup"><span data-stu-id="620a7-122">System Sensor Pool</span></span>](system-sensor-pool.md)<br/>     | <span data-ttu-id="620a7-123">Eine Auflistung von freigegeben-biometrischen Einheiten, die Zugriff auf die Windows-Authentifizierungsdienste bieten.</span><span class="sxs-lookup"><span data-stu-id="620a7-123">A collection of sharable biometric units that provide access to Windows authentication services.</span></span> <span data-ttu-id="620a7-124">Dieser Pool wird von Winlogon, UAC und einem beliebigen anderen Client verwendet, der einer bestimmten biometrischen Vorlage eine SID zuordnet.</span><span class="sxs-lookup"><span data-stu-id="620a7-124">This pool is used by Winlogon, UAC, and any other client that associates a SID with a specific biometric template.</span></span><br/>                                 |
| [<span data-ttu-id="620a7-125">System Pool Verhalten</span><span class="sxs-lookup"><span data-stu-id="620a7-125">System Pool Behavior</span></span>](system-pool-behavior.md)<br/> | <span data-ttu-id="620a7-126">Erörterung der Aktionen, die vom System Pool durchgeführt werden, wenn Ereignis Hinweise gesendet werden und keine biometrischen Vorgänge ausstehen.</span><span class="sxs-lookup"><span data-stu-id="620a7-126">Discussion about the actions taken by the system pool when event notices are sent and when no biometric operations are pending.</span></span><br/>                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="620a7-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="620a7-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="620a7-128">Informationen zur Windows-Biometrieframework-API</span><span class="sxs-lookup"><span data-stu-id="620a7-128">About the Windows Biometric Framework API</span></span>](./biometric-service-api-portal.md)
</dt> </dl>

 

