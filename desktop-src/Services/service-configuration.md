---
description: Das System verwendet die Konfigurationsinformationen, um zu bestimmen, wie der Dienst gestartet wird.
ms.assetid: fc8c631e-076c-4745-8db0-90f46a202e6a
title: Dienstkonfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5019469e17fdd0807aa101c7d1e4d6f6019da783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525823"
---
# <a name="service-configuration"></a><span data-ttu-id="54ddf-103">Dienstkonfiguration</span><span class="sxs-lookup"><span data-stu-id="54ddf-103">Service Configuration</span></span>

<span data-ttu-id="54ddf-104">Das System verwendet die Konfigurationsinformationen, um zu bestimmen, wie der Dienst gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="54ddf-104">The system uses the configuration information to determine how to start the service.</span></span> <span data-ttu-id="54ddf-105">Zu den Konfigurationsinformationen zählen auch der Anzeige Name des dienstanens und seine Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="54ddf-105">The configuration information also includes the service display name and its description.</span></span> <span data-ttu-id="54ddf-106">Für den DHCP-Dienst können Sie z. b. den anzeigen Amen "Dynamic Host Configuration Protocol Service" und die Beschreibung "stellt Internetadressen für Computer in Ihrem Netzwerk bereit" verwenden.</span><span class="sxs-lookup"><span data-stu-id="54ddf-106">For example, for the DHCP service, you could use the display name "Dynamic Host Configuration Protocol Service" and the description "Provides internet addresses for computer on your network."</span></span>

<span data-ttu-id="54ddf-107">Zum Ändern der Konfigurationsinformationen für ein Dienst Objekt verwendet ein Konfigurationsprogramm die [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) -oder [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="54ddf-107">To modify the configuration information for a service object, a configuration program uses the [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) or [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) function.</span></span> <span data-ttu-id="54ddf-108">Ein Beispiel finden Sie unter [Ändern einer Dienst Konfiguration](changing-a-service-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="54ddf-108">For an example, see [Changing a Service Configuration](changing-a-service-configuration.md).</span></span>

<span data-ttu-id="54ddf-109">Zum Abrufen der Konfigurationsinformationen für ein Dienst Objekt verwendet das Konfigurationsprogramm die Funktion [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) oder [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) .</span><span class="sxs-lookup"><span data-stu-id="54ddf-109">To retrieve the configuration information for a service object, the configuration program uses the [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) or [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) function.</span></span> <span data-ttu-id="54ddf-110">Ein Beispiel finden Sie unter [Abfragen der Konfiguration eines Dienstanbieter](querying-a-service-s-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="54ddf-110">For an example, see [Querying a Service's Configuration](querying-a-service-s-configuration.md).</span></span>

<span data-ttu-id="54ddf-111">Die Dienst Konfigurationsfunktionen [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) und [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) unterstützen die Verwendung von Triggern zum Steuern des Dienst Starts.</span><span class="sxs-lookup"><span data-stu-id="54ddf-111">The [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) and [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) service configuration functions support the use of triggers to control service start.</span></span>

<span data-ttu-id="54ddf-112">Zum Ändern der Sicherheits Beschreibung für ein scmanager-Objekt oder ein Dienst Objekt verwendet ein Konfigurationsprogramm die [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="54ddf-112">To modify the security descriptor for either an SCManager object or a service object, a configuration program uses the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function.</span></span> <span data-ttu-id="54ddf-113">Zum Abrufen einer Kopie der Sicherheits Beschreibung verwendet das Konfigurationsprogramm die Funktion [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) .</span><span class="sxs-lookup"><span data-stu-id="54ddf-113">To retrieve a copy of the security descriptor, the configuration program uses the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54ddf-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="54ddf-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54ddf-115">Konfigurieren eines Dienstanbieter mit SC</span><span class="sxs-lookup"><span data-stu-id="54ddf-115">Configuring a Service Using SC</span></span>](configuring-a-service-using-sc.md)
</dt> </dl>

 

 
