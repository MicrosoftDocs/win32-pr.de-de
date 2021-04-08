---
description: Das setreg-Tool legt den Wert der Registrierungsschlüssel fest, die das Verhalten der Authenticode-Zertifikat Überprüfung steuern.
ms.assetid: 6c456a59-ee6c-420d-b075-7de8bd2fd8ff
title: SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05da29d3eddf7e04ba5bd735e1032f388d9d204a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749568"
---
# <a name="setreg"></a>SetReg

Das setreg-Tool legt den Wert der Registrierungsschlüssel fest, die das Verhalten der Authenticode-Zertifikat Überprüfung steuern. Diese Schlüssel werden als Software Veröffentlichungs Zustands Schlüssel bezeichnet. Nachdem die angeforderte Aktion abgeschlossen ist, zeigt das Tool den aktuellen Zustand der Software Veröffentlichungs Zustands Schlüssel an.

**ABG** \[ *Optionen* \] \[ *Auswahl \#* {**true** \| **false**}\]

Das Registrierungs Tool festlegen wird nur mit der .NET Framework SDK-Version 1,0 und 1,1 ausgeliefert, die Sie aus dem [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=16217)herunterladen können.

## <a name="options"></a>Optionen

Die Optionen können einen der folgenden Werte aufweisen: Die in der folgenden Tabelle angegebenen Optionen können nur mit Internet Explorer 4,0 oder höher verwendet werden.



| Option | BESCHREIBUNG                                                                                                                                            |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-q** | Hiermit wird die Anzeige der Zustands Schlüsselwerte für den Software Publishing unterdrückt, nachdem die angeforderte Aktion von der Abmeldung abgeschlossen wurde. Die Werte werden standardmäßig angezeigt. |
| **-?** | Auflisten der Befehlssyntax und-Optionen.                                                                                                                       |



 

## <a name="choice-"></a>Wahl \#

*Auswahl \#* muss einen der folgenden Werte aufweisen.



| Auswahl | BESCHREIBUNG                                                                                                                       | Ergebnis                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------|-----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **1**  | Dem Test Stamm Vertrauen                                                                                                               | Dieser Wert wird ignoriert. **Windows XP/2000:** **True** gibt an, dass einem Test Stamm vertraut wird. Dies entspricht der Ausführung von "regedit wvtston. reg" in Internet Explorer 3. *x*.<br/> Der Standardwert ist **false**. Jede mit einem Test Stamm signierte Datei wird nicht überprüft, es sei denn, dieses Flag ist auf **true** festgelegt. Beachten Sie, dass sich dieses Verhalten in Windows XP mit Service Pack 1 (SP1) geändert hat, da dieser Wert von Windows XP mit SP1 ignoriert wird.<br/> <br/> |
| **2**  | Ablaufdatum für Zertifikate verwenden                                                                                               | Wenn der Wert **true** ist, wird das Ablaufdatum des Zertifikats überprüft. Legen Sie dieses Flag auf **false** fest, um Ablaufdaten zu ignorieren. Der Standardwert ist " **true**".                                                                                                                                                                                                                                                                                                       |
| **3**  | Überprüfen der Sperr [ *Liste*](../secgloss/c-gly.md) | Wenn **true**, wird die Sperr Überprüfung durchführt. Legen Sie dieses Flag auf **false** fest, um die Sperr Überprüfung zu umgehen. Der Standardwert ist " **true**". **Internet Explorer 3. *x*:** der Standardwert ist **false**.<br/>                                                                                                                                                                                                                                               |
| **4**  | Offline Sperr Server OK (einzeln)<br/>                                                                              | Wenn der Wert **true** ist, wird die Offline Genehmigung für einzelne Zertifikate ermöglicht. Der Standardwert ist **false**.                                                                                                                                                                                                                                                                                                                                                 |
| **5**  | Offline Sperr Server OK (kommerziell)<br/>                                                                              | Bei " **true**" wird die Offline Genehmigung für kommerzielle Zertifikate ermöglicht. Der Standardwert ist " **true**".                                                                                                                                                                                                                                                                                                                                                  |
| **6**  | Java-Offline Sperr Server OK (einzeln)<br/>                                                                         | Wenn der Wert **true** ist, wird die Offline Genehmigung für einzelne Zertifikate ermöglicht, und die Benutzeroberfläche für ungültige Zertifikate wird nicht angezeigt. Der Standardwert ist **false**.                                                                                                                                                                                                                                                                                    |
| **7**  | Java-Offline Sperr Server OK (kommerziell)<br/>                                                                         | Wenn der Wert **true** ist, wird die Offline Genehmigung für kommerzielle Zertifikate ermöglicht, und die Benutzeroberfläche für ungültige Zertifikate wird nicht angezeigt. Der Standardwert ist " **true**".                                                                                                                                                                                                                                                                                     |
| **8**  | Signierte Objekte der Version 1 nicht mehr gültig machen                                                                                     | **True** gibt an, dass Version 1 signierte Objekte nicht mehr gültig ist. Der Standardwert ist **false**.                                                                                                                                                                                                                                                                                                                                                      |
| **9**  | Überprüfen Sie die Sperr Liste des Zeitstempel Servers.                                                                                | Wenn der Wert **true** ist, wird die Sperr Überprüfung für das Zertifikat des Zeitstempel Servers durchführt. Der Standardwert ist **false**. **Internet Explorer 3. *x*:** dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                            |
| **10** | Nur Vertrauens Elemente in der Vertrauensstellungs Datenbank gefunden                                                                                      | Bei " **true**" werden Downloads von Verlegern zugelassen, die in der persönlichen Vertrauensstellungs Datenbank enthalten sind. Der Standardwert ist **false**. **Internet Explorer 3. *x*:** dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                             |



 

 

 
