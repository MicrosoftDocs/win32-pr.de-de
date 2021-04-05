---
title: Veröffentlichen mit Dienst Verbindungs Punkten
description: Das Active Directory Schema definiert eine serviceConnectionPoint-Objektklasse (SCP), um es einem Dienst zu erleichtern, Dienst spezifische Daten im Verzeichnis zu veröffentlichen.
ms.assetid: 3544aa64-ecb0-48a1-ae49-05247a983842
ms.tgt_platform: multiple
keywords:
- Veröffentlichen mit Dienst Verbindungs Punkten AD
- Dienst Verbindungspunkte AD
- Dienst Verbindungspunkte AD, Veröffentlichung mit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a458822f6c5e4d764b2e330c7ba084021b586548
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707577"
---
# <a name="publishing-with-service-connection-points"></a><span data-ttu-id="f47e1-106">Veröffentlichen mit Dienst Verbindungs Punkten</span><span class="sxs-lookup"><span data-stu-id="f47e1-106">Publishing with Service Connection Points</span></span>

<span data-ttu-id="f47e1-107">Das Active Directory Schema definiert eine **serviceConnectionPoint** -Objektklasse (SCP), um es einem Dienst zu erleichtern, Dienst spezifische Daten im Verzeichnis zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="f47e1-107">The Active Directory Schema defines a **serviceConnectionPoint** (SCP) object class to make it easy for a service to publish service-specific data in the directory.</span></span> <span data-ttu-id="f47e1-108">Clients des Dienstanbieter verwenden die Daten in einem Dienst Verbindungspunkt, um eine Instanz des Dienstanbieter zu suchen, zu verbinden und zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="f47e1-108">Clients of the service use the data in an SCP to locate, connect to, and authenticate an instance of your service.</span></span>

<span data-ttu-id="f47e1-109">Dieser Abschnitt enthält eine Übersicht über Dienst Verbindungspunkte und Codebeispiele, die zeigen, wie eine Client-/Dienstanwendung SCPs verwendet.</span><span class="sxs-lookup"><span data-stu-id="f47e1-109">This section provides an overview of service connection points and code examples that show how a client/service application uses SCPs.</span></span>

<span data-ttu-id="f47e1-110">Im Codebeispiel werden die folgenden Schritte ausgeführt, um eine Dienst Veröffentlichung mit SCPs zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="f47e1-110">The code example follows these steps to implement service publication with SCPs.</span></span>

