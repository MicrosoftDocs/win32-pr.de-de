---
title: Dienstprinzipalnamen
description: Ein Dienst Prinzipal Name (Service Principal Name, SPN) ist ein eindeutiger Bezeichner einer Dienst Instanz.
ms.assetid: 54b02853-4097-4e37-b7a2-6b5cfd168ece
ms.tgt_platform: multiple
keywords:
- Dienstprinzipalnamen
- SPN siehe Dienst Prinzipal Namen
- Dienst Prinzipal Name AD
- Dienst Prinzipal Name AD, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa34b7d90803a324faced7d67b56c0b6a1f13af
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858119"
---
# <a name="service-principal-names"></a><span data-ttu-id="30b80-107">Dienstprinzipalnamen</span><span class="sxs-lookup"><span data-stu-id="30b80-107">Service Principal Names</span></span>

<span data-ttu-id="30b80-108">Ein Dienst Prinzipal Name (Service Principal Name, SPN) ist ein eindeutiger Bezeichner einer Dienst Instanz.</span><span class="sxs-lookup"><span data-stu-id="30b80-108">A service principal name (SPN) is a unique identifier of a service instance.</span></span> <span data-ttu-id="30b80-109">SPNs werden von der [Kerberos-Authentifizierung](mutual-authentication-using-kerberos.md) verwendet, um eine Dienst Instanz einem Dienst Anmelde Konto zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="30b80-109">SPNs are used by [Kerberos authentication](mutual-authentication-using-kerberos.md) to associate a service instance with a service logon account.</span></span> <span data-ttu-id="30b80-110">Dadurch kann eine Client Anwendung anfordern, dass der Dienst ein Konto authentifiziert, auch wenn der Client nicht über den Kontonamen verfügt.</span><span class="sxs-lookup"><span data-stu-id="30b80-110">This allows a client application to request that the service authenticate an account even if the client does not have the account name.</span></span>

<span data-ttu-id="30b80-111">Wenn Sie mehrere Instanzen eines Diensts auf Computern innerhalb einer Gesamtstruktur installieren, muss jede Instanz über einen eigenen SPN verfügen.</span><span class="sxs-lookup"><span data-stu-id="30b80-111">If you install multiple instances of a service on computers throughout a forest, each instance must have its own SPN.</span></span> <span data-ttu-id="30b80-112">Eine Dienstinstanz kann mehrere SPNs aufweisen, falls mehrere Namen vorhanden sind, die von den Clients zur Authentifizierung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="30b80-112">A given service instance can have multiple SPNs if there are multiple names that clients might use for authentication.</span></span> <span data-ttu-id="30b80-113">Ein SPN enthält z. b. immer den Namen des Host Computers, auf dem die Dienst Instanz ausgeführt wird, sodass eine Dienst Instanz möglicherweise einen SPN für jeden Namen oder Alias des Hosts registriert.</span><span class="sxs-lookup"><span data-stu-id="30b80-113">For example, an SPN always includes the name of the host computer on which the service instance is running, so a service instance might register an SPN for each name or alias of its host.</span></span> <span data-ttu-id="30b80-114">Weitere Informationen zum SPN-Format und zum Verfassen eines eindeutigen SPN finden Sie unter [namens Formate für eindeutige SPNs](name-formats-for-unique-spns.md).</span><span class="sxs-lookup"><span data-stu-id="30b80-114">For more information about SPN format and composing a unique SPN, see [Name Formats for Unique SPNs](name-formats-for-unique-spns.md).</span></span>

