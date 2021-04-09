---
title: Dateityp und URI-Zuordnungs Modell
description: Dateityp und URI-Zuordnungs Modell
ms.assetid: 4DE7DD08-088A-4E09-B1C7-AE9033EA533D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c78540a072405aade01a9f94503999ad105d2078
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104039744"
---
# <a name="file-type-and-uri-associations-model"></a><span data-ttu-id="70a16-103">Dateityp und URI-Zuordnungs Modell</span><span class="sxs-lookup"><span data-stu-id="70a16-103">File type and URI associations model</span></span>

## <a name="platforms"></a><span data-ttu-id="70a16-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="70a16-104">Platforms</span></span>

 <span data-ttu-id="70a16-105">**Clients** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="70a16-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="70a16-106">**Server** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="70a16-106">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="70a16-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70a16-107">Description</span></span>

<span data-ttu-id="70a16-108">Der Dateityp und das URI-Zuordnungs Modell wurden in Windows 8 geändert.</span><span class="sxs-lookup"><span data-stu-id="70a16-108">The file type and URI association model has changed in Windows 8.</span></span> <span data-ttu-id="70a16-109">Apps können nicht mehr Programm gesteuert als Standard Handler für einen Dateityp oder URI festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="70a16-109">Apps are no longer able to programmatically set themselves as the default handler for a file type or URI.</span></span> <span data-ttu-id="70a16-110">Stattdessen steuert der Benutzer nun immer, was der Standard Handler für einen Dateityp oder ein URI-Schema ist.</span><span class="sxs-lookup"><span data-stu-id="70a16-110">Instead, now the user always controls what the default handler is for a file type or URI scheme.</span></span>

## <a name="manifestation"></a><span data-ttu-id="70a16-111">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="70a16-111">Manifestation</span></span>

<span data-ttu-id="70a16-112">Welche Auswirkungen diese Änderung auf den Benutzer hat, hängt davon ab, wie die APP entworfen wurde, z. b.:</span><span class="sxs-lookup"><span data-stu-id="70a16-112">How this change presents to the user depends upon how the app is designed, for example:</span></span>

-   <span data-ttu-id="70a16-113">Viele apps überprüfen, ob Sie bei jedem Ausführen der Standardeinstellung sind. wenn dies nicht der Fall ist, wird der Benutzer aufgefordert, Sie als Standard festzulegen.</span><span class="sxs-lookup"><span data-stu-id="70a16-113">Many apps check to see if they are the default every time they run and, if they are not, they prompt the user to set them as default.</span></span> <span data-ttu-id="70a16-114">Da apps jedoch nicht mehr genau Abfragen können, um zu bestimmen, welche App der Standard Handler für einen Dateityp oder ein URI-Schema ist, funktioniert keiner dieser Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="70a16-114">However, because apps can no longer accurately query to determine which app is the default handler for a file type or URI scheme, neither of these operations works.</span></span>
-   <span data-ttu-id="70a16-115">Viele apps verfügen über ein Dialogfeld oder ein Menü, das bzw. das in das Installationsprogramm integriert ist, das die Dateitypen angibt, für die die APP als Standard fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="70a16-115">Many apps have a dialog box or menu built in or in their installer that specifies the file types for which the app should serve as the default.</span></span> <span data-ttu-id="70a16-116">Da apps jedoch nicht mehr Programm gesteuert als Standard Handler für einen Dateityp oder ein URI-Schema festgelegt werden können, funktioniert das nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="70a16-116">However, because apps can no longer programmatically set themselves as the default handler for a file type or URI scheme, this no longer works.</span></span>

## <a name="mitigation"></a><span data-ttu-id="70a16-117">Minderung</span><span class="sxs-lookup"><span data-stu-id="70a16-117">Mitigation</span></span>

<span data-ttu-id="70a16-118">Es gibt mehrere Möglichkeiten, wie Benutzer diese Änderungen durchführen können:</span><span class="sxs-lookup"><span data-stu-id="70a16-118">There are several things users can do to accommodate these changes:</span></span>

