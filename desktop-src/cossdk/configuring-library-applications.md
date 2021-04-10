---
description: Konfigurieren von Bibliotheksanwendungen
ms.assetid: db375e0f-74ca-44df-918a-b0e48742a594
title: Konfigurieren von Bibliotheksanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51e00626d42044797881ccb86553ddfda38a089
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041383"
---
# <a name="configuring-library-applications"></a><span data-ttu-id="a3b30-103">Konfigurieren von Bibliotheksanwendungen</span><span class="sxs-lookup"><span data-stu-id="a3b30-103">Configuring Library Applications</span></span>

<span data-ttu-id="a3b30-104">Da com+-Bibliotheksanwendungen im Client Prozess ausgeführt werden, unterscheiden sich die konfigurierbaren Elemente für Bibliotheksanwendungen erheblich von der für Server Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="a3b30-104">Because COM+ library applications run in the client's process, the configurable elements for library applications are considerably different than for server applications.</span></span> <span data-ttu-id="a3b30-105">Es ist nicht möglich, einen Aspekt der Anwendung zu konfigurieren, der vom Hostingprozess bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="a3b30-105">You cannot configure any aspect of the application that is determined by the hosting process.</span></span>

<span data-ttu-id="a3b30-106">Auf Anwendungsebene sind mehrere Einstellungen für Bibliotheksanwendungen entweder eingeschränkt oder nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a3b30-106">At the application level, several settings are either limited or unavailable for library applications.</span></span> <span data-ttu-id="a3b30-107">Diese Einschränkungen werden in der folgenden Tabelle beschrieben:</span><span class="sxs-lookup"><span data-stu-id="a3b30-107">These constraints are described in the following table:</span></span>



| <span data-ttu-id="a3b30-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="a3b30-108">Attribute</span></span>                                       | <span data-ttu-id="a3b30-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3b30-109">Description</span></span>                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3b30-110">Sicherheitsstufe</span><span class="sxs-lookup"><span data-stu-id="a3b30-110">Security level</span></span><br/>                       | <span data-ttu-id="a3b30-111">Sie müssen Zugriffs Überprüfungen auf Komponentenebene auswählen.</span><span class="sxs-lookup"><span data-stu-id="a3b30-111">You must choose component-level access checks.</span></span> <span data-ttu-id="a3b30-112">Die Bibliotheks Anwendung kann keine Zugriffs Überprüfungen auf Prozessebene beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="a3b30-112">The library application cannot influence process-level access checks.</span></span> <span data-ttu-id="a3b30-113">Weitere Informationen finden Sie unter [Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="a3b30-113">See [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span><br/>             |
| <span data-ttu-id="a3b30-114">Aktivieren oder Deaktivieren der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="a3b30-114">Enabling or disabling authentication</span></span><br/> | <span data-ttu-id="a3b30-115">Sie können angeben, ob die Bibliotheks Anwendung an der vom Host Prozess ausgeführten Authentifizierung beteiligt sein soll.</span><span class="sxs-lookup"><span data-stu-id="a3b30-115">You can indicate whether the library application will participate in authentication performed by the host process.</span></span> <span data-ttu-id="a3b30-116">Siehe [Aktivieren der Authentifizierung für eine Bibliotheks Anwendung](enabling-authentication-for-a-library-application.md).</span><span class="sxs-lookup"><span data-stu-id="a3b30-116">See [Enabling Authentication for a Library Application](enabling-authentication-for-a-library-application.md).</span></span><br/> |
| <span data-ttu-id="a3b30-117">Ebene des Identitätswechsels</span><span class="sxs-lookup"><span data-stu-id="a3b30-117">Impersonation level</span></span><br/>                  | <span data-ttu-id="a3b30-118">Vorübergehend.</span><span class="sxs-lookup"><span data-stu-id="a3b30-118">Unavailable.</span></span> <span data-ttu-id="a3b30-119">Die Einstellung des Host Prozesses wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3b30-119">The setting of the host process is used.</span></span> <br/>                                                                                                                                                                             |
| <span data-ttu-id="a3b30-120">Sicherheitsidentität</span><span class="sxs-lookup"><span data-stu-id="a3b30-120">Security identity</span></span><br/>                    | <span data-ttu-id="a3b30-121">Vorübergehend.</span><span class="sxs-lookup"><span data-stu-id="a3b30-121">Unavailable.</span></span> <span data-ttu-id="a3b30-122">Die Anwendung wird mit der Identität des Host Prozesses ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3b30-122">The application runs under the identity of the host process.</span></span><br/>                                                                                                                                                          |
| <span data-ttu-id="a3b30-123">Server Prozess wird heruntergefahren</span><span class="sxs-lookup"><span data-stu-id="a3b30-123">Server process shutdown</span></span><br/>              | <span data-ttu-id="a3b30-124">Vorübergehend.</span><span class="sxs-lookup"><span data-stu-id="a3b30-124">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="a3b30-125">Unterstützung für 3 GB aktivieren</span><span class="sxs-lookup"><span data-stu-id="a3b30-125">Enable 3-GB support</span></span><br/>                  | <span data-ttu-id="a3b30-126">Vorübergehend.</span><span class="sxs-lookup"><span data-stu-id="a3b30-126">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="a3b30-127">Im Debugger starten</span><span class="sxs-lookup"><span data-stu-id="a3b30-127">Launch in debugger</span></span><br/>                   | <span data-ttu-id="a3b30-128">Vorübergehend.</span><span class="sxs-lookup"><span data-stu-id="a3b30-128">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="a3b30-129">Aktivieren von CRM</span><span class="sxs-lookup"><span data-stu-id="a3b30-129">Enable CRM</span></span><br/>                           | <span data-ttu-id="a3b30-130">Vorübergehend.</span><span class="sxs-lookup"><span data-stu-id="a3b30-130">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="a3b30-131">Queuing</span><span class="sxs-lookup"><span data-stu-id="a3b30-131">Queuing</span></span><br/>                              | <span data-ttu-id="a3b30-132">Vorübergehend.</span><span class="sxs-lookup"><span data-stu-id="a3b30-132">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="a3b30-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a3b30-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3b30-134">Übersicht über die COM+-Anwendung</span><span class="sxs-lookup"><span data-stu-id="a3b30-134">COM+ Application Overview</span></span>](com--application-overview.md)
</dt> </dl>

 

 




