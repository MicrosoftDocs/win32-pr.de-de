---
description: Eine Liste mit einigen der möglichen Rückgabecodes für Methoden und Funktionen.
ms.assetid: 391b56a1-d0aa-4d35-8dba-cf7de66513d8
title: S_PRESENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4146a65e9092dcd3fed261c127e84fe8552128a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213882"
---
# <a name="s_present"></a><span data-ttu-id="ef514-103">S \_ vorhanden</span><span class="sxs-lookup"><span data-stu-id="ef514-103">S\_PRESENT</span></span>

<span data-ttu-id="ef514-104">Eine Liste mit einigen der möglichen Rückgabecodes für Methoden und Funktionen.</span><span class="sxs-lookup"><span data-stu-id="ef514-104">A list of some of the possible return codes for methods and functions.</span></span>



|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef514-105">\#definieren</span><span class="sxs-lookup"><span data-stu-id="ef514-105">\#define</span></span>                  | <span data-ttu-id="ef514-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef514-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="ef514-107">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="ef514-107">S\_OK</span></span>                     | <span data-ttu-id="ef514-108">Das Gerät wird normal ausgeführt und kann zum Rendern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef514-108">The device is running normally and can be used for rendering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="ef514-109">S \_ sind \_ okkludiert.</span><span class="sxs-lookup"><span data-stu-id="ef514-109">S\_PRESENT\_OCCLUDED</span></span>      | <span data-ttu-id="ef514-110">Der Präsentationsbereich ist okkludiert.</span><span class="sxs-lookup"><span data-stu-id="ef514-110">The presentation area is occluded.</span></span> <span data-ttu-id="ef514-111">"Oksion" bedeutet, dass das Präsentations Fenster minimiert ist oder ein anderes Gerät in den Vollbildmodus auf demselben Monitor wie das Präsentations Fenster und das Präsentations Fenster vollständig auf diesem Monitor angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ef514-111">Occlusion means that the presentation window is minimized or another device entered the fullscreen mode on the same monitor as the presentation window and the presentation window is completely on that monitor.</span></span> <span data-ttu-id="ef514-112">Die Okklusion tritt nicht auf, wenn der Client Bereich von einem anderen Fenster abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="ef514-112">Occlusion will not occur if the client area is covered by another Window.</span></span><br/> <span data-ttu-id="ef514-113">Okdierte Anwendungen können das Rendering fortsetzen, und alle Aufrufe werden erfolgreich ausgeführt, aber das Fenster für die okkludierte Darstellung wird nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ef514-113">Occluded applications can continue rendering and all calls will succeed, but the occluded presentation window will not be updated.</span></span> <span data-ttu-id="ef514-114">Vorzugsweise sollte die Anwendung das Rendern im Präsentations Fenster mithilfe des Geräts übernehmen und den Aufruf von [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) fortsetzen, bis s OK ist, oder wenn der \_ \_ \_ Modus \_ geändert wird.</span><span class="sxs-lookup"><span data-stu-id="ef514-114">Preferably the application should stop rendering to the presentation window using the device and keep calling [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) until S\_OK or S\_PRESENT\_MODE\_CHANGED returns.</span></span><br/> |
| <span data-ttu-id="ef514-115">S der \_ aktuelle \_ Modus \_ geändert</span><span class="sxs-lookup"><span data-stu-id="ef514-115">S\_PRESENT\_MODE\_CHANGED</span></span> | <span data-ttu-id="ef514-116">Der Desktop Anzeigemodus wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="ef514-116">The desktop display mode has been changed.</span></span> <span data-ttu-id="ef514-117">Die Anwendung kann das Rendering fortsetzen, aber es kann eine Farbkonvertierung/-Streckung vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ef514-117">The application can continue rendering, but there might be color conversion/stretching.</span></span> <span data-ttu-id="ef514-118">Wählen Sie ein backpufferformat aus, das dem aktuellen Anzeigemodus ähnelt, und kehren Sie zum erneuten Erstellen der Austausch Ketten zurück.</span><span class="sxs-lookup"><span data-stu-id="ef514-118">Pick a back buffer format similar to the current display mode, and call Reset to recreate the swap chains.</span></span> <span data-ttu-id="ef514-119">Das Gerät verlässt diesen Zustand, nachdem eine zurück Setzung aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="ef514-119">The device will leave this state after a Reset is called.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="ef514-120">Andere Fehlercodes sind in [D3DERR](d3derr.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="ef514-120">Other error codes are contained in [D3DERR](d3derr.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef514-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ef514-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef514-122">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="ef514-122">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




