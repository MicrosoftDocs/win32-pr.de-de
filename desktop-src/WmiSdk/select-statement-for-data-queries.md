---
description: Beschreiben Sie die SELECT-Anweisung für eine Datenabfrage.
ms.assetid: 9c1a164e-4728-4fbe-8a49-b571005a46ec
ms.tgt_platform: multiple
title: SELECT-Anweisung für Daten Abfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06905cfd9ef5e55022b3fc2275ed705a670a0ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348527"
---
# <a name="select-statement-for-data-queries"></a>SELECT-Anweisung für Daten Abfragen

Sie können eine Vielzahl von SELECT-Anweisungen verwenden, um Informationen abzufragen. Die Anweisungen können einfache Anweisungen sein, oder Sie können restriktiver sein, um das Resultset einzugrenzen, das von der Abfrage zurückgegeben wird.

Das folgende Beispiel ist eine einfache SELECT-Anweisung, die zum Abfragen von Daten verwendet wird.


```sql
SELECT * FROM Class
```



Diese Anweisung gibt Instanzen der angegebenen Klasse und aller zugehörigen Unterklassen zurück. Alle System-und benutzerdefinierten Eigenschaften für die Klassen sind eingeschlossen. Wenn eine System Eigenschaft für eine bestimmte Abfrage nicht relevant ist, enthält Sie **null**.

Sie können mehrere Techniken verwenden, um die Bandbreite zu reduzieren, die zum Abrufen des Resultsets erforderlich ist, wenn die Ausführung der Abfrage zu viel mehr Aufwand verursacht und der Benutzer nur an einer Teilmenge der Eigenschaften interessiert ist. Zuerst können Abfragen das Sternchen durch die gewünschten Eigenschaften ersetzen.

Im folgenden Beispiel wird gezeigt, wie bestimmte Eigenschaften abgefragt werden.


```sql
SELECT property_1, property_2, property_3 FROM class
```



Das Resultset enthält alle Systemeigenschaften und die angegebenen nicht-Systemeigenschaften.

Ein weiteres Verfahren zum Einschränken des Gültigkeits Bereichs des Resultsets einer Abfrage ist die Verwendung der- [**\_ \_ Klassen**](wmi-system-properties.md) System Eigenschaft. Bei Abfragen werden standardmäßig alle Instanzen der angegebenen Klasse und ihrer Unterklassen zurückgegeben. Sie können die **\_ \_ Klassen** System Eigenschaft verwenden, um nur Instanzen der angegebenen Klasse anzufordern, ausgenommen deren Unterklassen.

Im folgenden Beispiel wird gezeigt, wie die- [**\_ \_ Klassen**](wmi-system-properties.md) System Eigenschaft in einer WHERE-Klausel verwendet wird.


```sql
SELECT * FROM Device WHERE __CLASS = "Device"
```



Sie können auch die [**\_ \_ Class**](wmi-system-properties.md) System-Eigenschaft verwenden, um das Resultset auf Instanzen bestimmter Unterklassen einzuschränken.

Im folgenden Beispiel wird gezeigt, wie das Resultset auf Instanzen bestimmter Unterklassen beschränkt wird.


```sql
SELECT * FROM Device WHERE __CLASS = "Modem" OR __CLASS = "Keyboard"
```



> [!Note]  
> Wenn Sie eine Abfrage mit einem ungültigen Pfad für ein eingebettetes Objekt erstellen, gibt die Abfrage keinen Fehler oder keine Ergebnisse zurück.

 

Im folgenden Beispiel wird eine Instanz der **MainClass** zurückgegeben, vorausgesetzt, dass eine Instanz der **MainClass** vorhanden ist, die das eingebettete Objekt **embedobj** mit der Eigenschaft **P \_ UInt32** enthält, die gleich "70011" ist.


```sql
SELECT * FROM MainClass WHERE EmbedObj.P_Uint32 = 70011
```



Im folgenden Beispiel werden keine Ergebnisse zurückgegeben, und es wird kein Fehler zurückgegeben, vorausgesetzt, dass das eingebettete Objekt **embedobj** in der Instanz der **MainClass** keine **ungültige** Eigenschaft besitzt.


```sql
SELECT * FROM MainClass WHERE StrongEmbedObj.INVALID = 70011
```



 

 



