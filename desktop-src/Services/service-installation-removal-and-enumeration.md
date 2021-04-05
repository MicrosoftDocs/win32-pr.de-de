---
description: Ein Konfigurationsprogramm verwendet die Funktion "| ateservice", um einen neuen Dienst in der SCM-Datenbank zu installieren.
ms.assetid: 554b9983-4e49-4b11-b420-a4754123d854
title: Dienst Installation, Entfernung und Enumeration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1069bba094205efd3257063a89c74326b2806455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751057"
---
# <a name="service-installation-removal-and-enumeration"></a><span data-ttu-id="05927-103">Dienst Installation, Entfernung und Enumeration</span><span class="sxs-lookup"><span data-stu-id="05927-103">Service Installation, Removal, and Enumeration</span></span>

<span data-ttu-id="05927-104">Ein Konfigurationsprogramm verwendet die Funktion "| [**ateservice**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) ", um einen neuen Dienst in der SCM-Datenbank zu installieren.</span><span class="sxs-lookup"><span data-stu-id="05927-104">A configuration program uses the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to install a new service in the SCM database.</span></span> <span data-ttu-id="05927-105">Diese Funktion gibt den Namen des Dienstanbieter an und stellt Konfigurationsinformationen bereit, die in der Datenbank gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="05927-105">This function specifies the name of the service and provides configuration information that is stored in the database.</span></span> <span data-ttu-id="05927-106">Eine Beschreibung der Informationen, die in der Datenbank für die einzelnen Dienste gespeichert sind, finden Sie unter [Datenbank der installierten Dienste](database-of-installed-services.md).</span><span class="sxs-lookup"><span data-stu-id="05927-106">For a description of the information stored in the database for each service, see [Database of Installed Services](database-of-installed-services.md).</span></span> <span data-ttu-id="05927-107">Beispielcode finden Sie unter [Installieren eines Dienstanbieter](installing-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="05927-107">For sample code, see [Installing a Service](installing-a-service.md).</span></span>

<span data-ttu-id="05927-108">Ein Konfigurationsprogramm verwendet die Funktion " [**Delta**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) Service", um einen installierten Dienst aus der Datenbank zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="05927-108">A configuration program uses the [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) function to remove an installed service from the database.</span></span> <span data-ttu-id="05927-109">Weitere Informationen finden Sie unter [Löschen eines Dienstanbieter](deleting-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="05927-109">For more information, see [Deleting a Service](deleting-a-service.md).</span></span>

<span data-ttu-id="05927-110">Um den Dienstnamen zu erhalten, rufen Sie die [**getservicekeyname**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="05927-110">To obtain the service name, call the [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea) function.</span></span> <span data-ttu-id="05927-111">Der Anzeige Name des Diensts, der in der System Steuerungs Option "Dienste" verwendet wird, kann durch Aufrufen der Funktion " [**getservicedisplayname**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="05927-111">The service display name, used in the Services control panel applet, can be obtained by calling the [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea) function.</span></span>

<span data-ttu-id="05927-112">Ein Dienst Konfigurationsprogramm kann die [**EnumServicesStatus usex**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) -Funktion verwenden, um alle Dienste und deren Status aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="05927-112">A service configuration program can use the [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) function to enumerate all services and their statuses.</span></span> <span data-ttu-id="05927-113">Sie kann auch die [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) -Funktion verwenden, um aufzulisten, welche Dienste von einem angegebenen Dienst Objekt abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="05927-113">It can also use the [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) function to enumerate which services are dependent on a specified service object.</span></span>

 

 



