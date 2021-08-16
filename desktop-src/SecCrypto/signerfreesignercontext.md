---
description: Gibt eine SIGNER \_ CONTEXT-Struktur frei, die durch einen vorherigen Aufruf der SignerSignEx-Funktion zugeordnet wurde.
ms.assetid: 190de302-50fe-488e-90ed-c9efd39dae70
title: SignerFreeSignerContext-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerFreeSignerContext
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 8338e346db49b21f9eccfca11a7e1a1fff0c42f0a013139a097385fbbe90c76f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973191"
---
# <a name="signerfreesignercontext-function"></a>SignerFreeSignerContext-Funktion

Die **SignerFreeSignerContext-Funktion** gibt eine [**SIGNER \_ CONTEXT-Struktur**](signer-context.md) frei, die durch einen vorherigen Aufruf der [**SignerSignEx-Funktion zugeordnet**](signersignex.md) wurde.

> [!Note]  
> Dieser Funktion ist keine Headerdatei oder Importbibliothek zugeordnet. Zum Aufrufen dieser Funktion müssen Sie eine benutzerdefinierte Headerdatei erstellen und die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um eine dynamische Verknüpfung mit Mssign32.dll.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI SignerFreeSignerContext(
  _In_ SIGNER_CONTEXT *pSignerContext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSignerContext* \[ In\]
</dt> <dd>

Ein Zeiger auf die [**frei zu gebende SIGNER \_ CONTEXT-Struktur.**](signer-context.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt sie S \_ OK zurück.

Wenn die Funktion fehlschlägt, wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_SIGNER-KONTEXT**](signer-context.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
