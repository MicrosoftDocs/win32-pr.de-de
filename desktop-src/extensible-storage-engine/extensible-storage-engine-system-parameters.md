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
ms.openlocfilehash: 501f98ec1b360e3eaa10988c140f30b86dcacb5a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987343"
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


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>Der Standardwert des Parameters.</p> | 
| <p>Typ:</p> | <p>Der Datentyp des Parameters.</p> | 
| <p>Gültiger Bereich:</p> | <p>Die rechtlichen Werte für den Parameter.</p> | 
| <p>Umfang:</p> | <p>Ist der Parameter global oder pro Instanz?</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Kann der Parameter festgelegt werden, wenn Instanzen vorhanden sind?</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Kann der Parameter bei der Initialisierung festgelegt werden?</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Wirkt sich der Parameter auf die Dateien auf dem Datenträger aus?</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Wirkt sich der Parameter auf die Zuverlässigkeit der Engine aus?</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Wirkt sich der Parameter auf die Engine-Leistung aus?</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Wirkt sich der Parameter auf Engine-Ressourcen aus?</p> | 
| <p>Verfügbarkeit:</p> | <p>Releases von Windows, die den -Parameter unterstützen.</p> | 

