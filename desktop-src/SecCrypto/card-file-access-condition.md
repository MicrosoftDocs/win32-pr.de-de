---
description: Gibt Zugriffssteuerungsberechtigungen für eine Datei auf einer Smartcard an.
ms.assetid: 995d959f-30dc-4e5c-be2d-6b447499415a
title: CARD_FILE_ACCESS_CONDITION -Enumeration (Cardmod.h)
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
ms.openlocfilehash: e9a38e7d67e413352de693f52b07ba11bf34858854fa708b41a735152ad3ed2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771986"
---
# <a name="card_file_access_condition-enumeration"></a>CARD \_ FILE \_ ACCESS \_ CONDITION-Enumeration

Die **CARD FILE ACCESS \_ \_ \_ CONDITION-Enumeration** gibt Zugriffssteuerungsberechtigungen für eine Datei auf einer [*Smartcard an.*](../secgloss/s-gly.md)

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

<span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**
</dt> <dd>

Dieser Wert ist ungültig.

</dd> <dt>

<span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**EveryoneReadUserWriteAc**
</dt> <dd>

Jeder kann die Datei lesen. Bestimmte Benutzer können in die Datei schreiben.

</dd> <dt>

<span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**UserWriteExecuteAc**
</dt> <dd>

Nur bestimmte Benutzer können die Datei lesen oder in diese schreiben.

</dd> <dt>

<span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**EveryoneReadAdminWriteAc**
</dt> <dd>

Jeder kann die Datei lesen. Administratoren können in die Datei schreiben.

</dd> <dt>

<span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**UnknownAc**
</dt> <dd>

Zugriffsberechtigungen für die Datei sind unbekannt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP- Windows \[ XP-Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2003 Windows Server \[ 2003-Desktop-Apps\]<br/>            |
| Header<br/>                   | <dl> <dt>Cardmod.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Microsoft-Basis-Smartcard-Kryptografiedienstanbieter](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[**\_ \_ KARTENDATEIINFORMATIONEN**](/previous-versions/windows/desktop/secsmart/card-file-info)
</dt> <dt>

[**CardCreateFile**](/previous-versions/windows/desktop/secsmart/cardcreatefile)
</dt> </dl>

 

 