<span data-ttu-id="f47e1-111">Weitere Informationen und ein Codebeispiel, in dem diese Schritte ausgeführt werden, finden Sie unter [Erstellen eines Dienst Verbindungs Punkts](creating-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="f47e1-111">For more information and a code example that performs these steps, see [Creating a Service Connection Point](creating-a-service-connection-point.md).</span></span>

<span data-ttu-id="f47e1-112">**So erstellen Sie SCPs im Verzeichnis bei der Dienst Installation**</span><span class="sxs-lookup"><span data-stu-id="f47e1-112">**To create SCPs in the directory at service installation**</span></span>

1.  <span data-ttu-id="f47e1-113">Binden Sie an das Computer Objekt für den Host Computer, auf dem die Dienst Instanz installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f47e1-113">Bind to the computer object for the host computer on which the service instance is installed.</span></span>
2.  <span data-ttu-id="f47e1-114">Erstellen Sie ein SCP-Objekt als untergeordnetes Element des Computer Objekts, und geben Sie die Anfangswerte für die Attribute des Dienst Verbindungs Punkts an.</span><span class="sxs-lookup"><span data-stu-id="f47e1-114">Create an SCP object as a child of the computer object, specifying the initial values for the attributes of the SCP.</span></span>
3.  <span data-ttu-id="f47e1-115">Legen Sie Zugriffs Steuerungs Einträge (Access Control Entries, ACEs) in der Sicherheits Beschreibung des SCP-Objekts fest, damit der Dienst SCP-Eigenschaften zur Laufzeit ändern kann.</span><span class="sxs-lookup"><span data-stu-id="f47e1-115">Set access control entries (ACEs) in the security descriptor of the SCP object to enable the service to modify SCP properties at run time.</span></span>
4.  <span data-ttu-id="f47e1-116">Speichern Sie die **objectGUID** des Dienst Verbindungs Diensts in der Registrierung auf dem Host Computer des Diensts.</span><span class="sxs-lookup"><span data-stu-id="f47e1-116">Cache the **objectGUID** of the SCP in the registry on the service's host computer.</span></span>

<span data-ttu-id="f47e1-117">Weitere Informationen und ein Codebeispiel, das diese Schritte ausführt, finden Sie unter [Aktualisieren eines Dienst Verbindungs Punkts](updating-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="f47e1-117">For more information and a code example that performs these steps, see [Updating a Service Connection Point](updating-a-service-connection-point.md).</span></span>

<span data-ttu-id="f47e1-118">**So aktualisieren Sie die SCP-Attribute beim Dienst Start**</span><span class="sxs-lookup"><span data-stu-id="f47e1-118">**To update the SCP attributes at service startup**</span></span>

1.  <span data-ttu-id="f47e1-119">Rufen Sie die **objectGUID** aus der Registrierung ab, und verwenden Sie Sie zum Binden an den SCP.</span><span class="sxs-lookup"><span data-stu-id="f47e1-119">Retrieve the **objectGUID** from the registry and use it to bind to the SCP.</span></span>
2.  <span data-ttu-id="f47e1-120">Abrufen von Attributen (z. b. **servicednsname** und **serviceBindingInformation**) vom SCP.</span><span class="sxs-lookup"><span data-stu-id="f47e1-120">Retrieve attributes, such as **serviceDNSName** and **serviceBindingInformation**, from the SCP.</span></span> <span data-ttu-id="f47e1-121">Vergleichen Sie diese Werte mit den aktuellen Werten, und aktualisieren Sie ggf. den Dienst Verbindungspunkt.</span><span class="sxs-lookup"><span data-stu-id="f47e1-121">Compare these values to the current values and update the SCP if necessary.</span></span>

<span data-ttu-id="f47e1-122">Weitere Informationen und ein Codebeispiel, in dem diese Schritte ausgeführt werden, finden Sie unter [wie Clients einen Dienst Verbindungspunkt suchen und verwenden](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="f47e1-122">For more information and a code example that performs these steps, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span>

<span data-ttu-id="f47e1-123">**So suchen und verwenden Sie einen SCP durch eine Client Anwendung**</span><span class="sxs-lookup"><span data-stu-id="f47e1-123">**To find and use an SCP by a client application**</span></span>

1.  <span data-ttu-id="f47e1-124">Binden Sie an den globalen Katalog, und suchen Sie nach Objekten mit einem **Schlüssel** Wort Attribut, das der Produkt-GUID des dienstanzdienstan</span><span class="sxs-lookup"><span data-stu-id="f47e1-124">Bind to the Global Catalog and search for objects with a **keywords** attribute that matches the service's product GUID.</span></span> <span data-ttu-id="f47e1-125">Jedes gefundene Objekt ist eine Instanz des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="f47e1-125">Each object found is an instance of the service.</span></span> <span data-ttu-id="f47e1-126">Wählen Sie eine Instanz aus, und rufen Sie den Distinguished Name des Dienst Verbindungs Punkts ab.</span><span class="sxs-lookup"><span data-stu-id="f47e1-126">Select an instance and retrieve the distinguished name of the SCP.</span></span>
2.  <span data-ttu-id="f47e1-127">Verwenden Sie den definierten Namen, um eine Bindung mit dem Dienstverbindungspunkt herzustellen.</span><span class="sxs-lookup"><span data-stu-id="f47e1-127">Use the distinguished name to bind to the SCP.</span></span>
3.  <span data-ttu-id="f47e1-128">Rufen Sie die Werte verschiedener Attribute aus dem SCP ab, z. b. **servicednsname** und **serviceBindingInformation**.</span><span class="sxs-lookup"><span data-stu-id="f47e1-128">Retrieve the values of various attributes from the SCP, such as **serviceDNSName** and **serviceBindingInformation**.</span></span> <span data-ttu-id="f47e1-129">Verwenden Sie diese Werte, um sich mit der Dienstinstanz zu verbinden und sich bei dieser zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="f47e1-129">Use these values to connect to and authenticate the service instance.</span></span>

<span data-ttu-id="f47e1-130">Weitere Informationen zu den Rollen, die ein SCP erstellen und aktualisieren können, finden Sie unter [Sicherheitsprobleme bei der Dienst Veröffentlichung](security-issues-for-service-publication.md).</span><span class="sxs-lookup"><span data-stu-id="f47e1-130">For more information about what roles can create and update an SCP, see [Security Issues for Service Publication](security-issues-for-service-publication.md).</span></span>

<span data-ttu-id="f47e1-131">Weitere Informationen zum Erstellen eines Dienst Verbindungs Punkts finden Sie unter [Erstellen eines Dienst Verbindungs Punkts](where-to-create-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="f47e1-131">For more information about where to create an SCP, see [Where to Create a Service Connection Point](where-to-create-a-service-connection-point.md).</span></span>

<span data-ttu-id="f47e1-132">Weitere Informationen zur Art der Daten, die in einem SCP gespeichert werden sollen, finden Sie unter [Eigenschaften von Dienst Verbindungs Punkten](service-connection-point-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f47e1-132">For more information about the kind of data to store in an SCP, see [Service Connection Point Properties](service-connection-point-properties.md).</span></span>

<span data-ttu-id="f47e1-133">Weitere Informationen darüber, wie ein Dienst Installationsprogramm und der Dienst zusammenarbeiten, um aktuelle Daten in einem Dienst Verbindungspunkt beizubehalten, finden Sie unter [Erstellen und Verwalten eines Dienst Verbindungs Punkts](creating-and-maintaining-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="f47e1-133">For more information about how a service installer and the service work together to maintain current data in an SCP, see [Creating and Maintaining a Service Connection Point](creating-and-maintaining-a-service-connection-point.md).</span></span>

 

 




