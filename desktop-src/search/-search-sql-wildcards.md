---
description: Das enthält-Prädikat unterstützt die Verwendung des Sternchen ( \* ) als Platzhalter Zeichen zum Darstellen von Wörtern und Ausdrücken. Das Sternchen kann nur am Ende des Worts oder Ausdrucks hinzugefügt werden. Wenn das Sternchen vorhanden ist, wird der Modus für die Präfix Übereinstimmung aktiviert.
ms.assetid: 9d141c7a-a721-416e-aa61-dabdb6533462
title: Verwenden von Platzhalter Zeichen im enthält-Prädikat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013e49f97cf23c7a00aca7bb287edd19951520f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128525"
---
# <a name="using-wildcard-characters-in-the-contains-predicate"></a>Verwenden von Platzhalter Zeichen im enthält-Prädikat

Das enthält-Prädikat unterstützt die Verwendung des Sternchen ( \* ) als Platzhalter Zeichen zum Darstellen von Wörtern und Ausdrücken. Das Sternchen kann nur am Ende des Worts oder Ausdrucks hinzugefügt werden. Wenn das Sternchen vorhanden ist, wird der Modus für die Präfix Übereinstimmung aktiviert. In diesem Modus werden Übereinstimmungen zurückgegeben, wenn in der Spalte das angegebene Suchwort gefolgt von NULL oder mehr anderen Zeichen enthalten ist. Wenn ein Ausdruck bereitgestellt wird, werden Übereinstimmungen erkannt, wenn die Spalte alle angegebenen Wörter mit 0 (null) oder mehr anderen Zeichen nach dem letzten Wort enthält.

## <a name="examples"></a>Beispiele

Im ersten Beispiel werden Dokumente mit einem beliebigen Wort in der Dateiname-Spalte, beginnend mit "Serv", abgeglichen. Beispiele für übereinstimmende Wörter sind "Server", "Server" und "Service".


```
...WHERE CONTAINS(System.FileName, '"serv*"')
```



Im zweiten Beispiel werden Dokumente mit einem beliebigen Ausdruck in der Dateiname-Spalte abgeglichen, der mit "Comp" beginnt und in dem das nächste Wort mit "Serv" beginnt. Beispiele für übereinstimmende Wörter sind "Comp Server", "Comp Servers" und "Comp Service".


```
...WHERE CONTAINS(System.FileName, '"comp serv*"')
```



Das Sternchen funktioniert nur für Präfix Vergleiche und kann nur am Ende des Worts oder Ausdrucks eingefügt werden. Es funktioniert nicht für Suffixvergleiche. Die folgende Syntax ist ungültig und entspricht nicht den Dokumenten mit einem Wort in der Dateiname-Spalte, die mit "Service" enden.


```
WHERE CONTAINS(System.FileName, '"*serve"')
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Frei Text Prädikat](-search-sql-freetext.md)
</dt> <dt>

[WHERE-Klausel](-search-sql-where.md)
</dt> </dl>

 

 



