---
description: Die networkinfo-Struktur beschreibt eine NIC.
ms.assetid: 40169409-7de5-44d1-8dff-dfa9f647edc9
title: Networkinfo-Struktur (Netmon. h)
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
ms.openlocfilehash: 8917966d2e090417a95a9ca20158c6c5935bda3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760129"
---
# <a name="networkinfo-structure"></a>Networkinfo-Struktur

Die networkinfo-Struktur beschreibt eine NIC.

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

**Permanent addr**
</dt> <dd>

Permanente Mac-Adresse.

</dd> <dt>

**Currentaddr**
</dt> <dd>

Aktuelle Mac-Adresse.

</dd> <dt>

**OtherAddress**
</dt> <dd>

Weitere Adresse, die dies unterstützt (z. b. IP, IPX).

</dd> <dt>

**LinkSpeed**
</dt> <dd>

Verbindungsgeschwindigkeit in Mbit/s.

</dd> <dt>

**MacType**
</dt> <dd>

Medientyp.

</dd> <dt>

**MaxFrameSize**
</dt> <dd>

Maximale Frame Größe zulässig.

</dd> <dt>

**Flags**
</dt> <dd>

Dieser Parameter kann eine der folgenden informationsflags sein:



| Wert                                                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NETWORKINFO_FLAGS_PMODE_NOT_SUPPORTED"></span><span id="networkinfo_flags_pmode_not_supported"></span><dl> <dt>**networkinfo- \_ Flags \_ pmode \_ \_ wird nicht unterstützt.**</dt> </dl>    | Die Netzwerkkarte unterstützt den gemischten-Modus nicht. Dies bedeutet, dass nur Datenverkehr erfasst wird, der in der Natur übertragen wird, oder nur den lokalen Computer einbezieht.<br/> |
| <span id="NETWORKINFO_FLAGS_RAS"></span><span id="networkinfo_flags_ras"></span><dl> <dt>**networkinfo- \_ Flags ( \_ RAS)**</dt> </dl>                                                      | Dies ist eine virtuelle Netzwerkkarte, bei der es sich um eine RAS-Verbindung (RAS-Server) über ein Modem oder eine andere Netzwerkkarte handelt.<br/>                                        |
| <span id="NETWORKINFO_FLAGS_REMOTE_CARD"></span><span id="networkinfo_flags_remote_card"></span><dl> <dt>**networkinfo- \_ Flags- \_ Remote \_ Karte**</dt> </dl>                             | Die Netzwerkkarte befindet sich nicht auf dem lokalen Computer, sondern wird auf einem Remote Computer auf dem Weg des lokalen Computers erfasst.<br/>                                      |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL"></span><span id="networkinfo_flags_remote_nal"></span><dl> <dt>**networkinfo- \_ Flags \_ Remote- \_ nal**</dt> </dl>                                | Veralteten Verwenden Sie nicht.<br/>                                                                                                                                          |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL_CONNECTED"></span><span id="networkinfo_flags_remote_nal_connected"></span><dl> <dt>**networkinfo \_ Flags \_ Remote- \_ nal- \_ Verbindung**</dt> </dl> | Veralteten Verwenden Sie nicht.<br/>                                                                                                                                          |



 

</dd> <dt>

**Timestampscalefactor**
</dt> <dd>

Der Wert 1 gibt z. b. 1/1 MS an, 10 gibt 1/10 MS an, 100 gibt 1/100 MS an usw.

</dd> <dt>

**NodeName**
</dt> <dd>

Name der Remote Arbeitsstation.

</dd> <dt>

**Pmodesupported**
</dt> <dd>

Support Indikator für den NIC-P-Modus.

</dd> <dt>

**Kommentar**
</dt> <dd>

Feld für den Adapter Kommentar.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




