---
description: Die Extract-Funktion extrahiert Dateien aus einem Schränk.
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
ms.openlocfilehash: cbcb53aae008423ac56bb489d43f6fd78016a9b1f716be21390a6dfc1de00404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162064"
---
# <a name="extract-function"></a>Extract-Funktion

\[Diese Funktion wird nicht mehr unterstützt, sodass ihr Verhalten nicht garantiert werden kann.\]

Die **Extract-Funktion** extrahiert Dateien aus einem Schränk.

## <a name="syntax"></a>Syntax


```C++
HRESULT Extract(
   PSESSION ps,
   LPCSTR   lpCabName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ps* 
</dt> <dd>

Zeiger auf eine [**SESSION-Struktur,**](session.md) die Informationen über die aktuelle Sitzung enthält.

</dd> <dt>

*lpCabName* 
</dt> <dd>

Zeiger auf den Namen des Schränks, aus dem Dateien extrahiert werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben. Andernfalls wird ein Fehlercode zurückgegeben.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DeleteExtractedFiles**](deleteextractedfiles.md)
</dt> <dt>

[**Erf**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf)
</dt> <dt>

[**Sitzung**](session.md)
</dt> </dl>

 

 
