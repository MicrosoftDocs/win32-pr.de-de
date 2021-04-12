---
title: Container Steuerelemente
description: Container Steuerelemente
ms.assetid: 4fa59272-54b6-4da9-a7f5-e1b4eab7fa80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69228bcc03017442880d41156f67397ee26bb13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471788"
---
# <a name="container-controls"></a><span data-ttu-id="91433-103">Container Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="91433-103">Container Controls</span></span>

<span data-ttu-id="91433-104">Wie oben beschrieben, sind Container Steuerelemente ActiveX-Steuerelemente, die visuell andere Steuerelemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="91433-104">As described above, container controls are ActiveX controls that visually contain other controls.</span></span> <span data-ttu-id="91433-105">Die ActiveX-Steuerelement Architektur gibt die [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) -Schnittstelle zum Aktivieren von Container Steuerelementen an.</span><span class="sxs-lookup"><span data-stu-id="91433-105">The ActiveX controls architecture specifies the [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) interface to enable container controls.</span></span> <span data-ttu-id="91433-106">Container können auch Container-Steuerelemente unterstützen, ohne **ISimpleFrameSite** zu unterstützen, obwohl das Verhalten nicht garantiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="91433-106">Containers may also support container controls without supporting **ISimpleFrameSite**, although the behavior cannot be guaranteed.</span></span> <span data-ttu-id="91433-107">Aus diesem Grund ist eine Komponenten Kategorie für simpleframesite-Steuerelemente vorhanden, bei der die vollständige Funktionalität dieser Schnittstelle erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="91433-107">For this reason, a component category exists for SimpleFrameSite controls where the full functionality of this interface is required.</span></span>

<span data-ttu-id="91433-108">Zur Unterstützung von Container Steuerelementen ohne Implementierung von [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)muss ein ActiveX-Steuerelement Container Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="91433-108">To support container controls without implementing [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), an ActiveX control container must:</span></span>

-   <span data-ttu-id="91433-109">Alle Steuerelemente jederzeit aktivieren.</span><span class="sxs-lookup"><span data-stu-id="91433-109">Activate all controls at all times.</span></span>
-   <span data-ttu-id="91433-110">Ordnen Sie die enthaltenen Steuerelemente dem HWND des enthaltenden Steuer Elements zu.</span><span class="sxs-lookup"><span data-stu-id="91433-110">Reparent the contained controls to the hWnd of the containing control.</span></span>
-   <span data-ttu-id="91433-111">Bleibt das übergeordnete Element des Container Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="91433-111">Remain the parent of the container control.</span></span>

 

 




