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
# <a name="default-behavior-of-drivers"></a>Standardverhalten von Treibern

In vielen Fällen definieren die MCI-Befehls Spezifikationen die Standardwerte und das Verhalten für Treiber eines bestimmten Gerätetyps. Da multimediaregeräte über eine Vielzahl von Features (und Einschränkungen) verfügen können, kann es zu undefiniertem Verhalten kommen. Außerdem können Ausnahmen auf der Grundlage der Funktionen des Geräts anders behandelt werden.

Sehen Sie sich beispielsweise die folgenden Befehle an, die mithilfe der Funktion " [**mciSendString**](/previous-versions//dd757161(v=vs.85)) " an einen Waveform-Audiotreiber gesendet werden:


```C++
mciSendString("open sound.wav alias sound", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("play sound notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("record sound from 0 notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



Der [**Datensatz**](record.md) -Befehl gibt einen Wert vom Typ "Parameter außerhalb des gültigen Bereichs" zurück und beendet die Wiedergabe, die vom vorherigen [**Wiedergabe**](play.md) Befehl gestartet wurde. Möglicherweise wird davon ausgegangen, dass der Treiber den Datensatz-Befehl überprüft, bevor die Wiedergabe beendet wird

 

 