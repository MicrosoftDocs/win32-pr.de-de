---
title: Imemoryzuordcator-Klasse
description: Wird von der Arbeitsspeicher Zuweisung für die stgconvertpropertytovariant-Funktion implementiert.
ms.assetid: a0735b62-5ed3-42df-a320-b58c742645a8
keywords:
- Strukturierte Speicherung der imemoryzuordcator-Klasse
- Strukturierte Speicherung der imemoryzuordcator-Klasse, beschrieben
topic_type:
- apiref
api_name:
- IMemoryAllocator
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421162fd0ee6228f1dbae03eeb52e5643b0e0b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391965"
---
# <a name="imemoryallocator-class"></a>Imemoryzuordcator-Klasse

Die **imemoryzuordcator** -Klasse wird von der Speicherzuweisung für die [**stgconvertpropertytovariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) -Funktion implementiert.

## <a name="methods"></a>Methoden



| Name                                                     | BESCHREIBUNG                                                                                                                                                                                                        |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Jugend**](imemoryallocator-allocate.md)<br/> | Weist Speicher für die [**stgconvertpropertytovariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) -Funktion zu, wenn die-Funktion einen **serializedpropertyvalue** -Datentyp in einen **PROPVARIANT** -Datentyp konvertiert.<br/> |
| [**Kostenlos**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize)<br/>        | Gibt den von der Zuordnungs [**Methode belegten**](imemoryallocator-allocate.md) Arbeitsspeicher frei.<br/>                                                                                                                 |



 

## <a name="remarks"></a>Bemerkungen

Diese Klasse wird nur von der [**stgconvertpropertydevariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) -Funktion verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Bibliothek<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |



 

