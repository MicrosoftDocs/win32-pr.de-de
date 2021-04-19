---
description: Gibt Zugriffs Steuerungs Berechtigungen für eine Datei auf einer Smartcard an.
ms.assetid: 995d959f-30dc-4e5c-be2d-6b447499415a
title: CARD_FILE_ACCESS_CONDITION-Enumeration (cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_FILE_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: d3ef9fc81c9ab3bff5f3992c3aedeb3f923648ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356733"
---
# <a name="card_file_access_condition-enumeration"></a>\_ \_ Zugriffsbedingungs-Enumeration für Kartendatei \_

Die Enumeration der **\_ kartendateizugriffsbedingung \_ \_** gibt Zugriffs Steuerungs Berechtigungen für eine Datei auf einer [*Smartcard*](../secgloss/s-gly.md)an.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  InvalidAc                 = 0,
  EveryoneReadUserWriteAc   = 1,
  UserWriteExecuteAc        = 2,
  EveryoneReadAdminWriteAc  = 3,
  UnknownAc                 = 4
} CARD_FILE_ACCESS_CONDITION;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**Invalidac**
</dt> <dd>

Dieser Wert ist ungültig.

</dd> <dt>

<span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**Everyonereaduserschreiteac**
</dt> <dd>

Alle Benutzer können die Datei lesen. Bestimmte Benutzer können in die Datei schreiben.

</dd> <dt>

<span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**Userschreiteexecuteac**
</dt> <dd>

Nur bestimmte Benutzer können die Datei lesen oder in diese schreiben.

</dd> <dt>

<span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**Everyonereadadminschreiteac**
</dt> <dd>

Alle Benutzer können die Datei lesen. Administratoren können in die Datei schreiben.

</dd> <dt>

<span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**Unknownac**
</dt> <dd>

Die Zugriffsberechtigungen für die Datei sind unbekannt.

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

[**Informationen zur Karten \_ Datei \_**](/previous-versions/windows/desktop/secsmart/card-file-info)
</dt> <dt>

[**Cardkreatefile**](/previous-versions/windows/desktop/secsmart/cardcreatefile)
</dt> </dl>

 

 
