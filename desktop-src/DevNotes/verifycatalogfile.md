---
description: Überprüft eine einzelne Katalogdatei.
ms.assetid: 4b2de733-ef95-4b0a-8f53-7bc73ffaa2c2
title: VerifyCatalogFile-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: eb4012a04b4da9e353a5d771f9b9e61d4bfba8b45ed6a7d5c65a81c197ff9be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075744"
---
# <a name="verifycatalogfile-function"></a>VerifyCatalogFile-Funktion

\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden.\]

Überprüft eine einzelne Katalogdatei.

## <a name="syntax"></a>Syntax


```C++
DWORD VerifyCatalogFile(
   LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*CatalogFullPath* 
</dt> <dd>

Der vollqualifizierte Pfad der Katalogdatei, die überprüft werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, wird **ERROR \_ SUCCESS zurückgegeben.** Andernfalls wird der Fehler von [**WinVerifyTrust zurückgegeben.**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)

Wenn der Katalog ein authenticodesigniertes Katalog ist, gibt diese Funktion **ERROR \_ AUTHENTICODE \_ TRUSTED \_ PUBLISHER** zurück, wenn er erfolgreich ist. Andernfalls wird **ERROR \_ AUTHENTICODE TRUST NOT ESTABLISHED \_ \_ \_ zurückgegeben.**

Wenn die Funktion nicht ermitteln kann, ob der Herausgeber vertrauenswürdig ist, gibt sie möglicherweise auch **ERROR \_ UNIDENTIFIED \_ ERROR zurück.**

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
