---
description: Ruft die Druckerfunktionen ab, die in Übereinstimmung mit dem XML-Druck Schema formatiert sind.
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
ms.openlocfilehash: eb60f1cdabad6287e236fc099fc304e9e7de83ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368793"
---
# <a name="getprintcapabilitiesthunk2-function"></a>GetPrintCapabilitiesThunk2-Funktion

\[Diese Funktion wird nicht unterstützt und wird in zukünftigen Versionen von Windows möglicherweise deaktiviert oder gelöscht. [**Ptgetprintworks**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) bietet entsprechende Funktionen und sollte stattdessen verwendet werden.\]

Ruft die Funktionen des Druckers ab, die in Übereinstimmung mit dem XML- [Druck Schema](./printschema.md)formatiert sind.

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

*hprovider* \[ in\]
</dt> <dd>

Ein Handle für einen geöffneten Druck ticketanbieter. Dieses Handle wird von der [**bindptproviderthunk**](bindptproviderthunk.md) -Funktion zurückgegeben.

</dd> <dt>

*pprintticket* \[ in\]
</dt> <dd>

Der Puffer, der die Druck Ticketdaten enthält, wie im [Druck Schema](./printschema.md)beschrieben, in XML ausgedrückt.

</dd> <dt>

*cbprintticket* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des Puffers, auf den *pprintticket* verweist.

</dd> <dt>

*ppbprint-Funktionen* \[ vorgenommen\]
</dt> <dd>

Die Adresse des Puffers, der von dieser Funktion zugeordnet wird, und enthält die gültigen Druck Funktions Informationen, die als XML codiert sind. Diese Funktion Ruft die [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) -Funktion auf, um diesen Puffer zuzuordnen. Wenn der Puffer nicht mehr benötigt wird, muss der Aufrufer ihn durch Aufrufen von [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)freigeben.

</dd> <dt>

*pcbprintcapabilitieslength* \[ vorgenommen\]
</dt> <dd>

Die Größe (in Bytes) des Puffers, auf den *ppbprint-Funktionen* verweist.

</dd> <dt>

*pbstrauerrormessage* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die angibt, was, wenn nichts, für *pprintticket* ungültig ist. Wenn Sie gültig ist, ist dieser Wert **null**. Wenn *pbstrauerrormessage* bei Rückgabe der Funktion nicht **null** ist, muss der Aufrufer die Zeichenfolge mit [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)freigeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück; andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben. Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ptgetprint-Funktionen**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)
</dt> <dt>

[Druck Schema](./printschema.md)
</dt> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

