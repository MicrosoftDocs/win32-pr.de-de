---
title: Bereitstellen der RDP-Client Sicherheit
description: Einige Eigenschaften des Remotedesktop ActiveX-Steuerelement Objekts sind auf bestimmte Internet Explorer-URL-Sicherheitszonen beschränkt.
ms.assetid: fd20ec03-a5e4-4c3e-9bf5-5fa841e869c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15bbb143abd3ec09a7f1aeff67a7b6dfa224b56b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710187"
---
# <a name="providing-for-rdp-client-security"></a><span data-ttu-id="8553d-103">Bereitstellen der RDP-Client Sicherheit</span><span class="sxs-lookup"><span data-stu-id="8553d-103">Providing for RDP client security</span></span>

<span data-ttu-id="8553d-104">Um es Clients zu ermöglichen, sich selbst vor potenziell nicht vertrauenswürdigen Servern zu schützen, werden einige Eigenschaften des Remotedesktop ActiveX-Steuerelement Objekts auf bestimmte Internet Explorer-URL-Sicherheitszonen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="8553d-104">To allow clients to protect themselves from potentially untrustworthy servers, some properties of the Remote Desktop ActiveX control object are restricted to specific Internet Explorer URL security zones.</span></span> <span data-ttu-id="8553d-105">Dies bedeutet Folgendes: Wenn ein Benutzer, der das Internet durchsucht, auf die Seite zugreift und sich die Seite in einer höheren URL-Sicherheitszone als der Computer befindet, mit dem Sie das Web durchsuchen, sind diese Eigenschaften deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8553d-105">This means that, when a user browsing the web accesses the page and the page is in a higher URL security zone than the computer they are browsing the web with, these properties are disabled.</span></span> <span data-ttu-id="8553d-106">Auf diese eingeschränkten Eigenschaften wird mithilfe der [**imstscsecuredsettings**](imstscsecuredsettings-interface.md) -Schnittstelle und der [**imsrdpclientsecuredsettings**](imsrdpclientsecuredsettings-interface.md) -Schnittstelle zugegriffen, und Sie sind in den folgenden Sicherheitszonen für Internet Explorer-URLs verfügbar:</span><span class="sxs-lookup"><span data-stu-id="8553d-106">These restricted properties are accessed using the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface and the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface, and are available in the following Internet Explorer URL security zones:</span></span>

-   <span data-ttu-id="8553d-107">Arbeitsplatz</span><span class="sxs-lookup"><span data-stu-id="8553d-107">My computer</span></span>
-   <span data-ttu-id="8553d-108">Lokales Intranet</span><span class="sxs-lookup"><span data-stu-id="8553d-108">Local intranet</span></span>
-   <span data-ttu-id="8553d-109">Vertrauenswürdige Sites</span><span class="sxs-lookup"><span data-stu-id="8553d-109">Trusted sites</span></span>

<span data-ttu-id="8553d-110">Sie sind in diesen Zonen deaktiviert:</span><span class="sxs-lookup"><span data-stu-id="8553d-110">They are disabled in these zones:</span></span>

-   <span data-ttu-id="8553d-111">Internet</span><span class="sxs-lookup"><span data-stu-id="8553d-111">Internet</span></span>
-   <span data-ttu-id="8553d-112">Eingeschränkte Websites</span><span class="sxs-lookup"><span data-stu-id="8553d-112">Restricted sites</span></span>

<span data-ttu-id="8553d-113">Wenn Sie diese eingeschränkten Eigenschaften in der Remotedesktopdienste-Webanwendung aufrufen, sollten Sie [**imstscax:: get \_ securedsettings**](imstscax-securedsettings.md) und [**imstscax:: get \_ securedsettingsenabled**](imstscax-securedsettingsenabled.md) aufrufen, um auf die Eigenschaften der gesicherten Einstellungen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="8553d-113">If you call these restricted properties within your Remote Desktop Services web application, you should call [**IMsTscAx::get\_SecuredSettings**](imstscax-securedsettings.md) and [**IMsTscAx::get\_SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) to access the Secured Settings properties.</span></span>

<span data-ttu-id="8553d-114">Die eingeschränkten Eigenschaften, auf die die **imstscsecuredsettings** -Schnittstelle zugreift, lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8553d-114">The restricted properties that the **IMsTscSecuredSettings** interface accesses are the following:</span></span>

