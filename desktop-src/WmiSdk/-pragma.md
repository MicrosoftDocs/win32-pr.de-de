---
description: Ähnelt einem Befehls Zeilenschalter. Sie müssen jedoch nicht \# jedes Mal, wenn Sie eine MOF-Datei kompilieren, einen pragma-Befehl erneut eingeben.
ms.assetid: 3cf22686-dd56-43a3-9584-3d707a20a3a0
ms.tgt_platform: multiple
title: '#pragma'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ae13d5f960e0b415f34dce97a40cff6cba8056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353929"
---
# <a name="pragma"></a>\#pragma

Der **\# pragma** -Präprozessorbefehl ähnelt einem Befehls Zeilenschalter. Sie müssen jedoch nicht jedes Mal, wenn Sie eine MOF-Datei kompilieren, einen **\# pragma** -Befehl erneut eingeben. Im folgenden Beispiel wird die **\# pragma** -Befehlssyntax veranschaulicht:


```mof
#pragma [command]
```



Normalerweise platzieren Sie einen **\# pragma** -Befehl am Anfang einer MOF-Datei. Sie können jedoch einige Befehle, z. b. den **\# pragma** -Befehl, im Text Ihres MOF-Codes platzieren. Das folgende Beispiel zeigt **\# pragma** -Befehle, die dem MOF-Compiler zeigen, dass Sie Klassen und Instanzen im root \\ CIMV2-Namespace platzieren und die Datei kompilieren müssen, in der die Befehle bei der Wiederherstellung des Repository enthalten sind:


```mof
#pragma autorecover
#pragma namespace ("\\\\.\\root\\cimv2")
```



Im folgenden werden die verfügbaren **\# pragma** -Befehle aufgeführt.



| Get-Help                                         | BESCHREIBUNG                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**trag**](pragma-amendment.md)           | Weist den MOF-Compiler an, eine MOF-Datei in sprachneutrale und sprachspezifische Versionen aufzuteilen. |
| [**Auto Wiederherstellen**](pragma-autorecover.md)       | Fügt eine MOF-Datei zur Liste der Dateien hinzu, die während der Wiederherstellung des Repository kompiliert wurden.                             |
| [**classflags**](pragma-classflags.md)         | Steuert die Art und Weise, wie Klassen abhängig von den angegebenen Flags erstellt oder aktualisiert werden.                     |
| [**deleteclass**](pragma-deleteclass.md)       | Löscht eine vorhandene Klasse und deren Instanzen aus dem Repository.                                      |
| [**DeleteInstance**](pragma-deleteinstance.md) | Löscht eine vorhandene Instanz einer Klasse aus dem Repository.                                          |
| [**instanceflags**](pragma-instanceflags.md)   | Steuert die Art und Weise, in der Instanzen abhängig von den angegebenen Flags erstellt oder aktualisiert werden.                   |
| [**namespace**](pragma-namespace.md)           | Fordert an, dass der Compiler die MOF-Datei in den Namespace lädt, der als *Wert von NamespacePath* angegeben ist.         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präprozessorbefehle](preprocessor-commands.md)
</dt> </dl>

 

 



