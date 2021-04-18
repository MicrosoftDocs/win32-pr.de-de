---
description: Überprüft eine einzelne Katalog Datei.
ms.assetid: 4b2de733-ef95-4b0a-8f53-7bc73ffaa2c2
title: Verifycatalogfile-Funktion
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
ms.openlocfilehash: 52083b23041f7f21aa51e326bc00d4cabc76eca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365178"
---
# <a name="verifycatalogfile-function"></a>Verifycatalogfile-Funktion

\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden.\]

Überprüft eine einzelne Katalog Datei.

## <a name="syntax"></a>Syntax


```C++
DWORD VerifyCatalogFile(
   LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Catalogfullpath* 
</dt> <dd>

Der voll qualifizierte Pfad der Katalog Datei, die überprüft werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird ein **Fehler \_ Erfolg** zurückgegeben; andernfalls wird der Fehler von [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)zurückgegeben.

Wenn es sich bei dem Katalog um einen mit Authenticode signierten Katalog handelt, gibt diese Funktion **Fehler \_ Authenticode \_ vertrauenswürdiger \_ Verleger** zurück, wenn Sie erfolgreich ist. andernfalls wird der **Fehler \_ Authenticode- \_ Vertrauensstellung \_ nicht \_ festgelegt**.

Wenn die Funktion nicht ermitteln kann, ob der Verleger vertrauenswürdig ist, kann der Fehler **nicht \_ \_ identifiziert werden.**

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
