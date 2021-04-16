---
description: Ruft einen Wert ab, der bestimmt, ob der angegebene dynamische Code im Arbeitsspeicher oder auf dem Datenträger mit der Device Guard-Richtlinie vertrauenswürdig ist.
ms.assetid: 9C12894D-98AF-4408-A11A-865E4DA1DA68
title: Wldpquerydynamiccodetrust-Funktion (wldp. h)
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
ms.openlocfilehash: 1b9b3cc30f5a02ae86fd8a30043a9ab417ec1ac7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523467"
---
# <a name="wldpquerydynamiccodetrust-function"></a>Wldpquerydynamiccodetrust-Funktion

Ruft einen Wert ab, der bestimmt, ob der angegebene dynamische Code im Arbeitsspeicher oder auf dem Datenträger mit der Device Guard-Richtlinie vertrauenswürdig ist.

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

*file handle* 
</dt> <dd>

Handle für die zu überprüfende dynamische Codedatei auf dem Datenträger. Wenn *File Handle* nicht **null** ist, sollte *baseImage* **null** sein.

</dd> <dt>

*baseImage* 
</dt> <dd>

Zeiger auf die zu Überprüfung der in-Memory-PE-Datei. Wenn *baseImage* nicht **null** ist, sollte *FILEHANDLE* **null** sein.

</dd> <dt>

*ImageSize* 
</dt> <dd>

Wenn *baseImage* ungleich **null** ist, gibt die Puffergröße an, auf die *baseImage* zeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt bei Erfolg **S \_ OK** zurück oder andernfalls einen Fehlercode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




