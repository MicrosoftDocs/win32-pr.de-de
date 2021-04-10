---
description: Konfigurieren der Software Einschränkungs Richtlinie
ms.assetid: 22c1897a-abb5-4ce9-9d09-21b6aed4f1d8
title: Konfigurieren der Software Einschränkungs Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522f216af6957ebd23bc9f17c70f61cab2cabc5c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041505"
---
# <a name="configuring-the-software-restriction-policy"></a><span data-ttu-id="995a9-103">Konfigurieren der Software Einschränkungs Richtlinie</span><span class="sxs-lookup"><span data-stu-id="995a9-103">Configuring the Software Restriction Policy</span></span>

<span data-ttu-id="995a9-104">Wenn Sie die Vertrauens Ebenen der Software Einschränkungs Richtlinie in einer COM+-Anwendung explizit festlegen, überschreiben Sie die standardmäßigen systemweiten-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="995a9-104">When you explicitly set the software restriction policy trust levels of a COM+ application, you are overriding the default systemwide settings.</span></span> <span data-ttu-id="995a9-105">Dies ist häufig für com+-Server Anwendungen erforderlich, da die systemweite Vertrauens Ebene für alle Server Anwendungen identisch ist (da Sie alle in derselben Datei ausgeführt werden, dllhost.exe).</span><span class="sxs-lookup"><span data-stu-id="995a9-105">This is often necessary for COM+ server applications because the systemwide trust level is set the same for all server applications (because they all run in the same file, dllhost.exe).</span></span> <span data-ttu-id="995a9-106">Wenn Sie jedoch die Vertrauens Ebene der Software Einschränkungs Richtlinie einer COM+-Bibliotheks Anwendung festlegen, wirkt sich dies auf die systemweite Konfiguration für diese Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="995a9-106">However, when you set the software restriction policy trust level of a COM+ library application, you are affecting the systemwide configuration for that application.</span></span> <span data-ttu-id="995a9-107">Eine Erläuterung zur Verwendung der Software Einschränkungs Richtlinie in com+ finden [Sie unter Verwenden der Software Einschränkungs Richtlinie in com+](using-the-software-restriction-policy-in-com-.md).</span><span class="sxs-lookup"><span data-stu-id="995a9-107">For a discussion of how to use the software restriction policy in COM+, see [Using the Software Restriction Policy in COM+](using-the-software-restriction-policy-in-com-.md).</span></span>

<span data-ttu-id="995a9-108">**So legen Sie die Software Einschränkungs Richtlinie fest**</span><span class="sxs-lookup"><span data-stu-id="995a9-108">**To set the software restriction policy**</span></span>

1.  <span data-ttu-id="995a9-109">Klicken Sie mit der rechten Maustaste auf die COM+-Anwendung, für die Sie die Software Einschränkungs Richtlinie festlegen, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="995a9-109">Right-click the COM+ application for which you are setting the software restriction policy, and then click **Properties**.</span></span>

2.  <span data-ttu-id="995a9-110">Klicken Sie im Dialogfeld Anwendungseigenschaften auf die Registerkarte **Sicherheit** .</span><span class="sxs-lookup"><span data-stu-id="995a9-110">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="995a9-111">Aktivieren Sie unter **Software Einschränkungs Richtlinie** das Kontrollkästchen **Software Einschränkungs Richtlinie anwenden** . Dies ermöglicht es Ihnen, die Vertrauens Ebene festzulegen.</span><span class="sxs-lookup"><span data-stu-id="995a9-111">Under **Software Restriction Policy**, select the **Apply software restriction policy** check box; this enables you to set the trust level.</span></span> <span data-ttu-id="995a9-112">Das Deaktivieren des Kontrollkästchens bewirkt, dass com+ die systemweite Konfiguration der Software Einschränkungs Richtlinie für die Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="995a9-112">Clearing the check box will cause COM+ to use the systemwide configuration of the software restriction policy for the application.</span></span> <span data-ttu-id="995a9-113">Dieses Kontrollkästchen entspricht der srpabled-Eigenschaft der [**Applications**](applications.md) -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="995a9-113">This check box corresponds to the SRPEnabled property of the [**Applications**](applications.md) collection.</span></span>

4.  <span data-ttu-id="995a9-114">Wählen Sie im Feld **Einschränkungs Ebene** die geeignete Ebene aus.</span><span class="sxs-lookup"><span data-stu-id="995a9-114">In the **Restriction Level** box, select the appropriate level.</span></span> <span data-ttu-id="995a9-115">Dieses Dropdown Feld entspricht der SRPTrustLevel-Eigenschaft der [**Applications**](applications.md) -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="995a9-115">This drop-down box corresponds to the SRPTrustLevel property of the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="995a9-116">Die folgenden Ebenen sind von der niedrigsten zum vertrauenswürdigsten:</span><span class="sxs-lookup"><span data-stu-id="995a9-116">The levels are as follows, ordered from least to most trusted:</span></span>

    -   <span data-ttu-id="995a9-117">Nicht **zulässig**.</span><span class="sxs-lookup"><span data-stu-id="995a9-117">**Disallowed**.</span></span> <span data-ttu-id="995a9-118">Die Anwendung ist nicht berechtigt, die vollständigen Berechtigungen des Benutzers zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="995a9-118">The application is disallowed from using the full privileges of the user.</span></span> <span data-ttu-id="995a9-119">Komponenten mit Vertrauens Ebene können darin geladen werden.</span><span class="sxs-lookup"><span data-stu-id="995a9-119">Components with any trust level can be loaded into it.</span></span>
    -   <span data-ttu-id="995a9-120">**Uneingeschränkt**.</span><span class="sxs-lookup"><span data-stu-id="995a9-120">**Unrestricted**.</span></span> <span data-ttu-id="995a9-121">Die Anwendung hat uneingeschränkten Zugriff auf die Berechtigungen des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="995a9-121">The application has unrestricted access to the user's privileges.</span></span> <span data-ttu-id="995a9-122">Es können nur Komponenten mit einer uneingeschränkten Vertrauens Ebene in diese geladen werden.</span><span class="sxs-lookup"><span data-stu-id="995a9-122">Only components with an Unrestricted trust level can be loaded into it.</span></span>

5.  <span data-ttu-id="995a9-123">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="995a9-123">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="995a9-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="995a9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="995a9-125">Konfigurieren von Role-Based Sicherheit</span><span class="sxs-lookup"><span data-stu-id="995a9-125">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="995a9-126">Aktivieren der Authentifizierung für eine Bibliotheks Anwendung</span><span class="sxs-lookup"><span data-stu-id="995a9-126">Enabling Authentication for a Library Application</span></span>](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[<span data-ttu-id="995a9-127">Festlegen einer Authentifizierungs Ebene für eine Server Anwendung</span><span class="sxs-lookup"><span data-stu-id="995a9-127">Setting an Authentication Level for a Server Application</span></span>](setting-an-authentication-level-for-a-server-application.md)
</dt> <dt>

[<span data-ttu-id="995a9-128">Festlegen einer Identitätswechsel Ebene</span><span class="sxs-lookup"><span data-stu-id="995a9-128">Setting an Impersonation Level</span></span>](setting-an-impersonation-level.md)
</dt> </dl>

 

 



