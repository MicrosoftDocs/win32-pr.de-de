---
title: Verbinden eines Aufzeichnungs Fensters mit einem Aufzeichnungs Treiber
description: Verbinden eines Aufzeichnungs Fensters mit einem Aufzeichnungs Treiber
ms.assetid: 78d4aaf5-6216-4eec-84d4-6727d1822983
keywords:
- WM_CAP_DRIVER_CONNECT Meldung
- capdriverconnect-Makro
- capgetdriverdescription-Funktion
- WM_CAP_DRIVER_GET_NAME Meldung
- capdrivergetname-Makro
- WM_CAP_DRIVER_GET_VERSION Meldung
- capdrivergetversion-Makro
- WM_CAP_DRIVER_DISCONNECT Meldung
- capdriverdisconnect-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c189ad3ea5631e269ffbe85f20a143b074486f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710157"
---
# <a name="connecting-a-capture-window-to-a-capture-driver"></a><span data-ttu-id="6e708-112">Verbinden eines Aufzeichnungs Fensters mit einem Aufzeichnungs Treiber</span><span class="sxs-lookup"><span data-stu-id="6e708-112">Connecting a Capture Window to a Capture Driver</span></span>

<span data-ttu-id="6e708-113">Sie können ein Aufzeichnungs Fenster dynamisch verbinden oder mit einem Aufzeichnungs Treiber verbinden.</span><span class="sxs-lookup"><span data-stu-id="6e708-113">You can dynamically connect or disconnect a capture window to a capture driver.</span></span> <span data-ttu-id="6e708-114">Sie können ein Aufzeichnungs Fenster mithilfe der [**WM- \_ Cap-Treiber- \_ \_ Connect**](wm-cap-driver-connect.md) -Nachricht (oder dem [**capdriverconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) -Makro) mit einem Aufzeichnungs Treiber verbinden oder zuordnen.</span><span class="sxs-lookup"><span data-stu-id="6e708-114">You can connect or associate a capture window with a capture driver by using the [**WM\_CAP\_DRIVER\_CONNECT**](wm-cap-driver-connect.md) message (or the [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) macro).</span></span> <span data-ttu-id="6e708-115">Nachdem ein Erfassungsfenster und ein Erfassungs Treiber verbunden sind, können Sie gerätespezifische Nachrichten an den mit einem Aufzeichnungs Fenster verknüpften Erfassungs Treiber senden.</span><span class="sxs-lookup"><span data-stu-id="6e708-115">After a capture window and capture driver are connected, you can send device-specific messages to the capture driver associated with a capture window.</span></span>

<span data-ttu-id="6e708-116">Wenn Sie mehr als ein Erfassungsgerät auf einem System installiert haben, können Sie ein Aufzeichnungs Fenster mit einem bestimmten Gerätetreiber für die Video Erfassung verbinden, indem Sie eine ganze Zahl für den *wParam* -Parameter der WM- \_ Cap-Treiber- \_ \_ Verbindungs Nachricht angeben.</span><span class="sxs-lookup"><span data-stu-id="6e708-116">If you have more than one capture device installed on a system, you can connect a capture window to a particular video capture device driver by specifying an integer for the *wParam* parameter of the WM\_CAP\_DRIVER\_CONNECT message.</span></span> <span data-ttu-id="6e708-117">Die ganze Zahl ist ein Index, der einen Video Erfassungs Treiber identifiziert, der in der Registrierung oder im \[ \] Abschnitt Drivers der SYSTEM.INI Datei aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="6e708-117">The integer is an index that identifies a video capture driver listed in the registry or in the \[drivers\] section of the SYSTEM.INI file.</span></span> <span data-ttu-id="6e708-118">NULL für den ersten Index Eintrag verwenden.</span><span class="sxs-lookup"><span data-stu-id="6e708-118">Use zero for the first index entry.</span></span>

<span data-ttu-id="6e708-119">Sie können den Namen und die Version eines installierten Erfassungs Treibers mithilfe der [**capgetdriverdescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) -Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="6e708-119">You can retrieve the name and version of an installed capture driver by using the [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) function.</span></span> <span data-ttu-id="6e708-120">Die Anwendung kann diese Funktion zum Auflisten der installierten Erfassungsgeräte und Treiber verwenden, sodass der Benutzer ein Erfassungsgerät auswählen kann, um eine Verbindung mit einem Aufzeichnungs Fenster herzustellen.</span><span class="sxs-lookup"><span data-stu-id="6e708-120">Your application can use this function to enumerate the installed capture devices and drivers, so the user can select a capture device to connect to a capture window.</span></span>

<span data-ttu-id="6e708-121">Sie können den Namen des Erfassungsgeräte Treibers, der mit einem Aufzeichnungs Fenster verbunden ist, mit der " [**WM \_ Cap \_ Driver \_ get \_ Name**](wm-cap-driver-get-name.md) Message" (oder dem " [**capdrivergetname**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) "-Makro) abrufen.</span><span class="sxs-lookup"><span data-stu-id="6e708-121">You can retrieve the name of the capture device driver connected to a capture window by using the [**WM\_CAP\_DRIVER\_GET\_NAME**](wm-cap-driver-get-name.md) message (or the [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) macro).</span></span> <span data-ttu-id="6e708-122">Um die Version eines installierten Erfassungs Treibers abzurufen, verwenden [**Sie die Version des WM- \_ Cap- \_ Treibers \_ get \_ Version**](wm-cap-driver-get-version.md) (oder das " [**capdrivergetversion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) "-Makro).</span><span class="sxs-lookup"><span data-stu-id="6e708-122">To retrieve the version of an installed capture driver, use the [**WM\_CAP\_DRIVER\_GET\_VERSION**](wm-cap-driver-get-version.md) message (or the [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) macro).</span></span>

<span data-ttu-id="6e708-123">Sie können ein Erfassungsfenster von einem Aufzeichnungs Treiber trennen, indem Sie die " [**WM \_ Cap \_ Driver \_ Disconnect**](wm-cap-driver-disconnect.md) "-Nachricht (oder das " [**capdriverdisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) "-Makro) verwenden.</span><span class="sxs-lookup"><span data-stu-id="6e708-123">You can disconnect a capture window from a capture driver by using the [**WM\_CAP\_DRIVER\_DISCONNECT**](wm-cap-driver-disconnect.md) message (or the [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) macro).</span></span>

<span data-ttu-id="6e708-124">Wenn ein Erfassungsfenster zerstört wird, werden alle angeschlossenen Gerätetreiber für die Geräte Erfassung automatisch getrennt.</span><span class="sxs-lookup"><span data-stu-id="6e708-124">When an capture window is destroyed, any connected video capture device drivers are automatically disconnected.</span></span>

 

 




