---
description: Das SetReg-Tool legt den Wert der Registrierungsschlüssel fest, die das Verhalten des Authenticode-Zertifikatüberprüfungsprozesses steuern.
ms.assetid: 6c456a59-ee6c-420d-b075-7de8bd2fd8ff
title: Setreg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5267aa140cad713e550ddf8afd0281d489bdd90ac0b26a7f7a4781240ecac24c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900300"
---
# <a name="setreg"></a>Setreg

Das SetReg-Tool legt den Wert der Registrierungsschlüssel fest, die das Verhalten des Authenticode-Zertifikatüberprüfungsprozesses steuern. Diese Schlüssel werden als Schlüssel für den Softwareveröffentlichungsstatus bezeichnet. Nach Abschluss der angeforderten Aktion zeigt das Tool den aktuellen Status der Schlüssel für den Softwareveröffentlichungsstatus an.

**SetReg** \[ *Optionen* \] \[ *Choice \#* {**TRUE** \| **FALSE**}\]

Das Set Registry-Tool ist nur im .NET Framework SDK 1.0 und .1.1 enthalten, das Sie aus dem [Microsoft Download Center herunterladen können.](https://www.microsoft.com/download/details.aspx?id=16217)

## <a name="options"></a>Optionen

Die Optionen können einen der folgenden Werte haben. Die in der folgenden Tabelle angegebenen Optionen können nur mit Internet Explorer 4.0 oder höher verwendet werden.



| Option | BESCHREIBUNG                                                                                                                                            |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-q** | Unterdrücken Sie die Anzeige der Schlüsselwerte für den Softwareveröffentlichungszustand, nachdem SetReg die angeforderte Aktion abgeschlossen hat. Die Werte werden standardmäßig angezeigt. |
| **-?** | Listet die Befehlssyntax und Optionen auf.                                                                                                                       |



 

## <a name="choice-"></a>Wahl \#

*Auswahl \#* muss einer der folgenden Werte sein.



| Auswahl | BESCHREIBUNG                                                                                                                       | Ergebnis                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------|-----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **1**  | Vertrauen des Teststamms                                                                                                               | Dieser Wert wird ignoriert. **Windows XP/2000:** True **gibt an,** dass einem Teststamm vertraut. Dies entspricht der Ausführung von "regedit wvtston.reg" in Internet Explorer 3. *x*.<br/> Der Standardwert ist **FALSE.** Dateien, die mit einem Teststamm signiert sind, werden nur überprüft, wenn dieses Flag auf **TRUE festgelegt ist.** Beachten Sie, dass sich dieses Verhalten bei Windows XP mit Service Pack 1 (SP1) geändert hat, da Windows XP mit SP1 diesen Wert ignoriert.<br/> <br/> |
| **2**  | Verwenden des Ablaufdatums für Zertifikate                                                                                               | True **gibt an,** dass das Ablaufdatum des Zertifikats überprüft wird. Um Ablaufdaten zu ignorieren, legen Sie dieses Flag auf **FALSE fest.** Der Standardwert ist **TRUE.**                                                                                                                                                                                                                                                                                                       |
| **3**  | Überprüfen der [ *Sperrliste*](../secgloss/c-gly.md) | True **gibt an,** dass die Sperrprüfung ausführt. Um die Sperrprüfung zu umgehen, legen Sie dieses Flag auf **FALSE fest.** Der Standardwert ist **TRUE.** **Internet Explorer 3. *x*:** Der Standardwert ist **FALSE.**<br/>                                                                                                                                                                                                                                               |
| **4**  | Offlinesperrserver OK (einzeln)<br/>                                                                              | True **gibt an,** dass die Offlinegenehmigung für einzelne Zertifikate möglich ist. Der Standardwert ist **FALSE.**                                                                                                                                                                                                                                                                                                                                                 |
| **5**  | Offlinesperrserver OK (kommerzieller Modus)<br/>                                                                              | True **gibt an,** dass die Offlinegenehmigung für kommerzielle Zertifikate möglich ist. Der Standardwert ist **TRUE.**                                                                                                                                                                                                                                                                                                                                                  |
| **6**  | Java-Offlinesperrserver OK (einzeln)<br/>                                                                         | True **gibt an,** dass die Offlinegenehmigung für einzelne Zertifikate zulässt und die Benutzeroberfläche für fehlerhafte Zertifikate nicht angezeigt wird. Der Standardwert ist **FALSE.**                                                                                                                                                                                                                                                                                    |
| **7**  | Java-Offlinesperrserver OK (commercial)<br/>                                                                         | True **gibt an,** dass die Offlinegenehmigung für kommerzielle Zertifikate zulässt und die Benutzeroberfläche für fehlerhafte Zertifikate nicht angezeigt wird. Der Standardwert ist **TRUE.**                                                                                                                                                                                                                                                                                     |
| **8**  | Ungültige signierte Objekte der Version 1                                                                                     | True **gibt an,** dass signierte Objekte der Version 1 nicht mehr gültig sind. Der Standardwert ist **FALSE.**                                                                                                                                                                                                                                                                                                                                                      |
| **9**  | Überprüfen der Sperrliste des Zeitstempelservers                                                                                | True **gibt an,** dass die Sperrprüfung für das Zertifikat des Zeitstempelservers ausgeführt wird. Der Standardwert ist **FALSE.** **Internet Explorer 3. *x:*** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                            |
| **10** | Nur vertrauenswürdige Elemente, die in der Vertrauensdatenbank gefunden wurden                                                                                      | True **gibt an,** dass Downloads von Herausgebern zulässt, die in der Persönlichen Vertrauensdatenbank enthalten sind. Der Standardwert ist **FALSE.** **Internet Explorer 3. *x:*** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                             |



 

 

 
