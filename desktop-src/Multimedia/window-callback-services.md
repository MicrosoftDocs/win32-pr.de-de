---
title: Fenster Rückruf Dienste
description: Fenster Rückruf Dienste
ms.assetid: 227602e5-7ea1-4afd-ac88-cfeabe746d1f
keywords:
- Multimedia-Audiodaten, Fenster Rückruf Dienste
- Audiodienste, Fenster Rückruf Dienste
- Audiomixer, Fenster Rückruf Dienste
- Mixer, Fenster Rückruf Dienste
- Fenster Rückruf Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48faf2dd94b61f5d4fc47e073fe0f3875bcbb503
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472972"
---
# <a name="window-callback-services"></a><span data-ttu-id="e9bb5-108">Fenster Rückruf Dienste</span><span class="sxs-lookup"><span data-stu-id="e9bb5-108">Window Callback Services</span></span>

<span data-ttu-id="e9bb5-109">Die Mixer Dienste stellen Fenster Rückruf Dienste bereit, sodass Ihre Anwendung Nachrichten von Mixer-Treibern verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="e9bb5-109">The mixer services provide window callback services so that your application can process messages from mixer drivers.</span></span> <span data-ttu-id="e9bb5-110">Wenn Sie diese Dienste verwenden möchten, geben Sie das Rückruf \_ Fenster-Flag im *fdwopen* -Parameter und ein Fenster Handle im *dwcallback* -Parameter der [**mixeropen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) -Funktion an.</span><span class="sxs-lookup"><span data-stu-id="e9bb5-110">To use these services, specify the CALLBACK\_WINDOW flag in the *fdwOpen* parameter and a window handle in the *dwCallback* parameter of the [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) function.</span></span> <span data-ttu-id="e9bb5-111">Treiber Meldungen werden an die Fenster Prozedur Funktion für das Fenster gesendet, das durch das Handle in *dwcallback* identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e9bb5-111">Driver messages are sent to the window procedure function for the window identified by the handle in *dwCallback*.</span></span> <span data-ttu-id="e9bb5-112">Die Nachrichten sind spezifisch für den audiogerätetyp.</span><span class="sxs-lookup"><span data-stu-id="e9bb5-112">The messages are specific to the audio device type.</span></span>

 

 