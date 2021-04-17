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
# <a name="creating-a-where-clause-for-the-registry-provider"></a>Erstellen einer WHERE-Klausel für den Registrierungs Anbieter

Die wichtigsten Punkte, die beim Erstellen einer ordnungsgemäßen WHERE-Klausel für den System Registrierungs Anbieter zu beachten sind, besteht darin, dass jede Ereignis Abfrage Complete und explizit sein muss. Wenn der Vorgang nicht durchgeführt werden kann, führt dies zu einer Fehlermeldung.

Um den Vorgang abzuschließen, muss jede Ereignis Abfrage im *bstrinquery* -Parameter von [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) eine WHERE-Klausel enthalten, die jede der Eigenschaften in der angegebenen Ereignisklasse enthält.

Im folgenden Beispiel wird gezeigt, wie *btrequery* zum Registrieren für Struktur Änderungs Ereignisse in der Struktur "HKEY \_ local \_ Machine Software" festgelegt wird \\ .


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE Hive = "HKEY_LOCAL_MACHINE" AND Rootpath = "Software"
```



Um explizit zu sein, sollte der Anbieter in der Lage sein, von der Abfrage eine Liste möglicher Werte für jede Eigenschaft in der Ereignisklasse abzuleiten.

Im folgenden Beispiel wird die Ereignis Abfrage gezeigt, die für Struktur Änderungs Ereignisse ordnungsgemäß registriert.


```sql
SELECT * FROM RegistryTreeChangeEvent 
    WHERE (hive = "hkey_local_machine" AND rootpath = "software") 
    OR    (hive = "hkey_current_user" AND rootpath = "console")
```



Im folgenden finden Sie ein Beispiel für eine falsche Registrierung.


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE hive = "hkey_local_machine" OR rootpath ="software"
```



Da es keine Möglichkeit gibt, die möglichen Werte für die einzelnen Eigenschaften auszuwerten, lehnt WMI mit dem Fehler WBEM \_ E \_ zu \_ weit eine Abfrage ab, die entweder nicht über eine WHERE-Klausel verfügt, oder wenn die WHERE-Klausel zu breit ist, um verwendet werden zu können.

 

 



