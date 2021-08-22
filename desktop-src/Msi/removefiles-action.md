---
description: Die Aktion RemoveFiles entfernt Dateien, die zuvor von der InstallFiles-Aktion installiert wurden.
ms.assetid: 1079be89-515c-443e-8927-46ddf7891a59
title: RemoveFiles-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b50e23a7d2eb3c9bb23575d83d000b053f0de06907541777e43b5476f8c722ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626450"
---
# <a name="removefiles-action"></a>RemoveFiles-Aktion

Die Aktion RemoveFiles entfernt Dateien, die zuvor von der [InstallFiles-Aktion](installfiles-action.md) installiert wurden. Jede dieser Dateien wird durch einen Link zu einem Eintrag in der [Tabelle Komponente](component-table.md) geschlossen. Nur dateien mit Komponenten, die entweder in den *MsiInstallStateAbsent-Zustand* oder in den *msiInstallStateLocal-Zustand* aufgelöst wurden, wenn die Komponente lokal installiert ist, werden entfernt.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die [InstallValidate-Aktion](installvalidate-action.md) muss aufgerufen werden, bevor RemoveFiles aufgerufen wird. Wenn eine [InstallFiles-Aktion](installfiles-action.md) verwendet wird, muss sie nach RemoveFiles angezeigt werden.

## <a name="actiondata-messages"></a>ActionData-Nachrichten



| Feld | Beschreibung der Aktionsdaten                    |
|-------|-----------------------------------------------|
| \[1\] | Bezeichner der entfernten Datei.                   |
| \[9\] | Bezeichner des Verzeichnisses, das die entfernte Datei enthält. |



 

## <a name="remarks"></a>Hinweise

Die [RemoveFile-Tabelle](removefile-table.md) kann aus der Installer-Datenbank weggelassen werden, wenn keine anderen Dateien entfernt werden müssen.

Die Aktion RemoveFiles kann auch vom Autor angegebene Dateien entfernen, die nicht von der InstallFiles-Aktion installiert werden. Diese Dateien werden in der [Tabelle RemoveFile](removefile-table.md) angegeben. Jede dieser Dateien wird durch einen Link zu einem Eintrag in der [Tabelle Komponente](component-table.md) geschlossen. Die Dateien, deren Komponenten in einen beliebigen aktiven Aktionsstatus aufgelöst werden (d. h. nicht im Aus- oder NULL-Zustand), werden entfernt, wenn die Datei im angegebenen Verzeichnis vorhanden ist. Das Entfernen von Dateien, die in der RemoveFile-Tabelle angegeben sind, wird versucht, wenn die verknüpfte Komponente zum ersten Mal installiert wird, während einer Neuinstallation und erneut, wenn die verknüpfte Komponente entfernt wird.

Die Aktion RemoveFiles kann auch Ordner entfernen. Ein leerer Ordner wird entfernt, wenn der Wert in der FileName-Spalte der RemoveFile-Tabelle NULL ist.

Wenn Sie zuvor installierte Dateien entfernen, fragt die RemoveFiles-Aktion die gleichen Felder in denselben Tabellen ab wie die von der [InstallFiles-Aktion](installfiles-action.md) abgefragten Felder, mit der Ausnahme, dass die [Media-Tabelle](media-table.md) nicht von der RemoveFiles-Aktion verwendet wird.

Der Zieldateiname kann in lokalisierten Text in der FileName -Spalte der RemoveFile-Tabelle angegeben werden.

 

 



