---
title: Zugreifen auf den Reservierungs Speicher
description: Die HTTP-Server-API verwaltet die Liste der Namespace Reservierungen für alle Benutzer auf dem Computer.
ms.assetid: 4b1291fc-cc62-4d4f-9150-18cbb1f6e5c0
keywords:
- Zugreifen auf den Reservierungs Speicher http
- Reservierungs Speicher http, zugreifen auf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a138a0a2385e6338877e5e8623527a64a6eca796
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388321"
---
# <a name="accessing-the-reservation-store"></a><span data-ttu-id="de2eb-105">Zugreifen auf den Reservierungs Speicher</span><span class="sxs-lookup"><span data-stu-id="de2eb-105">Accessing the Reservation Store</span></span>

<span data-ttu-id="de2eb-106">Die HTTP-Server-API verwaltet die Liste der Namespace Reservierungen für alle Benutzer auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="de2eb-106">The HTTP Server API maintains the namespace reservation list for all users on the computer.</span></span> <span data-ttu-id="de2eb-107">Ein Reservierungs Eintrag besteht aus einem [URLPrefix](urlprefix-strings.md) und einer entsprechenden ACL.</span><span class="sxs-lookup"><span data-stu-id="de2eb-107">A reservation entry consists of a [UrlPrefix](urlprefix-strings.md) and corresponding ACL.</span></span> <span data-ttu-id="de2eb-108">Jedes URLPrefix im Speicher verfügt über eine ACL, die alle Benutzer auflistet, die sich für den Empfang von Anforderungen für den Namespace registrieren dürfen.</span><span class="sxs-lookup"><span data-stu-id="de2eb-108">Each UrlPrefix in the store has an ACL that lists all the users that are permitted to register to receive requests for the namespace.</span></span> <span data-ttu-id="de2eb-109">Benutzer mit Delegierungs Berechtigungen können Teil Strukturen des Namespace, den Sie besitzen, an andere Benutzer delegieren oder vorhandene Reservierungen mithilfe der Konfigurations-APIs löschen.</span><span class="sxs-lookup"><span data-stu-id="de2eb-109">Users with delegation privileges can delegate subtrees of the namespace that they own to other users or delete existing reservations using the configuration APIs.</span></span>

<span data-ttu-id="de2eb-110">Um dem permanenten Reservierungs Speicher eine Reservierung hinzuzufügen, ruft die Anwendung die [**httpsetserviceconfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) -Funktion auf, wobei der Konfigurations-ID-Parameter auf den **httpserviceconfigurlaclinfo** -Wert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="de2eb-110">To add a reservation to the persistent reservation store, the application calls the [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) function with the configuration ID parameter set to the **HttpServiceConfigUrlAclInfo** value.</span></span> <span data-ttu-id="de2eb-111">Die HTTP-Server-API überprüft den Besitz des Namespace und der Benutzer-ID, bevor eine Reservierung zum Speicher hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="de2eb-111">The HTTP Server API verifies the ownership of the namespace and the user ID before adding a reservation to the store.</span></span>

<span data-ttu-id="de2eb-112">Die HTTP-Server-API stellt auch Funktionen zum Abfragen und Löschen der Dienst Konfigurationen für URL-Namespaces bereit.</span><span class="sxs-lookup"><span data-stu-id="de2eb-112">The HTTP Server API also supplies functions to query and delete the Service configurations for URL namespaces.</span></span> <span data-ttu-id="de2eb-113">Die [**httpqueryserviceconfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) -Funktion, die mit dem Parameter "Configuration ID" aufgerufen wurde, ist auf die **httpserviceconfigurlaclinfo** -Wert Abfragen festgelegt, und die Funktion " [**httpdelta eteserviceconfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) " wird im URL-Namespace Speicher gelöscht.</span><span class="sxs-lookup"><span data-stu-id="de2eb-113">The [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) function called with the configuration ID parameter set to the **HttpServiceConfigUrlAclInfo** value queries, and the [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) function deletes on the URL namespace store.</span></span>

 

 




