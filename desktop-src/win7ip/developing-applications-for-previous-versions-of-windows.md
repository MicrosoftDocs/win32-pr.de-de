---
title: Entwickeln von Anwendungen für frühere Versionen von Windows
description: Erläutert, was Sie tun müssen, um Anwendungen zu entwickeln, die unter früheren Versionen von Windows ausgeführt werden, und die API zu nutzen, die mit dem Platt Form Update für Windows Vista und dem Platt Form Update für Windows Server 2008 unterstützt wird.
ms.assetid: 9c46f894-e5cd-46a1-81c8-f63b09504735
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299d4c61b0e2b931c3833934c843bf964fc3fa7c
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104393890"
---
# <a name="developing-applications-for-previous-versions-of-windows"></a><span data-ttu-id="58d87-103">Entwickeln von Anwendungen für frühere Versionen von Windows</span><span class="sxs-lookup"><span data-stu-id="58d87-103">Developing Applications for Previous Versions of Windows</span></span>

<span data-ttu-id="58d87-104">Erläutert, was Sie tun müssen, um Anwendungen zu entwickeln, die unter früheren Versionen von Windows ausgeführt werden, und die API zu nutzen, die mit dem Platt Form Update für Windows Vista und dem Platt Form Update für Windows Server 2008 unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="58d87-104">Explains what to do to develop applications that run on previous versions of Windows and take advantage of the API that are supported with the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

## <a name="required-downloads"></a><span data-ttu-id="58d87-105">Erforderliche Downloads</span><span class="sxs-lookup"><span data-stu-id="58d87-105">Required Downloads</span></span>

<span data-ttu-id="58d87-106">Das herunterladen und Installieren der in den folgenden Abschnitten beschriebenen Pakete ist erforderlich, wenn Sie Anwendungen entwickeln möchten, die API verwenden, die mit dem Microsoft Windows Software Development Kit (SDK) für Windows 7 eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="58d87-106">Download and installation of the packages described in the following sections is required if you want to develop applications that use API that are introduced with the Microsoft Windows Software Development Kit (SDK) for Windows 7.</span></span>

### <a name="microsoft-windows-sdk"></a><span data-ttu-id="58d87-107">Microsoft Windows SDK</span><span class="sxs-lookup"><span data-stu-id="58d87-107">Microsoft Windows SDK</span></span>

<span data-ttu-id="58d87-108">Die Windows SDK für Windows 7 ist erforderlich, um Anwendungen zu erstellen, die APIs verwenden, die mit dem Platt Form Update für Windows Vista unterstützt werden, und das Platt Form Update für Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="58d87-108">The Windows SDK for Windows 7 is required for creating applications that use APIs supported with the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

