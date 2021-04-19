---
description: Die \_ Struktur Port Info \_ 2 identifiziert einen unterstützten Druckerport.
ms.assetid: 93675294-61d4-40e4-b84c-f252978e0285
title: PORT_INFO_2 Struktur (winspool. h)
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
ms.openlocfilehash: 1d2186193318387bb6e37a228bd4d2fd64eca6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349332"
---
# <a name="port_info_2-structure"></a>Port \_ Info \_ 2-Struktur

Die Struktur **Port \_ Info \_ 2** identifiziert einen unterstützten Druckerport.

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

**pportname**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die einen unterstützten Druckerport identifiziert (z. b. "LPT1:").

</dd> <dt>

**pmonitorname**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die einen installierten Monitor identifiziert (z. b. "PJL-Monitor"). Dieser Wert kann **null** sein.

</dd> <dt>

**pdescription**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Port ausführlicher beschreibt (z. b. wenn " **pportname** " den Wert "LPT1:" hat, " **pdescription** " ist "Printer Port"). Dieser Wert kann **null** sein.

</dd> <dt>

**"f"**
</dt> <dd>

Bitmaske, die den Porttyp beschreibt. Dieser Member kann eine Kombination der folgenden Werte sein:

<dl><span id="PORT_TYPE_WRITE"></span><span id="port_type_write"></span><dt>

**\_Porttyp \_ schreiben**
</dt><span id="PORT_TYPE_READ"></span><span id="port_type_read"></span><dt>

**\_Porttyp \_ Lesen**
</dt><span id="PORT_TYPE_REDIRECTED"></span><span id="port_type_redirected"></span><dt>

**\_umgeleitete Porttyp \_**
</dt><span id="PORT_TYPE_NET_ATTACHED"></span><span id="port_type_net_attached"></span><dt>

**\_Porttyp \_ Netzwerk \_ angefügt**
</dt> </dl> </dd> <dt>

**Reserved**
</dt> <dd>

Bleiben muss 0 (null) sein.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **Port \_ Info \_ 2** -Struktur beim Aufrufen von [**enumports**](enumports.md) , wenn mehrere Monitore installiert sind, die die gleichen Ports unterstützen.

Der **fporttype** -Member kann abgefragt werden, um Informationen über den Port zu ermitteln. Beachten Sie, dass die Port Einstellungen keine Drucker Attribute beeinflussen (wie vom **Attribute** -Member von [**Printer \_ Info \_ 2**](printer-info-2.md)zurückgegeben).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Port \_ Info \_ 2W** (Unicode) und **\_ Port \_ Info \_ 2a** (ANSI)<br/>                                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




