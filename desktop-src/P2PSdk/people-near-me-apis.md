---
description: APIs für Personen in meiner Umgebung
ms.assetid: 3b142d23-a9b2-465c-9bdc-484afbde154e
title: APIs für Personen in meiner Umgebung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132d358a7d51a1069f7a4d1dc1ddfe2752dbdd1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959782"
---
# <a name="people-near-me-apis"></a><span data-ttu-id="028a7-103">APIs für Personen in meiner Umgebung</span><span class="sxs-lookup"><span data-stu-id="028a7-103">People Near Me APIs</span></span>

<span data-ttu-id="028a7-104">Alle Anwendungen, die [Personen in meiner](about-people-near-me.md) Umgebung (PNM) unterstützen, können die folgenden Win32-APIs verwenden:</span><span class="sxs-lookup"><span data-stu-id="028a7-104">Any applications capable of [People Near Me](about-people-near-me.md) (PNM) can use the following Win32 APIs:</span></span>

### <a name="contacts-api"></a><span data-ttu-id="028a7-105">Kontakte-API</span><span class="sxs-lookup"><span data-stu-id="028a7-105">Contacts API</span></span>

<span data-ttu-id="028a7-106">Die Contacts-API wird für den Zugriff auf die Kontaktinformationen des angemeldeten Benutzers, zum Abrufen von Informationen zu zuvor gespeicherten Kontakten oder zum Speichern der Kontaktinformationen und des digitalen Zertifikats eines neuen Kontakts verwendet.</span><span class="sxs-lookup"><span data-stu-id="028a7-106">The Contacts API is used to access the contact information for the logged on user, retrieve information about previously stored contacts, or store the contact information and digital certificate of a new contact.</span></span>

### <a name="people-near-me-api"></a><span data-ttu-id="028a7-107">API für Personen in meiner Umgebung</span><span class="sxs-lookup"><span data-stu-id="028a7-107">People Near Me API</span></span>

<span data-ttu-id="028a7-108">Die PNM-API wird verwendet, um nach Benutzern in der Nähe, ihren angekündigten Interessen, beliebigen Objekten, die Sie veröffentlichen möchten, und angekündigten Anwendungen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="028a7-108">The PNM API is used to find users nearby, their advertised interests, any arbitrary objects they choose to publish, and advertised applications.</span></span>

### <a name="publication-api"></a><span data-ttu-id="028a7-109">Veröffentlichungs-API</span><span class="sxs-lookup"><span data-stu-id="028a7-109">Publication API</span></span>

<span data-ttu-id="028a7-110">Die Veröffentlichungs-API wird für die Interaktion mit Remote Kontakten verwendet.</span><span class="sxs-lookup"><span data-stu-id="028a7-110">The Publication API is used to interact with remote contacts.</span></span> <span data-ttu-id="028a7-111">Die [Peer-Signal](windows-peer-components-for-people-near-me.md) Schicht, die vom Veröffentlichungs-Manager verwendet wird, wird auch vom PNM-Modul zum Herstellen von Verbindungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="028a7-111">The [Peer Signaling](windows-peer-components-for-people-near-me.md) layer used by the Publication Manager is also used by the PNM module for establishing connections.</span></span>

### <a name="invitation-api"></a><span data-ttu-id="028a7-112">Einladungs-API</span><span class="sxs-lookup"><span data-stu-id="028a7-112">Invitation API</span></span>

<span data-ttu-id="028a7-113">Die Einladungs-API wird von einer Zusammenarbeits Anwendung verwendet, um bestimmte Peers in eine Zusammenarbeits Aktivität einzuladen.</span><span class="sxs-lookup"><span data-stu-id="028a7-113">The Invitation API is used by a collaboration application to invite specific peer(s) into a collaboration activity.</span></span>

### <a name="application-registration-api"></a><span data-ttu-id="028a7-114">Anwendungsregistrierungs-API</span><span class="sxs-lookup"><span data-stu-id="028a7-114">Application Registration API</span></span>

<span data-ttu-id="028a7-115">Die anwendungsregistrierungs-API wird vom Installationsprogramm einer Zusammenarbeits Anwendung verwendet, um die Anwendung zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="028a7-115">The Application Registration API is used by the installer of a collaboration application to register the application.</span></span> <span data-ttu-id="028a7-116">Eine PNM-fähige Anwendung fordert den Benutzer während des Installationsvorgangs auf, um zu bestimmen, ob die Anwendung für Benutzer im Subnetz zur Verfügung gestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="028a7-116">A PNM-capable application will prompt the user during the installation process to determine whether the application should be made available to users on the subnet.</span></span>

 

 



