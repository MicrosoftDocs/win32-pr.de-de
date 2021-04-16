---
description: Gibt an, dass ein BLOB signiert werden soll.
ms.assetid: 214c9c05-5c95-4803-8993-23a87266f991
title: SIGNER_BLOB_INFO Struktur
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
ms.openlocfilehash: a05e99cc4d7fa2eff196159bb449fa7dbfbf3026
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530290"
---
# <a name="signer_blob_info-structure"></a>Signer \_ BLOB- \_ Informationsstruktur

\[Die Struktur der Signatur Geber- **\_ BLOB- \_ Informationen** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Die **Signatur Geber- \_ BLOB- \_ Informations** Struktur gibt ein [*BLOB*](../secgloss/b-gly.md) an, das signiert werden soll.

> [!Note]  
> Diese Struktur ist nicht in einer Header Datei definiert. Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.

 

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

**CBSIZE**
</dt> <dd>

Die Größe der-Struktur in Bytes.

</dd> <dt>

**pguidsubject**
</dt> <dd>

Ein Zeiger auf eine **GUID** , die das zu ladende "Subject Interface Package" (SIP) angibt.

</dd> <dt>

**cbblob**
</dt> <dd>

Die Größe des zu Signier enden BLOBs in Byte.

</dd> <dt>

**pbBlob**
</dt> <dd>

Ein Zeiger auf das zu Signier-BLOB.

</dd> <dt>

**pwszdisplayname**
</dt> <dd>

Der Anzeige Name des BLOBs. Dieser Member kann auf **null** festgelegt werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Betreff- \_ Informationen des Signatur Gebers \_**](signer-subject-info.md)
</dt> </dl>

 

 
