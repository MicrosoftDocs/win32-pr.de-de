---
description: Weitere Informationen finden Sie unter Erweiterbare Storage-Engine-Systemparameter.
title: Erweiterbare Storage-Engine-Systemparameter
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
ms.openlocfilehash: 531e599c66279312f80216f1eb09fc612636821227e76f3572645ab6b4ee5137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118256447"
---
# <a name="extensible-storage-engine-system-parameters"></a>Erweiterbare Storage-Engine-Systemparameter


_**Gilt für:** Windows | Windows Server_

## <a name="extensible-storage-engine-system-parameters"></a>Erweiterbare Storage-Engine-Systemparameter

Die folgenden Konstanten werden als Werte für den *par parameters* der [JetGetSystemParameter-](./jetgetsystemparameter-function.md) und [JetSetSystemParameter-Funktionen](./jetsetsystemparameter-function.md) verwendet.

  - [Sicherungs- und Wiederherstellungsparameter](./backup-and-restore-parameters.md)

  - [Rückrufparameter](./callback-parameters.md)

  - [Datenbankparameter](./database-parameters.md)

  - [Parameter des Datenbankcaches](./database-cache-parameters.md)

  - [Fehlerbehandlungsparameter](./error-handling-parameters.md)

  - [Ereignisprotokollparameter](./event-log-parameters.md)

  - [E/A-Parameter](./i-o-parameters.md)

  - [Indexparameter](./index-parameters.md)

  - [Informationsparameter](./informational-parameters.md)

  - [Metaparameter](./meta-parameters.md)

  - [Ressourcenparameter](./resource-parameters.md)

  - [Temporäre Datenbankparameter](./temporary-database-parameters.md)

  - [Transaktionsprotokollparameters](./transaction-log-parameters.md)

### <a name="system-parameter-description-format"></a>Beschreibungsformat des Systemparameters

Jeder Systemparameter wird im folgenden Format beschrieben:

JET_paramX

Beschreibung des JET_paramX Systemparameters.

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
<td><p>Die rechtlichen Werte für den Parameter.</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Ist der Parameter global oder pro Instanz?</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p></td>
<td><p>Kann der Parameter festgelegt werden, wenn Instanzen vorhanden sind?</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Kann der Parameter bei der Initialisierung festgelegt werden?</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Wirkt sich der Parameter auf die Dateien auf dem Datenträger aus?</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Wirkt sich der Parameter auf die Zuverlässigkeit der Engine aus?</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf die Leistung aus:</p></td>
<td><p>Wirkt sich der Parameter auf die Engine-Leistung aus?</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf Ressourcen aus:</p></td>
<td><p>Wirkt sich der Parameter auf Engine-Ressourcen aus?</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Releases von Windows, die den Parameter unterstützen.</p></td>
</tr>
</tbody>
</table>
