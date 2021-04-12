---
description: Weitere Informationen finden Sie in den System Parametern für Extensible Storage Engine.
title: System Parameter für Extensible Storage Engine
TOCTitle: Extensible Storage Engine System Parameters
ms:assetid: f95c2e87-b25e-4be5-8c17-8486ba37dad4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294139(v=EXCHG.10)
ms:contentKeyID: 32765753
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43473f1bf5f599ba8efd06bd31345485acc07061
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527989"
---
# <a name="extensible-storage-engine-system-parameters"></a>System Parameter für Extensible Storage Engine


_**Gilt für:** Windows | Windows Server_

## <a name="extensible-storage-engine-system-parameters"></a>System Parameter für Extensible Storage Engine

Die folgenden Konstanten werden als Werte für den *paramID* -Parameter der Funktionen [jetgetsystemparameter](./jetgetsystemparameter-function.md) und [jetsetsystemparameter](./jetsetsystemparameter-function.md) verwendet.

  - [Sicherungs-und Wiederherstellungs Parameter](./backup-and-restore-parameters.md)

  - [Rückruf Parameter](./callback-parameters.md)

  - [Datenbankparameter](./database-parameters.md)

  - [Daten Bank Cache Parameter](./database-cache-parameters.md)

  - [Fehler Behandlungsparameter](./error-handling-parameters.md)

  - [Ereignisprotokoll Parameter](./event-log-parameters.md)

  - [I/O-Parameter](./i-o-parameters.md)

  - [Indexparameter](./index-parameters.md)

  - [Informations Parameter](./informational-parameters.md)

  - [Meta-Parameter](./meta-parameters.md)

  - [Ressourcenparameter](./resource-parameters.md)

  - [Temporäre Daten Bank Parameter](./temporary-database-parameters.md)

  - [Transaktionsprotokollparameters](./transaction-log-parameters.md)

### <a name="system-parameter-description-format"></a>Systemparameterbeschreibungs-Format

Jeder Systemparameter wird im folgenden Format beschrieben:

JET_paramX

Die Beschreibung des JET_paramX System Parameters.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>Der Standardwert des Parameters.</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Der Datentyp des Parameters.</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>Die zulässigen Werte für den Parameter.</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Ist der Parameter Global oder pro Instanz?</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Kann der Parameter festgelegt werden, wenn Instanzen vorhanden sind?</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Kann der Parameter bei der Initialisierung festgelegt werden?</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Wirkt sich der Parameter auf die Dateien auf dem Datenträger aus?</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
<td><p>Wirkt sich der Parameter auf die Engine-Zuverlässigkeit aus?</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Wirkt sich der Parameter auf die Engine-Leistung aus?</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Wirkt sich der Parameter auf Engine-Ressourcen aus?</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Versionen von Windows, die den-Parameter unterstützen.</p></td>
</tr>
</tbody>
</table>
