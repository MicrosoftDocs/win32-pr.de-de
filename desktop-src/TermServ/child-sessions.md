---
title: Untergeordnete Sitzungen
description: Ab Windows Server 2012 und Windows 8 unterstützt Remotedesktop das Konzept einer untergeordneten Sitzung, bei der es sich um eine spezielle Loopback Remotedesktop Sitzung handelt, die an die vorhandene Sitzung eines Benutzers gebunden ist.
ms.assetid: 65B9DB67-4EE8-40B5-B465-CA425792C62B
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788b36bf9799da9b0cb7486963f3154451ca5392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206295"
---
# <a name="child-sessions"></a><span data-ttu-id="3a78e-103">Untergeordnete Sitzungen</span><span class="sxs-lookup"><span data-stu-id="3a78e-103">Child Sessions</span></span>

<span data-ttu-id="3a78e-104">Ab Windows Server 2012 und Windows 8 unterstützt Remotedesktop das Konzept einer untergeordneten *Sitzung*, bei der es sich um eine spezielle Loopback Remotedesktop Sitzung handelt, die an die vorhandene Sitzung eines Benutzers gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="3a78e-104">Beginning with Windows Server 2012 and Windows 8, Remote Desktop supports the concept of a *child session*, which is a special loopback Remote Desktop session that is tied to a user's existing session.</span></span>

<span data-ttu-id="3a78e-105">Untergeordnete Sitzungen werden unter den folgenden Betriebssystemen nicht unterstützt:</span><span class="sxs-lookup"><span data-stu-id="3a78e-105">Child sessions are not supported on the following operating systems:</span></span>

<dl> <span data-ttu-id="3a78e-106">Windows RT</span><span class="sxs-lookup"><span data-stu-id="3a78e-106">Windows RT</span></span>  
<span data-ttu-id="3a78e-107">Windows Server 2012 Server Core-Installationsoption</span><span class="sxs-lookup"><span data-stu-id="3a78e-107">Windows Server 2012 Server Core installation option</span></span>  
<span data-ttu-id="3a78e-108">Microsoft Hyper-V Server 2012</span><span class="sxs-lookup"><span data-stu-id="3a78e-108">Microsoft Hyper-V Server 2012</span></span>  
</dl>

<span data-ttu-id="3a78e-109">Ein System kann zu einem bestimmten Zeitpunkt nur eine aktive und verbundene untergeordnete Sitzung haben.</span><span class="sxs-lookup"><span data-stu-id="3a78e-109">A system can only have one active and connected child session at any given time.</span></span>

<span data-ttu-id="3a78e-110">Die untergeordnete Sitzung kann beendet werden, indem Sie sich direkt von ihr abmelden, oder Sie wird beendet, wenn die übergeordnete Sitzung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="3a78e-110">The child session can be terminated by logging off directly from it, or it will be terminated when its parent session terminates.</span></span>

<span data-ttu-id="3a78e-111">Bevor untergeordnete Sitzungen in einem System verwendet werden können, müssen Sie die Funktion der untergeordneten Sitzung aktivieren, indem Sie die [**wtsenablechildsessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3a78e-111">Before child sessions can be used on a system, you must enable the child session functionality by calling the [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) function.</span></span> <span data-ttu-id="3a78e-112">Mithilfe der [**wtsischildsessionsenabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled) -Funktion können Sie auch feststellen, ob untergeordnete Sitzungen aktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="3a78e-112">You can also determine if child sessions have been enabled by using the [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled) function.</span></span>

<span data-ttu-id="3a78e-113">Eine untergeordnete Sitzung kann nur aus einer vorhandenen Benutzersitzung erstellt werden, indem das [Remotedesktop ActiveX-Steuer](remote-desktop-activex-control.md) Element verwendet wird und die Eigenschaft "connectdechildsession" mit [**imsrdpextendedsettings. Property**](imsrdpextendedsettings-property.md) vor dem Herstellen der Verbindung festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3a78e-113">A child session can only be created from within an existing user's session by using the [Remote Desktop ActiveX control](remote-desktop-activex-control.md) and setting the "ConnectToChildSession" property with [**IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md) prior to connecting.</span></span> <span data-ttu-id="3a78e-114">Wenn die [**imstscax. Connect**](imstscax-connect.md) -Methode aufgerufen wird, meldet sich das Remotedesktop ActiveX-Steuerelement automatisch bei der untergeordneten Sitzung an, ohne zur Eingabe von Anmelde Informationen aufgefordert zu werden, es sei denn, der Benutzer ist über eine Smartcard bei der übergeordneten Sitzung angemeldet.</span><span class="sxs-lookup"><span data-stu-id="3a78e-114">When the [**IMsTscAx.Connect**](imstscax-connect.md) method is called, the Remote Desktop ActiveX control will automatically log on to the child session without prompting for credentials, except when the user is logged into the parent session using a smart card.</span></span> <span data-ttu-id="3a78e-115">Anders als bei einer regulären Remotedesktop Sitzung benötigt ein Benutzer nicht das interaktive Remote Recht, um sich bei der untergeordneten Sitzung anzumelden, da es sich um eine Loopback Sitzung handelt.</span><span class="sxs-lookup"><span data-stu-id="3a78e-115">Unlike a regular Remote Desktop session, a user does not need the Remote Interactive right to log on to the child session because this is a loopback session.</span></span>

<span data-ttu-id="3a78e-116">Eine untergeordnete Sitzung kann nicht gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="3a78e-116">A child session cannot be locked.</span></span> <span data-ttu-id="3a78e-117">Sie verfügt über keinen Bildschirmschoner und keinen Anmeldebildschirm.</span><span class="sxs-lookup"><span data-stu-id="3a78e-117">It will have no screen saver and no logon screen.</span></span> <span data-ttu-id="3a78e-118">Anders als bei einer regulären Sitzung wird der Anmelde Text in dieser untergeordneten Sitzung nicht angezeigt, wenn die Winlogon-Anmelde Text Richtlinie festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3a78e-118">Also, unlike a regular session, if the WinLogon logon text policy is set, the logon text will not be displayed in this child session.</span></span> <span data-ttu-id="3a78e-119">Außerdem werden Remotedesktopverbindung Timeout-Gruppenrichtlinien in der untergeordneten Sitzung nicht wirksam, wenn diese Richtlinien festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="3a78e-119">Also, there will be no effect of Remote Desktop Connection Timeout Group policies on the child session if these policies are set.</span></span>

<span data-ttu-id="3a78e-120">Die folgenden APIs werden in Verbindung mit untergeordneten Sitzungen verwendet:</span><span class="sxs-lookup"><span data-stu-id="3a78e-120">The following APIs are used in conjunction with child sessions:</span></span>

-   [<span data-ttu-id="3a78e-121">**Wtsenablechildsessions**</span><span class="sxs-lookup"><span data-stu-id="3a78e-121">**WTSEnableChildSessions**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
-   [<span data-ttu-id="3a78e-122">**Wtsischildsessionsenabled**</span><span class="sxs-lookup"><span data-stu-id="3a78e-122">**WTSIsChildSessionsEnabled**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
-   [<span data-ttu-id="3a78e-123">**Wout getchildsessionid**</span><span class="sxs-lookup"><span data-stu-id="3a78e-123">**WTSGetChildSessionId**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
-   <span data-ttu-id="3a78e-124">Eigenschaft "connectdechildsession" in [ **imsrdpextendedsettings. Property**](imsrdpextendedsettings-property.md)</span><span class="sxs-lookup"><span data-stu-id="3a78e-124">"ConnectToChildSession" property in [**IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md)</span></span>

 

 




