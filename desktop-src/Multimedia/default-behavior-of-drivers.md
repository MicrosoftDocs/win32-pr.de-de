---
title: Standardverhalten von Treibern
description: Standardverhalten von Treibern
ms.assetid: ed6905eb-67ad-421d-be00-4a5585dff7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61312010759ddd1bf152f0e51f7605bda1954329096913b61dac14a671908f0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144523"
---
# <a name="default-behavior-of-drivers"></a>Standardverhalten von Treibern

In vielen Situationen definieren die MCI-Befehlsspezifikationen die Standardwerte und das Verhalten für Treiber eines bestimmten Gerätetyps. Da Multimediageräte eine Vielzahl von Features (und Einschränkungen) aufweisen können, kann es nicht definierte Verhaltensbereiche geben. Außerdem können Treiber Ausnahmen basierend auf den Funktionen des Geräts unterschiedlich behandeln.

Betrachten Sie beispielsweise die folgenden Befehle, die mithilfe der [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) an einen Waveform-Audiotreiber gesendet werden:


```C++
mciSendString("open sound.wav alias sound", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("play sound notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("record sound from 0 notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



Der [**Datensatzbefehl**](record.md) gibt den Wert "Parameter außerhalb des Bereichs" zurück und beendet die Wiedergabe, die mit dem vorherigen [**Wiedergabebefehl**](play.md) gestartet wurde. Es kann erwartet werden, dass der Treiber den Aufzeichnungsbefehl überprüft, bevor die Wiedergabe beendet wird, aber der Treiber beendet die Wiedergabe zuerst.

 

 