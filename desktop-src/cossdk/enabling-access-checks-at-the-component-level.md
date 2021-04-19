---
description: Aktivieren von Zugriffs Überprüfungen auf Komponentenebene
ms.assetid: b9ff5296-9076-4492-833c-7402b7090f8f
title: Aktivieren von Zugriffs Überprüfungen auf Komponentenebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5da2de5f9d2f4f2d39f43330c8320c0bb0218bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342982"
---
# <a name="enabling-access-checks-at-the-component-level"></a><span data-ttu-id="e86db-103">Aktivieren von Zugriffs Überprüfungen auf Komponentenebene</span><span class="sxs-lookup"><span data-stu-id="e86db-103">Enabling Access Checks at the Component Level</span></span>

<span data-ttu-id="e86db-104">Wenn Ihre Anwendung eine Komponente enthält, die keine Sicherheitsüberprüfungen benötigt, können Sie die Rollen Überprüfung für diese Komponente deaktivieren, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="e86db-104">If your application includes a component that does not need security checks, you might decide to disable role checks for that component to improve performance.</span></span> <span data-ttu-id="e86db-105">Oder beim Debuggen ist es möglicherweise hilfreich, die Sicherheit zu deaktivieren, sodass Sie sich auf andere Aspekte der Programmfunktionalität konzentrieren können.</span><span class="sxs-lookup"><span data-stu-id="e86db-105">Or when debugging, it might be helpful to disable security so that you can concentrate on other aspects of program functionality.</span></span>

<span data-ttu-id="e86db-106">Wenn Sie eine Komponente installieren, werden standardmäßig Zugriffs Überprüfungen auf Komponentenebene aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e86db-106">By default, when you install a component, component-level access checks are enabled.</span></span> <span data-ttu-id="e86db-107">Dies wird jedoch nur wirksam, wenn [Zugriffs Überprüfungen auf Anwendungsebene](enabling-access-checks-for-an-application.md) aktiviert sind und die [Sicherheitsstufe](setting-a-security-level-for-access-checks.md) festgelegt ist, um **Zugriffs Überprüfungen auf Prozess-und Komponentenebene durchzuführen**.</span><span class="sxs-lookup"><span data-stu-id="e86db-107">However, this takes effect only when [application-level access checks](enabling-access-checks-for-an-application.md) are enabled and when the [security level](setting-a-security-level-for-access-checks.md) is set to **Perform access checks at the process and component level**.</span></span>

<span data-ttu-id="e86db-108">**So aktivieren oder deaktivieren Sie Zugriffs Überprüfungen auf Komponentenebene**</span><span class="sxs-lookup"><span data-stu-id="e86db-108">**To enable or disable access checks at the component level**</span></span>

1.  <span data-ttu-id="e86db-109">Suchen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste die COM+-Anwendung, die die Komponente enthält, für die Sie Rollen Überprüfungen deaktivieren (oder aktivieren) möchten.</span><span class="sxs-lookup"><span data-stu-id="e86db-109">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the component for which you want to disable (or enable) role checks.</span></span> <span data-ttu-id="e86db-110">Erweitern Sie die Ansicht in der Struktur, um die Komponenten im Ordner **Komponenten** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e86db-110">Expand the view in the tree to view the components in the **Components** folder.</span></span>

2.  <span data-ttu-id="e86db-111">Klicken Sie mit der rechten Maustaste auf die Komponente, für die Sie Rollen Überprüfungen aktivieren möchten, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="e86db-111">Right-click the component for which you want to enable role checks, and then click **Properties**.</span></span>

3.  <span data-ttu-id="e86db-112">Klicken Sie im Dialogfeld Komponenteneigenschaften auf die Registerkarte **Sicherheit** .</span><span class="sxs-lookup"><span data-stu-id="e86db-112">In the component properties dialog box, click the **Security** tab.</span></span>

4.  <span data-ttu-id="e86db-113">Wählen Sie **Zugriffs Überprüfungen auf Komponentenebene erzwingen** , um Überprüfungen auf Komponentenebene zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="e86db-113">Select **Enforce component level access checks** to enforce component-level checks.</span></span>

5.  <span data-ttu-id="e86db-114">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e86db-114">Click **OK**.</span></span>

<span data-ttu-id="e86db-115">Die neue Einstellung wird wirksam, wenn die Anwendung das nächste Mal gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e86db-115">The new setting will take effect the next time the application is started.</span></span>

> [!Note]  
> <span data-ttu-id="e86db-116">Ab Windows Server 2003 sind Zugriffs Überprüfungen auf Komponentenebene beim Erstellen einer COM+-Anwendung standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e86db-116">As of Windows Server 2003, component-level access checks are disabled by default when creating a COM+ application.</span></span> <span data-ttu-id="e86db-117">Zugriffs Überprüfungen werden standardmäßig auf Anwendungsebene aktiviert und auf Komponentenebene standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e86db-117">Access checks are enabled by default at the application level and disabled by default at the component level.</span></span> <span data-ttu-id="e86db-118">Zuvor waren Zugriffs Überprüfungen standardmäßig auf Anwendungsebene deaktiviert und auf Komponentenebene standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e86db-118">Previously, access checks were disabled by default at the application level and enabled by default at the component level.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e86db-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e86db-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e86db-120">Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden</span><span class="sxs-lookup"><span data-stu-id="e86db-120">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="e86db-121">Konfigurieren von Role-Based Sicherheit</span><span class="sxs-lookup"><span data-stu-id="e86db-121">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="e86db-122">Definieren von Rollen für eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="e86db-122">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="e86db-123">Aktivieren von Zugriffs Überprüfungen für eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="e86db-123">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="e86db-124">Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen</span><span class="sxs-lookup"><span data-stu-id="e86db-124">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



