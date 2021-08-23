---
description: Beschreibt die Anzeigesenkenobjektdaten, die in einem Benachrichtigungs- oder Benachrichtigungsergebnis enthalten sind.
ms.assetid: 40D931F6-C068-48EB-A968-9CBAA3F9FAD8
title: WFD_DISPLAY_SINK_OBJECT_HEADER -Struktur (Wfdsink.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: e4c9e4d83fbac1cccb2dbc0643acc707176be433dfca7854395a0f97c9c36435
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800470"
---
# <a name="wfd_display_sink_object_header-structure"></a>WFD \_ DISPLAY SINK OBJECT \_ \_ \_ HEADER-Struktur

Die **WFD \_ DISPLAY SINK OBJECT \_ \_ \_ HEADER-Struktur** beschreibt die Anzeigesenkenobjektdaten, die in einem Benachrichtigungs- oder Benachrichtigungsergebnis enthalten sind.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WFD_DISPLAY_SINK_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Length;
} WFD_DISPLAY_SINK_OBJECT_HEADER, *PWFD_DISPLAY_SINK_OBJECT_HEADER;
```



## <a name="members"></a>Member

<dl> <dt>

**Typ**
</dt> <dd>

Der Typ des Anzeigesenkenobjekts. Sie können den Bezeichner **WFD \_ DISPLAY SINK OBJECT TYPE \_ \_ \_ \_ DEFAULT** verwenden, der als Wert 1 definiert ist.

</dd> <dt>

**Revision**
</dt> <dd>

Die Revisionsversion des Anzeigesenkenobjekts. Sie können den Bezeichner **WFD \_ DISPLAY SINK OBJECT REVISION VERSION \_ \_ \_ \_ \_ 1** verwenden, der als Wert 1 definiert ist.

</dd> <dt>

**Länge**
</dt> <dd>

Die Länge der Daten im Benachrichtigungs- oder Benachrichtigungsergebnis.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Wfdsink.h</dt> </dl> |



 

 




