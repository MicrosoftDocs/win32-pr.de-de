---
description: Die HANDOFFENTRY-Struktur definiert einen bestimmten Protokolleintrag in einer HANDOFFTABLE-Struktur.
ms.assetid: 85793326-3007-4dd9-9325-3447d6e09883
title: HANDOFFENTRY-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 692b9e925442920a67434f74c9e8a8ebd225fc417cbbf419b6eb568aa9eee2df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117981413"
---
# <a name="handoffentry-structure"></a>HANDOFFENTRY-Struktur

Die **HANDOFFENTRY-Struktur** definiert einen bestimmten Protokolleintrag in einer **HANDOFFTABLE-Struktur.**

Diese Struktur wird auf der Grundlage Netzwerkmonitor informationen in einer vom Benutzer bereitgestellten Datei .ini [**CreateHandoffTable-Funktion**](createhandofftable.md) ausgefüllt. Diese Struktur sollte nie explizit von einer Anwendung geändert werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _SESSIONSTATS {
  DWORD      hoe_sig;
  DWORD      hoe_ProtIdentNumber;
  HPPROTOCOL hoe_ProtocolHandle;
  DWORD      hoe_ProtocolData;
} HANDOFFENTRY, *LPHANDOFFENTRY;
```



## <a name="members"></a>Member

<dl> <dt>

**\_sig**
</dt> <dd>

Signatur, die diesen Eintrag als Übergabetabelleneintrag identifiziert.

</dd> <dt>

**ite \_ ProtIdentNumber**
</dt> <dd>

Protokollnummer, die von der vom Benutzer bereitgestellten .ini wird.

</dd> <dt>

**ub \_ ProtocolHandle**
</dt> <dd>

Handle des Protokolls, das mit dem Protokollnamen erstellt wurde, der vom Benutzer bereitgestellt .ini wird.

</dd> <dt>

**Protokolldaten \_**
</dt> <dd>

Protokollinstanzdaten, die vom Benutzer bereitgestellt .ini werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird durch die Netzwerkmonitor, wenn Netzwerkmonitor eine Übergabetabelle erstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[HANDOFFTABLE](handofftable.md)
</dt> </dl>

 

 




