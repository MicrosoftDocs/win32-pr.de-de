---
title: Erstellen einer WHERE-Klausel für den Registrierungsanbieter
description: Die wichtigsten Punkte, die beim Erstellen einer richtigen WHERE-Klausel für den Systemregistrierungsanbieter zu berücksichtigen sind, ist, dass jede Ereignisabfrage vollständig und explizit sein muss. Wenn der Fehler nicht vollständig und explizit ist, wird eine Fehlermeldung ausgegeben.
ms.assetid: cdef2900-8d1a-4f0b-8318-7463d90e4152
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0fc037b746233bd9eb2f9bdd4afad942d07dc832b4dfd60cd9ca6ae9f273efca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679830"
---
# <a name="creating-a-where-clause-for-the-registry-provider"></a>Erstellen einer WHERE-Klausel für den Registrierungsanbieter

Die wichtigsten Punkte, die beim Erstellen einer richtigen WHERE-Klausel für den Systemregistrierungsanbieter zu berücksichtigen sind, ist, dass jede Ereignisabfrage vollständig und explizit sein muss. Wenn der Fehler nicht vollständig und explizit ist, wird eine Fehlermeldung ausgegeben.

Um abgeschlossen zu werden, muss jede Ereignisabfrage im *bstrQuery-Parameter* von [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) eine WHERE-Klausel enthalten, die jede der Eigenschaften in der angegebenen Ereignisklasse enthält.

Das folgende Beispiel zeigt, wie *bstrQuery* so festgelegt wird, dass es für Strukturänderungsereignisse in der Struktur "HKEY \_ LOCAL MACHINE \_ \\ Software" registriert wird.


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE Hive = "HKEY_LOCAL_MACHINE" AND Rootpath = "Software"
```



Um explizit zu sein, sollte der Anbieter aus der Abfrage eine Liste möglicher Werte für jede Eigenschaft in der Ereignisklasse ablesen können.

Das folgende Beispiel zeigt die Ereignisabfrage, die ordnungsgemäß für Strukturänderungsereignisse registriert wird.


```sql
SELECT * FROM RegistryTreeChangeEvent 
    WHERE (hive = "hkey_local_machine" AND rootpath = "software") 
    OR    (hive = "hkey_current_user" AND rootpath = "console")
```



Im Folgenden finden Sie ein Beispiel für eine falsche Registrierung.


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE hive = "hkey_local_machine" OR rootpath ="software"
```



Da es keine Möglichkeit gibt, die möglichen Werte für jede der Eigenschaften auswerten zu können, lehnt WMI mit dem Fehler WBEM E TOO BROAD jede Abfrage ab, die entweder keine WHERE-Klausel aufweist oder wenn die WHERE-Klausel zu breit ist, um von Nutzen zu \_ \_ \_ sein.

 

 



