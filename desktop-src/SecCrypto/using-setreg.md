---
description: Das SetReg-Tool legt den Wert der Registrierungsschlüssel fest, die das Verhalten des Authenticode-Zertifikatüberprüfungsprozesses steuern.
ms.assetid: c34c00fe-da99-4c2e-9e9a-0ef6406ae5ae
title: Verwenden von SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0de37d236b978217d8c2a713e9595fbaad70afb69beb32cd0f5200738d2d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896737"
---
# <a name="using-setreg"></a>Verwenden von SetReg

Das SetReg-Tool legt den Wert der Registrierungsschlüssel fest, die das Verhalten des Authenticode-Zertifikatüberprüfungsprozesses steuern. Diese Schlüssel, die als Schlüssel für den Softwareveröffentlichungsstatus bezeichnet werden, steuern, ob einem Teststamm vertraut werden soll, lassen die Offlinegenehmigung von Zertifikaten zu, testen das Ablaufdatum des Zertifikats und führen Sperrprüfungen durch.

Der folgende Befehl listet die Syntax und Optionen für die Verwendung von SetReg auf.

**setreg -?**

Mit dem folgenden Befehl wird ein Teststamm als vertrauenswürdig eingestuft. Standardmäßig ist ein Teststamm nicht vertrauenswürdig. Nachdem Änderungen an den Schlüsselwerten vorgenommen wurden, wird eine Liste mit dem aktuellen Wert aller Schlüsselwerte angezeigt. Wenn die **Option -q** verwendet wird, werden die Schlüsselwerte nicht angezeigt.

**setreg 1 TRUE**

Mit dem folgenden Befehl wird ein Teststamm nicht vertrauenswürdig und bewirkt, dass alle Überprüfungen auf Sperrung überprüft werden. Die **Option -q** wird verwendet, damit die Liste der Schlüsselwerte nicht angezeigt wird.

**setreg -q 1 FALSE 3 TRUE**

> [!Note]  
> Bei Befehlen, Optionen und Argumenten wird die Kleinschreibung nicht beachtet.

 

 

 



