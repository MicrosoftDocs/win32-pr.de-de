---
description: Eine Liste einiger möglicher Rückgabecodes für Methoden und Funktionen.
ms.assetid: 391b56a1-d0aa-4d35-8dba-cf7de66513d8
title: S_PRESENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6cd860fcc8268bf2b63a9498b9960da359ca210
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999337"
---
# <a name="s_present"></a><span data-ttu-id="becca-103">S \_ PRESENT</span><span class="sxs-lookup"><span data-stu-id="becca-103">S\_PRESENT</span></span>

<span data-ttu-id="becca-104">Eine Liste einiger möglicher Rückgabecodes für Methoden und Funktionen.</span><span class="sxs-lookup"><span data-stu-id="becca-104">A list of some of the possible return codes for methods and functions.</span></span>



| <span data-ttu-id="becca-105">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="becca-105">\#define</span></span>                  | <span data-ttu-id="becca-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="becca-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="becca-107">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="becca-107">S\_OK</span></span>                     | <span data-ttu-id="becca-108">Das Gerät wird normal ausgeführt und kann zum Rendern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="becca-108">The device is running normally and can be used for rendering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="becca-109">S \_ PRESENT \_ OCCLUDED</span><span class="sxs-lookup"><span data-stu-id="becca-109">S\_PRESENT\_OCCLUDED</span></span>      | <span data-ttu-id="becca-110">Der Präsentationsbereich ist umschließend.</span><span class="sxs-lookup"><span data-stu-id="becca-110">The presentation area is occluded.</span></span> <span data-ttu-id="becca-111">Okklusion bedeutet, dass das Präsentationsfenster minimiert wird oder ein anderes Gerät auf demselben Monitor wie das Präsentationsfenster in den Vollbildmodus übertrat und sich das Präsentationsfenster vollständig auf diesem Monitor befindet.</span><span class="sxs-lookup"><span data-stu-id="becca-111">Occlusion means that the presentation window is minimized or another device entered the fullscreen mode on the same monitor as the presentation window and the presentation window is completely on that monitor.</span></span> <span data-ttu-id="becca-112">Okklusion tritt nicht auf, wenn der Clientbereich von einem anderen Fenster abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="becca-112">Occlusion will not occur if the client area is covered by another Window.</span></span><br/> <span data-ttu-id="becca-113">Okcluded applications can continue rendering and all calls will succeed, but the occluded presentation window will not be updated. (Okcluded applications can continue rendering and all calls will succeed, but the occluded presentation window will not be updated. (Okcluded applications can continue rendering and all calls will succeed, but the occluded presentation window will not be updated.</span><span class="sxs-lookup"><span data-stu-id="becca-113">Occluded applications can continue rendering and all calls will succeed, but the occluded presentation window will not be updated.</span></span> <span data-ttu-id="becca-114">Vorzugsweise sollte die Anwendung das Rendern im Präsentationsfenster mithilfe des Geräts beenden und [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) weiterhin aufrufen, bis S OK oder \_ S PRESENT MODE CHANGED zurückgegeben \_ \_ \_ wird.</span><span class="sxs-lookup"><span data-stu-id="becca-114">Preferably the application should stop rendering to the presentation window using the device and keep calling [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) until S\_OK or S\_PRESENT\_MODE\_CHANGED returns.</span></span><br/> |
| <span data-ttu-id="becca-115">S \_ PRESENT \_ MODE \_ CHANGED</span><span class="sxs-lookup"><span data-stu-id="becca-115">S\_PRESENT\_MODE\_CHANGED</span></span> | <span data-ttu-id="becca-116">Der Desktopanzeigemodus wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="becca-116">The desktop display mode has been changed.</span></span> <span data-ttu-id="becca-117">Die Anwendung kann das Rendering fortsetzen, es kann jedoch eine Farbkonvertierung/Streckung geben.</span><span class="sxs-lookup"><span data-stu-id="becca-117">The application can continue rendering, but there might be color conversion/stretching.</span></span> <span data-ttu-id="becca-118">Wählen Sie ein Zurückpufferformat aus, das dem aktuellen Anzeigemodus ähnelt, und rufen Sie Zurücksetzen auf, um die Swapketten neu zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="becca-118">Pick a back buffer format similar to the current display mode, and call Reset to recreate the swap chains.</span></span> <span data-ttu-id="becca-119">Das Gerät verlässt diesen Zustand, nachdem eine Zurücksetzung aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="becca-119">The device will leave this state after a Reset is called.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="becca-120">Andere Fehlercodes sind in [D3DERR enthalten.](d3derr.md)</span><span class="sxs-lookup"><span data-stu-id="becca-120">Other error codes are contained in [D3DERR](d3derr.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="becca-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="becca-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="becca-122">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="becca-122">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




