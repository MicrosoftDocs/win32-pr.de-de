---
description: Die Extract-Funktion extrahiert Dateien aus einer CAB-Datei.
ms.assetid: c6a79d81-7adf-4b8e-a1ef-fec868f7fdbf
title: Extract-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extract
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 2e1096cdb7909f49fbcac7c32891210b25637c90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359658"
---
# <a name="extract-function"></a>Extract-Funktion

\[Diese Funktion wird nicht mehr unterstützt, sodass Ihr Verhalten nicht garantiert werden kann.\]

Die **extract** -Funktion extrahiert Dateien aus einer CAB-Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT Extract(
   PSESSION ps,
   LPCSTR   lpCabName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Psel* 
</dt> <dd>

Ein Zeiger auf eine [**Sitzungs**](session.md) Struktur, die Informationen über die aktuelle Sitzung enthält.

</dd> <dt>

*lpcabname* 
</dt> <dd>

Ein Zeiger auf den Namen der CAB-Datei, aus der Dateien extrahiert werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück; andernfalls wird ein Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Deleteextractedfiles**](deleteextractedfiles.md)
</dt> <dt>

[**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf)
</dt> <dt>

[**Sitzung**](session.md)
</dt> </dl>

 

 
