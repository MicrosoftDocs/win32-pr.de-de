---
title: Informationen zu NPS-Erweiterungen
description: In diesem Abschnitt wird beschrieben, wie DLLs implementiert werden, um die Funktionalität von NPS zu erweitern. Es beschreibt die Interaktion zwischen NPS und den DLLs und zeigt einige Entwurfs Überlegungen hinsichtlich der DLLs an.
ms.assetid: 3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05878a5243774046c1ca052052d59be9378483d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339898"
---
# <a name="about-nps-extensions"></a><span data-ttu-id="8b82c-104">Informationen zu NPS-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="8b82c-104">About NPS Extensions</span></span>

> [!Note]  
> <span data-ttu-id="8b82c-105">Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt.</span><span class="sxs-lookup"><span data-stu-id="8b82c-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="8b82c-106">Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS.</span><span class="sxs-lookup"><span data-stu-id="8b82c-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="8b82c-107">Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="8b82c-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="8b82c-108">In diesem Abschnitt wird beschrieben, wie DLLs implementiert werden, um die Funktionalität von NPS zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="8b82c-108">This section describes how to implement DLLs to extend the functionality of NPS.</span></span> <span data-ttu-id="8b82c-109">Es beschreibt die Interaktion zwischen NPS und den DLLs und zeigt einige Entwurfs Überlegungen hinsichtlich der DLLs an.</span><span class="sxs-lookup"><span data-stu-id="8b82c-109">It describes the interaction between NPS and the DLLs, and presents some design considerations regarding the DLLs.</span></span>

<span data-ttu-id="8b82c-110">NPS bietet zwei Erweiterungs Punkte, eine für die Authentifizierung und die andere für die Autorisierung.</span><span class="sxs-lookup"><span data-stu-id="8b82c-110">NPS provides two extension points, one for authentication and the other for authorization.</span></span> <span data-ttu-id="8b82c-111">Authentifizierung bezieht sich auf die Überprüfung der Identität des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="8b82c-111">Authentication refers to verifying the identity of the user.</span></span> <span data-ttu-id="8b82c-112">Autorisierung bezieht sich auf die Bestimmung der Dienste, die das Netzwerk für den Benutzer bereitstellen soll.</span><span class="sxs-lookup"><span data-stu-id="8b82c-112">Authorization refers to determining what services the network should provide to the user.</span></span> <span data-ttu-id="8b82c-113">Die beiden Erweiterungs Punkte entsprechen authentifizierungserweiterungs-DLLs und DLLs für Autorisierungs Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="8b82c-113">The two extension points correspond to Authentication Extension DLLs and Authorization Extension DLLs.</span></span> <span data-ttu-id="8b82c-114">Jeder Erweiterungs Punkt kann mehrere DLLs unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8b82c-114">Each extension point can support multiple DLLs.</span></span>

<span data-ttu-id="8b82c-115">NPS bietet Authentifizierungs-und Autorisierungs Dienste.</span><span class="sxs-lookup"><span data-stu-id="8b82c-115">NPS provides both authentication and authorization services.</span></span> <span data-ttu-id="8b82c-116">Authentifizierungserweiterungs-DLLs werden von NPS vor der integrierten NPS-Authentifizierung und-Autorisierung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8b82c-116">Authentication Extension DLLs are called by NPS prior to the built-in NPS authentication and authorization.</span></span> <span data-ttu-id="8b82c-117">Autorisierungs Erweiterungs-DLLs werden nach der NPS-Authentifizierung und-Autorisierung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8b82c-117">Authorization Extension DLLs are called after NPS authentication and authorization.</span></span>

<span data-ttu-id="8b82c-118">Das folgende Diagramm veranschaulicht den Fluss von Paketen über einen NPS-RADIUS-Server, der mithilfe von Erweiterungs-DLLs erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="8b82c-118">The following diagram illustrates the flow of packets through an NPS RADIUS server that is expanded using Extension DLLs.</span></span>

![NPS-Authentifizierungs-und-Autorisierungs Prozess](images/ias03.png)

<span data-ttu-id="8b82c-120">Wenn eine authentifizierungserweiterungs-dll "Accept" zurückgibt, überspringt das Paket die NPS-Authentifizierung und wechselt direkt zur NPS-Autorisierung.</span><span class="sxs-lookup"><span data-stu-id="8b82c-120">If an Authentication Extension DLL returns ACCEPT, the packet skips the NPS authentication and goes directly to NPS authorization.</span></span>

> [!Note]  
> <span data-ttu-id="8b82c-121">Wenn mehrere authentifizierungserweiterungs-DLLs vorhanden sind, können die restlichen Erweiterungs-DLLs ebenfalls übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="8b82c-121">When multiple Authentication Extension DLLs are present, the rest of the Extension DLLs might be skipped as well.</span></span> <span data-ttu-id="8b82c-122">Weitere Informationen finden [Sie unter Einrichten der Erweiterungs-DLLs](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) .</span><span class="sxs-lookup"><span data-stu-id="8b82c-122">See [Setting Up the Extension DLLs](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) for more information.</span></span>

 

<span data-ttu-id="8b82c-123">Wenn eine Authentifizierungs Erweiterungs-DLL "Continue" zurückgibt, wird das Paket an die NPS-Authentifizierung und dann an die NPS-Autorisierung geleitet.</span><span class="sxs-lookup"><span data-stu-id="8b82c-123">If an Authentication Extension DLL returns CONTINUE, the packet goes to NPS authentication, and then to NPS authorization.</span></span>

> [!Note]  
> <span data-ttu-id="8b82c-124">Wenn mehrere authentifizierungserweiterungs-DLLs vorhanden sind, werden die restlichen authentifizierungserweiterungs-DLLs vor der NPS-Authentifizierung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8b82c-124">When multiple Authentication Extension DLLs are present, the rest of the Authentication Extension DLLs are invoked before NPS authentication.</span></span>

 

<span data-ttu-id="8b82c-125">In den folgenden Themen werden die Erweiterungs-DLLs ausführlicher beschrieben:</span><span class="sxs-lookup"><span data-stu-id="8b82c-125">The following topics describe the Extension DLLs in more detail:</span></span>

-   [<span data-ttu-id="8b82c-126">Einrichten der Erweiterungs-DLLs</span><span class="sxs-lookup"><span data-stu-id="8b82c-126">Setting Up the Extension DLLs</span></span>](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
-   [<span data-ttu-id="8b82c-127">Aufrufen der Erweiterungs-DLLs</span><span class="sxs-lookup"><span data-stu-id="8b82c-127">Invoking the Extension DLLs</span></span>](/windows/desktop/Nps/ias-authentication-and-authorization-process)
-   [<span data-ttu-id="8b82c-128">Benutzer Identifizierungs Attribute</span><span class="sxs-lookup"><span data-stu-id="8b82c-128">User Identification Attributes</span></span>](/windows/desktop/Nps/ias-user-identification-attributes)

 

 