---
description: Der SCM unterstützt handle-Typen, um den Zugriff auf die folgenden Objekte zuzulassen.
ms.assetid: 5ffdd1a9-1a66-4fc4-b35d-4f744bae4897
title: SCM-Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8a84fb09dbc95f3e1b5f5cee432de616f5ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366182"
---
# <a name="scm-handles"></a><span data-ttu-id="d6549-103">SCM-Handles</span><span class="sxs-lookup"><span data-stu-id="d6549-103">SCM Handles</span></span>

<span data-ttu-id="d6549-104">Der SCM unterstützt handle-Typen, um den Zugriff auf die folgenden Objekte zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="d6549-104">The SCM supports handle types to allow access to the following objects.</span></span>

-   <span data-ttu-id="d6549-105">Die Datenbank der installierten Dienste.</span><span class="sxs-lookup"><span data-stu-id="d6549-105">The database of installed services.</span></span>
-   <span data-ttu-id="d6549-106">Ein-Dienst.</span><span class="sxs-lookup"><span data-stu-id="d6549-106">A service.</span></span>
-   <span data-ttu-id="d6549-107">Die Datenbanksperre.</span><span class="sxs-lookup"><span data-stu-id="d6549-107">The database lock.</span></span>

<span data-ttu-id="d6549-108">Ein scmanager-Objekt stellt die Datenbank der installierten Dienste dar.</span><span class="sxs-lookup"><span data-stu-id="d6549-108">An SCManager object represents the database of installed services.</span></span> <span data-ttu-id="d6549-109">Es handelt sich um ein Container Objekt, das Dienst Objekte enthält.</span><span class="sxs-lookup"><span data-stu-id="d6549-109">It is a container object that holds service objects.</span></span> <span data-ttu-id="d6549-110">Die [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) -Funktion gibt ein Handle für ein scmanager-Objekt auf einem angegebenen Computer zurück.</span><span class="sxs-lookup"><span data-stu-id="d6549-110">The [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function returns a handle to an SCManager object on a specified computer.</span></span> <span data-ttu-id="d6549-111">Dieses Handle wird beim Installieren, löschen, öffnen und Auflisten von Diensten sowie beim Sperren der Dienst Datenbank verwendet.</span><span class="sxs-lookup"><span data-stu-id="d6549-111">This handle is used when installing, deleting, opening, and enumerating services and when locking the services database.</span></span>

<span data-ttu-id="d6549-112">Ein Dienst Objekt stellt einen installierten Dienst dar.</span><span class="sxs-lookup"><span data-stu-id="d6549-112">A service object represents an installed service.</span></span> <span data-ttu-id="d6549-113">Die Funktionen [**"-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) " und " [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) " geben Handles an installierte Dienste zurück.</span><span class="sxs-lookup"><span data-stu-id="d6549-113">The [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) functions return handles to installed services.</span></span>

<span data-ttu-id="d6549-114">Die Funktionen " [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)", " [**forateservice**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)" und " [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) " können unterschiedliche Typen von Zugriff auf scmanager-und Dienst Objekte anfordern.</span><span class="sxs-lookup"><span data-stu-id="d6549-114">The [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera), [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea), and [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) functions can request different types of access to SCManager and service objects.</span></span> <span data-ttu-id="d6549-115">Der angeforderte Zugriff wird abhängig vom Zugriffs Token des aufrufenden Prozesses und der Sicherheits Beschreibung, die dem scmanager-oder Dienst Objekt zugeordnet ist, gewährt oder verweigert.</span><span class="sxs-lookup"><span data-stu-id="d6549-115">The requested access is granted or denied depending on the access token of the calling process and the security descriptor associated with the SCManager or service object.</span></span>

<span data-ttu-id="d6549-116">Die [**closeservicehandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) -Funktion schließt Handles zu scmanager-und Dienst Objekten.</span><span class="sxs-lookup"><span data-stu-id="d6549-116">The [**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) function closes handles to SCManager and service objects.</span></span> <span data-ttu-id="d6549-117">Wenn Sie diese Handles nicht mehr benötigen, sollten Sie Sie schließen.</span><span class="sxs-lookup"><span data-stu-id="d6549-117">When you no longer need these handles, be sure to close them.</span></span>

 

 



