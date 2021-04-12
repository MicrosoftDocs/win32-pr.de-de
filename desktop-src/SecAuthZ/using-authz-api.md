---
description: Mit der Authz-API können Anwendungen anpassbare Zugriffs Überprüfungen durchführen, um die Leistung zu verbessern und die Access Control Entwicklung zu vereinfachen.
ms.assetid: 83df96ff-f3d6-43f8-88b2-6387914b3503
title: Verwenden der Authz-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86394c0df408307ae4c49377af4a1ae8cc1f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349708"
---
# <a name="using-authz-api"></a><span data-ttu-id="1369f-103">Verwenden der Authz-API</span><span class="sxs-lookup"><span data-stu-id="1369f-103">Using Authz API</span></span>

<span data-ttu-id="1369f-104">Mit der Authz-API können Anwendungen anpassbare Zugriffs Überprüfungen durchführen, um die Leistung zu verbessern und die [Access Control](low-level-access-control.md)Entwicklung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="1369f-104">Authz API allows applications to perform customizable access checks with better performance and more simplified development than [Low-level Access Control](low-level-access-control.md).</span></span>

<span data-ttu-id="1369f-105">Mit der Authz-API können Anwendungen Zugriffs Überprüfungen Zwischenspeichern, um die Leistung zu verbessern, Client Kontexte abzufragen und zu ändern und Geschäftsregeln zu definieren, die zum dynamischen Auswerten der Zugriffsberechtigung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="1369f-105">Authz API allows applications to cache access checks for improved performance, to query and modify client contexts, and to define business rules that can be used to evaluate access permission dynamically.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1369f-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="1369f-106">In This Section</span></span>



| <span data-ttu-id="1369f-107">Thema</span><span class="sxs-lookup"><span data-stu-id="1369f-107">Topic</span></span>                                                                             | <span data-ttu-id="1369f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1369f-108">Description</span></span>                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1369f-109">Initialisieren eines Client Kontexts</span><span class="sxs-lookup"><span data-stu-id="1369f-109">Initializing a Client Context</span></span>](initializing-a-client-context.md)<br/>     | <span data-ttu-id="1369f-110">Eine Anwendung muss einen Client Kontext erstellen, bevor Sie mit der Authz-API Zugriffs Überprüfungen oder-Überwachungen durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="1369f-110">An application must create a client context before it can use Authz API to perform access checks or auditing.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="1369f-111">Abfragen eines Client Kontexts</span><span class="sxs-lookup"><span data-stu-id="1369f-111">Querying a Client Context</span></span>](querying-a-client-context.md)<br/>             | <span data-ttu-id="1369f-112">Anwendungen können die [**AuthZGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) -Funktion aufrufen, um Informationen über einen vorhandenen Client Kontext abzufragen.</span><span class="sxs-lookup"><span data-stu-id="1369f-112">Applications can call the [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) function to query information about an existing client context.</span></span><br/>                                                                                       |
| [<span data-ttu-id="1369f-113">Hinzufügen von SIDs zu einem Client Kontext</span><span class="sxs-lookup"><span data-stu-id="1369f-113">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)<br/> | <span data-ttu-id="1369f-114">Eine Anwendung kann einem vorhandenen Client Kontext [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -IDs (SIDs) hinzufügen, indem Sie die [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1369f-114">An application can add [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) to an existing client context by calling the [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) function.</span></span><br/> |
| [<span data-ttu-id="1369f-115">Überprüfen des Zugriffs mit der Authz-API</span><span class="sxs-lookup"><span data-stu-id="1369f-115">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)<br/>   | <span data-ttu-id="1369f-116">Anwendungen bestimmen, ob der Zugriff auf Sicherungs fähige Objekte durch Aufrufen der [**authzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) -Funktion gewährt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1369f-116">Applications determine whether to grant access to securable objects by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="1369f-117">Caching-Zugriffs Überprüfungen</span><span class="sxs-lookup"><span data-stu-id="1369f-117">Caching Access Checks</span></span>](caching-access-checks.md)<br/>                     | <span data-ttu-id="1369f-118">Wenn eine Anwendung eine Zugriffs Überprüfung durch Aufrufen der [**authzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) -Funktion durchführt, können die Ergebnisse dieser Zugriffs Überprüfung zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1369f-118">When an application performs an access check by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function, the results of that access check can be cached.</span></span><br/>                                                                                       |



 

 

