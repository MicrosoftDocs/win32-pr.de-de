---
description: Zum Delegieren von Anmelde Informationen für die Credential Security Support Provider Protocol (aufzurufende Anmelde Informationen) müssen Sie angeben, an welche Server delegiert werden kann.
ms.assetid: 15ed9a62-2eee-4f29-92c5-ccf2754cdf13
title: Einstellungen für den Gruppenrichtlinie ""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a159b7a162df3eda692462a3d3972159e61797e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362302"
---
# <a name="credssp-group-policy-settings"></a><span data-ttu-id="399cf-103">Einstellungen für den Gruppenrichtlinie ""</span><span class="sxs-lookup"><span data-stu-id="399cf-103">CredSSP Group Policy Settings</span></span>

<span data-ttu-id="399cf-104">Zum Delegieren von Anmelde Informationen für die [Credential Security Support Provider Protocol (](credential-security-support-provider.md) aufzurufende Anmelde Informationen) müssen Sie angeben, an welche Server delegiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="399cf-104">For [Credential Security Support Provider protocol (CredSSP)](credential-security-support-provider.md) to delegate credentials, you must specify which servers can be delegated to.</span></span> <span data-ttu-id="399cf-105">Um diese Server anzugeben, ändern Sie die Einstellungen im MMC-Snap-in (Microsoft Management Console) des Gruppenrichtlinie-Editors (gpe).</span><span class="sxs-lookup"><span data-stu-id="399cf-105">To specify those servers, modify settings in the Group Policy Editor (GPE) Microsoft Management Console (MMC) snap-in.</span></span> <span data-ttu-id="399cf-106">Die gpe-Einstellungen, die die Delegierung steuern, sind unter **Computer Konfiguration \| Administrative Vorlagen \| \| Delegierung von System Anmelde** Informationen</span><span class="sxs-lookup"><span data-stu-id="399cf-106">The GPE settings that control delegation are under **Computer Configuration \| Administrative Templates \| System \| Credentials Delegation**.</span></span>

> [!Caution]  
> <span data-ttu-id="399cf-107">Dies ist keine eingeschränkte Delegierung.</span><span class="sxs-lookup"><span data-stu-id="399cf-107">This is not constrained delegation.</span></span> <span data-ttu-id="399cf-108">"Kredssp" übergibt die vollständigen Anmelde Informationen des Benutzers ohne Einschränkung an den Server.</span><span class="sxs-lookup"><span data-stu-id="399cf-108">CredSSP passes the user's full credentials to the server without any constraint.</span></span>

 

<span data-ttu-id="399cf-109">Die Delegierung der folgenden Anmelde Informationstypen wird von Gruppenrichtlinien Einstellungen gesteuert.</span><span class="sxs-lookup"><span data-stu-id="399cf-109">Group policy settings control delegation of the following types of credentials.</span></span>



| <span data-ttu-id="399cf-110">Typ der Anmelde Informationen</span><span class="sxs-lookup"><span data-stu-id="399cf-110">Credentials Type</span></span>                                                                                                                                 | <span data-ttu-id="399cf-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="399cf-111">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="399cf-112"><span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Standard Anmelde Informationen</span><span class="sxs-lookup"><span data-stu-id="399cf-112"><span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Default credentials</span></span><br/> | <span data-ttu-id="399cf-113">Die Anmelde Informationen, die bei der ersten Anmeldung des Benutzers bei Windows abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="399cf-113">The credentials obtained when the user first logs on to Windows.</span></span><br/>                   |
| <span data-ttu-id="399cf-114"><span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Neue Anmelde Informationen</span><span class="sxs-lookup"><span data-stu-id="399cf-114"><span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Fresh credentials</span></span><br/>         | <span data-ttu-id="399cf-115">Die Anmelde Informationen, nach denen der Benutzer beim Ausführen einer Anwendung gefragt wird.</span><span class="sxs-lookup"><span data-stu-id="399cf-115">The credentials that the user is prompted for when executing an application.</span></span><br/>       |
| <span data-ttu-id="399cf-116"><span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Gespeicherte Anmelde Informationen</span><span class="sxs-lookup"><span data-stu-id="399cf-116"><span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Saved credentials</span></span><br/>         | <span data-ttu-id="399cf-117">Die Anmelde Informationen, die mit [Credential Manager](credential-manager.md)gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="399cf-117">The credentials that are saved using [Credential Manager](credential-manager.md).</span></span><br/> |



 

<span data-ttu-id="399cf-118">Fügen Sie den [*Dienst Prinzipal Namen*](/windows/desktop/SecGloss/s-gly) (SPN) dieses Servers der Liste der Server für diese Gruppenrichtlinien Einstellung hinzu, um einen Server in die Kategorie aufzunehmen, die einer bestimmten Gruppenrichtlinien Einstellung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="399cf-118">To include a server in the category associated with a particular group policy setting, add the [*Service Principal Name*](/windows/desktop/SecGloss/s-gly) (SPN) of that server to the list of servers for that group policy setting.</span></span> <span data-ttu-id="399cf-119">Der SPN kann ein einzelnes Platzhalter Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="399cf-119">The SPN can contain a single wildcard character.</span></span>

 

