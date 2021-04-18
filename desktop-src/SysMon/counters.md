---
title: Zähler Sammlung (isysmon. h)
description: Verwenden Sie diese Klasse, um die Auflistung der "count"-Objekte zu verwalten. Um dieses Objekt abzurufen, rufen Sie Systemmonitor. Counters auf.
ms.assetid: 01542569-3fee-440a-8722-db377380b73c
keywords:
- Leistungsindikator Sammlung (Sysmon)
- Leistungsindikator Sammlung (Sysmon), beschrieben
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
ms.openlocfilehash: dbcbf8da93f13dce2ce2a290adeab9394ee8addb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345501"
---
# <a name="counters-collection"></a>Zähler Sammlung

Verwenden Sie diese Klasse, um die Auflistung der " [**count**](counteritem.md) "-Objekte zu verwalten.

Um dieses Objekt abzurufen, rufen Sie [**Systemmonitor. Counters**](systemmonitor-counters.md)auf.

## <a name="members"></a>Member

Die  indikatorenauflistung enthält diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die  indikatorenauflistung verfügt über diese Methoden.



| Methode                            | BESCHREIBUNG                                                                           |
|:----------------------------------|:--------------------------------------------------------------------------------------|
| [**Eren**](counters-add.md)       | Fügt der [**Auflistung eine-**](counteritem.md) Instanz hinzu.<br/>      |
| [**Aufgeh**](counters-remove.md) | Entfernt eine [**-**](counteritem.md) Instanz aus der Auflistung.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Zähler** Sammlung verfügt über diese Eigenschaften.



| Eigenschaft                                   | BESCHREIBUNG                                                                                         |
|:-------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**Countdown**](counters-count.md)<br/> | Ruft die [**Anzahl von Instanzen in der-**](counteritem.md) Auflistung ab.<br/>  |
| [**Element**](counters-item.md)<br/>   | Ruft [**die angegebene-**](counteritem.md) Instanz aus der Auflistung ab.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das **Counters** -Objekt ist die Standard Eigenschaft des [**Systemmonitor**](systemmonitor.md) -Objekts.

Fügen Sie dieser Sammlung die Leistungsindikatoren hinzu, die Sie grafisch abbilden möchten. Sysmon Ruft die Werte des Zählers entweder aus dem System oder aus einer Protokolldatei ab, abhängig von der von Ihnen angegebenen [**Datenquelle**](systemmonitor-datasourcetype.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Isysmon. h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





