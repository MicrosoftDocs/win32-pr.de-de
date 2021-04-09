---
description: Konvertiert ein Druck Ticket in eine DEVMODE-Struktur.
ms.assetid: 3b0a6afd-fa9d-434e-a95f-b051296d4567
title: ConvertPrintTicketToDevModeThunk2-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertPrintTicketToDevModeThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: cf05ab6739dad09332ebc6746a05f3c40ef32de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042635"
---
# <a name="convertprinttickettodevmodethunk2-function"></a>ConvertPrintTicketToDevModeThunk2-Funktion

\[Diese Funktion wird nicht unterstützt und wird in zukünftigen Versionen von Windows möglicherweise deaktiviert oder gelöscht. [**Ptconvertprintticketdedevmode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) bietet gleichwertige Funktionen und sollte stattdessen verwendet werden.\]

Konvertiert ein Druck Ticket in eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur.

## <a name="syntax"></a>Syntax


```C++
HRESULT ConvertPrintTicketToDevModeThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      ULONG       cbSize,
  _In_      INT         baseType,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppDevmode,
  _Out_     ULONG       *pcbDevModeLength,
  _Out_opt_ BSTR        *errMsg
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

Der Puffer, der das zu konvertierende Druck Ticket enthält.

</dd> <dt>

*CBSIZE* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des Puffers, der in *pprintticket* übergeben wird.

</dd> <dt>

*BaseType* \[ in\]
</dt> <dd>

Ein Wert, der angibt, ob der standardmäßige [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) des Benutzers oder der standardmäßige **DEVMODE** der Druck Warteschlange verwendet wird, um Werte für den **DEVMODE** -Ausgabemodus bereitzustellen, wenn *pprintticket* nicht jede mögliche Einstellung für einen **DEVMODE**-Wert angibt. Der Wert dieses Parameters muss ein Member der [**edefaultdevmodetype**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) -Enumeration sein, der als **int** umgewandelt wird.

</dd> <dt>

*Bereich* \[ in\]
</dt> <dd>

Ein-Wert, der den Bereich von *pprintticket* angibt. Dieser Wert kann eine einzelne Seite, ein gesamtes Dokument oder alle Dokumente im Druckauftrag angeben. Der Wert dieses Parameters muss ein Member der [**eprintticketscope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) -Enumeration sein, die als **DWORD** umgewandelt wird.

</dd> <dt>

*ppdevmode* \[ vorgenommen\]
</dt> <dd>

Die Adresse des neu erstellten [**DEVMODE-Ausdrucks**](/windows/win32/api/wingdi/ns-wingdi-devmodea). Diese Funktion Ruft die [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) -Funktion auf, um diesen Puffer zuzuordnen. Wenn der Puffer nicht mehr benötigt wird, muss der Aufrufer ihn durch Aufrufen von [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)freigeben.

</dd> <dt>

*pcbdevmodelength* \[ vorgenommen\]
</dt> <dd>

Die Größe (in Bytes) des [**DEVMODE-Ausdrucks**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , der in *ppdevmode* zurückgegeben wurde.

</dd> <dt>

*errmsg* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die angibt, was, wenn überhaupt, für das Druck Ticket in *pprintticket* ungültig ist. Wenn Sie gültig ist, ist dies **null**. Wenn *errmsg* bei Rückgabe der Funktion nicht **null** ist, muss der Aufrufer die Zeichenfolge mit [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)freigeben.

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

[Druck Schema](./printschema.md)
</dt> <dt>

[**Ptconvertprintticketdedevmode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)
</dt> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

