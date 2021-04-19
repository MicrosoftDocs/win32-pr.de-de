---
title: Tasknamedvaluepair-Objekt
description: Skript Objekt, das verwendet wird, um ein Name-Wert-Paar zu erstellen, in dem der Name dem Wert zugeordnet ist.
ms.assetid: def679b1-28d5-4c52-9dca-42a6de06a1ec
keywords:
- Tasknamedvaluepair-Objekt Taskplaner
- Tasknamedvaluepair-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- TaskNamedValuePair
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95229b5714d2cdcc43a071f2e51a50e04706429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341996"
---
# <a name="tasknamedvaluepair-object"></a>Tasknamedvaluepair-Objekt

Skript Objekt, das verwendet wird, um ein Name-Wert-Paar zu erstellen, in dem der Name dem Wert zugeordnet ist.

## <a name="members"></a>Member

Das **tasknamedvaluepair** -Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **tasknamedvaluepair** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                             | BESCHREIBUNG                                                                            |
|:-----------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**Name**](tasknamedvaluepair-name.md)<br/>   | Ruft den Namen ab, der einem Wert in einem Name-Wert-Paar zugeordnet ist, oder legt diesen fest.<br/> |
| [**Wert**](tasknamedvaluepair-value.md)<br/> | Ruft den Wert ab, der einem Namen in einem Name-Wert-Paar zugeordnet ist, oder legt diesen fest.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird ein Name-Wert-Paar mit dem [**valuequeries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) -Element des Taskplaner-Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Tasknamedvaluecollection**](tasknamedvaluecollection.md)
</dt> </dl>

 

 





