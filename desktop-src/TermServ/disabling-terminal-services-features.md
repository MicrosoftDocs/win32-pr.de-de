---
title: Deaktivieren von Remotedesktopdienste Features
description: Zur Erhöhung der Sicherheit können Sie Remotedesktopdienste Funktionen deaktivieren.
ms.assetid: 93505e3a-a4f8-4b94-8dbb-646140b6fa58
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f2f5534b062fe4e594d0400cf16adff4367af01
ms.sourcegitcommit: da6887b92d8ef51f6b3f0d9307632822e92a8648
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/01/2020
ms.locfileid: "103949297"
---
# <a name="disabling-remote-desktop-services-features"></a><span data-ttu-id="ccc7e-103">Deaktivieren von Remotedesktopdienste Features</span><span class="sxs-lookup"><span data-stu-id="ccc7e-103">Disabling Remote Desktop Services features</span></span>

<span data-ttu-id="ccc7e-104">Um die Sicherheit zu erhöhen, können Sie Remotedesktopdienste Funktionen wie die Zwischenablage Umleitung und die Drucker Umleitung für Clients, die mit Remotedesktop-Sitzungshost (RD-Sitzungshost)-Servern verbunden sind, deaktivieren, indem Sie das Remotedesktop ActiveX-Steuerelement verwenden.</span><span class="sxs-lookup"><span data-stu-id="ccc7e-104">For enhanced security, you might choose to disable Remote Desktop Services features such as clipboard redirection and printer redirection for clients that connect to Remote Desktop Session Host (RD Session Host) servers using the Remote Desktop ActiveX Control.</span></span>

<span data-ttu-id="ccc7e-105">**So deaktivieren Sie Remotedesktopdienste Features**</span><span class="sxs-lookup"><span data-stu-id="ccc7e-105">**To disable Remote Desktop Services features**</span></span>

1.  <span data-ttu-id="ccc7e-106">Bearbeiten Sie die Registrierung des Client Computers, und fügen Sie die folgenden Schlüssel hinzu:</span><span class="sxs-lookup"><span data-stu-id="ccc7e-106">Edit the registry of the client computer and add the following keys:</span></span>

    -   <span data-ttu-id="ccc7e-107">**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Terminal Server \\ disableclipboardredirection**</span><span class="sxs-lookup"><span data-stu-id="ccc7e-107">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server\\DisableClipboardRedirection**</span></span>
    -   <span data-ttu-id="ccc7e-108">**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Terminal Server \\ disabledriveredirection**</span><span class="sxs-lookup"><span data-stu-id="ccc7e-108">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server\\DisableDriveRedirection**</span></span>
    -   <span data-ttu-id="ccc7e-109">**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Terminal Server \\ disableprinterredirect**</span><span class="sxs-lookup"><span data-stu-id="ccc7e-109">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server\\DisablePrinterRedirection**</span></span>

2.  <span data-ttu-id="ccc7e-110">Legen Sie den Wert beider Schlüssel auf **reg \_ DWORD** 1 fest.</span><span class="sxs-lookup"><span data-stu-id="ccc7e-110">Set the value of both keys to **REG\_DWORD** 1.</span></span>

 

 




