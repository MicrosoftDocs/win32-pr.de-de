---
description: Predictive Dialing ist eine Anwendung, die in der Regel auf einem Callcenter-Telefonieserver ausgeführt wird.
ms.assetid: c8d0b2b5-61eb-4ab0-b09d-c54c282b730e
title: Predictive Dialing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d930a0a49751c7f1851600e277d2cf201f0acbe1a9da3f7be5aa9f2e4b38439c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060598"
---
# <a name="predictive-dialing"></a>Predictive Dialing

Predictive Dialing ist eine Anwendung, die in der Regel auf einem Callcenter-Telefonieserver ausgeführt wird. Sie verwendet eine Liste von Telefonnummern, die häufig aus einer Datenbank ermittelt werden, um ausgehende Anrufe zu versuchen. Wenn ein Aufruf abgeschlossen *ist,* wird der Aufruf automatisch einem Agent für die Verarbeitung zugewiesen. Die Anwendung kann einen  Vorhersagewahlport auf einem Switch verwenden. Dabei handelt es sich um ein Gerät, das ausgehende Anrufe tätigen kann und über besondere Fähigkeiten (über DSP und so weiter) verfügt, um Anrufstatustons und andere akustische Hinweise auf den Anrufzustand zu erkennen. Wenn ein Anruf an einem Vorhersagewahlport erfolgt, wird er in der Regel automatisch auf ein anderes Gerät auf dem Switch übertragen, wenn der Anruf einen bestimmten Zustand erreicht oder wenn ein bestimmter Medientyp erkannt wird. Dieses Zielgerät kann eine Warteschlange für Agents sein, die ausgehende Aufrufe behandeln.

Anwendungen identifizieren ein Gerät als Vorhersagewahlfunktion durch das LINEADDRCAPFLAGS \_ PREDICTIVEDIALER-Bit im **dwAddrCapFlags-Member** in [**LINEADDRESSCAPS.**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) Das **dwPredictiveAutoTransferStates-Mitglied** in **LINEADDRESSCAPS** gibt die Zustände an, in denen der Vorhersagewahlport zur automatischen Übertragung eines Anrufs aufgefordert werden kann. Wenn dieser Member 0 (null) ist, bedeutet dies, dass die automatische Übertragung nicht verfügbar ist und dass die Anwendung dafür verantwortlich ist, Aufrufe explizit zu übertragen, wenn der entsprechende Aufrufzustand (oder Medientyp oder andere Kriterien) erkannt wird. Vorzugsweise stellen Switchhersteller sowohl die automatische als auch die manuelle Übertragung zur Verfügung und ermöglichen es Anwendungen, den bevorzugten Mechanismus auszuwählen. Dienstanbieter müssten jedoch das Verhalten von Legacygeräten modellieren. Ein einzelner Vorhersagewählport (Gerät/Adresse der Linie) kann mehrere ausgehende Aufrufe gleichzeitig unterstützen, wie durch **das dwMaxNumActiveCalls-Mitglied** in **LINEADDRESSCAPS angegeben.** Die Funktion für predictive dialing kann auch auf jedem Gerät zur Verfügung gestellt werden, indem ein gemeinsamer Pool von Signalprozessoren für die Vorhersagewählfunktion verwendet wird, die auf Anforderung auf die Wählverbindung überbrückt werden.

Wenn die [**lineMakeCall-Funktion**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) in einer Linie verwendet wird, die predictive dialing kann (ein Port mit dem Set LINEADDRCAPFLAGS PREDICTIVEDIALER), und predictive dialing mit \_ LINECALLPARAMFLAGS PREDICTIVEDIAL angefordert wird, erfolgt der Aufruf auf prädiktive Weise mit verbesserter Erkennung des Status des \_ akustischen Anrufs. Zusätzliche Felder und Konstanten werden in der [**LINECALLPARAMS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) definiert, die an **lineMakeCall** übergeben wird, um das Verhalten des Vorhersagewahlports zu steuern. Das **dwPredictiveAutoTransferStates-Member** gibt den Zeilenaufruf an, der angibt, dass der Vorhersagewahlport beim Eingang des Aufrufs automatisch den Aufruf an das angegebene Ziel übertragen soll (die Bits müssen eine ordnungsgemäße Teilmenge der unterstützten automatischen Übertragungszustände sein, die in [**LINEADDRESSCAPS angegeben**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)sind). Die Anwendung kann das Feld auf 0 festlegen, wenn sie den Aufrufzustand selbst überwachen und [**lineBlindTransfer**](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer) verwenden möchte, um den Aufruf zu übertragen, wenn die gewünschte Bedingung erreicht wird. Die Anwendung muss die gewünschte Adresse angeben, an die der Aufruf automatisch im Variablenfeld übertragen werden soll, das von **den Membern dwTargetAddressSize** und **dwTargetAddressOffset** in **LINECALLPARAMS** definiert wird.

Anwendungen können auch ein Timeout für ausgehende Aufrufe festlegen, sodass der Dienstanbieter sie automatisch in einen nicht verbundenen Zustand über geht, wenn sie nicht beantwortet werden. Dies wird mithilfe des **dwNoAnswerTimeout-Mitglieds** in [**LINECALLPARAMS gesteuert.**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)

 

 



