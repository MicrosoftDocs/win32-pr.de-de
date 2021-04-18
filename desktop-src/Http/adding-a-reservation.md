---
title: Hinzufügen einer Reservierung
description: Die Routing Datenbank enthält die Reservierungsliste.
ms.assetid: c36e731c-6a0b-42a8-bc92-106a8e017b0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358181cbe57a046f5af54f7adf17bdadb24c3ddc
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104517201"
---
# <a name="adding-a-reservation"></a><span data-ttu-id="659f7-103">Hinzufügen einer Reservierung</span><span class="sxs-lookup"><span data-stu-id="659f7-103">Adding a Reservation</span></span>

<span data-ttu-id="659f7-104">Die Routing Datenbank enthält die Reservierungsliste.</span><span class="sxs-lookup"><span data-stu-id="659f7-104">The routing database contains the reservation list.</span></span> <span data-ttu-id="659f7-105">Die Reservierungsliste besteht aus den Benutzern, denen der Zugriff auf den Namespace gestattet ist, sowie der Zugriffsebene für jeden Benutzer, der unter der Reservierung aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="659f7-105">The reservation list consists of the users that are allowed access to the namespace, as well as the level of access for each user listed under the reservation.</span></span> <span data-ttu-id="659f7-106">Wenn Reservierungen hinzugefügt oder gelöscht werden, werden die Routing Datenbanken durchsucht, um die Zugriffsberechtigungen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="659f7-106">When reservations are added or deleted, the routing database is searched to determine access privileges.</span></span>

<span data-ttu-id="659f7-107">Zusätzlich zum Überprüfen der Benutzer-ID prüft die HTTP-Server-API auch, ob in vorhandenen Reservierungen vor der Installation einer neuen Reservierung Konflikte auftreten.</span><span class="sxs-lookup"><span data-stu-id="659f7-107">In addition to checking the users ID, the HTTP Server API also checks for conflicts in existing reservations before installing a new reservation.</span></span>

<span data-ttu-id="659f7-108">**So fügen Sie eine neue Reservierung hinzu**</span><span class="sxs-lookup"><span data-stu-id="659f7-108">**To add a new reservation**</span></span>

1.  <span data-ttu-id="659f7-109">Wenn die Portnummer im URLPrefix über Reservierungen oder Registrierungen für ein Schema verfügt, das sich von dem Schema im URLPrefix unterscheidet, schlägt die Registrierung fehl.</span><span class="sxs-lookup"><span data-stu-id="659f7-109">If the port number in the UrlPrefix has reservations or registrations for a scheme different from the scheme in the UrlPrefix, the registration fails.</span></span> <span data-ttu-id="659f7-110">HTTP und HTTPS können nicht auf demselben Port unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="659f7-110">HTTP and HTTPS cannot be supported on the same port.</span></span>
2.  <span data-ttu-id="659f7-111">Suchen Sie den entsprechenden Bucket für die Registrierung (siehe Abschnitt [Routing eingehender Anforderungen](routing-incoming-requests.md) ), basierend auf dem Hosttyp.</span><span class="sxs-lookup"><span data-stu-id="659f7-111">Locate the appropriate bucket for the registration (see the [Routing Incoming Requests](routing-incoming-requests.md) section), based on the host type.</span></span> <span data-ttu-id="659f7-112">Die restlichen Schritte sind relativ zu diesem Bucket.</span><span class="sxs-lookup"><span data-stu-id="659f7-112">The remaining steps are relative to this bucket.</span></span>
3.  <span data-ttu-id="659f7-113">Wählen Sie Reservierungs Einträge mit Schema-, Host-und Port Komponenten aus, die dem zu Reservier enden URLPrefix entsprechen.</span><span class="sxs-lookup"><span data-stu-id="659f7-113">Select reservation entries with scheme, host and port components that match the UrlPrefix being reserved.</span></span> <span data-ttu-id="659f7-114">Suchen Sie den Eintrag mit dem längsten übereinstimmenden *relativeUri* , der nicht gleich dem relativeUri in der Reservierung ist (d. h. dem über *geordneten Knoten*).</span><span class="sxs-lookup"><span data-stu-id="659f7-114">From these, locate the entry with the longest matching *relativeUri* that is not equal to the relativeUri in the reservation (that is, the *parent node*).</span></span> <span data-ttu-id="659f7-115">Wenn der Eintrag vorhanden ist, überprüfen Sie die Zugriffsrechte basierend auf der ACL, die diesem Eintrag zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="659f7-115">If the entry exists, then evaluate access rights based on the ACL assigned to that entry.</span></span>
4.  <span data-ttu-id="659f7-116">Wenn kein übergeordneter Knoten gefunden wurde, handelt es sich hierbei um eine Reservierung mit einer leeren relativeUri-oder *root-Reservierung*.</span><span class="sxs-lookup"><span data-stu-id="659f7-116">If a parent node was not found, this is a reservation with an empty relativeUri, or *root reservation*.</span></span> <span data-ttu-id="659f7-117">Erteilen Sie Zugriffsrechte nur, wenn der Aufrufer unter den LocalSystem-oder Administrator Konten registriert ist.</span><span class="sxs-lookup"><span data-stu-id="659f7-117">Grant access rights only if the caller is registered under the LocalSystem or Administrator accounts.</span></span>
5.  <span data-ttu-id="659f7-118">Wenn Zugriffsrechte gewährt werden, überprüfen Sie, ob doppelte Reservierungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="659f7-118">If access rights are granted, check for duplicate reservations.</span></span> <span data-ttu-id="659f7-119">Wenn ein Reservierungs Eintrag mit demselben Schema, Port, Host und relativeUri vorhanden ist, wird ein \_ Fehler \_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="659f7-119">If a reservation entry exists with the same scheme, port, host and relativeUri, an ERROR\_ALREADY\_EXISTS code is returned.</span></span>
    > [!Note]  
    > <span data-ttu-id="659f7-120">Das Aktualisieren eines vorhandenen Eintrags sollte in zwei Schritten ausgeführt werden: Löschen Sie den Eintrag, und fügen Sie einen neuen Eintrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="659f7-120">Updating an existing entry should be performed in two steps: delete the entry and add a new one.</span></span>

     

