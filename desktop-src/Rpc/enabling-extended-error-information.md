---
title: Aktivieren erweiterter Fehlerinformationen
description: Erweiterte Fehlerinformationen für Remote Prozedur Aufruf (RPC) werden aktiviert.
ms.assetid: 73b72d0a-8533-40ac-8b41-8af4d60f9631
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd6579069c840d8f6dba5a9cd0e0d4edc831f6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207017"
---
# <a name="enabling-extended-error-information"></a>Aktivieren erweiterter Fehlerinformationen

Führen Sie die folgenden Schritte aus, um erweiterte Fehlerinformationen zu aktivieren:

Öffnen Sie die Richtlinie für den lokalen Computer mithilfe der Schnittstelle gpeer dit. msc.

Navigieren Sie zu der Richtlinie, die unter Computer Konfiguration/administrative Vorlagen/System/remote Prozedur Aufruf/RPC-Problembehandlung bei der Problembehandlung/Weitergabe erweiterter Fehlerinformationen

Aktivieren Sie die Richtlinie, und legen Sie die Feld Weitergabe **Erweiterter Fehlerinformationen** auf "on" fest.

Durch diesen Vorgang wird die Weitergabe erweiterter Fehlerinformationen für alle Prozesse auf dem Computer eingeschaltet.

Um erweiterte Fehlerinformationen nur für bestimmte Prozesse auf einem Computer zu aktivieren oder um nur bestimmte Prozesse auf dem Computer zu deaktivieren, verwenden Sie die Optionen **off with Exceptions** oder **on with Exceptions** . Beide Optionen verwenden das Feld **Erweiterte Fehler Informations Ausnahmen** , um anzugeben, welche Prozesse die Standardeinstellung aufweisen und welche Prozesse das Gegenteil der Standardeinstellung aufweisen. **Ausnahmen für erweiterte Fehlerinformationen** enthalten eine Liste von Prozessnamen.

Wenn die Befehlszeile eines Prozesses mit einer Zeichenfolge beginnt, die in den **erweiterten Fehler Informations Ausnahmen** vorliegt, empfängt der Prozess das Gegenteil der Standardeinstellung. Wenn Sie z. b. möchten, dass der gesamte Prozess auf dem Computer erweiterte Fehlerinformationen (mit Ausnahme von LSASS) und den Prozess mit dem Namen **Secure Server** weitergibt, legen Sie die Weitergabe **Erweiterter Fehlerinformationen** **auf mit Ausnahmen** fest, und geben Sie im Feld **Erweiterte Fehler Informations Ausnahmen** die folgende Zeichenfolge ein: LSASS "Secure Server".

Zeichen folgen können in doppelte Anführungszeichen eingeschlossen werden. Dies ist jedoch optional, wenn die Zeichenfolge keine Leerzeichen enthält. Außerdem kann der Anfang der Verarbeitungs Befehlszeile angegeben werden. Wenn beispielsweise in der Weitergabe **von erweiterten Fehlerinformationen** das Feld **aus mit Ausnahmen** angegeben wird und im Feld **Ausnahmen für erweiterte Fehlerinformationen** Folgendes angegeben ist: Win.

Jeder Prozess, der mit "Win" beginnt, überträgt erweiterte Fehlerinformationen. Auf vielen Computern werden diese Prozesse beispielsweise winlogon.exe und WINWORD.EXE.

 

 




