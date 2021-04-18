---
description: Das Ausführen dieses Schritts ermöglicht entweder Prozess Zugriffs Überprüfungen oder vollständige rollenbasierte Sicherheit, je nachdem, welche Sicherheitsstufe Sie auswählen und ob Sie die Zugriffs Überprüfung für einzelne Komponenten aktivieren.
ms.assetid: 266bdac1-41be-45a5-a8c7-f9c6fe08445c
title: Aktivieren von Zugriffs Überprüfungen für eine Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d64a32b23467f85c368e088a870ebe5e4d683e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344814"
---
# <a name="enabling-access-checks-for-an-application"></a><span data-ttu-id="74f7f-103">Aktivieren von Zugriffs Überprüfungen für eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="74f7f-103">Enabling Access Checks for an Application</span></span>

<span data-ttu-id="74f7f-104">Das Ausführen dieses Schritts ermöglicht entweder Prozess Zugriffs Überprüfungen oder vollständige rollenbasierte Sicherheit, je nachdem, welche Sicherheitsstufe Sie auswählen und ob Sie die Zugriffs Überprüfung für einzelne Komponenten aktivieren.</span><span class="sxs-lookup"><span data-stu-id="74f7f-104">Performing this step enables either process access checks or full role-based security, depending on what security level you select and whether you enable access checking for individual components.</span></span>

<span data-ttu-id="74f7f-105">**So aktivieren Sie Zugriffs Überprüfungen für eine Anwendung**</span><span class="sxs-lookup"><span data-stu-id="74f7f-105">**To enable access checks for an application**</span></span>

1.  <span data-ttu-id="74f7f-106">Klicken Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste mit der rechten Maustaste auf die COM+-Anwendung, für die Sie die Zugriffs Überprüfungen aktivieren möchten, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="74f7f-106">In the console tree of the Component Services administrative tool, right-click the COM+ application for which you want to enable access checks, and then click **Properties**.</span></span>

2.  <span data-ttu-id="74f7f-107">Klicken Sie im Dialogfeld Anwendungseigenschaften auf die Registerkarte **Sicherheit** .</span><span class="sxs-lookup"><span data-stu-id="74f7f-107">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="74f7f-108">Aktivieren Sie das Kontrollkästchen **Zugriffs Überprüfungen für diese Anwendung erzwingen** .</span><span class="sxs-lookup"><span data-stu-id="74f7f-108">Select the **Enforce access checks for this application** check box.</span></span>

4.  <span data-ttu-id="74f7f-109">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="74f7f-109">Click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="74f7f-110">Ab Windows Server 2003 sind Zugriffs Überprüfungen beim Erstellen einer COM+-Anwendung standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="74f7f-110">As of Windows Server 2003, access checks are enabled by default when creating a COM+ application.</span></span> <span data-ttu-id="74f7f-111">Zugriffs Überprüfungen werden standardmäßig auf Anwendungsebene aktiviert und auf Komponentenebene standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="74f7f-111">Access checks are enabled by default at the application level and disabled by default at the component level.</span></span> <span data-ttu-id="74f7f-112">Zuvor waren Zugriffs Überprüfungen standardmäßig auf Anwendungsebene deaktiviert und auf Komponentenebene standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="74f7f-112">Previously, access checks were disabled by default at the application level and enabled by default at the component level.</span></span>

 

<span data-ttu-id="74f7f-113">Nachdem Sie die Zugriffs Überprüfungen aktiviert haben, sollten Sie die entsprechende Sicherheitsstufe auswählen.</span><span class="sxs-lookup"><span data-stu-id="74f7f-113">After enabling access checks, you should select the appropriate security level.</span></span> <span data-ttu-id="74f7f-114">Weitere Informationen finden Sie unter [Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="74f7f-114">See [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span> <span data-ttu-id="74f7f-115">Außerdem müssen Sie sicherstellen, dass Sie Rollen definieren und Sie der Anwendung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="74f7f-115">Also, you must be sure to define roles and add them to the application.</span></span> <span data-ttu-id="74f7f-116">Wenn Zugriffs Überprüfungen aktiviert sind, aber keine Rollen hinzugefügt wurden, schlagen alle Aufrufe der Anwendung fehl.</span><span class="sxs-lookup"><span data-stu-id="74f7f-116">If access checks are enabled but no roles have been added, all calls to the application will fail.</span></span> <span data-ttu-id="74f7f-117">Weitere Informationen finden Sie unter [Definieren von Rollen für eine Anwendung](defining-roles-for-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="74f7f-117">See [Defining Roles for an Application](defining-roles-for-an-application.md).</span></span>

> [!Note]  
> <span data-ttu-id="74f7f-118">Beim Debuggen Ihrer Anwendung ist es möglicherweise hilfreich, die Sicherheit zu deaktivieren, sodass Sie sich auf andere Aspekte des Verhaltens und Entwurfs des Programms konzentrieren können.</span><span class="sxs-lookup"><span data-stu-id="74f7f-118">When debugging your application, it might be helpful to disable security so that you can concentrate on other aspects of your program's behavior and design.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="74f7f-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="74f7f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74f7f-120">Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden</span><span class="sxs-lookup"><span data-stu-id="74f7f-120">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="74f7f-121">Konfigurieren von Role-Based Sicherheit</span><span class="sxs-lookup"><span data-stu-id="74f7f-121">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="74f7f-122">Definieren von Rollen für eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="74f7f-122">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="74f7f-123">Aktivieren von Zugriffs Überprüfungen auf Komponentenebene</span><span class="sxs-lookup"><span data-stu-id="74f7f-123">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[<span data-ttu-id="74f7f-124">Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen</span><span class="sxs-lookup"><span data-stu-id="74f7f-124">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