<span data-ttu-id="659f7-121">Wenn die oben genannten Schritte erfolgreich ausgeführt wurden, wird ein neuer Reservierungs Eintrag in die Reservierungs Datenbank eingegeben.</span><span class="sxs-lookup"><span data-stu-id="659f7-121">If the above steps succeed, a new reservation entry is entered into the reservation database.</span></span>

> [!Note]  
> <span data-ttu-id="659f7-122">Der neue Eintrag wird mit der angegebenen ACL erstellt und erbt keine ACLs vom über *geordneten* Eintrag.</span><span class="sxs-lookup"><span data-stu-id="659f7-122">The new entry is created with the specified ACL and does not inherit ACLs from the *parent* entry.</span></span>

 

<span data-ttu-id="659f7-123">In den folgenden Beispielen wird der Reservierungsprozess veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="659f7-123">The following examples illustrate the reservation process.</span></span>

-   <span data-ttu-id="659f7-124">Reservierung 1: `https://+:80/vroot/subdir/` vom Administrator für Benutzer A und Benutzer C ist erfolgreich und wird in den Bucket "+" eingegeben.</span><span class="sxs-lookup"><span data-stu-id="659f7-124">Reservation 1: `https://+:80/vroot/subdir/` by Admin for User A and User C succeeds and is entered into the "+" bucket.</span></span>
-   <span data-ttu-id="659f7-125">Reservierung 2: `https://adatum.com:80/vroot/` vom Administrator für Benutzer B ist erfolgreich und wird in den Bucket "Expliziter Host" eingetragen.</span><span class="sxs-lookup"><span data-stu-id="659f7-125">Reservation 2: `https://adatum.com:80/vroot/` by Admin for User B succeeds and is entered into the "Explicit host" bucket.</span></span>
-   <span data-ttu-id="659f7-126">Reservierung 3: `https://adatum.com:80/vroot/subdir/otherdir/` von Benutzer B für Benutzer C ist aufgrund von Reservierung 2 erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="659f7-126">Reservation 3: `https://adatum.com:80/vroot/subdir/otherdir/` by User B for User C succeeds due to reservation 2.</span></span>
-   <span data-ttu-id="659f7-127">Reservierung 4: `https://+:80/vroot/subdir/otherdir/` Benutzer A für Benutzer E ist aufgrund von Reservierung 1 erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="659f7-127">Reservation 4: `https://+:80/vroot/subdir/otherdir/` by User A for User E succeeds due to reservation 1.</span></span>
-   <span data-ttu-id="659f7-128">Reservierung 5: `https://adatum.com:80/vroot/subdir/otherdir/` Benutzer A für Benutzer E schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="659f7-128">Reservation 5: `https://adatum.com:80/vroot/subdir/otherdir/` by User A for User E fails.</span></span> <span data-ttu-id="659f7-129">Der Zugriff wurde aufgrund von Reservierung 2 verweigert.</span><span class="sxs-lookup"><span data-stu-id="659f7-129">Access denied due to reservation 2.</span></span>
-   <span data-ttu-id="659f7-130">Reservierung 6: `https://+:80/vroot/subdir/` der Administrator für Benutzer A schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="659f7-130">Reservation 6: `https://+:80/vroot/subdir/` by Admin for User A fails.</span></span> <span data-ttu-id="659f7-131">Die Reservierung steht in Konflikt mit Reservierung 1.</span><span class="sxs-lookup"><span data-stu-id="659f7-131">The reservation conflicts with reservation 1.</span></span>
-   <span data-ttu-id="659f7-132">Reservierung 7: `https://adatum.com:80/newroot/` von Benutzer a für Benutzer a schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="659f7-132">Reservation 7: `https://adatum.com:80/newroot/` by User A for User A fails.</span></span> <span data-ttu-id="659f7-133">Der Zugriff wurde aufgrund einer impliziten Stamm Reservierung von `https://adatum.com:80/` für "LocalSystem" oder "Administrator" verweigert.</span><span class="sxs-lookup"><span data-stu-id="659f7-133">Access denied due to implicit root reservation of `https://adatum.com:80/` for LocalSystem or Administrator.</span></span>

