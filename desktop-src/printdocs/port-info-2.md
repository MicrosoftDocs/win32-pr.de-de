---
description: Die \_ PORT INFO \_ 2-Struktur identifiziert einen unterstützten Druckerport.
ms.assetid: 93675294-61d4-40e4-b84c-f252978e0285
title: PORT_INFO_2-Struktur (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_2
- _PORT_INFO_2A
- _PORT_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 053745ff90e022ef2ed466518a9210d6dde18d3562fdb4232d9f4d262460ea7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470940"
---
# <a name="port_info_2-structure"></a>PORT \_ INFO \_ 2-Struktur

Die **PORT \_ INFO \_ 2-Struktur** identifiziert einen unterstützten Druckerport.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PORT_INFO_2 {
  LPTSTR pPortName;
  LPTSTR pMonitorName;
  LPTSTR pDescription;
  DWORD  fPortType;
  DWORD  Reserved;
} PORT_INFO_2, *PPORT_INFO_2;
```



## <a name="members"></a>Member

<dl> <dt>

**pPortName**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die einen unterstützten Druckerport identifiziert (z.B. "LPT1:").

</dd> <dt>

**pMonitorName**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die einen installierten Monitor identifiziert (z.B. "PJL-Monitor"). Dies kann **NULL** sein.

</dd> <dt>

**pDescription**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Port ausführlicher beschreibt (wenn **pPortName** z. B. "LPT1:" lautet, ist **pDescription** "Druckerport"). Dies kann **NULL** sein.

</dd> <dt>

**fPortType**
</dt> <dd>

Bitmaske, die den Typ des Ports beschreibt. Dieser Member kann eine Kombination der folgenden Werte sein:

<dl><span id="PORT_TYPE_WRITE"></span><span id="port_type_write"></span><dt>

**PORTTYP \_ \_ WRITE**
</dt><span id="PORT_TYPE_READ"></span><span id="port_type_read"></span><dt>

**PORTTYP \_ \_ READ**
</dt><span id="PORT_TYPE_REDIRECTED"></span><span id="port_type_redirected"></span><dt>

**PORTTYP \_ \_ UMGELEITET**
</dt><span id="PORT_TYPE_NET_ATTACHED"></span><span id="port_type_net_attached"></span><dt>

**PORTTYP \_ \_ NET \_ ATTACHED**
</dt> </dl> </dd> <dt>

**Reserved**
</dt> <dd>

Reserviert; muss 0 (null) sein.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie die **PORT \_ INFO \_ 2-Struktur** beim Aufrufen von [**EnumPorts,**](enumports.md) wenn mehrere Monitore installiert sind, die dieselben Ports unterstützen.

Der **fPortType-Member** kann abgefragt werden, um Informationen zum Port zu ermitteln. Beachten Sie, dass die Porteinstellungen keine Auswirkungen auf Druckerattribute haben (wie vom **Attributes-Member** von [**PRINTER INFO \_ \_ 2**](printer-info-2.md)zurückgegeben).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ PORT \_ INFO \_ 2W** (Unicode) und **\_ PORT INFO \_ \_ 2A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




