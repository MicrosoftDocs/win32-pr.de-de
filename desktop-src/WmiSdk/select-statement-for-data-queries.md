---
description: Beschreiben der SELECT-Anweisung für eine Datenabfrage.
ms.assetid: 9c1a164e-4728-4fbe-8a49-b571005a46ec
ms.tgt_platform: multiple
title: SELECT-Anweisung für Datenabfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44fec0526c5e5d47a74d6e165726222f9e521bd7102072e5a4b79e960f8dae19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315948"
---
# <a name="select-statement-for-data-queries"></a>SELECT-Anweisung für Datenabfragen

Sie können eine Vielzahl von SELECT-Anweisungen verwenden, um Informationen abzufragen. Die Anweisungen können einfache Anweisungen oder restriktiver sein, um das von der Abfrage zurückgegebene Resultset einzugrenzen.

Das folgende Beispiel ist eine einfache SELECT-Anweisung, die zum Abfragen von Daten verwendet wird.


```sql
SELECT * FROM Class
```



Diese Anweisung gibt Instanzen der angegebenen Klasse und eine ihrer Unterklassen zurück. Alle System- und benutzerdefinierten Eigenschaften für die Klassen sind enthalten. Wenn eine Systemeigenschaft für eine bestimmte Abfrage nicht relevant ist, enthält sie **NULL.**

Sie können mehrere Techniken verwenden, um die bandbreitenbezogene Menge zu reduzieren, die zum Abrufen des Resultset erforderlich ist, wenn die Ausführung der Abfrage zu viel Mehraufwand verursacht und der Benutzer nur an einer Teilmenge der Eigenschaften interessiert ist. Zuerst können Abfragen das Sternchen durch die gewünschten Eigenschaften ersetzen.

Im folgenden Beispiel wird veranschaulicht, wie bestimmte Eigenschaften abgefragt werden.


```sql
SELECT property_1, property_2, property_3 FROM class
```



Das Resultset enthält alle Systemeigenschaften und die angegebenen Nichtsystemeigenschaften.

Eine weitere Technik zum Eingrenzen des Gültigkeitsbereichs des Resultset einer Abfrage ist die Verwendung der [**\_ \_ CLASS-Systemeigenschaft.**](wmi-system-properties.md) Abfragen geben standardmäßig alle Instanzen der angegebenen Klasse und deren Unterklassen zurück. Sie können die **\_ \_ CLASS-Systemeigenschaft** verwenden, um nur Instanzen der angegebenen Klasse anzufordern, mit Ausnahme ihrer Unterklassen.

Das folgende Beispiel zeigt, wie die [**\_ \_ CLASS-Systemeigenschaft**](wmi-system-properties.md) in einer WHERE-Klausel verwendet wird.


```sql
SELECT * FROM Device WHERE __CLASS = "Device"
```



Sie können auch die [**\_ \_ CLASS-Systemeigenschaft**](wmi-system-properties.md) verwenden, um das Resultset auf Instanzen bestimmter Unterklassen zu beschränken.

Das folgende Beispiel zeigt, wie das Resultset auf Instanzen bestimmter Unterklassen beschränkt wird.


```sql
SELECT * FROM Device WHERE __CLASS = "Modem" OR __CLASS = "Keyboard"
```



> [!Note]  
> Wenn Sie eine Abfrage mit einem ungültigen Pfad für ein eingebettetes Objekt erstellen, gibt die Abfrage keinen Fehler oder keine Ergebnisse zurück.

 

Im folgenden Beispiel wird eine Instanz von **MainClass** zurückgegeben, vorausgesetzt, dass eine Instanz von **MainClass** vorhanden ist, die das **eingebettete Objekt EmbedObj** mit einer **P \_ Uint32-Eigenschaft** enthält, die gleich "70011" ist.


```sql
SELECT * FROM MainClass WHERE EmbedObj.P_Uint32 = 70011
```



Das folgende Beispiel gibt keine Ergebnisse zurück und gibt keinen Fehler zurück, vorausgesetzt, das **eingebettete Objekt EmbedObj** in der Instanz von **MainClass** verfügt nicht über die Eigenschaft **INVALID**.


```sql
SELECT * FROM MainClass WHERE StrongEmbedObj.INVALID = 70011
```



 

 



