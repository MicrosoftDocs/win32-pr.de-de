---
description: Definiert ein Paar aus 802.11-Authentifizierungs- und Verschlüsselungsalgorithmen, die gleichzeitig auf der 802.11-Station aktiviert werden können.
ms.assetid: 5fbe23f6-7902-46d4-a1f0-57f045d78662
title: DOT11_AUTH_CIPHER_PAIR-Struktur (Wlantypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_CIPHER_PAIR
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: 84e4abde6192cf1be92b21df0c6a79125a198e0fde28e304cf583d76ea91689f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801480"
---
# <a name="dot11_auth_cipher_pair-structure"></a>DOT11 \_ AUTH \_ CIPHER \_ PAIR-Struktur

Die **DOT11 \_ AUTH \_ CIPHER \_ PAIR-Struktur** definiert ein Paar aus 802.11-Authentifizierungs- und Verschlüsselungsalgorithmen, die gleichzeitig auf der 802.11-Station aktiviert werden können.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DOT11_AUTH_CIPHER_PAIR {
  DOT11_AUTH_ALGORITHM   AuthAlgoId;
  DOT11_CIPHER_ALGORITHM CipherAlgoId;
} DOT11_AUTH_CIPHER_PAIR, *PDOT11_AUTH_CIPHER_PAIR;
```



## <a name="members"></a>Member

<dl> <dt>

**AuthAlgoId**
</dt> <dd>

Ein Authentifizierungsalgorithmus, der einen [**DOT11 \_ AUTH ALGORITHM-Enumerationstyp \_**](dot11-auth-algorithm.md) verwendet.

</dd> <dt>

**CipherAlgoId**
</dt> <dd>

Ein Verschlüsselungsalgorithmus, der einen [**DOT11 \_ CIPHER ALGORITHM-Enumerationstyp \_**](dot11-cipher-algorithm.md) verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die DOT11 \_ AUTH \_ CIPHER \_ PAIR-Struktur definiert einen Authentifizierungs- und Verschlüsselungsalgorithmus, der zusammen für BSS-Netzwerkverbindungen (Basic Service Set) aktiviert werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP nur mit \[ SP3-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                        |
| Verteilbare Komponente<br/>          | WLAN-API für Windows XP mit SP2<br/>                                                         |
| Header<br/>                   | <dl> <dt>Wlantypes.h (einschließlich Windot11.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_DOT11-AUTHENTIFIZIERUNGSALGORITHMUS \_**](dot11-auth-algorithm.md)
</dt> <dt>

[**\_DOT11-VERSCHLÜSSELUNGSALGORITHMUS \_**](dot11-cipher-algorithm.md)
</dt> </dl>

 

 