-   <span data-ttu-id="70a16-119">Benutzer werden dazu aufgefordert, eine Standard-App zum Verarbeiten von Dateitypen, URI-Schemas oder beides auszuwählen, wenn keine Angabe erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="70a16-119">Users are prompted contextually to choose a default app to handle file types, URI schemes, or both when one has not been specified</span></span>
-   <span data-ttu-id="70a16-120">Benutzern wird die Option angeboten, Ihren Standard Handler nach der Installation neuer apps zu ändern, die einen Dateityp oder ein URI-Schema verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="70a16-120">Users are offered the option to change their default handler after installing new apps that can handle a file type or URI scheme</span></span>
-   <span data-ttu-id="70a16-121">Mithilfe der Systemsteuerung "Standardprogramme" können Benutzer Standardwerte für eine APP festlegen, oder für einen Dateityp, ein URI-Schema oder beides. Apps können mit der Systemsteuerung verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="70a16-121">The default programs control panel allows users to set defaults for an app, or for a file type, URI scheme, or both; apps can link to the control panel</span></span>
-   <span data-ttu-id="70a16-122">Standardwerte können im Windows-Explorer geändert werden.</span><span class="sxs-lookup"><span data-stu-id="70a16-122">Defaults can be changed from Windows Explorer</span></span>

## <a name="solution"></a><span data-ttu-id="70a16-123">Lösung</span><span class="sxs-lookup"><span data-stu-id="70a16-123">Solution</span></span>

<span data-ttu-id="70a16-124">Aufgrund dieser Änderungen wird diese API-Anleitung bereitgestellt:</span><span class="sxs-lookup"><span data-stu-id="70a16-124">As a result of these changes, this API guidance is provided:</span></span>

-   <span data-ttu-id="70a16-125">Die Funktionalität einiger Methodenaufrufe innerhalb der [iapplicationassociationregistration](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) -API wurde geändert und sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70a16-125">The functionality of some method calls within the [IApplicationAssociationRegistration](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) API has changed, and should no longer be used.</span></span>

    -   <span data-ttu-id="70a16-126">Rufen **Sie nicht** [queryappisdefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) / [queryappisdefaultall](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall) auf, um zu bestimmen, ob eine APP die Standardeinstellung ist.</span><span class="sxs-lookup"><span data-stu-id="70a16-126">**Do not** call [QueryAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault)/[QueryAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall) to determine if an app is the default</span></span>
    -   <span data-ttu-id="70a16-127">" [Querycurrentdefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault) " **nicht** aufzurufen, um zu bestimmen, welche app (sofern vorhanden) der aktuelle Standardwert ist</span><span class="sxs-lookup"><span data-stu-id="70a16-127">**Do not** call [QueryCurrentDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault) to determine which app (if any) is the current default</span></span>
    -   <span data-ttu-id="70a16-128"> [Setappisdefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault) / [setappisdefaultall](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall) nicht zum Festlegen der Standard-App anrufen</span><span class="sxs-lookup"><span data-stu-id="70a16-128">**Do not** call [SetAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault)/[SetAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall) to set the default app</span></span>

