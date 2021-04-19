---
description: Die RemoveFiles-Aktion entfernt Dateien, die zuvor von der InstallFiles-Aktion installiert wurden.
ms.assetid: 1079be89-515c-443e-8927-46ddf7891a59
title: RemoveFiles-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174e477d512401c8ff6f1ff091b7c67f26e86f16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349348"
---
# <a name="removefiles-action"></a>RemoveFiles-Aktion

Die RemoveFiles-Aktion entfernt Dateien, die zuvor von der [InstallFiles](installfiles-action.md) -Aktion installiert wurden. Jede dieser Dateien wird durch einen Link zu einem Eintrag in der [Komponenten](component-table.md) Tabelle abgegrenzt. Nur die Dateien, deren Komponenten entweder in den Zustand " *msiinstallstatemissing* " oder " *msiinstallstatelocal* " aufgelöst werden, wenn die Komponente lokal installiert ist, werden entfernt.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die [InstallValidate](installvalidate-action.md) -Aktion muss vor dem Aufrufen von RemoveFiles aufgerufen werden. Wenn eine [InstallFiles](installfiles-action.md) -Aktion verwendet wird, muss Sie nach RemoveFiles angezeigt werden.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                    |
|-------|-----------------------------------------------|
| \[1\] | Bezeichner der entfernten Datei.                   |
| \[9\] | Der Bezeichner des Verzeichnisses, das die entfernte Datei enthält. |



 

## <a name="remarks"></a>Bemerkungen

Die Tabelle " [RemoveFile](removefile-table.md) " kann aus der Installer-Datenbank weggelassen werden, wenn keine anderen Dateien entfernt werden müssen.

Mit der Aktion RemoveFiles können auch vom Autor angegebene Dateien entfernt werden, die nicht von der InstallFiles-Aktion installiert werden. Diese Dateien werden in der Tabelle " [RemoveFile](removefile-table.md) " angegeben. Jede dieser Dateien wird durch einen Link zu einem Eintrag in der [Komponenten](component-table.md) Tabelle abgegrenzt. Die Dateien, deren Komponenten in einen aktiven Aktionszustand aufgelöst werden (d. h. nicht in den Status OFF oder NULL), werden entfernt, wenn die Datei im angegebenen Verzeichnis vorhanden ist. Es wird versucht, die in der Tabelle "RemoveFile" angegebenen Dateien zu entfernen, wenn die verknüpfte Komponente zum ersten Mal installiert wird, während einer Neuinstallation und erneut, wenn die verknüpfte Komponente entfernt wird.

Mit der Aktion RemoveFiles können auch Ordner entfernt werden. Wenn der Wert in der Dateiname-Spalte der RemoveFile-Tabelle NULL ist, wird ein leerer Ordner entfernt.

Beim Entfernen zuvor installierter Dateien werden die gleichen Felder in denselben Tabellen abgefragt, die von der [InstallFiles](installfiles-action.md) -Aktion abgefragt wurden, mit der Ausnahme, dass die [Medien Tabelle](media-table.md) nicht von der RemoveFiles-Aktion verwendet wird.

Der Ziel Dateiname kann in lokalisiertem Text in der Dateiname-Spalte der RemoveFile-Tabelle angegeben werden.

 

 



