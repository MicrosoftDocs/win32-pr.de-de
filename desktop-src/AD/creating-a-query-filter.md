---
title: Erstellen eines Abfrage Filters
description: Ein Abfrage Filter weist Active Directory Domain Services an, Daten in einer LDAP-Abfrage Syntax zu suchen. Alle angegebenen Datenzugriffs Technologien, die im Thema auswählen der Suchtechnologie aufgeführt sind, unterstützen die LDAP-Abfrage Syntax.
ms.assetid: 0bd652f0-41a6-4a0d-8742-9d6a2a7f168a
ms.tgt_platform: multiple
keywords:
- Active Directory Beispiele Active Directory, Erstellen eines Abfrage Filters
- Abfrage Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2e0a4e4a02312fcc9affb681407044ba0d8e18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855203"
---
# <a name="creating-a-query-filter"></a>Erstellen eines Abfrage Filters

Ein Abfrage Filter weist Active Directory Domain Services an, Daten in einer LDAP-Abfrage Syntax zu suchen. Alle angegebenen Datenzugriffs Technologien, die im Thema [Auswählen der Suchtechnologie](choosing-the-search-technology.md) aufgeführt sind, unterstützen die LDAP-Abfrage Syntax.

Die LDAP-Abfrage Syntax lautet wie folgt:


```C++
<expression><expression>...
```



Ein Filter kann einen oder mehrere Ausdrücke enthalten. Ein Ausdruck weist die folgende Form auf:


```C++
(<logicaloperator><comparison><comparison...>)
```



dabei &lt; ist "logischeroperator &gt; " einer der folgenden:



| Operator        | Beschreibung                |
|-----------------|----------------------------|
| "\|"<br/> | Logisches **or**<br/>  |
| "&"<br/>  | Logisches **and**<br/> |
| "!"<br/>  | Logisches **Not**<br/> |



 

und " &lt; Vergleich &gt; " ist Folgendes:


```C++
(<attribute><operator><value>)
```



Dabei ist " &lt; Attribute &gt; " der **ldapDisplayName** des auszuwertenden Attributs &lt; . "Value &gt; " ist der Wert, mit dem verglichen werden soll, und " &lt; Operator &gt; " ist einer der folgenden Vergleichs Operatoren.



| Operator           | BESCHREIBUNG                         |
|--------------------|-------------------------------------|
| "="<br/>     | Equals<br/>                   |
| "~="<br/>    | Ungefähr Gleichheits<br/>     |
| "<="<br/> | Kleiner als oder gleich<br/>    |
| ">="<br/> | Größer als oder gleich<br/> |



 

Außerdem kann der Wert "Value" abhängig von der Attribut Syntax das Platzhalter &lt; &gt; Symbol (" \* ") enthalten. Ein " &lt; Wert &gt; ", der nur einen Platzhalter enthält, prüft, ob ein Wert in " &lt; Attribute &gt; " vorhanden ist. Wenn kein Wert für "Attribute" festgelegt ist &lt; &gt; , schlägt der Test fehl.

Wenn eines der folgenden Sonderzeichen als Literale im Abfrage Filter angezeigt werden muss, müssen Sie durch die aufgeführte Escapesequenz ersetzt werden.



| ASCII-Zeichen    | Escapesequenzersatz |
|--------------------|----------------------------|
| \*<br/>      | " \\ 2A"<br/>          |
| (<br/>       | " \\ 28"<br/>          |
| )<br/>       | " \\ 29"<br/>          |
| \\<br/>      | " \\ 5C"<br/>          |
| **NUL**<br/> | " \\ 00"<br/>          |



 

Darüber hinaus können beliebige Binärdaten mithilfe der Escapesequenzsyntax dargestellt werden, indem jedes Byte der Binärdaten mit dem umgekehrten Schrägstrich und zwei hexadezimalen Ziffern codiert wird. Beispielsweise wird der vier-Byte-Wert 0x00000004 \\ \\ \\ \\ in einer Filter Zeichenfolge als "00 00 00 04" codiert.

## <a name="examples"></a>Beispiele

Mit der folgenden Abfrage Zeichenfolge wird nach allen Objekten des Typs "Computer" gesucht.


```C++
(objectCategory=computer)
```



Die folgende Abfrage Zeichenfolge sucht nach allen Objekten des Typs "Computer" mit einem Namen, der mit "Desktop" beginnt.


```C++
(&(objectCategory=computer)(name=desktop*))
```



Die folgende Abfrage Zeichenfolge sucht nach allen Objekten des Typs "Computer" mit einem Namen, der mit "Desktop" beginnt, oder mit einem Namen, der mit "Notebook" beginnt.


```C++
(&(objectCategory=computer)(|(name=desktop*)(name=notebook*)))
```



Mit der folgenden Abfrage Zeichenfolge wird nach allen Objekten des Typs "User" gesucht, die eine privat Telefonnummer haben.


```C++
(&(objectCategory=user)(homePhone=*))
```



Weitere Informationen zu Abfrage Filter Zeichenfolgen und Verwendungs Beispielen finden Sie unter:

-   [Suchen nach Objekten nach Klasse](finding-objects-by-class.md)
-   [Suchen nach Objekten nach Namen](finding-objects-by-name.md)
-   [Suchen nach einer Liste der abzufragende Attribute](finding-a-list-of-attributes-to-query.md)
-   [Überprüfen der Abfrage Filter Syntax](checking-the-query-filter-syntax.md)
-   [Angeben von Vergleichswerten](how-to-specify-comparison-values.md)

 

 