-   <span data-ttu-id="8553d-115">[**StartProgram**](imstscsecuredsettings-startprogram.md).</span><span class="sxs-lookup"><span data-stu-id="8553d-115">[**StartProgram**](imstscsecuredsettings-startprogram.md).</span></span> <span data-ttu-id="8553d-116">Diese Eigenschaft gibt das Programm an, das bei der Verbindung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="8553d-116">This property specifies the program that will be started upon connection.</span></span>
-   <span data-ttu-id="8553d-117">[**WorkDir**](imstscsecuredsettings-workdir.md).</span><span class="sxs-lookup"><span data-stu-id="8553d-117">[**WorkDir**](imstscsecuredsettings-workdir.md).</span></span> <span data-ttu-id="8553d-118">Diese Eigenschaft gibt das Arbeitsverzeichnis des Programms an, das in [**StartProgram**](imstscsecuredsettings-startprogram.md)angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8553d-118">This property specifies the working directory of the program specified in [**StartProgram**](imstscsecuredsettings-startprogram.md).</span></span>
-   <span data-ttu-id="8553d-119">[**Vollbild**](imstscsecuredsettings-fullscreen.md).</span><span class="sxs-lookup"><span data-stu-id="8553d-119">[**FullScreen**](imstscsecuredsettings-fullscreen.md).</span></span> <span data-ttu-id="8553d-120">Diese Eigenschaft gibt an, ob sich der Zustand des Steuer Elements bei der Verbindung im Vollbildmodus oder im Fenstermodus befindet.</span><span class="sxs-lookup"><span data-stu-id="8553d-120">This property specifies whether the state of the control upon connection will be in full-screen or window mode.</span></span> <span data-ttu-id="8553d-121">Wenn der Wert dieser Eigenschaft **true** ist, wird die Verbindung im Vollbildmodus geöffnet.</span><span class="sxs-lookup"><span data-stu-id="8553d-121">If the value of this property is **TRUE**, the connection will be opened in full-screen mode.</span></span> <span data-ttu-id="8553d-122">Obwohl die Verwendung der **Fullscreen** -Eigenschaft auf die zuvor aufgeführten Internet Explorer-URL-Sicherheitszonen beschränkt ist, kann ein Benutzer nach der Verbindungs Herstellung jederzeit in den Vollbildmodus wechseln, indem er die [Tasten](terminal-services-shortcut-keys.md) Kombination für den Vollbildmodus (Strg + Alt + untbuggung) drückt.</span><span class="sxs-lookup"><span data-stu-id="8553d-122">Although the use of the **FullScreen** property is restricted to the Internet Explorer URL security zones listed earlier, a user can always change to full-screen mode after connection by pressing the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

<span data-ttu-id="8553d-123">Die Eigenschaften, auf die die **imsrdpclientsecuredsettings** -Schnittstelle zugreift, lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8553d-123">The properties that the **IMsRdpClientSecuredSettings** interface accesses are the following:</span></span>

-   <span data-ttu-id="8553d-124">[**Audioredirectionmode**](imsrdpclientsecuredsettings-autoredirectionmode.md).</span><span class="sxs-lookup"><span data-stu-id="8553d-124">[**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md).</span></span> <span data-ttu-id="8553d-125">Diese Eigenschaft gibt an, ob Sounds umgeleitet oder Sounds auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="8553d-125">This property specifies whether to redirect sounds, or play sounds at the Remote Desktop Session Host (RD Session Host) server.</span></span>
-   <span data-ttu-id="8553d-126">[**Keyboardhuokmode**](imsrdpclientsecuredsettings-keyboardhookmode.md).</span><span class="sxs-lookup"><span data-stu-id="8553d-126">[**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md).</span></span> <span data-ttu-id="8553d-127">Diese Eigenschaft gibt an, wie und wann Windows-Tastenkombinationen angewendet werden sollen. Beispiel: Alt + Tab.</span><span class="sxs-lookup"><span data-stu-id="8553d-127">This property specifies how and when to apply Windows key combinations; for example, ALT+TAB.</span></span>

<span data-ttu-id="8553d-128">Mit dem folgenden Skript wird Microsoft Notepad.exe bei der Verbindung gestartet.</span><span class="sxs-lookup"><span data-stu-id="8553d-128">The following script launches Microsoft Notepad.exe upon connection.</span></span> <span data-ttu-id="8553d-129">Führen Sie dieses Skript aus, bevor Sie die [**imstscax:: Connect**](imstscax-connect.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8553d-129">Run this script before calling the [**IMsTscAx::Connect**](imstscax-connect.md) method.</span></span>

``` syntax
if MsRdpClient.SecuredSettingsEnabled then
    MsRdpClient.SecuredSettings.StartProgram = "notepad.exe"
else
    msgbox "Cannot access secured setting (startprogram) in the current browser zone"
end if
```

 

 




