---
title: Counters-Auflistung (Isysmon.h)
description: Verwenden Sie diese Klasse, um die Auflistung von CounterItem-Objekten zu verwalten. Um dieses Objekt abzurufen, rufen Sie SystemMonitor.Counters auf.
ms.assetid: 01542569-3fee-440a-8722-db377380b73c
keywords:
- Counters collection SysMon
- Counters collection SysMon , beschrieben
topic_type:
- apiref
api_name:
- Counters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8349c1425450491c3fc658f6ac1ac3c5fcf75d3e617a92f6e34b91f2f5802e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883337"
---
# <a name="counters-collection"></a>Counters-Auflistung

Verwenden Sie diese Klasse, um die Auflistung von [**CounterItem-Objekten zu**](counteritem.md) verwalten.

Um dieses Objekt abzurufen, rufen Sie [**SystemMonitor.Counters auf.**](systemmonitor-counters.md)

## <a name="members"></a>Member

Die **Counters-Auflistung** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Counters-Auflistung** verfügt über diese Methoden.



| Methode                            | BESCHREIBUNG                                                                           |
|:----------------------------------|:--------------------------------------------------------------------------------------|
| [**Hinzufügen**](counters-add.md)       | Fügt der [**Auflistung eine CounterItem-Instanz**](counteritem.md) hinzu.<br/>      |
| [**Entfernen**](counters-remove.md) | Entfernt eine [**CounterItem-Instanz**](counteritem.md) aus der Auflistung.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Counters-Auflistung** verfügt über diese Eigenschaften.



| Eigenschaft                                   | BESCHREIBUNG                                                                                         |
|:-------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**Anzahl**](counters-count.md)<br/> | Ruft die Anzahl der [**CounterItem-Instanzen**](counteritem.md) in der Auflistung ab.<br/>  |
| [**Element**](counters-item.md)<br/>   | Ruft die angegebene [**CounterItem-Instanz**](counteritem.md) aus der Auflistung ab.<br/> |



 

## <a name="remarks"></a>Hinweise

Das **Counters-Objekt** ist die Standardeigenschaft des [**SystemMonitor-Objekts.**](systemmonitor.md)

Fügen Sie dieser Auflistung die Leistungsindikatoren hinzu, die Sie grafisch erstellen möchten. SYSMON ruft die Leistungsindikatorwerte abhängig von der angegebenen Datenquelle entweder aus dem System oder aus einer [**Protokolldatei**](systemmonitor-datasourcetype.md) ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Isysmon.h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





