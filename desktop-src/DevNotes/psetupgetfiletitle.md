---
description: Ruft den Datei Titel für den angegebenen Dateipfad ab.
ms.assetid: 9a559d71-4883-4905-b3ad-64b256a2f51e
title: psetupgetfiletitle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupGetFileTitle
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 0b7869833a66799a4e617557cdfe6fdab9d64f67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358251"
---
# <a name="psetupgetfiletitle-function"></a>psetupgetfiletitle-Funktion

\[Diese Funktion ist in Windows Vista oder Windows Server 2008 nicht verfügbar.\]

Ruft den Datei Titel für den angegebenen Dateipfad ab.

## <a name="syntax"></a>Syntax


```C++
PCTSTR pSetupGetFileTitle(
  _In_ PCTSTR FilePath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FilePath* \[ in\]
</dt> <dd>

Der Dateipfad.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein Zeiger auf eine Zeichenfolge, die den Datei Titel empfängt.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
