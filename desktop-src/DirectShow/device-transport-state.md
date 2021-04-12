---
description: Geräte Transport Status
ms.assetid: 15edded0-207c-41e8-81fe-deb6335045eb
title: Geräte Transport Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05f52ea846c79be6cb2d011b635da358f7ecd0a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392894"
---
# <a name="device-transport-state"></a><span data-ttu-id="98925-103">Geräte Transport Status</span><span class="sxs-lookup"><span data-stu-id="98925-103">Device Transport State</span></span>

<span data-ttu-id="98925-104">Um den aktuellen Zustand des Geräts abzurufen, z. b. wiedergeben, anhalten oder anhalten, rufen Sie die Methode [**IAMExtTransport:: get \_ Mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) auf.</span><span class="sxs-lookup"><span data-stu-id="98925-104">To retrieve the current state of the device, such as play, pause, or stop, call the [**IAMExtTransport::get\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) method.</span></span> <span data-ttu-id="98925-105">Die-Methode ruft eine Konstante ab, die den Gerätezustand angibt:</span><span class="sxs-lookup"><span data-stu-id="98925-105">The method retrieves a constant that indicates the device state:</span></span>



| <span data-ttu-id="98925-106">Wert</span><span class="sxs-lookup"><span data-stu-id="98925-106">Value</span></span>                    | <span data-ttu-id="98925-107">Device State</span><span class="sxs-lookup"><span data-stu-id="98925-107">Device State</span></span> |
|--------------------------|--------------|
| <span data-ttu-id="98925-108">\_Play-Modus wiedergeben \_</span><span class="sxs-lookup"><span data-stu-id="98925-108">ED\_MODE\_PLAY</span></span>           | <span data-ttu-id="98925-109">Abspielen</span><span class="sxs-lookup"><span data-stu-id="98925-109">Play</span></span>         |
| <span data-ttu-id="98925-110">Ed- \_ Modus wird \_ beendet</span><span class="sxs-lookup"><span data-stu-id="98925-110">ED\_MODE\_STOP</span></span>           | <span data-ttu-id="98925-111">Stop</span><span class="sxs-lookup"><span data-stu-id="98925-111">Stop</span></span>         |
| <span data-ttu-id="98925-112">Einfrieren des ED- \_ Modus \_</span><span class="sxs-lookup"><span data-stu-id="98925-112">ED\_MODE\_FREEZE</span></span>         | <span data-ttu-id="98925-113">Anhalten</span><span class="sxs-lookup"><span data-stu-id="98925-113">Pause</span></span>        |
| <span data-ttu-id="98925-114">Ed- \_ Modus- \_ FF</span><span class="sxs-lookup"><span data-stu-id="98925-114">ED\_MODE\_FF</span></span>             | <span data-ttu-id="98925-115">Schnell vorwärts</span><span class="sxs-lookup"><span data-stu-id="98925-115">Fast-forward</span></span> |
| <span data-ttu-id="98925-116">REW im ED- \_ Modus \_</span><span class="sxs-lookup"><span data-stu-id="98925-116">ED\_MODE\_REW</span></span>            | <span data-ttu-id="98925-117">Rewind</span><span class="sxs-lookup"><span data-stu-id="98925-117">Rewind</span></span>       |
| <span data-ttu-id="98925-118">Datensatz im ED- \_ Modus \_</span><span class="sxs-lookup"><span data-stu-id="98925-118">ED\_MODE\_RECORD</span></span>         | <span data-ttu-id="98925-119">Datensatz</span><span class="sxs-lookup"><span data-stu-id="98925-119">Record</span></span>       |
| <span data-ttu-id="98925-120">\_ \_ Daten Satz \_ Sperrung im ED-Modus</span><span class="sxs-lookup"><span data-stu-id="98925-120">ED\_MODE\_RECORD\_FREEZE</span></span> | <span data-ttu-id="98925-121">Datensatz-Pause</span><span class="sxs-lookup"><span data-stu-id="98925-121">Record-pause</span></span> |



 

<span data-ttu-id="98925-122">Der folgende Code überprüft den Gerätestatus:</span><span class="sxs-lookup"><span data-stu-id="98925-122">The following code checks the device state:</span></span>


```C++
LONG State;
hr = MyDevCap.pTransport->get_Mode(&State);
if (SUCCEEDED(hr))
{
    switch (State)
    {
        case ED_MODE_PLAY:
        // ... 
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="98925-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="98925-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98925-124">Steuern eines DV-Camcorder</span><span class="sxs-lookup"><span data-stu-id="98925-124">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



