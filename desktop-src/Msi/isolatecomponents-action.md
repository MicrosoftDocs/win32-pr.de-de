---
description: Die Aktion IsolateComponents installiert eine Kopie einer Komponente (im Allgemeinen eine freigegebene DLL) an einem privaten Speicherort zur Verwendung durch eine bestimmte Anwendung (in der Regel eine .exe).
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

Die Aktion IsolateComponents installiert eine Kopie einer Komponente (im Allgemeinen eine freigegebene DLL) an einem privaten Speicherort zur Verwendung durch eine bestimmte Anwendung (in der Regel eine .exe). Dadurch wird die Anwendung von anderen Kopien der Komponente isoliert, die an einem freigegebenen Speicherort auf dem Computer installiert werden können. Weitere Informationen finden Sie unter [Isolierte Komponenten.](isolated-components.md)

Die Aktion bezieht sich auf jeden Datensatz der [IsolatedComponent-Tabelle](isolatedcomponent-table.md) und ordnet die Dateien der Komponente, die im Feld Freigegebene Komponente aufgeführt sind, der komponente zu, die im Feld \_ Komponentenanwendung \_ aufgeführt ist. Das Installationsprogramm installiert die Dateien von Component \_ Shared im gleichen Verzeichnis wie die \_ Komponentenanwendung. Das Installationsprogramm generiert eine Datei in diesem Verzeichnis mit einer Länge von 0 Bytes, bei der der kurze Dateiname der Schlüsseldatei für die Komponentenanwendung (in der Regel der gleiche Dateiname wie die .exe) mit \_ .local angefügt wird. Die IsolatedComponent-Aktion wirkt sich nicht auf die Installation der Komponentenanwendung \_ aus. Durch das Deinstallieren \_ der Komponentenanwendung werden auch die freigegebenen \_ Komponentendateien und die LOCAL-Datei aus dem Verzeichnis entfernt.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die IsolateComponents-Aktion kann nur in der [InstallUISequence-Tabelle](installuisequence-table.md) und der [InstallExecuteSequence-Tabelle verwendet werden.](installexecutesequence-table.md) Diese Aktion muss nach der [CostInitialize-Aktion](costinitialize-action.md) und vor der [CostFinalize-Aktion stehen.](costfinalize-action.md)

## <a name="actiondata-messages"></a>ActionData-Meldungen

Es sind keine ActionData-Meldungen enthalten.

## <a name="remarks"></a>Hinweise

Wenn die Spalte Bedingung für die Aktion IsolateComponents als TRUE ausgewertet wird oder leer gelassen wird, isoliert das Installationsprogramm alle Komponenten, die in der [IsolatedComponent-Tabelle aufgeführt sind.](isolatedcomponent-table.md) Wenn die Spalte Bedingung falseist, ignoriert das Installationsprogramm die Tabelle IsolatedComponent und gibt die Komponenten wie gewohnt weiter. Die [**RedirectedDllSupport-Eigenschaft**](redirecteddllsupport.md) kann verwendet werden, um diese Aktion bedingungsbar zu machen. Weitere Informationen finden Sie unter [Verwenden einer Sequenztabelle.](using-a-sequence-table.md)

 

 



