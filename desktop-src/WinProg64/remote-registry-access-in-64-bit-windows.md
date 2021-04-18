---
title: Remote Registrierungs Zugriff in 64-Bit-Windows
description: Der registrierungsredirector bietet über die regconnectregistry-Funktion Remote Zugriff auf die Registrierung auf 64-Bit-Fenstern.
ms.assetid: 7873c1e2-53fb-4c93-bf4c-251a13cd8db7
keywords:
- Remote Registrierungs Zugriff 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a139198ca08e0fdb9d7bcb070dcabf89dfa5403
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340711"
---
# <a name="remote-registry-access-in-64-bit-windows"></a><span data-ttu-id="a9aa2-104">Remote Registrierungs Zugriff in 64-Bit-Windows</span><span class="sxs-lookup"><span data-stu-id="a9aa2-104">Remote Registry Access in 64-bit Windows</span></span>

<span data-ttu-id="a9aa2-105">Der registrierungsredirector bietet über die [**regconnectregistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) -Funktion Remote Zugriff auf die Registrierung auf 64-Bit-Fenstern.</span><span class="sxs-lookup"><span data-stu-id="a9aa2-105">The registry redirector provides remote access to the registry on 64-bit Windows through the [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) function.</span></span>

<span data-ttu-id="a9aa2-106">Handelt es sich bei dem Client um eine 32-Bit-Anwendung, greift er auf die standardmäßige 32-Bit-Registrierungs Ansicht des Servers zu.</span><span class="sxs-lookup"><span data-stu-id="a9aa2-106">If the client is a 32-bit application, it accesses the server's default 32-bit registry view.</span></span> <span data-ttu-id="a9aa2-107">Wenn es sich bei dem Client um eine 64-Bit-Anwendung handelt, greift er auf die 64-Bit-Registrierungs Ansicht zu.</span><span class="sxs-lookup"><span data-stu-id="a9aa2-107">If the client is a 64-bit application, it accesses the 64-bit registry view.</span></span>

<span data-ttu-id="a9aa2-108">**Windows Server 2003:** Alle Clients greifen auf die 64-Bit-Registrierungs Ansicht zu, es sei denn, die Anwendung verwendet das Key \_ WOW64 \_ 32key-Flag.</span><span class="sxs-lookup"><span data-stu-id="a9aa2-108">**Windows Server 2003:** All clients access the 64-bit registry view unless the application uses the KEY\_WOW64\_32KEY flag.</span></span> <span data-ttu-id="a9aa2-109">Dieses Verhalten hat sich in Windows Server 2003 mit Service Pack 1 (SP1) und Windows XP Professional x64 Edition geändert, vorausgesetzt, dass sowohl der Client als auch der Server diese Versionen von Windows ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9aa2-109">This behavior changed with Windows Server 2003 with Service Pack 1 (SP1) and Windows XP Professional x64 Edition, provided that both the client and the server are running these versions of Windows.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9aa2-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a9aa2-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9aa2-111">Registrierungs Redirector</span><span class="sxs-lookup"><span data-stu-id="a9aa2-111">Registry Redirector</span></span>](registry-redirector.md)
</dt> <dt>

[<span data-ttu-id="a9aa2-112">Registrierungs Reflektion</span><span class="sxs-lookup"><span data-stu-id="a9aa2-112">Registry Reflection</span></span>](registry-reflection.md)
</dt> </dl>

 

 