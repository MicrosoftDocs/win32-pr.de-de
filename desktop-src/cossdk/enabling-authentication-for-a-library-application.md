---
description: Aktivieren der Authentifizierung für eine Bibliotheks Anwendung
ms.assetid: 80c80c14-ceef-4a74-810d-6aa3cc320cef
title: Aktivieren der Authentifizierung für eine Bibliotheks Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cfa9f2a6a5e3c1312fa13e0aff1e9f4ea17e4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346029"
---
# <a name="enabling-authentication-for-a-library-application"></a><span data-ttu-id="1afc9-103">Aktivieren der Authentifizierung für eine Bibliotheks Anwendung</span><span class="sxs-lookup"><span data-stu-id="1afc9-103">Enabling Authentication for a Library Application</span></span>

<span data-ttu-id="1afc9-104">Da com+-Bibliotheksanwendungen von anderen Prozessen gehostet werden, unterscheiden sich die Sicherheitsanforderungen möglicherweise von denen der Server Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="1afc9-104">Because COM+ library applications are hosted by other processes, their security requirements may be different from those of server applications.</span></span> <span data-ttu-id="1afc9-105">Wenn die Bibliotheks Anwendung von einem Browser gehostet wird, muss Sie möglicherweise nicht authentifizierte Rückrufe empfangen.</span><span class="sxs-lookup"><span data-stu-id="1afc9-105">If the library application will be hosted by a browser, it might need to receive unauthenticated callbacks.</span></span>

<span data-ttu-id="1afc9-106">Um diese Anforderung zu erfüllen, können Sie die Authentifizierung deaktivieren, sodass der Hostingprozess keine Sicherheitsüberprüfungen für Aufrufer der Bibliotheks Anwendung ausführt.</span><span class="sxs-lookup"><span data-stu-id="1afc9-106">To address this need, you can disable authentication so that the hosting process does not perform security checks for callers of the library application.</span></span> <span data-ttu-id="1afc9-107">Wenn Sie die Authentifizierung deaktivieren, werden Aufrufe der Bibliotheks Anwendung nicht authentifiziert – alle Aufrufe an diese werden erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1afc9-107">When you disable authentication, calls to the library application effectively go unauthenticated—all calls to it will succeed.</span></span> <span data-ttu-id="1afc9-108">Weitere Informationen finden Sie unter [Bibliotheks Anwendungssicherheit](library-application-security.md).</span><span class="sxs-lookup"><span data-stu-id="1afc9-108">For more information, see [Library Application Security](library-application-security.md).</span></span>

<span data-ttu-id="1afc9-109">**So aktivieren (oder deaktivieren) Sie die Authentifizierung für eine Bibliotheks Anwendung**</span><span class="sxs-lookup"><span data-stu-id="1afc9-109">**To enable (or disable) authentication for a library application**</span></span>

1.  <span data-ttu-id="1afc9-110">Klicken Sie mit der rechten Maustaste auf die COM+-Anwendung, für die Sie die Authentifizierung aktivieren bzw. deaktivieren, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="1afc9-110">Right-click the COM+ application for which you are enabling or disabling authentication, and then click **Properties**.</span></span>

2.  <span data-ttu-id="1afc9-111">Klicken Sie im Dialogfeld Anwendungseigenschaften auf die Registerkarte **Sicherheit** .</span><span class="sxs-lookup"><span data-stu-id="1afc9-111">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="1afc9-112">Aktivieren Sie unter **Authentifizierung** das Kontrollkästchen **Authentifizierung aktivieren** , um die Authentifizierung zu aktivieren. durch Deaktivieren des Kontrollkästchens wird die Authentifizierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1afc9-112">Under **Authentication**, select the **Enable authentication** check box to enable authentication; clearing the check box will disable authentication.</span></span>

4.  <span data-ttu-id="1afc9-113">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="1afc9-113">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1afc9-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1afc9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1afc9-115">Festlegen einer Authentifizierungs Ebene für eine Server Anwendung</span><span class="sxs-lookup"><span data-stu-id="1afc9-115">Setting an Authentication Level for a Server Application</span></span>](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 



