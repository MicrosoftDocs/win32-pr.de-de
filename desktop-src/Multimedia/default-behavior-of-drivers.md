---
title: Standardverhalten von Treibern
description: Standardverhalten von Treibern
ms.assetid: ed6905eb-67ad-421d-be00-4a5585dff7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e5a4294ffc117041d3aca4273cd1f4b8378814
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726561"
---
# <a name="default-behavior-of-drivers"></a><span data-ttu-id="7fc6a-103">Standardverhalten von Treibern</span><span class="sxs-lookup"><span data-stu-id="7fc6a-103">Default Behavior of Drivers</span></span>

<span data-ttu-id="7fc6a-104">In vielen Fällen definieren die MCI-Befehls Spezifikationen die Standardwerte und das Verhalten für Treiber eines bestimmten Gerätetyps.</span><span class="sxs-lookup"><span data-stu-id="7fc6a-104">In many situations, the MCI command specifications define the default values and behavior for drivers of a particular device type.</span></span> <span data-ttu-id="7fc6a-105">Da multimediaregeräte über eine Vielzahl von Features (und Einschränkungen) verfügen können, kann es zu undefiniertem Verhalten kommen.</span><span class="sxs-lookup"><span data-stu-id="7fc6a-105">Since multimedia devices can have a wide range of features (and limitations), there can be undefined areas of behavior.</span></span> <span data-ttu-id="7fc6a-106">Außerdem können Ausnahmen auf der Grundlage der Funktionen des Geräts anders behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="7fc6a-106">Also, drivers might handle exceptions differently, based on the capabilities of the device.</span></span>

<span data-ttu-id="7fc6a-107">Sehen Sie sich beispielsweise die folgenden Befehle an, die mithilfe der Funktion " [**mciSendString**](/previous-versions//dd757161(v=vs.85)) " an einen Waveform-Audiotreiber gesendet werden:</span><span class="sxs-lookup"><span data-stu-id="7fc6a-107">For example, consider the following commands sent to a waveform-audio driver using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function:</span></span>


```C++
mciSendString("open sound.wav alias sound", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("play sound notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("record sound from 0 notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="7fc6a-108">Der [**Datensatz**](record.md) -Befehl gibt einen Wert vom Typ "Parameter außerhalb des gültigen Bereichs" zurück und beendet die Wiedergabe, die vom vorherigen [**Wiedergabe**](play.md) Befehl gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="7fc6a-108">The [**record**](record.md) command returns a "Parameter out of range" value and stops the playback started by the previous [**play**](play.md) command.</span></span> <span data-ttu-id="7fc6a-109">Möglicherweise wird davon ausgegangen, dass der Treiber den Datensatz-Befehl überprüft, bevor die Wiedergabe beendet wird</span><span class="sxs-lookup"><span data-stu-id="7fc6a-109">One might expect the driver to validate the record command before stopping playback, but the driver stops the playback first.</span></span>

 

 