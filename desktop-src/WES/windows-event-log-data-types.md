---
title: Windows-Ereignisprotokoll-Datentypen (winevt. h)
description: 'Das Windows-Ereignisprotokoll definiert die folgenden Datentypen:'
ms.assetid: 1aad25fe-7503-4ef8-a40a-63457bd9a007
keywords:
- EVT_HANDLE
- PEVT_HANDLE
- EVT_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a93794d8cc3a254fe182c439698324dccdfc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741385"
---
# <a name="windows-event-log-data-types"></a>Windows-Ereignisprotokoll Datentypen

Das Windows-Ereignisprotokoll definiert die folgenden Datentypen:


```C++
typedef HANDLE EVT_HANDLE;
typedef HANDLE* PEVT_HANDLE;
typedef HANDLE EVT_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

**EVT- \_ handle**
</dt> <dd>

Ein Handle für ein Windows-Ereignisprotokoll Objekt.

</dd> <dt>

**Peer- \_ handle**
</dt> <dd>

Ein Zeiger auf das Handle eines Windows-Ereignisprotokoll Objekts.

</dd> <dt>

**EVT- \_ Objekt \_ array- \_ Eigenschaften \_ handle**
</dt> <dd>

Ein Handle für ein Array von Windows-Ereignisprotokoll Objekten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Winevt. h</dt> </dl> |



 

 





