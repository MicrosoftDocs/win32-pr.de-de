---
description: Die deleteextractedfiles-Funktion löscht die Dateien, die von der Extract-Funktion extrahiert wurden.
ms.assetid: 253e6267-d4be-46d6-bad2-2eb20bbc7e33
title: Deleteextractedfiles-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteExtractedFiles
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 4ab032864e59d8e7379fe347d241874d9336e431
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358064"
---
# <a name="deleteextractedfiles-function"></a>Deleteextractedfiles-Funktion

\[Diese Funktion wird nicht mehr unterstützt, sodass Ihr Verhalten nicht garantiert werden kann.\]

Die **deleteextractedfiles** -Funktion löscht die Dateien, die von der [**extract**](extract.md) -Funktion extrahiert wurden.

## <a name="syntax"></a>Syntax


```C++
VOID WINAPI DeleteExtractedFiles(
   PSESSION ps
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Psel* 
</dt> <dd>

Ein Zeiger auf eine [**Sitzungs**](session.md) Struktur, die Informationen über die aktuelle Sitzung enthält.

Diese Funktion gibt den Arbeitsspeicher im **pfilelist** -Member dieser Struktur frei und legt **pfilelist** auf **null** fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Extrahieren**](extract.md)
</dt> <dt>

[**Sitzung**](session.md)
</dt> </dl>

 

 
