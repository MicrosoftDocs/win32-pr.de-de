---
title: Windows-Bereitstellungsdienste
description: Bereitstellen von Windows-Betriebssystemen. Richten Sie neue Clients mit einer netzwerkbasierten Installation ein, ohne dass Administratoren jeden Computer besuchen oder direkt von CD-oder DVD-Medien installieren.
ms.assetid: 790abc27-03cc-4f93-bf04-a4eb37e614bb
keywords:
- Windows-Bereitstellungs Dienste Windows-Bereitstellungs Dienste
- Windows-Bereitstellungs Dienste Windows-Bereitstellungs Dienste, Startseite
- Bereitstellungs Dienste Windows-Bereitstellungs Dienste
- WDS Windows-Bereitstellungs Dienste Siehe Windows-Bereitstellungs Dienste
- Remoteinstallations Dienste Windows-Bereitstellungs Dienste Weitere Informationen
- RIS Windows-Bereitstellungs Dienste Siehe Windows-Bereitstellungs Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b35bebb000b383552f12d259ca17552165e9247f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341327"
---
# <a name="windows-deployment-services"></a><span data-ttu-id="c2adc-110">Windows-Bereitstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="c2adc-110">Windows Deployment Services</span></span>

## <a name="purpose"></a><span data-ttu-id="c2adc-111">Zweck</span><span class="sxs-lookup"><span data-stu-id="c2adc-111">Purpose</span></span>

<span data-ttu-id="c2adc-112">Die Windows-Bereitstellungs Dienste (Windows Deployment Services, WDS) sind die überarbeitete Version der Remoteinstallations Dienste</span><span class="sxs-lookup"><span data-stu-id="c2adc-112">Windows Deployment Services (WDS) is the revised version of Remote Installation Services (RIS).</span></span> <span data-ttu-id="c2adc-113">WDS ermöglicht die Bereitstellung von Windows-Betriebssystemen.</span><span class="sxs-lookup"><span data-stu-id="c2adc-113">WDS enables the deployment of Windows operating systems.</span></span> <span data-ttu-id="c2adc-114">Sie können WDS verwenden, um neue Clients mit einer netzwerkbasierten Installation einzurichten, ohne dass Administratoren jeden Computer besuchen oder direkt von CD-oder DVD-Medien installieren müssen.</span><span class="sxs-lookup"><span data-stu-id="c2adc-114">You can use WDS to set up new clients with a network-based installation without requiring that administrators visit each computer or install directly from CD or DVD media.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="c2adc-115">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="c2adc-115">Developer audience</span></span>

<span data-ttu-id="c2adc-116">Die primäre Entwicklergruppe der WDS-API ist für Gruppen vorgesehen, die benutzerdefinierte Tools und Prozesse für Sie und andere Computer Verwaltungs Gruppen entwickeln.</span><span class="sxs-lookup"><span data-stu-id="c2adc-116">The primary developer audience of the WDS API is for groups that develop custom tools and processes for IT and other computer administration groups.</span></span> <span data-ttu-id="c2adc-117">In Umgebungen, in denen die Standardlösung für Windows-Bereitstellungs Dienste (WDS) nicht verwendet werden kann, ermöglicht die WDS-API den programmgesteuerten Zugriff auf einige WDS-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="c2adc-117">In environments where the standard Windows Deployment Services (WDS) solution cannot be used, the WDS API enables programmatic access to some WDS components.</span></span>

<span data-ttu-id="c2adc-118">Original Gerätehersteller (OEMs), System-Generatoren und IT-Experten von Unternehmen, die Informationen zur Bereitstellung von Windows auf neuen Computern suchen, sollten die Informationen zur Standardlösung für Windows-Bereitstellungs Dienste (Windows Deployment Services, WDS) in den [Schritt-für-Schritt-Anleitungen für die Windows-Bereitstellungs Dienste](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) und das [Windows Automated Installation Kit (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333)sehen.</span><span class="sxs-lookup"><span data-stu-id="c2adc-118">Original Equipment Manufacturers (OEMs), system builders, and corporate IT professionals looking for information on how to deploy Windows onto new computers, should see the information about the standard Windows Deployment Services (WDS) solution in the [Windows Deployment Services Update Step-by-Step Guide](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) and the [Windows Automated Installation Kit (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="c2adc-119">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="c2adc-119">Run-time requirements</span></span>

<span data-ttu-id="c2adc-120">WDS ist als Add-on für Windows Server 2003 mit Service Pack 1 (SP1) verfügbar und im Betriebssystem ab Windows Server 2003 mit Service Pack 2 (SP2) und Windows Server 2008 enthalten.</span><span class="sxs-lookup"><span data-stu-id="c2adc-120">WDS is available as an add-on for Windows Server 2003 with Service Pack 1 (SP1) and is included in the operating system starting with Windows Server 2003 with Service Pack 2 (SP2) and Windows Server 2008.</span></span> <span data-ttu-id="c2adc-121">Die WDS-PXE-Server-API erfordert, dass die WDS-Server Rolle auf dem Server benutzerdefinierte PXE-Anbieter implementiert.</span><span class="sxs-lookup"><span data-stu-id="c2adc-121">The WDS PXE Server API requires the WDS server role on the server to implement custom PXE providers.</span></span> <span data-ttu-id="c2adc-122">Die WDS-Client-API erfordert die Microsoft Windows Preinstallation Environment-Phase (Windows PE 2,0) der Setup Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="c2adc-122">The WDS Client API requires the Microsoft Windows Preinstallation Environment (Windows PE 2.0) phase of setup processing.</span></span> <span data-ttu-id="c2adc-123">Ein RAMDisk-Start fähiges Image von Windows PE 2,0 in der. Das WIM-Format muss als Teil des Netzwerkstart Vorgangs heruntergeladen werden, um benutzerdefinierte WDS-Clients implementieren zu können.</span><span class="sxs-lookup"><span data-stu-id="c2adc-123">A RAMDISK bootable image of Windows PE 2.0 in the .WIM format must be downloaded as part of the network boot process to implement custom WDS clients.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c2adc-124">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c2adc-124">In this section</span></span>



| <span data-ttu-id="c2adc-125">Thema</span><span class="sxs-lookup"><span data-stu-id="c2adc-125">Topic</span></span>                                                                                                 | <span data-ttu-id="c2adc-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2adc-126">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="c2adc-127">Informationen zur API für die Windows-Bereitstellungs Dienste</span><span class="sxs-lookup"><span data-stu-id="c2adc-127">About the Windows Deployment Services API</span></span>](about-the-windows-deployment-services-api.md)<br/> | <span data-ttu-id="c2adc-128">Allgemeine Informationen über die WDS-Server-API und die WDS-Client-API.</span><span class="sxs-lookup"><span data-stu-id="c2adc-128">General information about the WDS Server API and WDS Client API.</span></span><br/>    |
| [<span data-ttu-id="c2adc-129">Referenz zu Windows-Bereitstellungs Diensten</span><span class="sxs-lookup"><span data-stu-id="c2adc-129">Windows Deployment Services Reference</span></span>](windows-deployment-services-reference.md)<br/>         | <span data-ttu-id="c2adc-130">Beschreibt die Funktionen und Strukturen der Windows-Bereitstellungs Dienste.</span><span class="sxs-lookup"><span data-stu-id="c2adc-130">Describes the Windows Deployment Services functions and structures.</span></span><br/> |



 

 

