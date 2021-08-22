---
description: Installiert einen Katalog in einem Verzeichnis.
ms.assetid: 9741f8e3-d9db-46cd-886d-587f332b0ab8
title: InstallCatalog-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 240754024135b5bd5aa48529d49080afbdb04e170987102346cdda2c59b12427
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955929"
---
# <a name="installcatalog-function"></a>InstallCatalog-Funktion

\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden.\]

Installiert einen Katalog in einem Verzeichnis.

## <a name="syntax"></a>Syntax


```C++
DWORD InstallCatalog(
  _In_      LPCTSTR                  CatalogFullPath,
  _In_opt_  LPCTSTR                  NewBaseName,
  _Out_opt_ ecount_(MAX_Path) LPTSTR NewCatalogFullPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*CatalogFullPath* \[ In\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den vollständigen Pfad des Katalogs vor der Installation darstellt.

</dd> <dt>

*NewBaseName* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf den neuen Basisnamen.

</dd> <dt>

*NewCatalogFullPath* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den vollständigen Pfad des Katalogs nach der Installation darstellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion ist derzeit nicht implementiert und gibt daher keinen tatsächlichen Wert zurück.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
