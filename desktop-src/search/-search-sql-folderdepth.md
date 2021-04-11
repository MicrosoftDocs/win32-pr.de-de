---
description: Ordner Tiefe-Prädikate steuern den Bereich einer Suche, indem Sie einen Pfad angeben und angeben, ob eine Tiefe oder eine flache Durchquerung durchlaufen werden soll.
ms.assetid: 8eadbd42-3538-412e-9bf8-b2355d23437e
title: Bereichs-und Verzeichnis Prädikate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2418b2149a5bf05bd000460c787b7f967856c5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128548"
---
# <a name="scope-and-directory-predicates"></a>Bereichs-und Verzeichnis Prädikate

Ordner Tiefe-Prädikate steuern den Bereich einer Suche, indem Sie einen Pfad angeben und angeben, ob eine Tiefe oder eine flache Durchquerung durchlaufen werden soll. Das folgende Beispiel zeigt die Syntax der Ordner Tiefe-Prädikate:


```
... WHERE [{SCOPE | DIRECTORY}='<protocol>:[{SID}]<path>']
```



Auf das Prädikat folgt ein Gleichheitszeichen. Der Pfad wird in einfache Anführungszeichen eingeschlossen und muss mit einem Protokoll und einem Doppelpunkt beginnen (z `file:` . b `mapi:` ., oder `csc:` ). Das Bereichs Prädikat führt einen tiefen Durchlauf des Pfads aus, einschließlich aller Unterordner, während das Verzeichnis Prädikat nur einen flachen Durchlauf des angegebenen Ordners ausführt. Wie andere Structured Query Language (SQL)-Einschränkungen können Sie mehr als eine Ordner tiefen Einschränkung in einer einzelnen Abfrage angeben.

Um den lokalen Katalog eines Remote Computers abzufragen, müssen Sie den Computernamen vor dem Katalog und einen Universal Naming Convention (UNC)-Pfad auf dem Remote Computer in der Scope-oder Directory-Klausel einschließen.

## <a name="examples"></a>Beispiele


```
SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Reports'

SELECT System.ItemName FROM SystemIndex WHERE DIRECTORY='file:C:/Files/Reports' 

SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Published' OR SCOPE='file:C:/Files/Reports' AND NOT SCOPE='file:C:/Files/Reports/Confidential'

SELECT System.ItemName FROM zarasmachine.SystemIndex WHERE SCOPE='file://zarasmachine/C:/Files/Reports'

SELECT System.ItemURL FROM SystemIndex WHERE SCOPE='mapi://{S-1-5-21-2117521111-1604012920-1887927527-2285604}/Mailbox user/' AND CONTAINS('Microsoft')
```



Im ersten Bereichs Beispiel wird der Ordner "C: \\ Dateien \\ Berichte" und alle zugehörigen Unterordner durchsucht. Im Verzeichnis Beispiel werden nur der Stamm Ordner C: \\ Files-Berichte durchsucht \\ .

> [!Note]  
> Die umgekehrten Schrägstriche () des Dateisystems \\ werden zu einem URL-Schrägstrich (manchmal auch als Schrägstriche bezeichnet) (/).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[FROM-Klausel](-search-sql-from.md)
</dt> <dt>

[WHERE-Klausel](-search-sql-where.md)
</dt> </dl>

 

 



