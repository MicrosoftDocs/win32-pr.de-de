---
description: Weitere Informationen zu PWM-Strukturen
ms.assetid: 992E3913-C1C4-48C1-A550-475CF44AB065
title: PWM-Strukturen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99511820f8500cd8df827a80664f6c274d732665
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958332"
---
# <a name="pwm-structures"></a><span data-ttu-id="a25c3-103">PWM-Strukturen</span><span class="sxs-lookup"><span data-stu-id="a25c3-103">PWM Structures</span></span>

<span data-ttu-id="a25c3-104">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="a25c3-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a25c3-105">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="a25c3-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a25c3-106">Die folgenden Strukturen werden mit der Pulse Width-Modulation verwendet:</span><span class="sxs-lookup"><span data-stu-id="a25c3-106">The following structures are used with Pulse Width Modulation:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a25c3-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a25c3-107">In this section</span></span>



| <span data-ttu-id="a25c3-108">Thema</span><span class="sxs-lookup"><span data-stu-id="a25c3-108">Topic</span></span>                                                                                                                        | <span data-ttu-id="a25c3-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a25c3-109">Description</span></span>                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a25c3-110">**PWM- \_ Controller \_ get \_ Actual \_ Period \_ Output**</span><span class="sxs-lookup"><span data-stu-id="a25c3-110">**PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD\_OUTPUT**</span></span>](pwm-controller-get-actual-period-output.md)<br/>                   | <span data-ttu-id="a25c3-111">Enthält den effektiven Ausgabesignal Zeitraum für einen Pulse Width Modulation (PWM)-Controller.</span><span class="sxs-lookup"><span data-stu-id="a25c3-111">Contains the effective output signal period for a Pulse Width Modulation (PWM) controller.</span></span><br/>                    |
| [<span data-ttu-id="a25c3-112">**PWM- \_ Controller \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="a25c3-112">**PWM\_CONTROLLER\_INFO**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_controller_info)<br/>                                                              | <span data-ttu-id="a25c3-113">Stellt die statischen Informationen dar, die einen Pulse Width-modulcontroller (PWM) kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="a25c3-113">Represents the static information that characterizes a Pulse Width Modulation (PWM) controller.</span></span> <br/>              |
| [<span data-ttu-id="a25c3-114">**Eingabe des \_ \_ \_ gewünschten \_ Zeitraums \_ durch PWM-Controller**</span><span class="sxs-lookup"><span data-stu-id="a25c3-114">**PWM\_CONTROLLER\_SET\_DESIRED\_PERIOD\_INPUT**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_controller_set_desired_period_input)<br/>                   | <span data-ttu-id="a25c3-115">Enthält einen Eingabe Wert für eine vorgeschlagene Signal Periode für den Pulse Width-modulcontroller (PWM).</span><span class="sxs-lookup"><span data-stu-id="a25c3-115">Contains an input value for a suggested signal period for the Pulse Width Modulation (PWM) controller.</span></span> <br/>       |
| [<span data-ttu-id="a25c3-116">**Ausgabe des \_ \_ \_ gewünschten \_ Zeitraums \_ durch PWM-Controller festlegen**</span><span class="sxs-lookup"><span data-stu-id="a25c3-116">**PWM\_CONTROLLER\_SET\_DESIRED\_PERIOD\_OUTPUT**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_controller_set_desired_period_output)<br/>                 | <span data-ttu-id="a25c3-117">Enthält den effektiven Ausgabesignal Zeitraum des PWM-Controllers (Pulse Width Modulation).</span><span class="sxs-lookup"><span data-stu-id="a25c3-117">Contains the effective output signal period of the Pulse Width Modulation (PWM) controller.</span></span><br/>                   |
| [<span data-ttu-id="a25c3-118">**PWM- \_ Pin \_ get \_ Active \_ Duty \_ Cycle \_ Prozent \_ Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="a25c3-118">**PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_OUTPUT**</span></span>](pwm-pin-get-active-duty-cycle-percentage-output.md)<br/> | <span data-ttu-id="a25c3-119">Enthält den aktuellen Duty-Cycle-Prozentsatz für eine PIN oder einen Kanal in einem PWM-Controller (Pulse Width Modulation).</span><span class="sxs-lookup"><span data-stu-id="a25c3-119">Contains the current duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span><br/> |
| [<span data-ttu-id="a25c3-120">**PWM-Pin-Satz für \_ \_ \_ aktiven \_ Duty- \_ \_ Prozentsatz der \_ Eingabe**</span><span class="sxs-lookup"><span data-stu-id="a25c3-120">**PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_INPUT**</span></span>](pwm-pin-set-active-duty-cycle-percentage-input.md)<br/>   | <span data-ttu-id="a25c3-121">Enthält einen gewünschten Duty-Cycle-Prozentsatz für eine PIN oder einen Kanal in einem PWM-Controller (Pulse Width Modulation).</span><span class="sxs-lookup"><span data-stu-id="a25c3-121">Contains a desired duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span><br/>   |
| [<span data-ttu-id="a25c3-122">**PWM- \_ Pin \_ Get Polarität- \_ \_ Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="a25c3-122">**PWM\_PIN\_GET\_POLARITY\_OUTPUT**</span></span>](pwm-pin-get-polarity-output.md)<br/>                                            | <span data-ttu-id="a25c3-123">Enthält einen Wert, der zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="a25c3-123">Contains a polarity value to return.</span></span><br/>                                                                          |
| [<span data-ttu-id="a25c3-124">**PWM- \_ Pin \_ Set- \_ \_ poleleingabe**</span><span class="sxs-lookup"><span data-stu-id="a25c3-124">**PWM\_PIN\_SET\_POLARITY\_INPUT**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_pin_set_polarity_input)<br/>                                              | <span data-ttu-id="a25c3-125">Enthält einen gewünschten Wert für die Polarität einer PIN oder eines Kanals.</span><span class="sxs-lookup"><span data-stu-id="a25c3-125">Contains a desired value for polarity of a pin or channel.</span></span><br/>                                                    |
| [<span data-ttu-id="a25c3-126">**die Ausgabe der PWM- \_ PIN wurde \_ \_ gestartet \_ .**</span><span class="sxs-lookup"><span data-stu-id="a25c3-126">**PWM\_PIN\_IS\_STARTED\_OUTPUT**</span></span>](pwm-pin-is-started-output.md)<br/>                                                | <span data-ttu-id="a25c3-127">Enthält den aktuellen Signal Generierungs Status einer PIN.</span><span class="sxs-lookup"><span data-stu-id="a25c3-127">Contains the current signal generation state of a pin.</span></span><br/>                                                        |



 

 

 




