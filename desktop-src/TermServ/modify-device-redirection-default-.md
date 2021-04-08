---
title: Ändern der Standardeinstellung für Geräte Umleitung
description: Da Remotedesktop Gatewayserver versuchen, sichere Geräte Umleitungs Richtlinien zu erzwingen, bevor Sie die Client Verbindung an einen Remotedesktop-Sitzungshost Server weiterleiten, müssen Sie diese Standardeinstellung möglicherweise in einigen Fällen deaktivieren.
ms.assetid: 03F2617C-D478-4A51-9EEC-E9643CA831B7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 925099b94c75dca39d381bdf57ae9730fb840da7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856292"
---
# <a name="modify-device-redirection-default"></a><span data-ttu-id="93306-103">Ändern der Standardeinstellung für Geräte Umleitung</span><span class="sxs-lookup"><span data-stu-id="93306-103">Modify Device Redirection Default</span></span>

<span data-ttu-id="93306-104">Da Remotedesktop Gatewayserver versuchen, sichere Geräte Umleitungs Richtlinien zu erzwingen, bevor Sie die Client Verbindung an einen Remotedesktop-Sitzungshost Server weiterleiten, müssen Sie diese Standardeinstellung möglicherweise in einigen Fällen deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="93306-104">Because Remote Desktop Gateway servers attempt to enforce secure device redirection policies before passing the client connection through to a Remote Desktop Session Host server, you may need to disable this default in some cases.</span></span>

<span data-ttu-id="93306-105">Unter Windows Server 2008 R2 und höher wird von Remotedesktop Gatewayservern standardmäßig versucht, sichere Geräte Umleitungs Richtlinien zu erzwingen, bevor die Client Verbindung an einen Remotedesktop-Sitzungshost Server weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="93306-105">On Windows Server 2008 R2 and later, Remote Desktop Gateway servers will by default attempt to enforce secure device redirection policies before passing the client connection through to a Remote Desktop Session Host server.</span></span> <span data-ttu-id="93306-106">Diese Funktion wird jedoch von einigen Servern nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="93306-106">However, this feature is not supported by some servers.</span></span> <span data-ttu-id="93306-107">Dies wird z. b. für Verbindungen zu Hyper-V-Konsolen Sitzungen nicht unterstützt, und es ist möglicherweise erforderlich, die Standardeinstellung zu deaktivieren, um die Verbund Authentifizierung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="93306-107">For example, this is not supported for connections to Hyper-V console sessions, and it may be necessary to disable the default to support federated authentication.</span></span> <span data-ttu-id="93306-108">In diesen Fällen kann dieses Feature deaktiviert werden, indem Sie den folgenden Registrierungsschlüssel erstellen, um Verbindungen zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="93306-108">In these cases, this feature can be disabled by creating the following registry key to allow connections to go through.</span></span>

<span data-ttu-id="93306-109">**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Terminal Server Gateway \\ prerdpdisableregkey**</span><span class="sxs-lookup"><span data-stu-id="93306-109">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server Gateway\\preRDPDisableRegKey**</span></span>

<span data-ttu-id="93306-110">Wenn dieser Schlüssel vorhanden ist, erzwingt das Remotedesktop Gateway keine Geräte Umleitung.</span><span class="sxs-lookup"><span data-stu-id="93306-110">When this key exists, the Remote Desktop Gateway will not enforce device redirection.</span></span>

 

 




