---
description: Gibt Attribute für eine Authenticode-Signatur an.
ms.assetid: 1c1052c3-c5c5-48ae-8266-0b367800a84a
title: SIGNER_ATTR_AUTHCODE Struktur
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
ms.openlocfilehash: 952ed0f55a185d9a7ef9eeed3366f64c84423ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960898"
---
# <a name="signer_attr_authcode-structure"></a>Signer \_ attr \_ AuthCode-Struktur

Die **Signer \_ attr \_ AuthCode** -Struktur gibt Attribute für eine [*Authenticode*](../secgloss/a-gly.md) -Signatur an.

> [!Note]  
> Diese Struktur ist nicht in einer Header Datei definiert. Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.

 

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

**CBSIZE**
</dt> <dd>

Die Größe der-Struktur in Bytes.

</dd> <dt>

**gewerblich**
</dt> <dd>

" **True** ", um den Betreff als kommerzieller Verleger zu signieren. andernfalls **false**.

</dd> <dt>

**findividual**
</dt> <dd>

" **True** ", um den Betreff als einzelner Verleger zu signieren. andernfalls **false**.

</dd> <dt>

**pwszName**
</dt> <dd>

Der Anzeige Name der Datei beim herunterladen.

</dd> <dt>

**pwszinfo**
</dt> <dd>

Der Anzeige Name der URL der Datei beim herunterladen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_Signatur Informationen des Signatur Gebers \_**](signer-signature-info.md)
</dt> </dl>

 

 
