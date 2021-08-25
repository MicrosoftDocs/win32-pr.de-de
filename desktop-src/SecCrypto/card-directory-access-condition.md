---
description: Gibt Zugriffssteuerungsberechtigungen für ein Verzeichnis auf einer Smartcard an.
ms.assetid: 361d9fa0-286e-4d2c-8452-3b5f48e77779
title: CARD_DIRECTORY_ACCESS_CONDITION-Enumeration (Cardmod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_DIRECTORY_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: 8038179c7337edaff0138fc46c34191f99821250808c4ace16dc76cdfafd3b19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878960"
---
# <a name="card_directory_access_condition-enumeration"></a>CARD \_ DIRECTORY \_ ACCESS \_ CONDITION-Enumeration

Die **CARD DIRECTORY ACCESS \_ \_ \_ CONDITION-Enumeration** gibt Zugriffssteuerungsberechtigungen für ein Verzeichnis auf einer [*Smartcard*](../secgloss/s-gly.md)an.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  InvalidAc               = 0,
  UserCreateDeleteDirAc   = 1,
  AdminCreateDeleteDirAc  = 2
} CARD_DIRECTORY_ACCESS_CONDITION;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**
</dt> <dd>

Dieser Wert ist ungültig.

</dd> <dt>

<span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**UserCreateDeleteDirAc**
</dt> <dd>

Bestimmte Benutzer können das Verzeichnis lesen, schreiben und löschen.

</dd> <dt>

<span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**AdminCreateDeleteDirAc**
</dt> <dd>

Administratoren können das Verzeichnis lesen, schreiben und löschen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP- Windows \[ XP-Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2003- Windows Server \[ 2003-Desktop-Apps\]<br/>            |
| Header<br/>                   | <dl> <dt>Cardmod.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Microsoft Base Smart Card Cryptographic Service Provider](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[**CardCreateDirectory**](/previous-versions/windows/desktop/secsmart/cardcreatedirectory)
</dt> <dt>

[**CardDeleteDirectory**](/previous-versions/windows/desktop/secsmart/carddeletedirectory)
</dt> </dl>

 

 
