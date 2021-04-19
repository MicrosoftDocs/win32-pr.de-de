---
title: Dateien werden gesucht
description: Standardmäßig sucht RC nach Header Dateien und Ressourcen Dateien (z. b. Symbol-und Cursor Dateien) zuerst im aktuellen Verzeichnis und dann in den Verzeichnissen, die durch die include-Umgebungsvariable angegeben werden.
ms.assetid: 6c8c905d-b0f6-4665-9a93-62617ff30137
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078a04a4cf2f3461d03c7026e0f1d73d8fd38665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342073"
---
# <a name="searching-for-files"></a>Dateien werden gesucht

Standardmäßig sucht RC nach Header Dateien und Ressourcen Dateien (z. b. Symbol-und Cursor Dateien) zuerst im aktuellen Verzeichnis und dann in den Verzeichnissen, die durch die include-Umgebungsvariable angegeben werden. (Die PATH-Umgebungsvariable hat keine Auswirkung darauf, welche Verzeichnisse RC durchsucht.)

## <a name="adding-a-directory-to-search"></a>Hinzufügen eines zu suchenden Verzeichnisses

Sie können die **/i** -Option verwenden, um ein Verzeichnis zur Liste der Verzeichnisse RC-Suchvorgänge hinzuzufügen. Der Compiler durchsucht dann die Verzeichnisse in der folgenden Reihenfolge:

1.  Das aktuelle Verzeichnis
2.  Das Verzeichnis oder die Verzeichnisse, die Sie mithilfe der **/i** -Option angeben, in der Reihenfolge, in der Sie in der RC-Befehlszeile angezeigt werden.
3.  Die Liste der von der INCLUDE-Umgebungsvariablen angegebenen Verzeichnisse in der Reihenfolge, in der Sie von der Variablen aufgelistet werden, es sei denn, Sie geben die Option **/x** an.

Im folgenden Beispiel wird die Ressourcen Definitionsdatei MyApp. RC kompiliert:

**RC/i c: \\ Source \\ stuff/i d: \\ Ressourcen MyApp. RC**

Beim Kompilieren des Skripts MyApp. RC sucht RC zunächst im aktuellen Verzeichnis nach Header Dateien und Ressourcen Dateien, dann in C: \\ Quell \\ Sachen und D: \\ Ressourcen und dann in den Verzeichnissen, die durch die include-Umgebungsvariable angegeben werden.

## <a name="ignoring-the-include-environment-variable"></a>Die include-Umgebungs Variable wird ignoriert.

Sie können verhindern, dass RC die include-Umgebungsvariable verwendet, wenn Sie die zu durchsuchenden Verzeichnisse ermitteln. Verwenden Sie hierzu die Option **/x** . Der Compiler sucht dann nur im aktuellen Verzeichnis und in den Verzeichnissen, die Sie mithilfe der **/i** -Option angeben, nach Dateien.

Mit dem folgenden Befehl wird die Skriptdatei "MyApp. RC" kompiliert:

**RC/x/i c: \\ Source \\ Sachen MyApp. RC**

Beim Kompilieren des Skripts MyApp. RC sucht RC zunächst im aktuellen Verzeichnis nach Header Dateien und Ressourcen Dateien und dann in C: \\ Source \\ . Die von der INCLUDE-Umgebungsvariablen angegebenen Verzeichnisse werden nicht durchsucht.

 

 




