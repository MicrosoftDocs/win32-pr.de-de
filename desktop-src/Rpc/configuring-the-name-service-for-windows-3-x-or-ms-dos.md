---
title: Konfigurieren des Namens Dienstanbieter für Windows 3. x oder MS-DOS
description: Remote Prozedur Aufruf (RPC) und Konfigurieren des Namens Dienstanbieter für Windows 3. x oder MS-DOS.
ms.assetid: 7b22a12e-43d0-4e32-a191-d63a56559143
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533a0d8556f9cc51d0842768d0df1bdd0d553b5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037118"
---
# <a name="configuring-the-name-service-for-windows-3x-or-ms-dos"></a><span data-ttu-id="b4e4f-103">Konfigurieren des Namens Dienstanbieter für Windows 3. x oder MS-DOS</span><span class="sxs-lookup"><span data-stu-id="b4e4f-103">Configuring the Name Service for Windows 3.x or MS-DOS</span></span>

<span data-ttu-id="b4e4f-104">Wenn Sie Setup.exe ausführen, um die 16-Bit-RPC-Lauf Zeit Bibliothek zu installieren, werden Sie aufgefordert, einen Namen Dienstanbieter auszuwählen:</span><span class="sxs-lookup"><span data-stu-id="b4e4f-104">When you run Setup.exe to install the 16-bit RPC run-time library, it prompts you to select a name service provider:</span></span>

-   <span data-ttu-id="b4e4f-105">Wenn Sie die Option **Default Name Service Provider installieren** auswählen, wird der Standard-NSP, Microsoft Locator, installiert.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-105">If you choose **Install Default Name Service Provider**, the default NSP, Microsoft Locator, is installed.</span></span>
-   <span data-ttu-id="b4e4f-106">Wenn Sie **benutzerdefinierten Namen Dienstanbieter installieren** auswählen, vervollständigen Sie das Dialogfeld **Netzwerkadresse definieren** , um den DCE-Zell Verzeichnisdienst als NSP zu installieren.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-106">If you choose **Install Custom Name Service Provider**, complete the **Define Network Address** dialog box to install the DCE Cell Directory Service as your NSP.</span></span> <span data-ttu-id="b4e4f-107">Der DCE-Zell Verzeichnisdienst ist das NSP, das mit DCE-Servern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-107">The DCE Cell Directory Service is the NSP used with DCE servers.</span></span>

<span data-ttu-id="b4e4f-108">Die Netzwerkadresse ist der Name des Host Computers, auf dem der NSI-Daemon (nsid) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-108">The network address is the name of the host computer that runs the NSI daemon (nsid).</span></span> <span data-ttu-id="b4e4f-109">Dieser Computer fungiert als Gateway für den DCE-Zell Verzeichnisdienst und übergibt NSI-Funktionsaufrufe zwischen Computern, auf denen Microsoft-Betriebssysteme und DCE-Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-109">This computer acts as a gateway to the DCE Cell Directory Service, passing NSI function calls between computers that run Microsoft operating systems and DCE computers.</span></span> <span data-ttu-id="b4e4f-110">Die Netzwerkadresse kann 80 Zeichen oder weniger betragen – beispielsweise ist 11.1.9.169 eine gültige Adresse.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-110">The network address can be 80 characters or less—for example, 11.1.9.169 is a valid address.</span></span>

 

 




