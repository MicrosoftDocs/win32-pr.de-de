---
description: Die NETWORKINFO-Struktur beschreibt eine NIC.
ms.assetid: 40169409-7de5-44d1-8dff-dfa9f647edc9
title: NETWORKINFO-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b5b57d7f051c1409c4b691d78d9173341efda984f35498289cd1eacb8c8b3199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555710"
---
# <a name="networkinfo-structure"></a>NETWORKINFO-Struktur

Die NETWORKINFO-Struktur beschreibt eine NIC.

## <a name="syntax"></a>Syntax


```C++
typedef struct _NETWORKINFO {
  BYTE    PermanentAddr[6];
  BYTE    CurrentAddr[6];
  ADDRESS OtherAddress;
  DWORD   LinkSpeed;
  DWORD   MacType;
  DWORD   MaxFrameSize;
  DWORD   Flags;
  DWORD   TimestampScaleFactor;
  BYTE    NodeName[32];
  BOOL    PModeSupported;
  BYTE    Comment[ADAPTER_COMMENT_LENGTH];
} NETWORKINFO, *LPNETWORKINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**PermanentAddr**
</dt> <dd>

Permanente MAC-Adresse.

</dd> <dt>

**CurrentAddr**
</dt> <dd>

Aktuelle MAC-Adresse.

</dd> <dt>

**OtherAddress**
</dt> <dd>

Andere Adresse, die dies unterstützt (z. B. IP, IPX).

</dd> <dt>

**LinkSpeed**
</dt> <dd>

Verbindungsgeschwindigkeit in MBit/s.

</dd> <dt>

**MacType**
</dt> <dd>

Medientyp.

</dd> <dt>

**MaxFrameSize**
</dt> <dd>

Maximal zulässige Framegröße.

</dd> <dt>

**Flags**
</dt> <dd>

Dieser Parameter kann eines der folgenden Informationsflags sein:



| Wert                                                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NETWORKINFO_FLAGS_PMODE_NOT_SUPPORTED"></span><span id="networkinfo_flags_pmode_not_supported"></span><dl> <dt>**\_NETWORKINFO-FLAGS \_ PMODE \_ NICHT \_ UNTERSTÜTZT**</dt> </dl>    | Die Netzwerkkarte unterstützt keinen promiscuous-Modus, d. h., sie erfasst nur Datenverkehr, der übertragen wird oder nur den lokalen Computer betrifft.<br/> |
| <span id="NETWORKINFO_FLAGS_RAS"></span><span id="networkinfo_flags_ras"></span><dl> <dt>**\_NETWORKINFO-FLAGS \_ RAS**</dt> </dl>                                                      | Dies ist eine virtuelle Netzwerkkarte, bei der es sich um eine RAS-Verbindung (Ras Access Server) über ein Modem oder eine andere Netzwerkkarte handelt.<br/>                                        |
| <span id="NETWORKINFO_FLAGS_REMOTE_CARD"></span><span id="networkinfo_flags_remote_card"></span><dl> <dt>**NETWORKINFO \_ FLAGS \_ REMOTE \_ CARD**</dt> </dl>                             | Die Netzwerkkarte befindet sich nicht auf dem lokalen Computer, sondern wird auf einem Remotecomputer auf dem lokalen Computer erfasst.<br/>                                      |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL"></span><span id="networkinfo_flags_remote_nal"></span><dl> <dt>**NETWORKINFO \_ FLAGS \_ REMOTE \_ NAL**</dt> </dl>                                | Veraltet; nicht verwenden.<br/>                                                                                                                                          |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL_CONNECTED"></span><span id="networkinfo_flags_remote_nal_connected"></span><dl> <dt>**NETWORKINFO \_ FLAGS \_ REMOTE \_ NAL \_ CONNECTED**</dt> </dl> | Veraltet; nicht verwenden.<br/>                                                                                                                                          |



 

</dd> <dt>

**TimestampScaleFactor**
</dt> <dd>

Beispielsweise gibt der Wert 1 1/1 ms an, 10 steht für 1/10 ms, 100 für 1/100 ms und so weiter.

</dd> <dt>

**NodeName**
</dt> <dd>

Name der Remotearbeitsstation.

</dd> <dt>

**PModeSupported**
</dt> <dd>

NIC-P-Modus-Unterstützungsindikator.

</dd> <dt>

**Comment**
</dt> <dd>

Adapterkommentarfeld.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




