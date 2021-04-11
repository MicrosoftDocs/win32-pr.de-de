---
description: Gibt Zugriffs Steuerungs Berechtigungen für ein Verzeichnis auf einer Smartcard an.
ms.assetid: 361d9fa0-286e-4d2c-8452-3b5f48e77779
title: CARD_DIRECTORY_ACCESS_CONDITION-Enumeration (cardmod. h)
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
ms.openlocfilehash: 9879fa73f6bb45b56f433d7bca7765ab5fc0daef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214528"
---
# <a name="card_directory_access_condition-enumeration"></a>\_ \_ Enumeration der Zugriffsbedingung für Karten Verzeichnisse \_

Die Enumeration der **\_ \_ Zugriffsbedingung \_ für Karten Verzeichnisse** gibt Zugriffs Steuerungs Berechtigungen für ein Verzeichnis auf einer [*Smartcard*](../secgloss/s-gly.md)an.

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

<span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**Invalidac**
</dt> <dd>

Dieser Wert ist ungültig.

</dd> <dt>

<span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**Userkreatedeletedirac**
</dt> <dd>

Bestimmte Benutzer können das Verzeichnis lesen, schreiben und löschen.

</dd> <dt>

<span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**Adminkreatedeletedirac**
</dt> <dd>

Administratoren können das Verzeichnis lesen, schreiben und löschen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP, Windows XP \[ Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows Server 2003 \[ Desktop-Apps\]<br/>            |
| Header<br/>                   | <dl> <dt>Cardmod. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kryptografiedienstanbieter für Microsoft Base Smartcard](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[**Cardkreatedirectory**](/previous-versions/windows/desktop/secsmart/cardcreatedirectory)
</dt> <dt>

[**Carddeletedirectory**](/previous-versions/windows/desktop/secsmart/carddeletedirectory)
</dt> </dl>

 

 
