---
title: Fenster Station und Desktop Erstellung
description: Das System erstellt automatisch die interaktive Fenster Station.
ms.assetid: 5b908cb6-3a72-4afc-aed0-8411e8d0888f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34aff24a29432e3e394a199bf881aa386bf17e71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315141"
---
# <a name="window-station-and-desktop-creation"></a><span data-ttu-id="508e6-103">Fenster Station und Desktop Erstellung</span><span class="sxs-lookup"><span data-stu-id="508e6-103">Window Station and Desktop Creation</span></span>

<span data-ttu-id="508e6-104">Das System erstellt automatisch die interaktive Fenster Station.</span><span class="sxs-lookup"><span data-stu-id="508e6-104">The system automatically creates the interactive window station.</span></span> <span data-ttu-id="508e6-105">Wenn sich ein interaktiver Benutzer anmeldet, ordnet das System die interaktive Fenster Station der Benutzer Anmelde Sitzung zu.</span><span class="sxs-lookup"><span data-stu-id="508e6-105">When an interactive user logs on, the system associates the interactive window station with the user logon session.</span></span> <span data-ttu-id="508e6-106">Das System erstellt außerdem den standardmäßigen Eingabe Desktop für die interaktive Fenster Station (Winsta0 \\ Standard).</span><span class="sxs-lookup"><span data-stu-id="508e6-106">The system also creates the default input desktop for the interactive window station (Winsta0\\default).</span></span> <span data-ttu-id="508e6-107">Prozesse, die vom angemeldeten Benutzer gestartet wurden, werden dem Winsta0 \\ -Standard Desktop zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="508e6-107">Processes started by the logged-on user are associated with the Winsta0\\default desktop.</span></span>

