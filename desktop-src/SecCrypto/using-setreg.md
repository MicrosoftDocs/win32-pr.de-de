---
description: Das setreg-Tool legt den Wert der Registrierungsschlüssel fest, die das Verhalten der Authenticode-Zertifikat Überprüfung steuern.
ms.assetid: c34c00fe-da99-4c2e-9e9a-0ef6406ae5ae
title: Verwenden von "abtreg"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706463f86d38a03bc3416713be7427df55424d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130237"
---
# <a name="using-setreg"></a>Verwenden von "abtreg"

Das setreg-Tool legt den Wert der Registrierungsschlüssel fest, die das Verhalten der Authenticode-Zertifikat Überprüfung steuern. Diese Schlüssel, die als Software Publishing State Keys bezeichnet werden, Steuern, ob Sie einem Test Stamm Vertrauen, die Offline Genehmigung von Zertifikaten zulassen, Ablaufdaten für das Zertifikat testen und Sperr Überprüfungen durchführen.

Der folgende Befehl listet die Syntax und die Optionen für die Verwendung von "*" auf.

**-?**

Mit dem folgenden Befehl wird ein Test Stamm als vertrauenswürdig eingestuft. Standardmäßig ist ein Test Stamm nicht vertrauenswürdig. Nachdem alle Änderungen an den Schlüsselwerten vorgenommen wurden, wird eine Liste mit dem aktuellen Wert aller Schlüsselwerte angezeigt. Wenn die Option **-q** verwendet wird, werden die Schlüsselwerte nicht angezeigt.

**Eing 1 true**

Der folgende Befehl erstellt einen Test Stamm als nicht vertrauenswürdig und bewirkt, dass die Überprüfung auf die Sperrung überprüft wird. Die Option " **-q** " wird verwendet, sodass die Liste der Schlüsselwerte nicht angezeigt wird.

**Protokoll-q 1 false 3 true**

> [!Note]  
> Bei Befehlen, Optionen und Argumenten wird die Groß-/Kleinschreibung nicht beachtet.

 

 

 