<span data-ttu-id="30b80-115">Bevor der Kerberos-Authentifizierungsdienst einen SPN zum Authentifizieren eines Dienstanbieter verwenden kann, muss der SPN für das Konto Objekt registriert werden, das von der Dienst Instanz für die Anmeldung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="30b80-115">Before the Kerberos authentication service can use an SPN to authenticate a service, the SPN must be registered on the account object that the service instance uses to log on.</span></span> <span data-ttu-id="30b80-116">Ein angegebener SPN kann nur für ein Konto registriert werden.</span><span class="sxs-lookup"><span data-stu-id="30b80-116">A given SPN can be registered on only one account.</span></span> <span data-ttu-id="30b80-117">Bei Win32-Diensten gibt ein Dienst Installationsprogramm das Anmelde Konto an, wenn eine Instanz des Diensts installiert ist.</span><span class="sxs-lookup"><span data-stu-id="30b80-117">For Win32 services, a service installer specifies the logon account when an instance of the service is installed.</span></span> <span data-ttu-id="30b80-118">Der Installer fügt dann die SPNs ein und schreibt Sie als Eigenschaft des Account-Objekts in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="30b80-118">The installer then composes the SPNs and writes them as a property of the account object in Active Directory Domain Services.</span></span> <span data-ttu-id="30b80-119">Wenn das Anmelde Konto einer Dienst Instanz geändert wird, müssen die SPNs unter dem neuen Konto neu registriert werden.</span><span class="sxs-lookup"><span data-stu-id="30b80-119">If the logon account of a service instance changes, the SPNs must be re-registered under the new account.</span></span> <span data-ttu-id="30b80-120">Weitere Informationen finden Sie unter [wie ein Dienst seine SPNs registriert](how-a-service-registers-its-spns.md).</span><span class="sxs-lookup"><span data-stu-id="30b80-120">For more information, see [How a Service Registers its SPNs](how-a-service-registers-its-spns.md).</span></span>

<span data-ttu-id="30b80-121">Wenn ein Client eine Verbindung zu einem Dienst herstellen möchte, sucht er eine Instanz des Diensts, verfasst einen SPN für diese Instanz, stellt eine Verbindung zum Dienst her und übergibt den SPN zur Authentifizierung an den Dienst.</span><span class="sxs-lookup"><span data-stu-id="30b80-121">When a client wants to connect to a service, it locates an instance of the service, composes an SPN for that instance, connects to the service, and presents the SPN for the service to authenticate.</span></span> <span data-ttu-id="30b80-122">Weitere Informationen finden Sie unter [Funktionsweise eines Dienst-SPN durch Clients](how-clients-compose-a-serviceampaposs-spn.md).</span><span class="sxs-lookup"><span data-stu-id="30b80-122">For more information, see [How Clients Compose a Service's SPN](how-clients-compose-a-serviceampaposs-spn.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="30b80-123">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="30b80-123">In this Section</span></span>

## <a name="in-this-section"></a><span data-ttu-id="30b80-124">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="30b80-124">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="30b80-125">Namens Formate für eindeutige SPNs</span><span class="sxs-lookup"><span data-stu-id="30b80-125">Name Formats for Unique SPNs</span></span>](name-formats-for-unique-spns.md)
</dt> <dt>

[<span data-ttu-id="30b80-126">Wie ein Dienst seine SPNs verfasst hat</span><span class="sxs-lookup"><span data-stu-id="30b80-126">How a Service Composes its SPNs</span></span>](how-a-service-composes-its-spns.md)
</dt> <dt>

[<span data-ttu-id="30b80-127">Registrieren der SPNs durch einen Dienst</span><span class="sxs-lookup"><span data-stu-id="30b80-127">How a Service Registers its SPNs</span></span>](how-a-service-registers-its-spns.md)
</dt> <dt>

[<span data-ttu-id="30b80-128">Funktionsweise eines Dienst-SPN durch Clients</span><span class="sxs-lookup"><span data-stu-id="30b80-128">How Clients Compose a Service's SPN</span></span>](how-clients-compose-a-serviceampaposs-spn.md)
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="30b80-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="30b80-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30b80-130">Was ist ein SPN, und warum sollten Sie sich darauf kümmern?</span><span class="sxs-lookup"><span data-stu-id="30b80-130">What is an SPN and why should you care?</span></span>](/archive/blogs/autz_auth_stuff/what-is-a-spn-and-why-should-you-care)
</dt> <dt>

[<span data-ttu-id="30b80-131">Gegenseitige Authentifizierung mithilfe von Kerberos</span><span class="sxs-lookup"><span data-stu-id="30b80-131">Mutual Authentication Using Kerberos</span></span>](mutual-authentication-using-kerberos.md)
</dt> </dl>

 

 