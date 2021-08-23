---
title: Suchen nach Dateien
description: Standardmäßig sucht RC zuerst im aktuellen Verzeichnis und dann in den von der INCLUDE-Umgebungsvariablen angegebenen Verzeichnissen nach Header- und Ressourcendateien (z. B. Symbol- und Cursordateien).
ms.assetid: 6c8c905d-b0f6-4665-9a93-62617ff30137
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4fecaa3c20c9bedf498c30462d5e139da83f11d45a47c6d5e7554adb8ed325b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601560"
---
# <a name="searching-for-files"></a>Suchen nach Dateien

Standardmäßig sucht RC zuerst im aktuellen Verzeichnis und dann in den von der INCLUDE-Umgebungsvariablen angegebenen Verzeichnissen nach Header- und Ressourcendateien (z. B. Symbol- und Cursordateien). (Die PATH-Umgebungsvariable hat keine Auswirkungen darauf, welche Verzeichnisse RC durchsucht.)

## <a name="adding-a-directory-to-search"></a>Hinzufügen eines Verzeichnisses zur Suche

Sie können die Option **/i verwenden,** um der Liste der Verzeichnisse RC-Suchvorgänge ein Verzeichnis hinzuzufügen. Der Compiler durchsucht dann die Verzeichnisse in der folgenden Reihenfolge:

1.  Das aktuelle Verzeichnis
2.  Das Verzeichnis oder die Verzeichnisse, die Sie mithilfe der **Option /i** angeben, in der Reihenfolge, in der sie in der RC-Befehlszeile angezeigt werden
3.  Die Liste der Verzeichnisse, die von der INCLUDE-Umgebungsvariablen in der Reihenfolge angegeben werden, in der sie von der Variablen aufgeführt werden, es sei denn, Sie geben die **Option /x** an.

Im folgenden Beispiel wird die Ressourcendefinitionsdatei MyApp.rc kompiliert:

**rc /i c: \\ source \\ stuff /i d: \\ resources myapp.rc**

Beim Kompilieren des Skripts MyApp.rc sucht RC zuerst im aktuellen Verzeichnis nach Headerdateien und Ressourcendateien, dann in C: Source Stuff und D: Resources und dann in den verzeichnissen, die von der INCLUDE-Umgebungsvariablen angegeben \\ \\ \\ werden.

## <a name="ignoring-the-include-environment-variable"></a>Ignorieren der INCLUDE-Umgebungsvariablen

Sie können verhindern, dass RC die INCLUDE-Umgebungsvariable verwendet, wenn Sie die zu durchsuchenden Verzeichnisse bestimmen. Verwenden Sie dazu die Option **/x.** Der Compiler sucht dann nur im aktuellen Verzeichnis und in allen Verzeichnissen, die Sie mithilfe der **Option /i angeben, nach** Dateien.

Der folgende Befehl kompiliert die Skriptdatei MyApp.rc:

**rc /x /i c: \\ source \\ stuff myapp.rc**

Beim Kompilieren des Skripts MyApp.rc sucht RC zuerst im aktuellen Verzeichnis und dann in C: Source Stuff nach Header- und \\ \\ Ressourcendateien. Die von der INCLUDE-Umgebungsvariablen angegebenen Verzeichnisse werden nicht durchsucht.

 

 




