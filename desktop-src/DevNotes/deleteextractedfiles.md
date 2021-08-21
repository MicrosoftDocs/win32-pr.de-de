---
description: Die DeleteExtractedFiles-Funktion löscht die Dateien, die von der Extract-Funktion extrahiert wurden.
ms.assetid: 253e6267-d4be-46d6-bad2-2eb20bbc7e33
title: DeleteExtractedFiles-Funktion
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
ms.openlocfilehash: 500de4df41c82f1956f50abcc25dc84f11484b693dc8d1a5f8bc53ab556ade0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162091"
---
# <a name="deleteextractedfiles-function"></a>DeleteExtractedFiles-Funktion

\[Diese Funktion wird nicht mehr unterstützt, sodass ihr Verhalten nicht garantiert werden kann.\]

Die **DeleteExtractedFiles-Funktion** löscht die Dateien, die von der [**Extract-Funktion extrahiert**](extract.md) wurden.

## <a name="syntax"></a>Syntax


```C++
VOID WINAPI DeleteExtractedFiles(
   PSESSION ps
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ps* 
</dt> <dd>

Ein Zeiger auf eine [**SESSION-Struktur,**](session.md) die Informationen zur aktuellen Sitzung enthält.

Diese Funktion gibt den Arbeitsspeicher im **pFileList-Member** dieser Struktur frei und legt **pFileList auf** **NULL fest.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Extract**](extract.md)
</dt> <dt>

[**Sitzung**](session.md)
</dt> </dl>

 

 
