---
description: Ordnertiefeprädikate steuern den Bereich einer Suche, indem sie einen Pfad angeben und angeben, ob ein tiefer oder flacher Durchlauf ausgeführt werden soll.
ms.assetid: 8eadbd42-3538-412e-9bf8-b2355d23437e
title: SCOPE- und DIRECTORY-Prädikate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f221ba4048f1ab7f5096321cc00aed209acb5ca3e5616e6e6a4fbbc516dfc28b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462469"
---
# <a name="scope-and-directory-predicates"></a>SCOPE- und DIRECTORY-Prädikate

Ordnertiefeprädikate steuern den Bereich einer Suche, indem sie einen Pfad angeben und angeben, ob ein tiefer oder flacher Durchlauf ausgeführt werden soll. Im Folgenden wird die Syntax der Ordnertiefeprädikate veranschaulicht:


```
... WHERE [{SCOPE | DIRECTORY}='<protocol>:[{SID}]<path>']
```



Auf das Prädikat folgt ein Gleichheitszeichen. Der Pfad ist in einfachen Anführungszeichen enthalten und muss mit einem Protokoll und einem Doppelpunkt (z. B. `file:` , `mapi:` oder ) `csc:` beginnen. Das SCOPE-Prädikat führt einen tiefen Durchlauf des Pfads aus, einschließlich aller Unterordner, während das DIRECTORY-Prädikat einen flachen Durchlauf nur des angegebenen Ordners durchführt. Wie bei anderen strukturierte Abfragesprache -Einschränkungen (SQL) können Sie in einer einzelnen Abfrage mehrere Einschränkungen für die Ordnertiefe angeben.

Um den lokalen Katalog eines Remotecomputers abzufragen, fügen Sie den Computernamen vor dem Katalog und einen UNC-Pfad (Universal Naming Convention) auf dem Remotecomputer in die SCOPE- oder DIRECTORY-Klausel ein.

## <a name="examples"></a>Beispiele


```
SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Reports'

SELECT System.ItemName FROM SystemIndex WHERE DIRECTORY='file:C:/Files/Reports' 

SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Published' OR SCOPE='file:C:/Files/Reports' AND NOT SCOPE='file:C:/Files/Reports/Confidential'

SELECT System.ItemName FROM zarasmachine.SystemIndex WHERE SCOPE='file://zarasmachine/C:/Files/Reports'

SELECT System.ItemURL FROM SystemIndex WHERE SCOPE='mapi://{S-1-5-21-2117521111-1604012920-1887927527-2285604}/Mailbox user/' AND CONTAINS('Microsoft')
```



Im ersten SCOPE-Beispiel werden der Ordner C: \\ Files Reports und alle \\ zugehörigen Unterordner durchsucht. Im DIRECTORY-Beispiel wird nur der Stammordner C: \\ Files Reports durchsucht. \\

> [!Note]  
> Die umgekehrten Schrägstriche des Dateisystems \\ () werden zu einem SCHRÄGSTRICH im URL-Stil (manchmal als Schrägstriche bezeichnet) (/).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[FROM-Klausel](-search-sql-from.md)
</dt> <dt>

[WHERE-Klausel](-search-sql-where.md)
</dt> </dl>

 

 



