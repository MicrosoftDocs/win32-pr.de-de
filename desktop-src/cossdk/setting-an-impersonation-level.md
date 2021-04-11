---
description: Wenn Sie eine Identitätswechsel Ebene für eine Anwendung festlegen, legen Sie fest, in welchem Maß an Autorität die Anwendung anderen Anwendungen die Verwendung Ihrer Identität beim Aufrufen erteilt.
ms.assetid: 5b5b2c2d-dc3d-4edd-9e13-e6cb13022ceb
title: Festlegen einer Identitätswechsel Ebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1075ac3b10380892cdfdf770543a2dcbb32d56c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127013"
---
# <a name="setting-an-impersonation-level"></a><span data-ttu-id="9aaa9-103">Festlegen einer Identitätswechsel Ebene</span><span class="sxs-lookup"><span data-stu-id="9aaa9-103">Setting an Impersonation Level</span></span>

<span data-ttu-id="9aaa9-104">Wenn Sie eine Identitätswechsel Ebene für eine Anwendung festlegen, legen Sie fest, in welchem Maß an Autorität die Anwendung anderen Anwendungen die Verwendung Ihrer Identität beim Aufrufen erteilt.</span><span class="sxs-lookup"><span data-stu-id="9aaa9-104">When you set an impersonation level for an application, you determine what degree of authority the application grants other applications to use its identity when it calls them.</span></span> <span data-ttu-id="9aaa9-105">Dies kann nur für com+-Server Anwendungen festgelegt werden – Bibliotheksanwendungen werden mit der Identität des Host Prozesses ausgeführt und verwenden die von ihm festgelegte Identitätswechsel Ebene.</span><span class="sxs-lookup"><span data-stu-id="9aaa9-105">You can set this only for COM+ server applications—library applications run under the identity of the hosting process and use the impersonation level that it specifies.</span></span> <span data-ttu-id="9aaa9-106">Weitere Details finden Sie unter Identitätswechsel [Ebenen](/windows/desktop/com/impersonation-levels).</span><span class="sxs-lookup"><span data-stu-id="9aaa9-106">For more detail, see [Impersonation Levels](/windows/desktop/com/impersonation-levels).</span></span>

<span data-ttu-id="9aaa9-107">**So wählen Sie eine Identitätswechsel Ebene aus**</span><span class="sxs-lookup"><span data-stu-id="9aaa9-107">**To select an impersonation level**</span></span>

1.  <span data-ttu-id="9aaa9-108">Klicken Sie mit der rechten Maustaste auf die COM+-Anwendung, für die Sie den Identitätswechsel festlegen, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="9aaa9-108">Right-click the COM+ application for which you are setting impersonation, and then click **Properties**.</span></span>

