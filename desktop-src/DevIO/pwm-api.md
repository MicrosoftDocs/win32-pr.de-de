---
description: Die Pulse Width-Modulation (Pulse Width Modulation, PWM) ist das Verfahren, mit dem eine rechteckige Pulse-Wave erzeugt wird, die eine Pulsbreite aufweist, die für die Variation des durchschnittlichen Werts des Waveforms-Werts zur Folge hat.
ms.assetid: 16B1E46F-2C42-4D94-949E-BE8F53EB1E1E
title: PWM-API
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 10b1951d9d96f49a9df9a51604767dbce360f9e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523643"
---
# <a name="pwm-api"></a><span data-ttu-id="0f0e5-103">PWM-API</span><span class="sxs-lookup"><span data-stu-id="0f0e5-103">PWM API</span></span>

<span data-ttu-id="0f0e5-104">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="0f0e5-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0f0e5-105">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="0f0e5-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0f0e5-106">Die Pulse Width-Modulation (Pulse Width Modulation, PWM) ist das Verfahren, mit dem eine rechteckige Pulse-Wave erzeugt wird, die eine Pulsbreite aufweist, die für die Variation des durchschnittlichen Werts des Waveforms-Werts zur Folge hat.</span><span class="sxs-lookup"><span data-stu-id="0f0e5-106">Pulse Width Modulation (PWM) is the technique of generating a rectangular pulse wave that has a pulse width that is modulated to result in the variation of the average value of the waveform.</span></span> <span data-ttu-id="0f0e5-107">Zu den häufigsten Verwendungsmöglichkeiten gehören das Antreiben von Servomotoren, das Abdichten von LEDs oder andere verwandte Funktionen.</span><span class="sxs-lookup"><span data-stu-id="0f0e5-107">Most common uses include driving servo motors, dimming LEDs, or other related functions.</span></span> <span data-ttu-id="0f0e5-108">PWM ist für die Verwendung in erster Linie für Internet der Dinge Szenarien vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="0f0e5-108">PWM is intended to be used primarily for Internet of Things scenarios.</span></span>

## <a name="about-pulse-width-modulation"></a><span data-ttu-id="0f0e5-109">Informationen zur Pulse Width-Modulation</span><span class="sxs-lookup"><span data-stu-id="0f0e5-109">About Pulse Width Modulation</span></span>

<span data-ttu-id="0f0e5-110">Ein PWM-Wellenform kann nach zwei Parametern kategorisiert werden:</span><span class="sxs-lookup"><span data-stu-id="0f0e5-110">A PWM waveform can be categorized by two parameters:</span></span>

-   <span data-ttu-id="0f0e5-111">Ein Wellenform-Zeitraum (T)</span><span class="sxs-lookup"><span data-stu-id="0f0e5-111">A waveform period (T)</span></span>

-   <span data-ttu-id="0f0e5-112">Der Duty-Cycle, bei dem Wellenform Frequency (f) die gegenseitige des Zeitraums f = 1/T ist.</span><span class="sxs-lookup"><span data-stu-id="0f0e5-112">The duty cycle, where the waveform frequency (f) is the reciprocal of the period f=1/T</span></span>

<span data-ttu-id="0f0e5-113">Der Duty Cycle beschreibt den Anteil der **auf** dem / **aktiven** Zeitpunkt in Bezug auf das reguläre Intervall oder den **Zeitraum** .</span><span class="sxs-lookup"><span data-stu-id="0f0e5-113">The duty cycle describes the proportion of the **on**/**Active** time with respect to the regular interval or **Period** of time.</span></span> <span data-ttu-id="0f0e5-114">Ein kostengünstiger Zeitraum entspricht dem Mittelwert einer geringen Ausgabe Leistung, da die Stromversorgung in den meisten Fällen deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0f0e5-114">A low duty cycle corresponds to an average of low output power, because the power is off for most of the time.</span></span> <span data-ttu-id="0f0e5-115">Der Duty Cycle wird als Prozentsatz ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="0f0e5-115">Duty cycle is expressed as a percentage.</span></span> <span data-ttu-id="0f0e5-116">Vollständig auf ist 100%.</span><span class="sxs-lookup"><span data-stu-id="0f0e5-116">Fully on is 100%.</span></span> <span data-ttu-id="0f0e5-117">Vollständig deaktiviert ist 0%.</span><span class="sxs-lookup"><span data-stu-id="0f0e5-117">Fully off is 0%.</span></span> <span data-ttu-id="0f0e5-118">Die **Hälfte der** Hälfte der Zeit beträgt 50%.</span><span class="sxs-lookup"><span data-stu-id="0f0e5-118">**Active** half the time is 50%.</span></span>

<span data-ttu-id="0f0e5-119">Entwickler, die PWM in ihren IOT-Anwendungen implementieren möchten, sollten die [WinRT PWM-Dokumentation](/uwp/api/windows.devices.pwm) untersuchen.</span><span class="sxs-lookup"><span data-stu-id="0f0e5-119">Developers looking to implement PWM in their IoT applications should investigate the [WinRT PWM documentation.](/uwp/api/windows.devices.pwm)</span></span>

## <a name="pulse-width-modulation-types"></a><span data-ttu-id="0f0e5-120">Pulse Width-Modultyp</span><span class="sxs-lookup"><span data-stu-id="0f0e5-120">Pulse Width Modulation types</span></span>

<span data-ttu-id="0f0e5-121">PWM verwendet diese e/a- [Kontrollcodes](pwm-control-codes.md), [Strukturen](pwm-structures.md)und [Enumerationen.](pwm-enumeration-types.md)</span><span class="sxs-lookup"><span data-stu-id="0f0e5-121">PWM uses [these IO control codes](pwm-control-codes.md), [structures](pwm-structures.md), and [enumerations.](pwm-enumeration-types.md)</span></span>

<span data-ttu-id="0f0e5-122">PWM verwendet auch die folgende Funktion: [**pwmparamesepinpath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).</span><span class="sxs-lookup"><span data-stu-id="0f0e5-122">PWM also uses the following function: [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).</span></span>

 

 
