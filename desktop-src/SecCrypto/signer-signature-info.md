---
description: Enthält Informationen über eine digitale Signatur.
ms.assetid: 0b86fdf9-533f-4640-8c70-c3c8f4ef2c68
title: SIGNER_SIGNATURE_INFO Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SIGNATURE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8e2b1fa68da51a649a01d4356ebfb1519ceeffb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216203"
---
# <a name="signer_signature_info-structure"></a>Signer \_ Signature \_ Info-Struktur

Die Signatur Informationsstruktur der Signatur Geber enthält Informationen über eine digitale Signatur. **\_ \_**

> [!Note]  
> Diese Struktur ist nicht in einer Header Datei definiert. Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.

 

## <a name="syntax"></a>Syntax


```C++
typedef struct _SIGNER_SIGNATURE_INFO {
  DWORD             cbSize;
  ALG_ID            algidHash;
  DWORD             dwAttrChoice;
  union {
    SIGNER_ATTR_AUTHCODE *pAttrAuthcode;
  };
  PCRYPT_ATTRIBUTES psAuthenticated;
  PCRYPT_ATTRIBUTES psUnauthenticated;
} SIGNER_SIGNATURE_INFO, *PSIGNER_SIGNATURE_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**CBSIZE**
</dt> <dd>

Die Größe der-Struktur in Bytes.

</dd> <dt>

**algidhash**
</dt> <dd>

Der für die digitale Signatur verwendete Hash Algorithmus.

</dd> <dt>

**dwattrchoice**
</dt> <dd>

Gibt an, ob die Signatur über [*Authenticode*](../secgloss/a-gly.md) -Attribute verfügt. Dieser Member kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                      | Bedeutung                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_AUTHCODE_ATTR"></span><span id="signer_authcode_attr"></span><dl> <dt>**Signatur \_ Geber AuthCode \_ attr**</dt> <dt>1</dt> </dl> | Die Signatur verfügt über [*Authenticode*](../secgloss/a-gly.md) -Attribute.<br/>           |
| <span id="SIGNER_NO_ATTR"></span><span id="signer_no_attr"></span><dl> <dt>**Signatur \_ Geber Keine \_ attr**</dt> <dt>0</dt> </dl>                   | Die Signatur weist keine [*Authenticode*](../secgloss/a-gly.md) -Attribute auf.<br/> |



 

</dd> <dt>

**pattrauthcode**
</dt> <dd>

Gibt Attribute für eine [*Authenticode*](../secgloss/a-gly.md) -Signatur an. Dieser Member ist erforderlich, wenn der Wert des **dwattrchoice** -Members " **Signer \_ AuthCode \_ attr**" lautet.

</dd> <dt>

**psauthenticated**
</dt> <dd>

Von authentifizierten Benutzern angegebene Attribute, die der digitalen Signatur hinzugefügt werden.

</dd> <dt>

**psunauthenticated**
</dt> <dd>

Nicht authentifizierte benutzerdefinierte Attribute, die der digitalen Signatur hinzugefügt werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Signersign**](signersign.md)
</dt> <dt>

[**Signersignetx**](signersignex.md)
</dt> </dl>

 

 
