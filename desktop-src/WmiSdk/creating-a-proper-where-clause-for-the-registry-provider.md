---
title: Erstellen einer WHERE-Klausel für den Registrierungs Anbieter
description: Die wichtigsten Punkte, die beim Erstellen einer ordnungsgemäßen WHERE-Klausel für den System Registrierungs Anbieter zu beachten sind, besteht darin, dass jede Ereignis Abfrage Complete und explizit sein muss. Wenn der Vorgang nicht durchgeführt werden kann, führt dies zu einer Fehlermeldung.
ms.assetid: cdef2900-8d1a-4f0b-8318-7463d90e4152
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d1c7031d376fbd6b9d946fb9e41561ce4c4b1c7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485739"
---
# <a name="creating-a-where-clause-for-the-registry-provider"></a><span data-ttu-id="68fe5-104">Erstellen einer WHERE-Klausel für den Registrierungs Anbieter</span><span class="sxs-lookup"><span data-stu-id="68fe5-104">Creating a WHERE clause for the registry provider</span></span>

<span data-ttu-id="68fe5-105">Die wichtigsten Punkte, die beim Erstellen einer ordnungsgemäßen WHERE-Klausel für den System Registrierungs Anbieter zu beachten sind, besteht darin, dass jede Ereignis Abfrage Complete und explizit sein muss.</span><span class="sxs-lookup"><span data-stu-id="68fe5-105">The main points to consider when creating a proper WHERE clause for the System Registry provider is that each event query must be complete and explicit.</span></span> <span data-ttu-id="68fe5-106">Wenn der Vorgang nicht durchgeführt werden kann, führt dies zu einer Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="68fe5-106">Failure to be complete and explicit will result in an error message.</span></span>

<span data-ttu-id="68fe5-107">Um den Vorgang abzuschließen, muss jede Ereignis Abfrage im *bstrinquery* -Parameter von [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) eine WHERE-Klausel enthalten, die jede der Eigenschaften in der angegebenen Ereignisklasse enthält.</span><span class="sxs-lookup"><span data-stu-id="68fe5-107">To be complete, each event query in the *bstrQuery* parameter of [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) must contain a WHERE clause that includes each of the properties in the specified event class.</span></span>

<span data-ttu-id="68fe5-108">Im folgenden Beispiel wird gezeigt, wie *btrequery* zum Registrieren für Struktur Änderungs Ereignisse in der Struktur "HKEY \_ local \_ Machine Software" festgelegt wird \\ .</span><span class="sxs-lookup"><span data-stu-id="68fe5-108">The following example shows how to set *bstrQuery* to register for tree change events in the "HKEY\_LOCAL\_MACHINE\\Software" tree.</span></span>


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE Hive = "HKEY_LOCAL_MACHINE" AND Rootpath = "Software"
```



<span data-ttu-id="68fe5-109">Um explizit zu sein, sollte der Anbieter in der Lage sein, von der Abfrage eine Liste möglicher Werte für jede Eigenschaft in der Ereignisklasse abzuleiten.</span><span class="sxs-lookup"><span data-stu-id="68fe5-109">To be explicit, the provider should be able to infer from the query a list of possible values for every property in the event class.</span></span>

<span data-ttu-id="68fe5-110">Im folgenden Beispiel wird die Ereignis Abfrage gezeigt, die für Struktur Änderungs Ereignisse ordnungsgemäß registriert.</span><span class="sxs-lookup"><span data-stu-id="68fe5-110">The following example shows the event query that correctly registers for tree change events.</span></span>


```sql
SELECT * FROM RegistryTreeChangeEvent 
    WHERE (hive = "hkey_local_machine" AND rootpath = "software") 
    OR    (hive = "hkey_current_user" AND rootpath = "console")
```



<span data-ttu-id="68fe5-111">Im folgenden finden Sie ein Beispiel für eine falsche Registrierung.</span><span class="sxs-lookup"><span data-stu-id="68fe5-111">The following is an example of an incorrect registration.</span></span>


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE hive = "hkey_local_machine" OR rootpath ="software"
```



<span data-ttu-id="68fe5-112">Da es keine Möglichkeit gibt, die möglichen Werte für die einzelnen Eigenschaften auszuwerten, lehnt WMI mit dem Fehler WBEM \_ E \_ zu \_ weit eine Abfrage ab, die entweder nicht über eine WHERE-Klausel verfügt, oder wenn die WHERE-Klausel zu breit ist, um verwendet werden zu können.</span><span class="sxs-lookup"><span data-stu-id="68fe5-112">Because there is no way to evaluate the possible values for each of the properties, WMI rejects with the error WBEM\_E\_TOO\_BROAD any query that either does not have a WHERE clause or if the WHERE clause is too broad to be of any use.</span></span>

 

 



