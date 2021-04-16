---
description: In diesem Beispiel wird gezeigt, wie Sie eine verwaltete Tablet PC-Anwendung über das Internet mithilfe der No-Touchscreen-Bereitstellung bereitstellen.
ms.assetid: d226bd67-e20d-431b-b0c3-9361b00a9340
title: No-Touch Bereitstellungs-webbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0742deef8ea9b418fba6de4724975ee27693f8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104530443"
---
# <a name="no-touch-deployment-web-sample"></a><span data-ttu-id="9686a-103">No-Touch Bereitstellungs-webbeispiel</span><span class="sxs-lookup"><span data-stu-id="9686a-103">No-Touch Deployment Web Sample</span></span>

<span data-ttu-id="9686a-104">In diesem Beispiel wird gezeigt, wie Sie eine verwaltete Tablet PC-Anwendung über das Internet mithilfe der No-Touchscreen-Bereitstellung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9686a-104">This sample shows how to deploy a managed Tablet PC application over the Web by using no-touch deployment.</span></span> <span data-ttu-id="9686a-105">Sie sollten sich mit den Konzepten vertraut machen, die in [der .NET Framework bereit](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp)gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9686a-105">You should be familiar with the concepts discussed in [No-Touch Deployment in the .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp).</span></span> <span data-ttu-id="9686a-106">Auf dem Computer muss Microsoft Internetinformationsdienste (IIS) installiert sein, um dieses Beispiel ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="9686a-106">Your computer must have Microsoft Internet Information Services (IIS) installed to run this sample.</span></span>

## <a name="overview"></a><span data-ttu-id="9686a-107">Übersicht</span><span class="sxs-lookup"><span data-stu-id="9686a-107">Overview</span></span>

<span data-ttu-id="9686a-108">Bei der Bereitstellung ohne Fingereingabe können Tablet PCWindows Forms-Anwendungen-Desktop Anwendungen, die mithilfe der Klassen im System. Windows. Forms-Namespace von Microsoft .NET Framework und Microsoft Windows XP Tablet PC Edition Development Kit 1,7 erstellt wurden, heruntergeladen, installiert und direkt auf den Computern der Benutzer ausgeführt werden, ohne dass die Registrierung oder die freigegebenen System Komponenten geändert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="9686a-108">With no-touch deployment, Tablet PCWindows Forms applications-desktop applications built by using the classes in the System.Windows.Forms namespace of the Microsoft .NET Framework and the Microsoft Windows XP Tablet PC Edition Development Kit 1.7-can be downloaded, installed, and run directly on users' computers without any alteration of the registry or shared system components.</span></span>

<span data-ttu-id="9686a-109">In diesem Beispiel wird das ursprüngliche Projekt für das [Formular Beispiel "Automatische Ansprüche](auto-claims-form-sample.md)", "autoclaims" und ein Installer-Projekt, "autoclaims \_ notouchweb", bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9686a-109">This sample takes the original project for [Auto Claims Form Sample](auto-claims-form-sample.md), AutoClaims, and provides an installer project, AutoClaims\_NoTouchWeb.</span></span> <span data-ttu-id="9686a-110">Nachdem Sie kompiliert und ausgeführt wurden, erstellt das Installer-Projekt ein neues virtuelles Stammverzeichnis, das auch autoclaims \_ notouchweb genannt wird.</span><span class="sxs-lookup"><span data-stu-id="9686a-110">Once compiled and run, the installer project creates a new virtual root, also called AutoClaims\_NoTouchWeb.</span></span> <span data-ttu-id="9686a-111">Das Installationsprogramm kopiert eine Datei default.htm, die einen Link zur AutoClaims.exe Assembly enthält.</span><span class="sxs-lookup"><span data-stu-id="9686a-111">The installer copies a file, default.htm, that includes a link to the AutoClaims.exe assembly.</span></span> <span data-ttu-id="9686a-112">Navigieren Sie zum Starten der Rich Client-Anwendung mit Microsoft Internet Explorer zum virtuellen Stammverzeichnis, und klicken Sie dann auf der Seite default.htm auf den Link.</span><span class="sxs-lookup"><span data-stu-id="9686a-112">To launch the rich client application, navigate to the virtual root with Microsoft Internet Explorer, and then click the link in the default.htm page.</span></span>

> [!Note]  
> <span data-ttu-id="9686a-113">Zum virtuellen Stammverzeichnis müssen Sie IIS (z. b. https://localhost/AutoClaims\_NoTouchWeb/default.htm) und nicht direkt über das Dateisystem) navigieren, damit die Anwendung in der Internet Explorer-Anwendungsdomäne funktioniert.</span><span class="sxs-lookup"><span data-stu-id="9686a-113">You must navigate to the virtual root by way of IIS (for example, https://localhost/AutoClaims\_NoTouchWeb/default.htm) and not directly through the file system in order for the application to work in the Internet Explorer application domain.</span></span>

 


```C++
<html>
    <head>
        <title>AutoClaims (No Touch Web)</title>
      </head>
      <body>
          <a href="AutoClaims.exe">Launch AutoClaims Sample</a>
      </body>
</html>
```



## <a name="no-touch-deployment-requirements"></a><span data-ttu-id="9686a-114">No-Touch Bereitstellungs Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9686a-114">No-Touch Deployment Requirements</span></span>

<span data-ttu-id="9686a-115">Alle abhängigen Assemblys müssen sich entweder im Assemblysuchpfad oder im Stammverzeichnis des virtuellen Verzeichnisses der Website befinden.</span><span class="sxs-lookup"><span data-stu-id="9686a-115">All dependent assemblies must be located either in the assembly search path or the root of the virtual directory of the Web site.</span></span> <span data-ttu-id="9686a-116">Das \_ Bereitstellungs Projekt "autoclaims notouchweb" installiert die Assembly und die verweisende Seite (default.htm) im selben virtuellen Stammverzeichnis (autoclaims \_ notouchweb).</span><span class="sxs-lookup"><span data-stu-id="9686a-116">The AutoClaims\_NoTouchWeb deployment project installs the assembly and the referring page, default.htm, into the same virtual root (AutoClaims\_NoTouchWeb).</span></span>

> [!Note]  
> <span data-ttu-id="9686a-117">Die kompilierten webbeispiele werden von der Standard Installationsoption für das SDK nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="9686a-117">The compiled web samples are not installed by the default installation option for the SDK.</span></span> <span data-ttu-id="9686a-118">Sie müssen eine benutzerdefinierte Installation durchführen und die unter Option "vorkompilierte webbeispiele" auswählen, um Sie zu installieren.</span><span class="sxs-lookup"><span data-stu-id="9686a-118">You must complete a custom installation and select the "Pre-compiled Web Samples" sub-option to install them.</span></span>

 

<span data-ttu-id="9686a-119">Weitere Informationen zur Verwendung von frei Hand Eingaben im Web finden Sie unter frei Hand Eingaben [im Web](ink-on-the-web.md).</span><span class="sxs-lookup"><span data-stu-id="9686a-119">For more information about using ink on the Web, see [Ink on the Web](ink-on-the-web.md).</span></span>

 

 