2.  <span data-ttu-id="9aaa9-109">Klicken Sie im Dialogfeld Anwendungseigenschaften auf die Registerkarte **Sicherheit** .</span><span class="sxs-lookup"><span data-stu-id="9aaa9-109">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="9aaa9-110">Wählen Sie im Feld Identitätswechsel **Ebene** die entsprechende Ebene aus.</span><span class="sxs-lookup"><span data-stu-id="9aaa9-110">In the **Impersonation level** box, select the appropriate level.</span></span> <span data-ttu-id="9aaa9-111">Die folgenden Ebenen sind von der Gewährung der größtmöglichen Autorität abgeleitet:</span><span class="sxs-lookup"><span data-stu-id="9aaa9-111">The levels are as follows, ordered from granting least to greatest authority:</span></span>

    -   <span data-ttu-id="9aaa9-112">**Anonym**.</span><span class="sxs-lookup"><span data-stu-id="9aaa9-112">**Anonymous**.</span></span> <span data-ttu-id="9aaa9-113">Der Client ist gegenüber dem Server anonym.</span><span class="sxs-lookup"><span data-stu-id="9aaa9-113">The client is anonymous to the server.</span></span> <span data-ttu-id="9aaa9-114">Der Server kann die Identität des Clients annehmen, aber das Identitätswechsel Token (lokale Anmelde Informationen) enthält keine Informationen zum Client.</span><span class="sxs-lookup"><span data-stu-id="9aaa9-114">The server can impersonate the client, but the impersonation token (a local credential) does not contain any information about the client.</span></span>
    -   <span data-ttu-id="9aaa9-115">**Identifizieren** Sie.</span><span class="sxs-lookup"><span data-stu-id="9aaa9-115">**Identify**.</span></span> <span data-ttu-id="9aaa9-116">Der Server kann die Identität des Clients abrufen und die Identität des Clients annehmen, um ACL-Überprüfungen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="9aaa9-116">The server can obtain the client's identity and can impersonate the client to do ACL checks.</span></span>
    -   <span data-ttu-id="9aaa9-117">Identität **annehmen.**</span><span class="sxs-lookup"><span data-stu-id="9aaa9-117">**Impersonate**.</span></span> <span data-ttu-id="9aaa9-118">Der Server kann die Identität des Clients annehmen, während er in seinem Namen agiert, obwohl mit Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="9aaa9-118">The server can impersonate the client while acting on its behalf, although with restrictions.</span></span> <span data-ttu-id="9aaa9-119">Der Server kann auf Ressourcen auf dem gleichen Computer wie der Client zugreifen.</span><span class="sxs-lookup"><span data-stu-id="9aaa9-119">The server can access resources on the same computer as the client.</span></span> <span data-ttu-id="9aaa9-120">Wenn sich der Server auf demselben Computer wie der-Client befindet, kann er auf Netzwerkressourcen als Client zugreifen.</span><span class="sxs-lookup"><span data-stu-id="9aaa9-120">If the server is on the same computer as the client, it can access network resources as the client.</span></span> <span data-ttu-id="9aaa9-121">Wenn sich der-Server auf einem anderen Computer als der-Client befindet, kann er nur auf Ressourcen zugreifen, die sich auf demselben Computer wie der-Server befinden.</span><span class="sxs-lookup"><span data-stu-id="9aaa9-121">If the server is on a computer different from the client, it can access only resources that are on the same computer as the server.</span></span> <span data-ttu-id="9aaa9-122">Dies ist die Standardeinstellung für com+-Server Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="9aaa9-122">This is the default setting for COM+ server applications.</span></span>
    -   <span data-ttu-id="9aaa9-123">**Delegat.**</span><span class="sxs-lookup"><span data-stu-id="9aaa9-123">**Delegate**.</span></span> <span data-ttu-id="9aaa9-124">Der Server kann die Identität des Clients annehmen, während er in seinem Namen agiert, egal ob auf dem gleichen Computer wie der Client.</span><span class="sxs-lookup"><span data-stu-id="9aaa9-124">The server can impersonate the client while acting on its behalf, whether on the same computer as the client.</span></span> <span data-ttu-id="9aaa9-125">Während des Identitäts Wechsels können die Anmelde Informationen des Clients (sowohl mit lokalen als auch mit dem Netzwerk Gültigkeitsdauer) an eine beliebige Anzahl von Computern übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="9aaa9-125">During impersonation, the client's credentials (both those with local and those with network validity) can be passed to any number of machines.</span></span>

4.  <span data-ttu-id="9aaa9-126">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="9aaa9-126">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9aaa9-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9aaa9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9aaa9-128">Konfigurieren von Role-Based Sicherheit</span><span class="sxs-lookup"><span data-stu-id="9aaa9-128">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="9aaa9-129">Konfigurieren der Software Einschränkungs Richtlinie</span><span class="sxs-lookup"><span data-stu-id="9aaa9-129">Configuring the Software Restriction Policy</span></span>](configuring-the-software-restriction-policy.md)
</dt> <dt>

[<span data-ttu-id="9aaa9-130">Aktivieren der Authentifizierung für eine Bibliotheks Anwendung</span><span class="sxs-lookup"><span data-stu-id="9aaa9-130">Enabling Authentication for a Library Application</span></span>](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[<span data-ttu-id="9aaa9-131">Festlegen einer Authentifizierungs Ebene für eine Server Anwendung</span><span class="sxs-lookup"><span data-stu-id="9aaa9-131">Setting an Authentication Level for a Server Application</span></span>](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 
