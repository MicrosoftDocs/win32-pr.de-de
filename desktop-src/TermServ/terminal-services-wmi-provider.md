---
title: WMI-Anbieter Remotedesktopdienste
description: Der Remotedesktopdienste WMI-Anbieter ermöglicht programmgesteuerten Zugriff auf die Informationen und Einstellungen, die vom Microsoft Management Console (MMC)-Snap-in "Remotedesktopdienste Configuration/Connections" verfügbar gemacht werden.
ms.assetid: d205a3da-3f9a-4ee1-9c99-a39e9cce0a11
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste, WMI-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d947db18c0cde63bcb6c4c3954fc9811e0f0f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039153"
---
# <a name="remote-desktop-services-wmi-provider"></a><span data-ttu-id="f379c-104">WMI-Anbieter Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="f379c-104">Remote Desktop Services WMI provider</span></span>

<span data-ttu-id="f379c-105">Der Remotedesktopdienste WMI-Anbieter ermöglicht programmgesteuerten Zugriff auf die Informationen und Einstellungen, die vom Microsoft Management Console (MMC)-Snap-in "Remotedesktopdienste Configuration/Connections" verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="f379c-105">The Remote Desktop Services WMI provider provides programmatic access to the information and settings that are exposed by the Remote Desktop Services Configuration/Connections Microsoft Management Console (MMC) snap-in.</span></span>

<span data-ttu-id="f379c-106">Die Anbieter-DLL wird vom Windows-Verwaltungsprozess (Winmgmt.exe) geladen, wenn ein Client eine Anforderung an den Server sendet.</span><span class="sxs-lookup"><span data-stu-id="f379c-106">The provider DLL is loaded by the Windows Management process (Winmgmt.exe) when a client makes a request to the server.</span></span> <span data-ttu-id="f379c-107">Die Verwaltung ist möglich, indem die Anbieter Methoden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f379c-107">Administration is possible by using the provider methods.</span></span> <span data-ttu-id="f379c-108">Der Anbieter ist sowohl als Instanz als auch als Methoden Anbieter registriert.</span><span class="sxs-lookup"><span data-stu-id="f379c-108">The provider is registered as both an instance and a method provider.</span></span>

<span data-ttu-id="f379c-109">Der Remotedesktopdienste WMI-Anbieter wurde als dynamischer Anbieter implementiert, der von der [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) Basisklasse abgeleitet wurde, und erbt dabei alle seine Eigenschaften und Methoden sowie eine Prozess interne Dynamic Link Library.</span><span class="sxs-lookup"><span data-stu-id="f379c-109">The Remote Desktop Services WMI provider has been implemented as a dynamic provider derived from the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) base class, inheriting all of its properties and methods, and an in-process dynamic link library.</span></span>

<span data-ttu-id="f379c-110">Weitere Informationen finden Sie in der [Remotedesktopdienste WMI-Anbieter Referenz](terminal-services-wmi-provider-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f379c-110">For more information, see the [Remote Desktop Services WMI Provider reference](terminal-services-wmi-provider-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f379c-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f379c-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f379c-112">WMI-Anbieter Referenz Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="f379c-112">Remote Desktop Services WMI Provider Reference</span></span>](terminal-services-wmi-provider-reference.md)
</dt> </dl>

 

 