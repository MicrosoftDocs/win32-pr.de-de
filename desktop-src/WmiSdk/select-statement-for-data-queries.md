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
# <a name="select-statement-for-data-queries"></a><span data-ttu-id="f21cf-103">SELECT-Anweisung für Daten Abfragen</span><span class="sxs-lookup"><span data-stu-id="f21cf-103">SELECT Statement for Data Queries</span></span>

<span data-ttu-id="f21cf-104">Sie können eine Vielzahl von SELECT-Anweisungen verwenden, um Informationen abzufragen.</span><span class="sxs-lookup"><span data-stu-id="f21cf-104">You can use a variety of SELECT statements to query for information.</span></span> <span data-ttu-id="f21cf-105">Die Anweisungen können einfache Anweisungen sein, oder Sie können restriktiver sein, um das Resultset einzugrenzen, das von der Abfrage zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f21cf-105">The statements can be basic statements or they can be more restrictive to narrow the result set that is returned from the query.</span></span>

<span data-ttu-id="f21cf-106">Das folgende Beispiel ist eine einfache SELECT-Anweisung, die zum Abfragen von Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f21cf-106">The following example is a basic SELECT statement that is used to query for data.</span></span>


```sql
SELECT * FROM Class
```



<span data-ttu-id="f21cf-107">Diese Anweisung gibt Instanzen der angegebenen Klasse und aller zugehörigen Unterklassen zurück.</span><span class="sxs-lookup"><span data-stu-id="f21cf-107">This statement returns instances of the specified class and any of its subclasses.</span></span> <span data-ttu-id="f21cf-108">Alle System-und benutzerdefinierten Eigenschaften für die Klassen sind eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f21cf-108">All of the system and user-defined properties for the classes are included.</span></span> <span data-ttu-id="f21cf-109">Wenn eine System Eigenschaft für eine bestimmte Abfrage nicht relevant ist, enthält Sie **null**.</span><span class="sxs-lookup"><span data-stu-id="f21cf-109">If a system property is not relevant for a particular query, it contains **NULL**.</span></span>

<span data-ttu-id="f21cf-110">Sie können mehrere Techniken verwenden, um die Bandbreite zu reduzieren, die zum Abrufen des Resultsets erforderlich ist, wenn die Ausführung der Abfrage zu viel mehr Aufwand verursacht und der Benutzer nur an einer Teilmenge der Eigenschaften interessiert ist.</span><span class="sxs-lookup"><span data-stu-id="f21cf-110">You can use several techniques to reduce the bandwidth required to retrieve the result set, if the execution of the query results in too much overhead and the user is only interested in a subset of the properties.</span></span> <span data-ttu-id="f21cf-111">Zuerst können Abfragen das Sternchen durch die gewünschten Eigenschaften ersetzen.</span><span class="sxs-lookup"><span data-stu-id="f21cf-111">First, queries can replace the asterisk with the desired properties.</span></span>

<span data-ttu-id="f21cf-112">Im folgenden Beispiel wird gezeigt, wie bestimmte Eigenschaften abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="f21cf-112">The following example shows how to query for specific properties.</span></span>


```sql
SELECT property_1, property_2, property_3 FROM class
```



<span data-ttu-id="f21cf-113">Das Resultset enthält alle Systemeigenschaften und die angegebenen nicht-Systemeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f21cf-113">The result set includes all system properties and the specified nonsystem properties.</span></span>

<span data-ttu-id="f21cf-114">Ein weiteres Verfahren zum Einschränken des Gültigkeits Bereichs des Resultsets einer Abfrage ist die Verwendung der- [**\_ \_ Klassen**](wmi-system-properties.md) System Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f21cf-114">Another technique for narrowing the scope of a query's result set is to use the [**\_\_CLASS**](wmi-system-properties.md) system property.</span></span> <span data-ttu-id="f21cf-115">Bei Abfragen werden standardmäßig alle Instanzen der angegebenen Klasse und ihrer Unterklassen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f21cf-115">Queries by default return all instances of the specified class and its subclasses.</span></span> <span data-ttu-id="f21cf-116">Sie können die **\_ \_ Klassen** System Eigenschaft verwenden, um nur Instanzen der angegebenen Klasse anzufordern, ausgenommen deren Unterklassen.</span><span class="sxs-lookup"><span data-stu-id="f21cf-116">You can use the **\_\_CLASS** system property to request only instances of the specified class, excluding its subclasses.</span></span>

<span data-ttu-id="f21cf-117">Im folgenden Beispiel wird gezeigt, wie die- [**\_ \_ Klassen**](wmi-system-properties.md) System Eigenschaft in einer WHERE-Klausel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f21cf-117">The following example shows how to use the [**\_\_CLASS**](wmi-system-properties.md) system property in a WHERE clause.</span></span>


```sql
SELECT * FROM Device WHERE __CLASS = "Device"
```



<span data-ttu-id="f21cf-118">Sie können auch die [**\_ \_ Class**](wmi-system-properties.md) System-Eigenschaft verwenden, um das Resultset auf Instanzen bestimmter Unterklassen einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="f21cf-118">You can also use the [**\_\_CLASS**](wmi-system-properties.md) system property to restrict the result set to instances of particular subclasses.</span></span>

<span data-ttu-id="f21cf-119">Im folgenden Beispiel wird gezeigt, wie das Resultset auf Instanzen bestimmter Unterklassen beschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="f21cf-119">The following example shows how to restrict the result set to instances of particular subclasses.</span></span>


```sql
SELECT * FROM Device WHERE __CLASS = "Modem" OR __CLASS = "Keyboard"
```



> [!Note]  
> <span data-ttu-id="f21cf-120">Wenn Sie eine Abfrage mit einem ungültigen Pfad für ein eingebettetes Objekt erstellen, gibt die Abfrage keinen Fehler oder keine Ergebnisse zurück.</span><span class="sxs-lookup"><span data-stu-id="f21cf-120">If you construct a query with an invalid path for an embedded object, your query does not return an error or any results.</span></span>

 

<span data-ttu-id="f21cf-121">Im folgenden Beispiel wird eine Instanz der **MainClass** zurückgegeben, vorausgesetzt, dass eine Instanz der **MainClass** vorhanden ist, die das eingebettete Objekt **embedobj** mit der Eigenschaft **P \_ UInt32** enthält, die gleich "70011" ist.</span><span class="sxs-lookup"><span data-stu-id="f21cf-121">The following example returns an instance of **MainClass**, assuming that an instance of **MainClass** exists containing the embedded object **EmbedObj** with a property **P\_Uint32** that is equal to "70011".</span></span>


```sql
SELECT * FROM MainClass WHERE EmbedObj.P_Uint32 = 70011
```



<span data-ttu-id="f21cf-122">Im folgenden Beispiel werden keine Ergebnisse zurückgegeben, und es wird kein Fehler zurückgegeben, vorausgesetzt, dass das eingebettete Objekt **embedobj** in der Instanz der **MainClass** keine **ungültige** Eigenschaft besitzt.</span><span class="sxs-lookup"><span data-stu-id="f21cf-122">The following example returns no results and does not return an error, assuming that the embedded object **EmbedObj** in the instance of **MainClass** does not have a property **INVALID**.</span></span>


```sql
SELECT * FROM MainClass WHERE StrongEmbedObj.INVALID = 70011
```



 

 



