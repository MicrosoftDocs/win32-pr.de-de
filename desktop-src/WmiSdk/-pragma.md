---
description: Ähnelt einem Befehlszeilenschalter. Sie müssen jedoch nicht jedes Mal, wenn Sie eine MOF-Datei kompilieren, einen \# Pragmabefehl erneut ausführen.
ms.assetid: 3cf22686-dd56-43a3-9584-3d707a20a3a0
ms.tgt_platform: multiple
title: '#pragma'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3cb9541ceef51119ce521244282920ca88397afe13290e99bdc14ce7d98ab55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860560"
---
# <a name="pragma"></a>\#Pragma

Der **\# Pragma-Präprozessorbefehl** ähnelt einem Befehlszeilenschalter. Sie müssen jedoch nicht jedes Mal, wenn Sie eine MOF-Datei kompilieren, einen **\# Pragmabefehl** erneut ausführen. Das folgende Beispiel veranschaulicht die **Pragmabefehlssyntax: \#**


```mof
#pragma [command]
```



In der Regel platzieren Sie **\# einen Pragmabefehl** am Anfang einer MOF-Datei. Sie können jedoch einige Befehle, z. B. **\# den Pragmabefehl,** im Text des MOF-Codes platzieren. Das folgende Beispiel zeigt **\# Pragmabefehle,** die dem MOF-Compiler zeigen, dass Klassen und Instanzen im Cimv2-Stammnamespace gespeichert und die Datei kompiliert werden muss, in der die Befehle während der Repositorywiederherstellung enthalten \\ sind:


```mof
#pragma autorecover
#pragma namespace ("\\\\.\\root\\cimv2")
```



Im Folgenden werden die verfügbaren **\# Pragmabefehle** aufgeführt.



| Befehl                                         | BESCHREIBUNG                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**Änderung**](pragma-amendment.md)           | Leitet den MOF-Compiler an, eine MOF-Datei in sprachneutrale und sprachspezifische Versionen zu trennen. |
| [**Autowiederherstellen**](pragma-autorecover.md)       | Fügt der Liste der Dateien, die während der Repositorywiederherstellung kompiliert wurden, eine MOF-Datei hinzu.                             |
| [**classflags**](pragma-classflags.md)         | Steuert, wie Klassen in Abhängigkeit von den angegebenen Flags erstellt oder aktualisiert werden.                     |
| [**deleteclass**](pragma-deleteclass.md)       | Löscht eine vorhandene Klasse und ihre Instanzen aus dem Repository.                                      |
| [**deleteinstance**](pragma-deleteinstance.md) | Löscht eine vorhandene Instanz einer Klasse aus dem Repository.                                          |
| [**instanceflags**](pragma-instanceflags.md)   | Steuert die Art und Weise, wie Instanzen erstellt oder aktualisiert werden, abhängig von den angegebenen Flags.                   |
| [**Namespace**](pragma-namespace.md)           | Fordert an, dass der Compiler die MOF-Datei in den als *namespacepath angegebenen Namespace laden soll.*         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präprozessorbefehle](preprocessor-commands.md)
</dt> </dl>

 

 



