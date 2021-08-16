---
description: Gibt ein zu signierendes BLOB an.
ms.assetid: 214c9c05-5c95-4803-8993-23a87266f991
title: SIGNER_BLOB_INFO-Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_BLOB_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: a865a65b5fd9a1ec658dcc86b1eb2b3dd255804308f04bebf4fffdb0650d71e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898927"
---
# <a name="signer_blob_info-structure"></a>SIGNER \_ BLOB \_ INFO-Struktur

\[Die **\_ SIGNER-BLOB-INFO-Struktur \_** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Die **SIGNER \_ BLOB \_ INFO-Struktur** gibt ein zu signierendes [*BLOB*](../secgloss/b-gly.md) an.

> [!Note]  
> Diese Struktur ist in keiner Headerdatei definiert. Um diese Struktur zu verwenden, müssen Sie sie selbst definieren, wie in diesem Thema gezeigt.

 

## <a name="syntax"></a>Syntax


```C++
typedef struct _SIGNER_BLOB_INFO {
  DWORD   cbSize;
  GUID    *pGuidSubject;
  DWORD   cbBlob;
  BYTE    *pbBlob;
  LPCWSTR pwszDisplayName;
} SIGNER_BLOB_INFO, *PSIGNER_BLOB_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**cbSize**
</dt> <dd>

Die Größe der Struktur in Bytes.

</dd> <dt>

**pGuidSubject**
</dt> <dd>

Ein Zeiger auf eine **GUID,** die das zu ladende Subject Interface Package (SIP) angibt.

</dd> <dt>

**cbBlob**
</dt> <dd>

Die Größe des zu signierenden BLOB in Bytes.

</dd> <dt>

**pbBlob**
</dt> <dd>

Ein Zeiger auf das zu signierende BLOB.

</dd> <dt>

**pwszDisplayName**
</dt> <dd>

Der Anzeigename des BLOB. Dieser Member kann auf **NULL** festgelegt werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INFORMATIONEN ZUM ANTRAGSTELLER DES SIGNIERERS \_ \_**](signer-subject-info.md)
</dt> </dl>

 

 
