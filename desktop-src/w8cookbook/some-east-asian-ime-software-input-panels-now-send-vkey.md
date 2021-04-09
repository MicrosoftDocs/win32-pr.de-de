---
title: Einige ostasiatische IME-Software Eingabe Panels senden jetzt VKey.
description: Einige ostasiatische IME-Software Eingabe Panels senden jetzt VKey.
ms.assetid: 5E3BE112-D962-4C11-B31E-229584191FAE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c444091e4498582cccc4378dfa2f17216cbf810
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103857012"
---
# <a name="some-east-asian-ime-software-input-panels-now-send-vkey"></a>Einige ostasiatische IME-Software Eingabe Panels senden jetzt VKey.

## <a name="platforms"></a>Plattformen

<dl> Clients-Windows 8.1  
Server-Windows Server 2012 R2  
</dl>

## <a name="description"></a>BESCHREIBUNG

Wenn in Windows 8 eine der ostasiatischen IMEs ausgewählt ist, hat das Drücken eines Software Eingabe Panel-Schlüssels keine vkeys gesendet.

In Windows 8.1 werden vkeys für die folgenden Konfigurationen gesendet:



| Sprache            | IME                                 | Windows Store | Desktop |
|---------------------|-------------------------------------|---------------|---------|
| Chinesisch (vereinfacht)  | Microsoft Pinyin, Microsoft Wubi    | Ja           | Ja     |
| Chinesisch (traditionell) | Microsoft changlie, Microsoft Quick | Ja           | Ja     |
| Chinesisch (traditionell) | Microsoft Bopomofo                  | Nein            | Nein      |
| Koreanisch              | Microsoft-IME                       | Ja           | Nein      |
| Japanisch            | Microsoft-IME                       | Nein            | Nein      |



 

## <a name="manifestations"></a>Kundgebungen

Wenn der Benutzer eine IME auswählt, die keine vkeys sendet, funktionieren von VKey ausgelöste Funktionen nicht.

## <a name="solution"></a>Lösung

Anwendungen, die keine der obigen IME-Konfigurationen verwenden, müssen so entworfen werden, dass Benutzer die gewünschte Aufgabe ohne Verwendung von Funktionen, die vkeys erfordern, durchführen können.

Wenn der Benutzer eine IME auswählt, die vkeys sendet, aber die Anwendung ohne diese Erwartung entworfen wurde, muss die Anwendung so geändert werden, dass Sie erkennt, welche Version von Windows ausgeführt wird, und entsprechend reagieren.

 

 




