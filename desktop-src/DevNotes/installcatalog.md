---
description: Installiert einen Katalog in einem Verzeichnis.
ms.assetid: 9741f8e3-d9db-46cd-886d-587f332b0ab8
title: Installcatalog-Funktion
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
ms.openlocfilehash: 57b2a9d29b72db6c04673f30f41f26c44701c69c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356020"
---
# <a name="installcatalog-function"></a>Installcatalog-Funktion

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

*Catalogfullpath* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den vollständigen Pfad des Katalogs vor der Installation darstellt.

</dd> <dt>

*Newbasename* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf den neuen Basisnamen.

</dd> <dt>

*Newcatalogfullpath* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den vollständigen Pfad des Katalogs nach der Installation darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion ist zurzeit nicht implementiert, sodass Sie keinen tatsächlichen Wert zurückgibt.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
