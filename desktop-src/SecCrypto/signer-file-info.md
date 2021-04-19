---
description: Gibt eine Datei an, die signiert werden soll.
ms.assetid: 5b45d855-ede8-43eb-9253-e3fe1716686b
title: SIGNER_FILE_INFO Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_FILE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 71e7c360d0034d9435386cf31579299c6d047131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362926"
---
# <a name="signer_file_info-structure"></a>Struktur der Signatur Geber \_ Datei \_

Die **Signatur Geber \_ Datei \_ Info** -Struktur gibt eine zu Signier ender Datei an.

> [!Note]  
> Diese Struktur ist nicht in einer Header Datei definiert. Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.

 

## <a name="syntax"></a>Syntax


```C++
typedef struct _SIGNER_FILE_INFO {
  DWORD   cbSize;
  LPCWSTR pwszFileName;
  HANDLE  hFile;
} SIGNER_FILE_INFO, *PSIGNER_FILE_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**CBSIZE**
</dt> <dd>

Die Größe der-Struktur in Bytes.

</dd> <dt>

**pwszFileName**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen der zu Signier enden Datei enthält.

</dd> <dt>

**hFile**
</dt> <dd>

Ein geöffnetes Handle für die Datei, die vom **pwszFileName** -Member angegeben wird. Wenn dieser Member ein gültiges Handle enthält, wird dieser Handle für den Zugriff auf die Datei verwendet. Dieser Member kann auf **null** festgelegt werden.

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

 

 




