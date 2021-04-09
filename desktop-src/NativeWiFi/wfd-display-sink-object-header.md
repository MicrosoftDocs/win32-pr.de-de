---
description: Beschreibt die in einem Benachrichtigungs-oder Benachrichtigungs Ergebnis enthaltenen Daten der Senke-Objektdaten.
ms.assetid: 40D931F6-C068-48EB-A968-9CBAA3F9FAD8
title: WFD_DISPLAY_SINK_OBJECT_HEADER-Struktur (WF-Sink. h)
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
ms.openlocfilehash: cdefd6b0b91fefb0f42a6e37e7584f7cd966884b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864808"
---
# <a name="wfd_display_sink_object_header-structure"></a>WFD- \_ Anzeige \_ Sink- \_ Objekt \_ Header Struktur

Die **WFD- \_ Anzeige Sink-Objekt \_ \_ \_ Header** Struktur beschreibt die in einem Benachrichtigungs-oder Benachrichtigungs Ergebnis enthaltenen Daten der Senke-Objektdaten.

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

**Type**
</dt> <dd>

Der Typ des anzeigesenkjektobjekts. Sie können den Bezeichner **WFD \_ Display \_ Sink \_ Object \_ Type \_ default** verwenden, der als Wert 1 definiert ist.

</dd> <dt>

**Novel**
</dt> <dd>

Die Revisions Version des Objekts für die Anzeige Senke. Sie können den Bezeichner **WFD \_ Display \_ Sink \_ Object \_ Revision \_ Version \_ 1** verwenden, der als Wert 1 definiert ist.

</dd> <dt>

**Länge**
</dt> <dd>

Die Länge der Daten im Benachrichtigungs-oder Benachrichtigungs Ergebnis.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>WF-Senke. h</dt> </dl> |



 

 




