---
title: Windows Ereignisprotokolldatentypen (WinEvt.h)
description: Windows Das Ereignisprotokoll definiert die folgenden Datentypen.
ms.assetid: 1aad25fe-7503-4ef8-a40a-63457bd9a007
keywords:
- EVT_HANDLE
- PEVT_HANDLE
- EVT_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c309dd52471bd501aa2668220d39882ab8de7e1c23a646084364659df4ae4fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619990"
---
# <a name="windows-event-log-data-types"></a>Windows Ereignisprotokolldatentypen

Windows Das Ereignisprotokoll definiert die folgenden Datentypen:


```C++
typedef HANDLE EVT_HANDLE;
typedef HANDLE* PEVT_HANDLE;
typedef HANDLE EVT_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

**EVT \_ HANDLE**
</dt> <dd>

Ein Handle für ein Windows Ereignisprotokollobjekt.

</dd> <dt>

**\_PEVT-HANDLE**
</dt> <dd>

Ein Zeiger auf das Handle eines Windows Ereignisprotokollobjekts.

</dd> <dt>

**EIGENSCHAFTENHANDLE DES \_ EVT-OBJEKTARRAYS \_ \_ \_**
</dt> <dd>

Ein Handle für ein Array von Windows Ereignisprotokollobjekten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>WinEvt.h</dt> </dl> |



 

 





