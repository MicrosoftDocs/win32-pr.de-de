---
description: Ruft die Druckerfunktionen ab, die in Übereinstimmung mit dem XML-Druckschema formatiert sind.
ms.assetid: 15219c19-b64c-4c51-9357-15a797557693
title: GetPrintCapabilitiesThunk2-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintCapabilitiesThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: 55127d15eae41380fd5376ca54589488e255a740a7881042f54bc203873701f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971389"
---
# <a name="getprintcapabilitiesthunk2-function"></a>GetPrintCapabilitiesThunk2-Funktion

\[Diese Funktion wird nicht unterstützt und kann in zukünftigen Versionen des -Windows. [**PTGetPrintCapabilities bietet**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) die gleiche Funktionalität und sollte stattdessen verwendet werden.\]

Ruft die Funktionen des Druckers ab, die in Übereinstimmung mit dem XML-Druckschema [formatiert sind.](./printschema.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPrintCapabilitiesThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      INT         cbPrintTicket,
  _Out_     BYTE        **ppbPrintCapabilities,
  _Out_     INT         *pcbPrintCapabilitiesLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hProvider* \[ In\]
</dt> <dd>

Ein Handle für einen geöffneten Druckticketanbieter. Dieses Handle wird von der [**BindPTProviderThunk-Funktion**](bindptproviderthunk.md) zurückgegeben.

</dd> <dt>

*pPrintTicket* \[ In\]
</dt> <dd>

Der Puffer, der die Druckticketdaten enthält, ausgedrückt in XML, wie im [Druckschema beschrieben.](./printschema.md)

</dd> <dt>

*cbPrintTicket* \[ In\]
</dt> <dd>

Die Größe des Puffers in Bytes, auf den *pPrintTicket verweist.*

</dd> <dt>

*ppbPrintCapabilities* \[ out\]
</dt> <dd>

Die Adresse des Puffers, der von dieser Funktion zugeordnet wird und die gültigen Informationen zu Druckfunktionen enthält, die als XML codiert sind. Diese Funktion ruft [**CoTaskMemAlloc auf,**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) um diesen Puffer zu reservieren. Wenn der Puffer nicht mehr benötigt wird, muss er vom Aufrufer durch Aufrufen von [**CoTaskMemFree frei werden.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)

</dd> <dt>

*zeichenPrintCapabilitiesLength* \[ out\]
</dt> <dd>

Die Größe des Puffers in Bytes, auf den *ppbPrintCapabilities verweist.*

</dd> <dt>

*pbstrErrorMessage* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die angibt, was bei *pPrintTicket* ungültig ist. Wenn er gültig ist, ist dieser Wert **NULL.** Wenn *pbstrErrorMessage bei Rückgabe* der Funktion nicht **NULL** ist, muss der Aufrufer die Zeichenfolge mit [**SysFreeString freigibt.**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben. Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung.](../com/error-handling-in-com.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)
</dt> <dt>

[Druckschema](./printschema.md)
</dt> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

