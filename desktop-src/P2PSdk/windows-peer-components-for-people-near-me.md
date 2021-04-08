---
description: Windows-Peer Komponenten für "Personen in meiner Umgebung"
ms.assetid: aa9e7d4d-4131-4578-8bd1-298f04b826f9
title: Windows-Peer Komponenten für "Personen in meiner Umgebung"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c780ccad1abd5ce04c1672f66561285831e5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959774"
---
# <a name="windows-peer-components-for-people-near-me"></a><span data-ttu-id="57b65-103">Windows-Peer Komponenten für "Personen in meiner Umgebung"</span><span class="sxs-lookup"><span data-stu-id="57b65-103">Windows Peer Components for People Near Me</span></span>

<span data-ttu-id="57b65-104">Innerhalb der ausführbaren Windows-Peer-Netzwerkdatei (P2phost.exe) werden in der [Architektur "Personen in meiner](people-near-me-architecture.md) Umgebung" die folgenden Komponenten verwendet:</span><span class="sxs-lookup"><span data-stu-id="57b65-104">Within the main Windows Peer Networking executable (P2phost.exe), the [People Near Me Architecture](people-near-me-architecture.md) uses the following components:</span></span>

### <a name="people-near-me"></a><span data-ttu-id="57b65-105">Personen in meiner Umgebung</span><span class="sxs-lookup"><span data-stu-id="57b65-105">People Near Me</span></span>

<span data-ttu-id="57b65-106">Die Komponente "Personen in meiner Umgebung" (PNM) initiiert die Ermittlung mithilfe der Webdienst Ermittlung im lokalen Subnetz für die Benutzernamen von PNM-fähigen Computern.</span><span class="sxs-lookup"><span data-stu-id="57b65-106">The People Near Me (PNM) component initiates discovery using Web Services Discovery on the local subnet for the user names of PNM-capable computers.</span></span>

### <a name="people-near-me-publisher"></a><span data-ttu-id="57b65-107">"Personen in meiner Umgebung"</span><span class="sxs-lookup"><span data-stu-id="57b65-107">People Near Me Publisher</span></span>

<span data-ttu-id="57b65-108">Die Verleger Komponente "Personen in meiner Umgebung" veröffentlicht die Spitznamen angemeldeter Benutzer, um die Verfügbarkeit für andere Computer mit PNM im lokalen Subnetz anzugeben.</span><span class="sxs-lookup"><span data-stu-id="57b65-108">The People Near Me Publisher component publishes the nicknames of logged-on users to indicate availability to other computers using PNM on the local subnet.</span></span> <span data-ttu-id="57b65-109">Der angemeldete Benutzer muss seinen Spitznamen vor der Ankündigung veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="57b65-109">The logged-on user must elect to publish their nickname before it is advertised.</span></span> <span data-ttu-id="57b65-110">Der Spitzname wird im Subnetz mithilfe der Webdienst Ermittlung veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="57b65-110">The nickname is published on the subnet using Web Services Discovery.</span></span> <span data-ttu-id="57b65-111">Darüber hinaus können auch Objekte und Anwendungen veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="57b65-111">Additionally, objects and applications can also be published.</span></span> <span data-ttu-id="57b65-112">Der Benutzer muss jedoch die Objekt-und Anwendungs Veröffentlichung für die Bereiche "**Personen in meiner** Umgebung" oder "**alle**" angeben.</span><span class="sxs-lookup"><span data-stu-id="57b65-112">However, the user must specify object and application publication for the '**People Near Me**' or '**All**' scopes.</span></span>

### <a name="people-near-me-enumerator"></a><span data-ttu-id="57b65-113">Enumerator "Personen in meiner Umgebung"</span><span class="sxs-lookup"><span data-stu-id="57b65-113">People Near Me Enumerator</span></span>

<span data-ttu-id="57b65-114">Die enumeratorkomponente "Personen in meiner Umgebung" listet die Benutzer auf, die sich im lokalen Subnetz befinden.</span><span class="sxs-lookup"><span data-stu-id="57b65-114">The People Near Me Enumerator component enumerates the list of users on the local subnet.</span></span> <span data-ttu-id="57b65-115">Mithilfe dieser Liste sendet die Webdienst Ermittlung eine Multicast Abfrage und empfängt die Antworten.</span><span class="sxs-lookup"><span data-stu-id="57b65-115">Using this list, Web Services Discovery sends a multicast query and receives the responses.</span></span> <span data-ttu-id="57b65-116">Nachdem die Liste der Spitznamen abgerufen wurde, kann eine Anwendung die API verwenden, um weitere Daten abzurufen, die vom Benutzer veröffentlicht werden (der mithilfe von [SChannel](windows-vista-components-for-people-near-me.md)verschlüsselt wurde), z. b. die Liste der registrierten Anwendungen und alle Objekte, die veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="57b65-116">After the list of nicknames are obtained, an application can use the API to retrieve more data being published by the user (which is encrypted using [SChannel](windows-vista-components-for-people-near-me.md)), such as the list of applications registered and any objects being published.</span></span>

<span data-ttu-id="57b65-117">Der Such-und enumerationsprozess wird nicht automatisch durchgeführt, sondern muss von einem Benutzer oder einer Anwendung explizit initiiert werden, indem er sich bei PNM anmeldet.</span><span class="sxs-lookup"><span data-stu-id="57b65-117">The search and enumeration process does not happen automatically, but must be explicitly initiated by a user or an application by signing-in to PNM.</span></span> <span data-ttu-id="57b65-118">Die Suchergebnisse sind die Liste der Spitznamen anderer Benutzer im gleichen Subnetz, die ihre Spitznamen mithilfe der PNM-API ankündigen.</span><span class="sxs-lookup"><span data-stu-id="57b65-118">The search results are the list of nicknames of other users on the same subnet that are advertising their nicknames using the PNM API.</span></span>

### <a name="publication-manager"></a><span data-ttu-id="57b65-119">Veröffentlichungs-Manager</span><span class="sxs-lookup"><span data-stu-id="57b65-119">Publication Manager</span></span>

<span data-ttu-id="57b65-120">Die Veröffentlichungs-Manager-Komponente ist für das Veröffentlichen von Anwesenheits-, Anwendungs-oder Objekt Updates für Kontakte oder Personen in meiner Nähe zuständig, die Daten abonniert oder abgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="57b65-120">The Publication Manager component is responsible for publishing presence, application, or object updates to contacts or people near me that are subscribed or poll for data.</span></span>

### <a name="peer-signaling"></a><span data-ttu-id="57b65-121">Peer Signalisierung</span><span class="sxs-lookup"><span data-stu-id="57b65-121">Peer Signaling</span></span>

<span data-ttu-id="57b65-122">Die Peer Signalisierungs Komponente behandelt die Erstellung von Verbindungen zwischen Peers und Exchange-Daten.</span><span class="sxs-lookup"><span data-stu-id="57b65-122">The Peer Signaling component handles the creation of connections between peers to exchange data.</span></span> <span data-ttu-id="57b65-123">Für Personen in meiner Umgebung wird Peer Signalisierung verwendet, wenn ein Benutzer oder eine Anwendung die unicastabfrage an einen bestimmten Computer für seinen öffentlichen Schlüssel, seine Anwendungen und Objekte sendet.</span><span class="sxs-lookup"><span data-stu-id="57b65-123">For People Near Me, Peer Signaling is used when a user or application sends the unicast query to a specific computer for its public key, applications, and objects.</span></span>

### <a name="receive-invitation-handlerux"></a><span data-ttu-id="57b65-124">Einladungs Handler/UX empfangen</span><span class="sxs-lookup"><span data-stu-id="57b65-124">Receive Invitation Handler/UX</span></span>

<span data-ttu-id="57b65-125">Die Komponente empfangende Einladungs Handler/UX empfängt eine eingehende Einladung von einer anderen Person, fordert den Benutzer auf, zu bestimmen, ob die der Einladung zugeordnete Anwendung gestartet werden soll, und startet dann die Anwendung basierend auf dem Benutzer, der die Einladung annimmt.</span><span class="sxs-lookup"><span data-stu-id="57b65-125">The Receive Invitation Handler/UX component receives an incoming invitation from another person, prompts the user to determine whether they want to launch the application associated with the invitation, and then launches the application based on the user accepting the invitation.</span></span> <span data-ttu-id="57b65-126">Eine Einladung ist eine Nachricht von einer anderen Person zum Initiieren von Kollaborations Aktivitäten mithilfe einer bestimmten Anwendung, die auf den Computern der Benutzer installiert ist und von dem Benutzer angekündigt wird, der eingeladen wird.</span><span class="sxs-lookup"><span data-stu-id="57b65-126">An invitation is a message from another person to initiate collaboration activity using a specific application that is installed on both user's computers and is advertised by the user being invited.</span></span>

### <a name="peer-security"></a><span data-ttu-id="57b65-127">Peer Sicherheit</span><span class="sxs-lookup"><span data-stu-id="57b65-127">Peer Security</span></span>

<span data-ttu-id="57b65-128">Wenn Anwesenheit, Anwendung und Objekt gesendet werden, werden die Informationen über einen SSL-Kanal ([SChannel](windows-vista-components-for-people-near-me.md)) verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="57b65-128">When presence, application, and object are sent, the information is encrypted using an SSL channel ([Schannel](windows-vista-components-for-people-near-me.md)).</span></span> <span data-ttu-id="57b65-129">Der initiierende Computer verwendet den öffentlichen Schlüssel des eingeladenen Computers, um einen geheimen Schlüssel auszuhandeln, der zum Verschlüsseln der nachfolgenden Daten verwendet wird, die zwischen den beiden Peers gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="57b65-129">The initiating computer uses the public key of the invited computer to negotiate a secret key that is used for encrypting the subsequent data sent between the two peers.</span></span>

 

 