-   <span data-ttu-id="70a16-129">Die Anleitung lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="70a16-129">The guidance going forward is:</span></span>

    -   <span data-ttu-id="70a16-130">**Nicht** Abfragen, um zu sehen, welche App der Standard Handler für Dateitypen oder URI-Schemas ist</span><span class="sxs-lookup"><span data-stu-id="70a16-130">**Do not** query to see which app is the default handler for file types or URI schemes</span></span>

    -   <span data-ttu-id="70a16-131">Versuchen **Sie nicht** , Änderungen im Standard Handler für Dateitypen oder URI-Schemas zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="70a16-131">**Do not** attempt to monitor changes in the default handler for file types or URI schemes</span></span>

    -   <span data-ttu-id="70a16-132">Versuchen **Sie nicht** , eine App als Standard Handler für Dateitypen oder URI-Schemas festzulegen.</span><span class="sxs-lookup"><span data-stu-id="70a16-132">**Do not** attempt to set an app as the default handler for file types or URI schemes</span></span>

    -   <span data-ttu-id="70a16-133">Versuchen **Sie nicht** , Standardwerte für Dateitypen oder URI-Schemas innerhalb einer APP zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="70a16-133">**Do not** attempt to manage defaults for file types or URI schemes from within an app</span></span>

    -   <span data-ttu-id="70a16-134">**Verwenden** Sie die Systemsteuerung " [Standardprogramme festlegen](../shell/default-programs.md) ", wenn Sie Benutzern Ihrer APP den Zugriff auf die standardmäßige Verwaltungs Benutzeroberfläche gestatten möchten (die Verwaltungs Benutzeroberfläche innerhalb der APP wird nicht mehr unterstützt).</span><span class="sxs-lookup"><span data-stu-id="70a16-134">**Do** integrate with the [Set Default Programs](../shell/default-programs.md) control panel if you want to allow users of your app to access the default management UI (the management UI within the app is no longer supported)</span></span>

        -   <span data-ttu-id="70a16-135">Durch Aufrufen von [iapplicationassociationregistrationui:: launchadvancedassociationui](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) kann der Benutzer auf die System Steuerungs Seite "[Standardprogramme festlegen](../shell/default-programs.md)" für die angegebene App zugreifen.</span><span class="sxs-lookup"><span data-stu-id="70a16-135">Calling [IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) allows the user to access the ‘[Set Default Programs](../shell/default-programs.md)’ control panel page for the specified app</span></span>

## <a name="tests"></a><span data-ttu-id="70a16-136">Tests</span><span class="sxs-lookup"><span data-stu-id="70a16-136">Tests</span></span>

-   <span data-ttu-id="70a16-137">Testen Sie, ob apps ordnungsgemäß in der Systemsteuerung "Standardprogramme festlegen" registriert sind.</span><span class="sxs-lookup"><span data-stu-id="70a16-137">Test to verify that apps register properly in Set Default Programs control panel</span></span>
-   <span data-ttu-id="70a16-138">Testen Sie, ob apps ordnungsgemäß registriert werden, damit Sie in der openWith-Liste für die Dateitypen, URI-Schemas oder beides angezeigt werden, die Sie für die Behandlung von</span><span class="sxs-lookup"><span data-stu-id="70a16-138">Test to verify that apps register properly to appear in the OpenWith list for the file types, URI schemes, or both, that they register to handle</span></span>
-   <span data-ttu-id="70a16-139">Testen Sie, ob nach der Installation der APP neue APP-Benachrichtigungen angezeigt werden und der Benutzer einen Dateityp, ein URI-Schema oder beides aufruft, das Ihre APP für die Verarbeitung registriert hat.</span><span class="sxs-lookup"><span data-stu-id="70a16-139">Test to verify that new app notifications appear after your app is installed and the user invokes a file type, URI scheme, or both, that your app has registered to handle</span></span>

## <a name="resources"></a><span data-ttu-id="70a16-140">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="70a16-140">Resources</span></span>

-   <span data-ttu-id="70a16-141">[Bewährte Methoden für Dateityp-und URI-Zuordnungen in Windows 8-Desktop-Apps](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="70a16-141">[Best Practices for File Type and URI Associations in Windows 8 Desktop Apps](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))</span></span>
-   [<span data-ttu-id="70a16-142">Dateityp Zuordnungen und Präsentation der buildkonferenz</span><span class="sxs-lookup"><span data-stu-id="70a16-142">File Type Associations and AutoPlay Build Conference Presentation</span></span>](https://channel9.msdn.com/events/BUILD/BUILD2011/PLAT-282T)

 

 