---
description: Die "SCard \_ IO Request"- \_ Struktur beginnt mit einer Protokoll Steuerungs Informationsstruktur.
ms.assetid: 80fd7c6e-e768-42db-8302-29e92c9552f0
title: SCARD_IO_REQUEST Struktur (winsmcrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCARD_IO_REQUEST
api_type:
- HeaderDef
api_location:
- Winsmcrd.h
ms.openlocfilehash: fe3205311789ee51bb9b96b3b425b735e1fdf887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345319"
---
# <a name="scard_io_request-structure"></a>SCard \_ IO- \_ Anforderungs Struktur

Die " **SCard \_ IO \_ Request** "-Struktur beginnt mit einer Protokoll Steuerungs Informationsstruktur. Alle Protokoll spezifischen Informationen folgen dann direkt dieser Struktur. Die gesamte Länge der Struktur muss an der zugrunde liegenden Größe des Hardwarearchitektur Worts ausgerichtet werden. In Win32 muss die Länge aller PCI-Informationen z. b. ein Vielfaches von vier Bytes sein, damit Sie sich an einer 32-Bit-Grenze anpasst.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD dwProtocol;
  DWORD cbPciLength;
} SCARD_IO_REQUEST;
```



## <a name="members"></a>Member

<dl> <dt>

**dwprotocol**
</dt> <dd>

Das verwendete Protokoll.

</dd> <dt>

**cbpcilength**
</dt> <dd>

Länge (in Byte) der Anforderungs-e/a- **\_ \_ Anforderungs** Struktur zuzüglich der folgenden PCI-spezifischen Informationen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Winsmcrd. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Scardüberträgt**](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)
</dt> </dl>

 

 




