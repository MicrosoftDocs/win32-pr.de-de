---
description: Gibt Attribute für eine Authenticode-Signatur an.
ms.assetid: 1c1052c3-c5c5-48ae-8266-0b367800a84a
title: SIGNER_ATTR_AUTHCODE-Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_ATTR_AUTHCODE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2cce522403e4b4e416bd3d1ecb9d6c4a551ef3bb67407f853f586bd061f3d8e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898947"
---
# <a name="signer_attr_authcode-structure"></a>SIGNER \_ ATTR \_ AUTHCODE-Struktur

Die **SIGNER \_ ATTR \_ AUTHCODE-Struktur** gibt Attribute für eine [*Authenticode-Signatur*](../secgloss/a-gly.md) an.

> [!Note]  
> Diese Struktur ist in einer Headerdatei nicht definiert. Um diese Struktur zu verwenden, müssen Sie sie selbst definieren, wie in diesem Thema gezeigt.

 

## <a name="syntax"></a>Syntax


```C++
typedef struct _SIGNER_ATTR_AUTHCODE {
  DWORD   cbSize;
  BOOL    fCommercial;
  BOOL    fIndividual;
  LPCWSTR pwszName;
  LPCWSTR pwszInfo;
} SIGNER_ATTR_AUTHCODE, *PSIGNER_ATTR_AUTHCODE;
```



## <a name="members"></a>Member

<dl> <dt>

**cbSize**
</dt> <dd>

Die Größe der -Struktur in Bytes.

</dd> <dt>

**fCommercial**
</dt> <dd>

**TRUE,** um den Betreff als kommerziellen Herausgeber zu signieren; andernfalls **FALSE**.

</dd> <dt>

**fIndividual**
</dt> <dd>

**TRUE,** um den Betreff als einzelnen Herausgeber zu signieren; andernfalls **FALSE**.

</dd> <dt>

**pwszName**
</dt> <dd>

Der Anzeigename der Datei beim Download.

</dd> <dt>

**pwszInfo**
</dt> <dd>

Der Anzeigename der URL der Datei beim Download.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SIGNATURINFORMATIONEN \_ FÜR \_ SIGNATUR**](signer-signature-info.md)
</dt> </dl>

 

 