<span data-ttu-id="508e6-108">Ein Prozess kann mit der Funktion "Funktion erstellen" eine neue Fenster Station erstellen, und mit [**der Funktion "**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) up **Desktop** " oder " [**kreatedesktopex**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) " können Sie einen neuen Desktop erstellen.</span><span class="sxs-lookup"><span data-stu-id="508e6-108">A process can use the [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) function to create a new window station, and the **CreateDesktop** or [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) function to create a new desktop.</span></span> <span data-ttu-id="508e6-109">Die Anzahl der Desktops, die erstellt werden können, ist durch die Größe des System Desktop Heaps beschränkt.</span><span class="sxs-lookup"><span data-stu-id="508e6-109">The number of desktops that can be created is limited by the size of the system desktop heap.</span></span> <span data-ttu-id="508e6-110">Weitere Informationen finden Sie unter " [**kreatedesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa)".</span><span class="sxs-lookup"><span data-stu-id="508e6-110">For more information, see [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span></span>

<span data-ttu-id="508e6-111">Wenn ein nicht interaktiver Prozess (z. b. eine Dienst Anwendung) versucht, eine Verbindung mit einer Fenster Station herzustellen, und keine Fenster Station für die Prozess Anmelde Sitzung vorhanden ist, versucht das System, eine Fenster Station und einen Desktop für die Sitzung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="508e6-111">When a noninteractive process such as a service application attempts to connect to a window station and no window station exists for the process logon session, the system attempts to create a window station and desktop for the session.</span></span> <span data-ttu-id="508e6-112">Der Name der erstellten Fenster Station basiert auf dem Anmelde Sitzungs Bezeichner, und der Desktop hat den Namen Default, wie hier beschrieben:</span><span class="sxs-lookup"><span data-stu-id="508e6-112">The name of the created window station is based on the logon session identifier, and the desktop is named default, as described here:</span></span>

-   <span data-ttu-id="508e6-113">Wenn ein Dienst im Sicherheitskontext des Kontos "LocalSystem" ausgeführt wird, aber nicht das interaktive Prozess Attribut des Diensts enthält \_ \_ , werden die folgende Fenster Station und der Desktop verwendet: Service-0x0-3e7 $ \\ default.</span><span class="sxs-lookup"><span data-stu-id="508e6-113">If a service is running in the security context of the LocalSystem account but does not include the SERVICE\_INTERACTIVE\_PROCESS attribute, it uses the following window station and desktop: Service-0x0-3e7$\\default.</span></span> <span data-ttu-id="508e6-114">Diese Fenster Station ist nicht interaktiv, sodass der Dienst keine Benutzeroberfläche anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="508e6-114">This window station is not interactive, so the service cannot display a user interface.</span></span> <span data-ttu-id="508e6-115">Außerdem können vom Dienst erstellte Prozesse keine Benutzeroberfläche anzeigen.</span><span class="sxs-lookup"><span data-stu-id="508e6-115">In addition, processes created by the service cannot display a user interface.</span></span>
-   <span data-ttu-id="508e6-116">Wenn der Dienst im Sicherheitskontext eines Benutzerkontos ausgeführt wird, basiert der Name der Fenster Station auf der Benutzer-SID-Dienst-0x *Z1* - *Z2*$, wobei " *Z1* " der hohe Teil der Anmelde-SID und " *Z2* " der niedrige Teil der Anmelde-SID ist.</span><span class="sxs-lookup"><span data-stu-id="508e6-116">If the service is running in the security context of a user account, the name of the window station is based on the user SID Service-0x *Z1*-*Z2*$, where *Z1* is the high part of the logon SID and *Z2* is the low part of the logon SID.</span></span> <span data-ttu-id="508e6-117">Da eine sid für die Anmelde Sitzung eindeutig ist, erhalten zwei Dienste, die im selben Sicherheitskontext ausgeführt werden, eindeutige Fenster Stationen.</span><span class="sxs-lookup"><span data-stu-id="508e6-117">Because a SID is unique to the logon session, two services running in the same security context receive unique window stations.</span></span> <span data-ttu-id="508e6-118">Diese Fenster Stationen sind nicht interaktiv.</span><span class="sxs-lookup"><span data-stu-id="508e6-118">These window stations are not interactive.</span></span>

<span data-ttu-id="508e6-119">Die freigegebene Zugriffs Steuerungs Liste (DACL) für die Fenster Station und den Desktop umfasst die folgenden Zugriffsrechte für das Benutzerkonto des dienstanweises:</span><span class="sxs-lookup"><span data-stu-id="508e6-119">The discretionary access control list (DACL) for the window station and desktop includes the following access rights for the service's user account:</span></span>

<span data-ttu-id="508e6-120">Fenster Station:</span><span class="sxs-lookup"><span data-stu-id="508e6-120">Window Station:</span></span>

<dl> <span data-ttu-id="508e6-121">winsta \_ accessclipboard</span><span class="sxs-lookup"><span data-stu-id="508e6-121">WINSTA\_ACCESSCLIPBOARD</span></span>  
<span data-ttu-id="508e6-122">winsta \_ accessglobalatome</span><span class="sxs-lookup"><span data-stu-id="508e6-122">WINSTA\_ACCESSGLOBALATOMS</span></span>  
<span data-ttu-id="508e6-123">winsta \_ -up-Desktop</span><span class="sxs-lookup"><span data-stu-id="508e6-123">WINSTA\_CREATEDESKTOP</span></span>  
<span data-ttu-id="508e6-124">winsta- \_ exitwindows</span><span class="sxs-lookup"><span data-stu-id="508e6-124">WINSTA\_EXITWINDOWS</span></span>  
<span data-ttu-id="508e6-125">winsta- \_ Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="508e6-125">WINSTA\_READATTRIBUTES</span></span>  
<span data-ttu-id="508e6-126">Standard \_ Rechte \_ erforderlich</span><span class="sxs-lookup"><span data-stu-id="508e6-126">STANDARD\_RIGHTS\_REQUIRED</span></span>  
</dl>

<span data-ttu-id="508e6-127">Desktop:</span><span class="sxs-lookup"><span data-stu-id="508e6-127">Desktop:</span></span>

<dl> <span data-ttu-id="508e6-128">desktopingdesktop \_</span><span class="sxs-lookup"><span data-stu-id="508e6-128">DESKTOP\_CREATEMENU</span></span>  
<span data-ttu-id="508e6-129">Desktop- \_ kreatewindow</span><span class="sxs-lookup"><span data-stu-id="508e6-129">DESKTOP\_CREATEWINDOW</span></span>  
<span data-ttu-id="508e6-130">Desktop \_ Aufzählung</span><span class="sxs-lookup"><span data-stu-id="508e6-130">DESKTOP\_ENUMERATE</span></span>  
<span data-ttu-id="508e6-131">Desktop- \_ Hostingsteuerelement</span><span class="sxs-lookup"><span data-stu-id="508e6-131">DESKTOP\_HOOKCONTROL</span></span>  
<span data-ttu-id="508e6-132">Desktop-Schreib \_ Objekte</span><span class="sxs-lookup"><span data-stu-id="508e6-132">DESKTOP\_READOBJECTS</span></span>  
<span data-ttu-id="508e6-133">Desktop-Schreib \_ Objekte</span><span class="sxs-lookup"><span data-stu-id="508e6-133">DESKTOP\_WRITEOBJECTS</span></span>  
<span data-ttu-id="508e6-134">Standard \_ Rechte \_ erforderlich</span><span class="sxs-lookup"><span data-stu-id="508e6-134">STANDARD\_RIGHTS\_REQUIRED</span></span>  
</dl>

 

 