---
description: Gibt eine zu signierende Datei an.
ms.assetid: 5b45d855-ede8-43eb-9253-e3fe1716686b
title: SIGNER_FILE_INFO-Struktur
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
ms.openlocfilehash: b0bb1bce810d87d70e05284e3d13942c5e2e49d07bd2d829c3839f793ae6a061
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898826"
---
# <a name="signer_file_info-structure"></a>SIGNER \_ FILE \_ INFO-Struktur

Die **SIGNER \_ FILE \_ INFO-Struktur** gibt eine zu signierende Datei an.

> [!Note]  
> Diese Struktur ist in einer Headerdatei nicht definiert. Um diese Struktur zu verwenden, müssen Sie sie selbst definieren, wie in diesem Thema gezeigt.

 

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

**cbSize**
</dt> <dd>

Die Größe der -Struktur in Bytes.

</dd> <dt>

**pwszFileName**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen der zu signierenden Datei enthält.

</dd> <dt>

**hFile**
</dt> <dd>

Ein geöffnetes Handle für die Datei, die vom **pwszFileName-Member angegeben** wird. Wenn dieser Member ein gültiges Handle enthält, wird dieses Handle für den Zugriff auf die Datei verwendet. Dieser Member kann auf NULL **festgelegt werden.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SIGNER \_ SUBJECT \_ INFO**](signer-subject-info.md)
</dt> </dl>

 

 




