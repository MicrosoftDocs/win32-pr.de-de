---
description: Ruft einen Wert ab, der bestimmt, ob der angegebene dynamische Code der .NET-CRL im Arbeitsspeicher oder auf dem Datenträger von der Device Guard-Richtlinie als vertrauenswürdig eingestuft wird.
ms.assetid: 9C12894D-98AF-4408-A11A-865E4DA1DA68
title: WldpQueryDynamicCodeTrust-Funktion (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 00b26c8d237a8c6d725751be064c7b82fc7a600c452598a590a747ba10ae56d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075724"
---
# <a name="wldpquerydynamiccodetrust-function"></a>WldpQueryDynamicCodeTrust-Funktion

Ruft einen Wert ab, der bestimmt, ob der angegebene dynamische Code der .NET-CRL im Arbeitsspeicher oder auf dem Datenträger von der Device Guard-Richtlinie als vertrauenswürdig eingestuft wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI WldpQueryDynamicCodeTrust(
   _When_(baseImage != NULL, _In_opt_)
    _When_(baseImage == NULL, _In_)
    HANDLE                                                 fileHandle,
   _When_(fileHandle == NULL, _In_reads_bytes_opt_(imageSize))
    _When_(fileHandle != NULL, _In_reads_bytes_(imageSize))
    PVOID  baseImage,
   _In_ ULONG                                                                                                                         ImageSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Filehandle* 
</dt> <dd>

Behandeln Sie die zu überprüfende dynamische Codedatei auf dem Datenträger. Wenn *fileHandle* ungleich **NULL** ist, sollte *baseImage* **NULL** sein.

</dd> <dt>

*baseImage* 
</dt> <dd>

Zeiger auf die zu überprüfende PE-Datei im Arbeitsspeicher. Wenn *baseImage* ungleich **NULL** ist, sollte *FileHandle* **NULL** sein.

</dd> <dt>

*Imagesize* 
</dt> <dd>

Wenn *baseImage* ungleich **NULL** ist, gibt die Puffergröße an, auf die *baseImage* zeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt **S \_ OK** zurück, wenn erfolgreich ist, oder andernfalls einen Fehlercode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wldp.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