<span data-ttu-id="58d87-109">Informationen zum Zugriff auf Weitere Ressourcen und Informationen, z. b. Downloads, Forumsbeiträge und den Windows SDK Teamblog, finden Sie im [Windows SDK Developer Center](https://msdn.microsoft.com/bb980924.aspx) ( https://msdn.microsoft.com/bb980924.aspx) .</span><span class="sxs-lookup"><span data-stu-id="58d87-109">For access to additional resources and information, such as downloads, forum posts, and the Windows SDK team blog, see the [Windows SDK Developer Center](https://msdn.microsoft.com/bb980924.aspx) (https://msdn.microsoft.com/bb980924.aspx).</span></span>

### <a name="net-framework"></a><span data-ttu-id="58d87-110">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="58d87-110">.NET Framework</span></span>

<span data-ttu-id="58d87-111">Das .NET Framework 3,5 Service Pack 1 ist erforderlich, um Anwendungen zu erstellen, die APIs verwenden, die vom Platt Form Update für Windows Vista unterstützt werden, und das Platt Form Update für Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="58d87-111">The .NET Framework 3.5 Service Pack 1 is required for creating applications that use APIs supported by the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

<span data-ttu-id="58d87-112">Weitere Ressourcen und Informationen finden Sie im [.NET Framework Developer Center](https://msdn.microsoft.com/netframework/default.aspx) () https://msdn.microsoft.com/netframework/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="58d87-112">For additional resources and information, see the [.NET Framework Developer Center](https://msdn.microsoft.com/netframework/default.aspx) (https://msdn.microsoft.com/netframework/default.aspx).</span></span>

### <a name="directx-sdk-required-when-using-direct3d"></a><span data-ttu-id="58d87-113">Beim Verwenden von Direct3D ist ein DirectX SDK erforderlich.</span><span class="sxs-lookup"><span data-stu-id="58d87-113">DirectX SDK Required When Using Direct3D</span></span>

<span data-ttu-id="58d87-114">Wenn Sie Anwendungen erstellen, die Direct3D verwenden, ist das [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) erforderlich für das Erstellen von Anwendungen, die APIs verwenden, die vom Platt Form Update für Windows Vista unterstützt werden, und das Platt Form Update für Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="58d87-114">If you create applications that use Direct3D, the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) is required for creating applications that use APIs supported by the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

### <a name="update-your-development-computer"></a><span data-ttu-id="58d87-115">Aktualisieren des Entwicklungs Computers</span><span class="sxs-lookup"><span data-stu-id="58d87-115">Update Your Development Computer</span></span>

<span data-ttu-id="58d87-116">Stellen Sie sicher, dass auf Ihrem Entwicklungs Computer alle neuesten Updates von Windows Update.</span><span class="sxs-lookup"><span data-stu-id="58d87-116">Ensure that your development computer has all of the latest updates from Windows Update.</span></span>

<span data-ttu-id="58d87-117">Wenn Sie Anwendungen in einer früheren Version von Windows entwickeln, müssen Sie das Platt Form Update für Windows Vista oder das Platt Form Update für Windows Server 2008-Update von Windows Update abrufen.</span><span class="sxs-lookup"><span data-stu-id="58d87-117">If you are developing applications on a previous version of Windows, you must obtain the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 update from Windows Update.</span></span> <span data-ttu-id="58d87-118">Wenn Sie eines dieser Updates installieren, können Sie die neue API nutzen, die von der Windows SDK für Windows 7 bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="58d87-118">Installing either of these updates will enable you to take advantage of the new API provided by the Windows SDK for Windows 7.</span></span>

<span data-ttu-id="58d87-119">Weitere Informationen zum Abrufen von Updates von Windows Update finden Sie im [Knowledge Base-Artikel über das Platt Form Update für Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) ( https://support.microsoft.com/kb/971644) .</span><span class="sxs-lookup"><span data-stu-id="58d87-119">For more information about how to obtain updates from Windows Update see the [Knowledge Base article about the Platform Update for Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) (https://support.microsoft.com/kb/971644).</span></span>

## <a name="development-environment"></a><span data-ttu-id="58d87-120">Entwicklungsumgebung</span><span class="sxs-lookup"><span data-stu-id="58d87-120">Development Environment</span></span>

### <a name="set-the-build-target-to-windows-7"></a><span data-ttu-id="58d87-121">Festlegen des Buildziels auf Windows 7</span><span class="sxs-lookup"><span data-stu-id="58d87-121">Set the Build Target to Windows 7</span></span>

<span data-ttu-id="58d87-122">Alle Anwendungen, die Bibliotheken im Platt Form Update für Windows Vista verwenden, müssen für die Zielplattform von Windows 7 erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="58d87-122">All applications that use libraries in the Platform Update for Windows Vista must be built against the Windows 7 target platform.</span></span>

<span data-ttu-id="58d87-123">Durch Festlegen von WINVER auf den Windows 7-Ziel Platt Form Wert können Sie Anwendungen entwickeln, die APIs verwenden, die mit dem Platt Form Update für Windows Vista unterstützt werden, oder das Platt Form Update für Windows Server 2008 auf einem Entwicklungs Computer mit Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="58d87-123">Setting WINVER to the Windows 7 target platform value enables you to develop applications that use APIs supported with the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 on a development machine running Windows Vista.</span></span>

<span data-ttu-id="58d87-124">Sie können die Zielplattform auf Windows 7 festlegen, entweder im Quellcode oder mithilfe der Option/D mit dem Visual Studio-Compiler.</span><span class="sxs-lookup"><span data-stu-id="58d87-124">You can set the target platform to Windows 7 either in your source code or by using the /D option with the Visual Studio compiler.</span></span>

<span data-ttu-id="58d87-125">Im folgenden Beispiel wird gezeigt, wie Sie in Ihrem Quellcode "winver" festlegen.</span><span class="sxs-lookup"><span data-stu-id="58d87-125">The following example shows how to set WINVER in your source code.</span></span>


```C++
#define WINVER 0x0601
```



<span data-ttu-id="58d87-126">Im folgenden Beispiel wird gezeigt, wie winver mithilfe der/D-Compileroption festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="58d87-126">The following example shows how to set WINVER using the /D compiler option.</span></span>

``` syntax
/DWINVER=0x0601
```

## <a name="application-deployment"></a><span data-ttu-id="58d87-127">Anwendungsbereitstellung</span><span class="sxs-lookup"><span data-stu-id="58d87-127">Application Deployment</span></span>

<span data-ttu-id="58d87-128">Wenn Sie Ihre Anwendung mit den Headern und Bibliotheken erstellen, die von der Windows SDK für Windows 7 bereitgestellt werden, werden die unterstützten APIs unter allen Windows-Versionen ausgeführt, auf denen das Platt Form Update für Windows Vista oder das Platt Form Update für Windows Server 2008 installiert ist.</span><span class="sxs-lookup"><span data-stu-id="58d87-128">If you build your application using the headers and libraries provided by the Windows SDK for Windows 7, supported APIs will run on any Windows version that has the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 installed.</span></span>

> [!Note]  
> <span data-ttu-id="58d87-129">Das Verhalten, die Leistung oder die Anforderungen für einige APIs, die mit dem Platt Form Update für Windows Vista oder dem Platt Form Update für Windows Server 2008 unterstützt werden, können in verschiedenen Windows-Versionen variieren.</span><span class="sxs-lookup"><span data-stu-id="58d87-129">The behavior, performance, or requirements for some APIs that are supported with the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 may vary across different versions of Windows.</span></span> <span data-ttu-id="58d87-130">Ausführliche Informationen zu einer bestimmten API, die von den Updates unterstützt wird, finden Sie unter [Informationen zum Platt Form Update für Windows Vista](platform-update-for-windows-vista-overview.md).</span><span class="sxs-lookup"><span data-stu-id="58d87-130">For details about a specific API that is supported by the updates, see [About Platform Update for Windows Vista](platform-update-for-windows-vista-overview.md).</span></span>

 

### <a name="no-redistributable-components"></a><span data-ttu-id="58d87-131">Keine weitervertreibbaren Komponenten</span><span class="sxs-lookup"><span data-stu-id="58d87-131">No Redistributable Components</span></span>

<span data-ttu-id="58d87-132">Die Anwendung muss keine weitervertreibbaren Komponenten installieren, z. b. DLLs oder andere Laufzeitdateien.</span><span class="sxs-lookup"><span data-stu-id="58d87-132">Your application does not need to install redistributable components, such as DLLs or other run-time files.</span></span>

### <a name="requires-updated-end-user-computer"></a><span data-ttu-id="58d87-133">Erfordert aktualisierte End-User Computer</span><span class="sxs-lookup"><span data-stu-id="58d87-133">Requires Updated End-User Computer</span></span>

<span data-ttu-id="58d87-134">Da das Platt Form Update für Windows Vista und das Platt Form Update für Windows Server 2008 von Windows Update gehostet werden, verfügen Endbenutzer mit aktivierten automatischen Updates höchstwahrscheinlich bereits über diese Updates und die erforderlichen Service Packs.</span><span class="sxs-lookup"><span data-stu-id="58d87-134">Because Platform Update for Windows Vista and Platform Update for Windows Server 2008 are hosted by Windows Update, end-users with automatic updates enabled are highly likely to already have these updates as well as the required service packs.</span></span>

<span data-ttu-id="58d87-135">Wenn auf dem Computer des Endbenutzers kein Platt Form Update für Windows Vista oder ein Platt Form Update für Windows Server 2008 installiert ist und Ihre Anwendung APIs erfordert, die von diesen Updates unterstützt werden, kann die Anwendung möglicherweise nicht auf dem Computer des Endbenutzers ausgeführt werden, oder es kann während der Ausführung zu Fehlern kommen.</span><span class="sxs-lookup"><span data-stu-id="58d87-135">If the end-user's computer does not have Platform Update for Windows Vista or Platform Update for Windows Server 2008 installed and your application requires APIs that are supported with these updates, your application may not be able to run on the end-user's computer or may encounter errors during execution.</span></span>

<span data-ttu-id="58d87-136">Um Probleme zu vermeiden, die möglicherweise durch einen veralteten Computer Ihres Benutzers verursacht werden, sollten Sie überprüfen, ob der Computer des Benutzers über das Platt Form Update für Windows Vista oder das Platt Form Update für Windows Server 2008-Update während der Installation der Anwendung verfügt.</span><span class="sxs-lookup"><span data-stu-id="58d87-136">To avoid the problems that could be caused by your user's computer being out-of-date, you want to verify that your user's computer has the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 update during the installation of your application.</span></span> <span data-ttu-id="58d87-137">Mit der Windows Update- [Agent-API](/windows/desktop/Wua_Sdk/portal-client) können Sie den Computer des Endbenutzers auf installierte Updates überprüfen.</span><span class="sxs-lookup"><span data-stu-id="58d87-137">You can use the [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client) to check your end-user's computer for installed updates.</span></span> <span data-ttu-id="58d87-138">Sie können auch die Windows Update-Agent-API verwenden, um erforderliche Updates während der Installation der Anwendung herunterzuladen und zu installieren, wenn die Updates nicht bereits von Endbenutzern installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="58d87-138">You can also use the Windows Update Agent API to download and install required updates during application installation if the end-user has not already installed the updates.</span></span>

<span data-ttu-id="58d87-139">Ein Beispiel für ein Installationsprogramm, das die Verwendung der [Windows Update-Agent-API](/windows/desktop/Wua_Sdk/portal-client)veranschaulicht, finden Sie unter [Bereitstellung von Direct3D 11 für Spieleentwickler](../direct3darticles/direct3d11-deployment.md) im [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) .</span><span class="sxs-lookup"><span data-stu-id="58d87-139">For an example of an installer that demonstrates how to use the [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client), see [Direct3D 11 Deployment for Game Developers](../direct3darticles/direct3d11-deployment.md) in the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx).</span></span>

<span data-ttu-id="58d87-140">Obwohl das D3D11InstallHelper Installer-Beispiel, das in der [Direct3D 11-Bereitstellung für Spieleentwickler](../direct3darticles/direct3d11-deployment.md)erläutert wird, für Anwendungen geschrieben wurde, die Direct3D 11 verwenden, bietet es ein gutes Beispiel für die Interaktion mit der [Windows Update-Agent-API](/windows/desktop/Wua_Sdk/portal-client) , um den Download und die Installation von Updates zu initiieren und zu verfolgen, die von Windows Update gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="58d87-140">Although the D3D11InstallHelper installer sample that is discussed in [Direct3D 11 Deployment for Game Developers](../direct3darticles/direct3d11-deployment.md), was written for applications that use Direct3D 11, it provides a good example of how to interact with the [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client) to initiate and track the download and installation of updates that are hosted by Windows Update.</span></span> <span data-ttu-id="58d87-141">Zum Kompilieren dieses Beispiels ist möglicherweise die Windows SDK für Windows 7 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="58d87-141">Compiling this sample may require the Windows SDK for Windows 7.</span></span> <span data-ttu-id="58d87-142">Weitere Informationen zum D3D11InstallHelper-Beispiel, einschließlich bekannter Probleme, finden Sie unter [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) Anmerkungen zu dieser Version von August 2009. Platt Form Update für Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="58d87-142">For additional information about the D3D11InstallHelper sample, including known issues, see the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) Release Notes for August 2009.Platform Update for Windows Vista</span></span>

## <a name="related-topics"></a><span data-ttu-id="58d87-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="58d87-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58d87-144">Platt Form Update für Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58d87-144">Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-portal.md)
</dt> <dt>

<span data-ttu-id="58d87-145">**Übersichten**</span><span class="sxs-lookup"><span data-stu-id="58d87-145">**Overviews**</span></span>
</dt> <dt>

[<span data-ttu-id="58d87-146">Informationen zum Platt Form Update für Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58d87-146">About Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[<span data-ttu-id="58d87-147">Knowledge Base-Artikel zum Platt Form Update für Windows Vista (KB 971644)</span><span class="sxs-lookup"><span data-stu-id="58d87-147">Knowledge Base article about the Platform Update for Windows Vista (KB 971644)</span></span>](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 