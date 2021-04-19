---
description: Gibt einen Betreff an, der signiert werden soll.
ms.assetid: ba569443-e50f-450b-82cc-b7328f0ca25a
title: SIGNER_SUBJECT_INFO Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SUBJECT_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 05b5d780e50f8ea10fcf68cc90ae7092bbc2c473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349807"
---
# <a name="signer_subject_info-structure"></a>Struktur der Signatur Geber \_ \_ Informationen

Die **\_ \_ betreffinformations** Struktur des Signatur Gebers gibt einen Betreff an, der signiert werden soll.

> [!Note]  
> Diese Struktur ist nicht in einer Header Datei definiert. Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.

 

## <a name="syntax"></a>Syntax


```C++
typedef struct _SIGNER_SUBJECT_INFO {
  DWORD cbSize;
  DWORD *pdwIndex;
  DWORD dwSubjectChoice;
  union {
    SIGNER_FILE_INFO *pSignerFileInfo;
    SIGNER_BLOB_INFO *pSignerBlobInfo;
  };
} SIGNER_SUBJECT_INFO, *PSIGNER_SUBJECT_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**CBSIZE**
</dt> <dd>

Die Größe der-Struktur in Bytes.

</dd> <dt>

**pdwindex**
</dt> <dd>

Dieser Member ist reserviert. Er muss auf 0 (null) festgelegt werden.

</dd> <dt>

**dwsubjetchoice**
</dt> <dd>

Gibt an, ob der Betreff eine Datei oder ein [*BLOB*](../secgloss/b-gly.md)ist. Dieser Member kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                         | Bedeutung                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SIGNER_SUBJECT_BLOB"></span><span id="signer_subject_blob"></span><dl> <dt>**Signatur \_ Geber Subject \_ BLOB**</dt> <dt>2 (0x2)</dt> </dl> | Der Betreff ist ein BLOB.<br/> |
| <span id="SIGNER_SUBJECT_FILE"></span><span id="signer_subject_file"></span><dl> <dt>**Signatur \_ Geber \_Betreffdatei**</dt> <dt>1 (0x1)</dt> </dl> | Der Betreff ist eine Datei.<br/> |



 

</dd> <dt>

**psignerfileingefo**
</dt> <dd>

Ein Zeiger auf die [**\_ \_ Informations**](signer-file-info.md) Struktur der Signatur Geber Datei, die die zu Signier ender Datei angibt.

</dd> <dt>

**psignerblobinfo**
</dt> <dd>

Ein Zeiger auf eine [**Signatur Geber- \_ BLOB- \_ Informations**](signer-blob-info.md) Struktur, die das zu Signier ender BLOB angibt.

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

 

 
