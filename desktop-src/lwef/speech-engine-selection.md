---
title: Sprachmodul Auswahl
description: Sprachmodul Auswahl
ms.assetid: f5afedc6-093f-4247-a5c8-277d6b2d646c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a548f0201ba37c8acb867091cc690a913277ff06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855979"
---
# <a name="speech-engine-selection"></a>Sprachmodul Auswahl

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Die Sprach-ID-Einstellung eines Zeichens bestimmt die Standardsprache für die Spracheingabe. Der Microsoft-Agent fordert SAPI für ein installiertes Modul an, das dieser Sprache entspricht. Wenn eine Client Anwendung keine Spracheinstellung angibt, versucht der Microsoft-Agent, eine Spracherkennungs-Engine zu finden, die mit der Benutzer-ID der Standardsprache übereinstimmt (unter Verwendung der Hauptsprachen-ID, der Nebensprachen-ID). Wenn keine Engine verfügbar ist, die dieser Sprache entspricht, ist die Sprache für dieses Zeichen deaktiviert.

Sie können auch eine bestimmte Spracherkennungs-Engine anfordern, indem Sie die zugehörige Modus-ID angeben (mithilfe der Eigenschaft " [**srmodeid**](srmodeid-property.md) " des Zeichens). Wenn die Sprachen-ID für diese Modus-ID jedoch nicht mit der Spracheinstellung des Clients identisch ist, schlägt der-Befehl fehl (es wird ein Fehler im-Steuerelement ausgegeben). Die Spracherkennungs-Engine verbleibt dann vom Client die letzte erfolgreich festgelegte Engine, oder, wenn keine, die Engine, die mit der aktuellen Systemsprachen-ID übereinstimmt. Wenn es immer noch keine Entsprechung gibt, ist die Spracheingabe für diesen Client nicht verfügbar.

Der Microsoft-Agent lädt automatisch eine Spracherkennungs-Engine, wenn die Spracheingabe durch einen Benutzer initiiert wird, der den lauschenden Hotkey drückt, oder wenn der Input-Active Client die [**Abhör Methode aufruft**](listen-method.md) . Eine Engine kann jedoch auch geladen werden, wenn Sie die Mode-ID festlegen oder Abfragen, die Eigenschaften des Fensters "Sprachbefehle" festlegen oder Abfragen, [**srstatus**](srstatus-property.md)Abfragen oder die Sprache aktiviert ist und der Benutzer die Spracheingabe Seite der erweiterten Zeichen Optionen anzeigt. Der Microsoft-Agent lädt jedoch nur die Sprach-Engines, die von Clients verwendet werden.

 

 