<span data-ttu-id="659f7-134">Reservierungen können den Satz von URLs in Anforderungen beeinflussen, die an einen Prozess übermittelt wurden, der zuvor ein URLPrefix registriert hat.</span><span class="sxs-lookup"><span data-stu-id="659f7-134">Reservations can affect the set of URLs in requests delivered to a process that has previously registered a UrlPrefix.</span></span> <span data-ttu-id="659f7-135">Ein Beispiel:</span><span class="sxs-lookup"><span data-stu-id="659f7-135">For example, consider the following scenario.</span></span>

-   <span data-ttu-id="659f7-136">Registrierung: `https://adatum.com:80/vroot/` von Anwendung 1 für Benutzer A.</span><span class="sxs-lookup"><span data-stu-id="659f7-136">Registration: `https://adatum.com:80/vroot/` by application 1 for User A.</span></span>
-   <span data-ttu-id="659f7-137">Eine Anforderung für `https://adatum.com:80/vroot/subdir/file.htm` wird an Anwendung 1 übermittelt.</span><span class="sxs-lookup"><span data-stu-id="659f7-137">A request for `https://adatum.com:80/vroot/subdir/file.htm` is delivered to application 1.</span></span>
-   <span data-ttu-id="659f7-138">Reservierung: `https://+:80/vroot/subdir/` für Benutzer B.</span><span class="sxs-lookup"><span data-stu-id="659f7-138">Reservation: `https://+:80/vroot/subdir/` for User B.</span></span>
-   <span data-ttu-id="659f7-139">Eine Anforderung für `https://adatum.com:80/vroot/subdir/file.htm` wird jetzt abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="659f7-139">A request for `https://adatum.com:80/vroot/subdir/file.htm` is now rejected.</span></span>
-   <span data-ttu-id="659f7-140">Registrierung: `https://adatum.com:80/vroot/subdir/` von Anwendung 2 für Benutzer B.</span><span class="sxs-lookup"><span data-stu-id="659f7-140">Registration: `https://adatum.com:80/vroot/subdir/` by application 2 for User B.</span></span>
-   <span data-ttu-id="659f7-141">Eine Anforderung für `https://adatum.com:80/vroot/subdir/file.htm` wird an Anwendung 2 übermittelt.</span><span class="sxs-lookup"><span data-stu-id="659f7-141">A request for `https://adatum.com:80/vroot/subdir/file.htm` is delivered to application 2.</span></span>

 

 




