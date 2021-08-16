---
description: Die IsolateComponents-Aktion installiert eine Kopie einer Komponente (üblicherweise eine freigegebene DLL) an einem privaten Speicherort zur Verwendung durch eine bestimmte Anwendung (in der Regel ein .exe).
ms.assetid: 3f39ad5d-5539-48cc-8369-bd4d3127fbdd
title: IsolateComponents-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2919a026fb8243d7f2f73bc856390865ea3bed19e228da780e39f9dce68bc3f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629733"
---
# <a name="isolatecomponents-action"></a>IsolateComponents-Aktion

Die IsolateComponents-Aktion installiert eine Kopie einer Komponente (üblicherweise eine freigegebene DLL) an einem privaten Speicherort zur Verwendung durch eine bestimmte Anwendung (in der Regel ein .exe). Dadurch wird die Anwendung von anderen Kopien der Komponente isoliert, die möglicherweise an einem freigegebenen Speicherort auf dem Computer installiert werden. Weitere Informationen finden Sie unter [Isolierte Komponenten.](isolated-components.md)

Die Aktion bezieht sich auf jeden Datensatz der [Tabelle IsolatedComponent](isolatedcomponent-table.md) und ordnet die Dateien der Komponente, die im Feld Komponente freigegeben aufgeführt ist, \_ der Komponente zu, die im Feld Komponentenanwendung aufgeführt \_ ist. Das Installationsprogramm installiert die Dateien von Component \_ Shared in demselben Verzeichnis wie die \_ Komponentenanwendung. Das Installationsprogramm generiert eine Datei in diesem Verzeichnis mit einer Länge von 0 Byte, wobei der kurze Dateiname der Schlüsseldatei für \_ komponentenanwendung (in der Regel ist dies derselbe Dateiname wie der .exe) mit .local angefügt wird. Die IsolatedComponent-Aktion wirkt sich nicht auf die Installation der \_ Komponentenanwendung aus. Durch das Deinstallieren der \_ Komponentenanwendung werden auch die \_ freigegebenen Komponentendateien und die LOKALE DATEI aus dem Verzeichnis entfernt.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die IsolateComponents-Aktion kann nur in der [Tabelle InstallUISequence](installuisequence-table.md) und der [Tabelle InstallExecuteSequence](installexecutesequence-table.md)verwendet werden. Diese Aktion muss nach der [CostInitialize-Aktion](costinitialize-action.md) und vor der [CostFinalize-Aktion](costfinalize-action.md)erfolgen.

## <a name="actiondata-messages"></a>ActionData-Nachrichten

Es sind keine ActionData-Meldungen vorhanden.

## <a name="remarks"></a>Hinweise

Wenn die Spalte Bedingung für die IsolateComponents-Aktion zu True ausgewertet wird oder leer gelassen wird, isoliert das Installationsprogramm alle Komponenten, die in der [Tabelle IsolatedComponent](isolatedcomponent-table.md)aufgeführt sind. Wenn die Spalte Bedingung als False ausgewertet wird, ignoriert das Installationsprogramm die Tabelle IsolatedComponent und gibt die üblichen Komponenten gemeinsam. Die [**RedirectedDllSupport-Eigenschaft**](redirecteddllsupport.md) kann verwendet werden, um diese Aktion zu bedingungslos zu machen. Weitere Informationen finden Sie unter [Verwenden einer Sequenztabelle.](using-a-sequence-table.md)

 

 



