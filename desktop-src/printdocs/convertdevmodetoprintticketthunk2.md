---
description: Konvertiert eine DEVMODE-Struktur in ein Druck Ticket.
ms.assetid: c03371f8-a978-4fb7-82cc-f76a65f3904c
title: ConvertDevModeToPrintTicketThunk2-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertDevModeToPrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: f13d597a11a4d6cfd1ad6f5d70b3a386560f5106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358872"
---
# <a name="convertdevmodetoprintticketthunk2-function"></a>ConvertDevModeToPrintTicketThunk2-Funktion

\[Diese Funktion wird nicht unterstützt und wird in zukünftigen Versionen von Windows möglicherweise deaktiviert oder gelöscht. [**Ptconvertdevmodetoprintticket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) bietet gleichwertige Funktionen und sollte stattdessen verwendet werden.\]

Konvertiert eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur in ein Druck Ticket.

## <a name="syntax"></a>Syntax


```C++
HRESULT ConvertDevModeToPrintTicketThunk2(
  _In_  HPTPROVIDER hProvider,
  _In_  BYTE        *pDevmode,
  _In_  ULONG       cbSize,
  _In_  DWORD       scope,
  _Out_ BYTE        **ppPrintTicket,
  _Out_ INT         *pcbPrintTicketLength
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprovider* \[ in\]
</dt> <dd>

Ein Handle für einen geöffneten Druck ticketanbieter. Dieses Handle wird von der [**bindptproviderthunk**](bindptproviderthunk.md) -Funktion zurückgegeben.

</dd> <dt>

*pdevmode* \[ in\]
</dt> <dd>

Ein Zeiger auf den zu konvertierenden [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Typ.

</dd> <dt>

*CBSIZE* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des [**DEVMODE-Ausdrucks**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , der im *pdevmode-Modus* übergeben wird.

</dd> <dt>

*Bereich* \[ in\]
</dt> <dd>

Ein-Wert, der den Bereich von *ppprintticket* angibt. Dieser Wert kann eine einzelne Seite, ein gesamtes Dokument oder alle Dokumente im Druckauftrag angeben. Der Wert dieses Parameters muss ein Member der [**eprintticketscope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) -Enumeration sein, die als **DWORD** umgewandelt wird.

</dd> <dt>

*ppprintticket* \[ vorgenommen\]
</dt> <dd>

Die Adresse des Puffers, der ein Druck Ticket enthält, das den im *pdevmode* weiter gegebenen [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Wert darstellt. Diese Funktion Ruft die [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) -Funktion auf, um diesen Puffer zuzuordnen. Wenn der Puffer nicht mehr benötigt wird, muss der Aufrufer ihn durch Aufrufen von [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)freigeben.

</dd> <dt>

*pcbprintticketlength* \[ vorgenommen\]
</dt> <dd>

Die Größe (in Bytes) des in *ppprintticket* zurückgegebenen Druck Tickets.

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

[**Ptconvertdevmodetoprintticket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)
</dt> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

