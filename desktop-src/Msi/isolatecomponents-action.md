---
description: Die isolatecomponents-Aktion installiert eine Kopie einer Komponente (in der Regel eine freigegebene DLL) an einem privaten Speicherort, der von einer bestimmten Anwendung (i. a. exe) verwendet wird.
ms.assetid: 3f39ad5d-5539-48cc-8369-bd4d3127fbdd
title: Isolatecomponents-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fe36f8c30e67591662ca2fce6c0b0ac2150ebb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348979"
---
# <a name="isolatecomponents-action"></a>Isolatecomponents-Aktion

Die isolatecomponents-Aktion installiert eine Kopie einer Komponente (in der Regel eine freigegebene DLL) an einem privaten Speicherort, der von einer bestimmten Anwendung (i. a. exe) verwendet wird. Dadurch wird die Anwendung von anderen Kopien der Komponente isoliert, die möglicherweise an einem freigegebenen Speicherort auf dem Computer installiert ist. Weitere Informationen finden Sie unter [isolierte Komponenten](isolated-components.md).

Die Aktion bezieht sich auf jeden Datensatz der [isolatedcomponent-Tabelle](isolatedcomponent-table.md) und ordnet die Dateien der Komponente, die im Feld für die freigegebene Komponente aufgeführt sind, der Komponente zu, die \_ im Feld Komponenten Anwendung aufgelistet ist \_ . Das Installationsprogramm installiert die Dateien der-Komponente, die \_ in demselben Verzeichnis wie die Komponenten Anwendung freigegeben werden \_ . Das Installationsprogramm generiert eine Datei in diesem Verzeichnis mit einer Länge von 0 (null) Bytes, wobei der kurze Dateiname der Schlüsseldatei für die Komponenten \_ Anwendung (in der Regel der Dateiname der exe-Datei) mit dem Namen. local vorhanden ist. Die isolatedcomponent-Aktion wirkt sich nicht auf die Installation der Komponenten \_ Anwendung aus. Beim Deinstallieren \_ der Komponenten Anwendung werden auch die frei \_ gegebenen Komponenten Dateien und die lokale Datei aus dem Verzeichnis entfernt.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die isolatecomponents-Aktion kann nur in der Tabelle [InstallUISequence](installuisequence-table.md) und in der [Tabelle InstallExecuteSequence](installexecutesequence-table.md)verwendet werden. Diese Aktion muss nach der [Aktion "costinitialize](costinitialize-action.md) " und vor der [Aktion "costfinalize](costfinalize-action.md)" erfolgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

## <a name="remarks"></a>Bemerkungen

Wenn die Spalte Bedingung für die isolatecomponents-Aktion als true ausgewertet wird oder leer gelassen wird, isoliert das Installationsprogramm alle in der [isolatedcomponent-Tabelle](isolatedcomponent-table.md)aufgeführten Komponenten. Wenn die Spalte Bedingung als false ausgewertet wird, wird die isolatedcomponent-Tabelle vom Installationsprogramm ignoriert, und die Komponenten werden normalerweise gemeinsam freigelegt. Die [**redirecteddllsupport**](redirecteddllsupport.md) -Eigenschaft kann verwendet werden, um diese Aktion zu bedinieren. Weitere Informationen finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).

 

 



