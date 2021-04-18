---
description: Definiert ein paar von 802,11-Authentifizierungs-und Verschlüsselungsalgorithmen, die gleichzeitig auf der 802,11-Station aktiviert werden können.
ms.assetid: 5fbe23f6-7902-46d4-a1f0-57f045d78662
title: DOT11_AUTH_CIPHER_PAIR Struktur (wlantypes. h)
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
ms.openlocfilehash: fd1a8ef03d5c5cb897d95b768f8ab48705098d74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358541"
---
# <a name="dot11_auth_cipher_pair-structure"></a>DOT11 \_ auth- \_ Chiffre- \_ paar-Struktur

Die **DOT11 \_ auth- \_ Chiffre- \_ paar** -Struktur definiert ein paar von 802,11-Authentifizierungs-und Verschlüsselungsalgorithmen, die gleichzeitig auf der 802,11-Station aktiviert werden können.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DOT11_AUTH_CIPHER_PAIR {
  DOT11_AUTH_ALGORITHM   AuthAlgoId;
  DOT11_CIPHER_ALGORITHM CipherAlgoId;
} DOT11_AUTH_CIPHER_PAIR, *PDOT11_AUTH_CIPHER_PAIR;
```



## <a name="members"></a>Member

<dl> <dt>

**Authalgoid**
</dt> <dd>

Ein Authentifizierungsalgorithmus, der einen enumerierten Typ des [**DOT11 \_ auth- \_ Algorithmus**](dot11-auth-algorithm.md) verwendet.

</dd> <dt>

**Cipheralgoid**
</dt> <dd>

Ein Verschlüsselungsalgorithmus, der einen enumerierten Typ des [**DOT11 \_ Chiffre \_ Algorithmus**](dot11-cipher-algorithm.md) verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die DOT11 \_ auth- \_ Chiffre \_ -paar-Struktur definiert einen Authentifizierungs-und Chiffre Algorithmus, der zusammen für Basic Service Set (BSS)-Netzwerkverbindungen aktiviert werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                        |
| Verteilbare Komponente<br/>          | Drahtlose LAN-API für Windows XP mit SP2<br/>                                                         |
| Header<br/>                   | <dl> <dt>Wlantypes. h (Include Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DOT11 \_ auth- \_ Algorithmus**](dot11-auth-algorithm.md)
</dt> <dt>

[**DOT11- \_ Chiffre \_ Algorithmus**](dot11-cipher-algorithm.md)
</dt> </dl>

 

 




