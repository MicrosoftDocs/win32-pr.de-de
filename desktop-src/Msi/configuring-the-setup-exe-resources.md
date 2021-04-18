---
description: In den Windows SDK Komponenten für Windows Installer Entwickler ist eine konfigurierbare Bootstrap-Datei (Setup.exe) und ein Konfigurationstool (Msistuff.exe) enthalten.
ms.assetid: 95fcea5c-b107-48b7-9ae8-84629353c554
title: Konfigurieren der Setup.exe Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41b7907310ff6efcf41e984bf132bbbaedf38b6a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "106371875"
---
# <a name="configuring-the-setupexe-resources"></a><span data-ttu-id="72d98-103">Konfigurieren der Setup.exe Ressourcen</span><span class="sxs-lookup"><span data-stu-id="72d98-103">Configuring the Setup.exe Resources</span></span>

<span data-ttu-id="72d98-104">In den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)ist eine konfigurierbare Bootstrap-Datei (Setup.exe) und ein Konfigurationstool ( [Msistuff.exe](msistuff-exe.md)) enthalten.</span><span class="sxs-lookup"><span data-stu-id="72d98-104">A configurable bootstrap executable (Setup.exe) and configuration tool ( [Msistuff.exe](msistuff-exe.md)) is included in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="72d98-105">Wenn Sie Msistuff.exe verwenden, um die Ressourcen in Setup.exe zu konfigurieren, können Entwickler problemlos eine Webinstallation eines Windows Installer Pakets erstellen.</span><span class="sxs-lookup"><span data-stu-id="72d98-105">By using Msistuff.exe to configure the resources in Setup.exe, developers can easily create a web installation of a Windows Installer package.</span></span> <span data-ttu-id="72d98-106">Weitere Informationen finden [Sie unter Internet Download Bootstrapping](internet-download-bootstrapping.md).</span><span class="sxs-lookup"><span data-stu-id="72d98-106">For more information see [Internet Download Bootstrapping](internet-download-bootstrapping.md).</span></span>

<span data-ttu-id="72d98-107">Wenn Sie die folgende Befehlszeile eingeben, werden die Ressourcen für das Beispiel konfiguriert, das in [einem URL-basierten Windows Installer Installations Beispiel](a-url-based-windows-installer-installation-example.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="72d98-107">Entering the following command line configures the resources for the sample described in [A URL Based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md).</span></span>

`MsiStuff setup.exe /u https://www.blueyonderairlines.com/Products/MySetup /d MySetup.msi /n MySetup /v 150 /i https://www.blueyonderairlines.com/Products/Common/InstMsi /a Ansi/Instmsi.exe /w Unicode/Instmsi.exe`

[<span data-ttu-id="72d98-108">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="72d98-108">Continue</span></span>](sign-setup-exe-and-mysetup-msi.md)

 

 



