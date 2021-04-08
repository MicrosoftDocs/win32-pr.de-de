---
title: Wie ein Dienst seine SPNs verfasst hat
description: 'Ein Dienst kann zwei Funktionen verwenden, um seine SPNs zu verfassen: Es handelt sich um eine allgemeine Funktion zum Verfassen von SPNs, und DsServerRegisterSpn ist eine spezialisierte Funktion zum Verfassen und registrieren einfacher SPNs für einen Host basierten Dienst.'
ms.assetid: 8710409a-67b1-45e5-9cd7-5125443ab921
ms.tgt_platform: multiple
keywords:
- Dienst Prinzipal Name AD, wie ein Dienst zusammensetzt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5611527cc3c240eebc195058ce39daab71aeef23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855428"
---
# <a name="how-a-service-composes-its-spns"></a><span data-ttu-id="83a26-104">Wie ein Dienst seine SPNs verfasst hat</span><span class="sxs-lookup"><span data-stu-id="83a26-104">How a Service Composes its SPNs</span></span>

<span data-ttu-id="83a26-105">Ein Dienst kann seine SPNs mithilfe von zwei Funktionen zusammensetzen: [**dsgetspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) ist eine allgemeine Funktion zum Verfassen von SPNs, und [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) ist eine spezialisierte Funktion zum Erstellen und registrieren einfacher SPNs für einen Host basierten Dienst.</span><span class="sxs-lookup"><span data-stu-id="83a26-105">A service can use two functions to compose its SPNs: [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) is a general-purpose function for composing SPNs and [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) is a specialized function for composing and registering simple SPNs for a host-based service.</span></span>

<span data-ttu-id="83a26-106">Ein Dienst Installationsprogramm verwendet in der Regel die [**dsgetspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) -Funktion zum Verfassen von SPNs, die dann mithilfe der [**dswrite-accountspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) -Funktion für das Anmelde Konto des Diensts registriert werden.</span><span class="sxs-lookup"><span data-stu-id="83a26-106">A service installer typically uses the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) function to compose SPNs, which it then registers on the service's logon account using the [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) function.</span></span> <span data-ttu-id="83a26-107">Der **dsgetspn** kann die folgenden Funktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="83a26-107">The **DsGetSpn** can perform the following functions.</span></span>

-   <span data-ttu-id="83a26-108">Erstellen Sie einen einfachen SPN mit dem <service class> / <host> Format "" für einen Host basierten Dienst.</span><span class="sxs-lookup"><span data-stu-id="83a26-108">Create a simple SPN with the "<service class>/<host>" format for a host-based service.</span></span>
-   <span data-ttu-id="83a26-109">Erstellen Sie einen komplexen Dienst Prinzipal Namen, der die &lt; Komponente "Dienst Name" enthält, die &gt; von replizierungsdiensten verwendet wird, oder die &lt; Komponente "Port &gt; ", die mehrere Instanzen eines Diensts auf einem einzelnen Host unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="83a26-109">Create a complex SPN that includes the "&lt;service name&gt;" component used by replicable services or the "&lt;port&gt;" component that distinguishes multiple instances of a service on a single host.</span></span>
-   <span data-ttu-id="83a26-110">Erstellen Sie einen einzelnen SPN, wobei die " &lt; Host &gt; "-Komponente entweder auf den Namen eines angegebenen Hosts oder auf den Namen des lokalen Computers standardmäßig festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="83a26-110">Create a single SPN with the "&lt;host&gt;" component set to either the name of a specified host or the name of the local computer by default.</span></span>
-   <span data-ttu-id="83a26-111">Erstellen Sie ein Array von SPNs für mehrere Dienst Instanzen, die auf mehreren Hosts in der Gesamtstruktur ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="83a26-111">Create an array of SPNs for multiple service instances that will run on multiple hosts throughout the forest.</span></span> <span data-ttu-id="83a26-112">Jeder SPN gibt den Namen des Hosts für eine Dienst Instanz an.</span><span class="sxs-lookup"><span data-stu-id="83a26-112">Each SPN specifies the name of the host for a service instance.</span></span>
-   <span data-ttu-id="83a26-113">Erstellen Sie ein Array von SPNs für mehrere Dienst Instanzen, die auf demselben Host ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="83a26-113">Create an array of SPNs for multiple service instances that will run on the same host.</span></span> <span data-ttu-id="83a26-114">Jeder SPN gibt den Namen des Hosts und eine Portnummer für eine Dienst Instanz an.</span><span class="sxs-lookup"><span data-stu-id="83a26-114">Each SPN specifies the name of the host and a port number for a service instance.</span></span>

<span data-ttu-id="83a26-115">Das von [**dsgetspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) zurückgegebene Array von Namen muss durch Aufrufen der [**dsfreespnarray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya) -Funktion freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="83a26-115">The array of names returned by [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) must be freed by calling the [**DsFreeSpnArray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya) function.</span></span>

<span data-ttu-id="83a26-116">Beachten Sie, dass die Funktionen [**dsgetspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna), [**dswrite teaccountspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)und [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) nicht überprüfen, ob die SPNs eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="83a26-116">Be aware that the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna), [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna), and [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) functions do not verify that SPNs are unique.</span></span> <span data-ttu-id="83a26-117">Da die gegenseitige Authentifizierung fehlschlägt, wenn ein Client einen nicht eindeutigen SPN anzeigt, überprüfen Sie die Eindeutigkeit, bevor Sie einen SPN registrieren.</span><span class="sxs-lookup"><span data-stu-id="83a26-117">Because mutual authentication fails if a client presents an SPN that is not unique, verify uniqueness before registering an SPN.</span></span> <span data-ttu-id="83a26-118">Zu diesem Zweck Durchsuchen Sie den globalen Katalog (GC) nach **servicePrincipalName** -Attributen, die dem SPN entsprechen.</span><span class="sxs-lookup"><span data-stu-id="83a26-118">To do this, search the global catalog (GC) for **servicePrincipalName** attributes that match your SPN.</span></span> <span data-ttu-id="83a26-119">Weitere Informationen zum Durchsuchen des GC finden Sie unter durch [Suchen des globalen Katalogs](searching-global-catalog-contents.md).</span><span class="sxs-lookup"><span data-stu-id="83a26-119">For more information about searching the GC, see [Searching the Global Catalog](searching-global-catalog-contents.md).</span></span>

 

 




