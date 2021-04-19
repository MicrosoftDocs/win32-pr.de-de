---
description: Die References of-Anweisung ruft alle Assoziations Instanzen ab, die auf eine bestimmte Quell Instanz verweisen.
ms.assetid: 674be546-e7fd-4150-9d7c-2888d24bf1b3
ms.tgt_platform: multiple
title: Verweise der Anweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c7cc624a1e91220fc6bfc89ef0a75878a9cfb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350569"
---
# <a name="references-of-statement"></a>Verweise der Anweisung

Die References of-Anweisung ruft alle Assoziations Instanzen ab, die auf eine bestimmte Quell Instanz verweisen. Die References of-Anweisung ähnelt den assoziatoren der-Anweisung in der-Syntax. Anstatt Endpunkt Instanzen abzurufen, ruft Sie jedoch die dazwischen liegenden Zuordnungs Instanzen ab.

Die Verweise der WHERE-Klausel können ein oder mehrere der folgenden vordefinierten Schlüsselwörter und ihre Werte einschließen:


```sql
REFERENCES OF {SourceObject} WHERE 
    ClassDefsOnly
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    Role = PropertyName
```



Um ein Quell Objekt anzugeben, verwenden Sie einen beliebigen gültigen Objekt Pfad für SourceObject. Wie bei der SELECT-Anweisung ist die WHERE-Klausel optional und wird verwendet, um die Abfrage weiter zu definieren. Das heißt, dass die folgende Anweisung vollständig gültig ist:


```sql
REFERENCES OF {Adapter="AHA-294X"}
```



Das **classdefsonly** -Schlüsselwort gibt an, dass die Anweisung ein Resultset von Klassen Definitions Objekten anstelle tatsächlicher Instanzen der Zuordnungs Klassen zurückgibt. Diese Objekte enthalten Definitionen von Klassen, zu denen die Instanzen, die auf das Quell Objekt verweisen, gehören. Die folgende Anweisung gibt beispielsweise Definitionen für die **adapterdriver** -Klasse und die **adapterprotocol** -Klasse zurück:


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ClassDefsOnly
```



Das Requirements **dqualifier** -Schlüsselwort gibt an, dass die zurückgegebenen Zuordnungs Objekte den angegebenen Qualifizierer einschließen müssen Das "Requirements **dqualifier** "-Schlüsselwort kann verwendet werden, um bestimmte Instanzen von Zuordnungen in das Resultset einzubeziehen. Die folgende Anweisung gibt beispielsweise Association-Instanzen zurück, die einen Qualifizierer namens **adaptertag** enthalten:


```sql
REFERENCES OF {Adapter="AHA-294X"}  WHERE RequiredQualifier = AdapterTag
```



Das **resultClass** -Schlüsselwort gibt an, dass die zurückgegebenen Zuordnungs Objekte zu oder von der angegebenen Klasse abgeleitet werden müssen. Beispielsweise gibt die folgende Anweisung Zuordnungen der **adapterdriver** -Klasse oder Unterklassen von **adapterdriver** zurück:


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ResultClass = AdapterDriver
```



Die Schlüsselwörter **classdefsonly** und **resultClass** schließen sich gegenseitig aus. Die gemeinsame Verwendung verursacht einen ungültigen Abfrage Fehler.

Das **Role** -Schlüsselwort gibt an, dass die zurückgegebenen Zuordnungen nur solche sind, in denen das Quell Objekt eine bestimmte Rolle spielt. Die Rolle wird durch die angegebene Eigenschaft definiert, eine Verweis Eigenschaft vom Typ [ref](references.md). Das **Role** -Schlüsselwort ist hilfreich bei Zuordnungen, bei denen ein bestimmtes Objekt in einigen Fällen eine Rolle spielen kann, und eine andere Rolle in anderen, z. b. in hierarchischen Zuordnungen Das **Role** -Schlüsselwort kann verwendet werden, um alle Zuordnungen abzurufen, in denen das Quell Objekt z. b. die Rolle des übergeordneten Elements übernimmt. Die folgende Anweisung veranschaulicht die Syntax zum Abrufen von Zuordnungen, die über eine über **geordnete** Eigenschaft verfügen, die auf das Quell Objekt als übergeordnetes Element verweist:


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE Role = parent
```



> [!Note]  
> Komplexe Abfragen können nicht "and" oder "or" verwenden, um Schlüsselwörter für assoziatoren von und verweisen auf-Anweisungen zu trennen. Außerdem ist das Gleichheitszeichen der einzige gültige Operator, der mit den Schlüsselwörtern in diesen Abfragen verwendet werden kann. Beispielsweise ist die folgende Abfrage gültig:

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier = Dynamic"
```



> [!Note]  
> Die folgenden Beispiele sind ungültig. Im ersten Beispiel wird nicht das Gleichheitszeichen verwendet, und das zweite Beispiel versucht fälschlicherweise, das **-** Schlüsselwort und das-Schlüsselwort zu verwenden:

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier <> Dynamic"

"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
"WHERE resultclass = Win32_NetworkAdapterSetting " +
"AND requiredQualifier = Dynamic"
```



 

 



