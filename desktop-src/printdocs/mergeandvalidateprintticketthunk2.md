---
description: Führt zwei Druck Tickets zusammen und gibt ein gültiges, brauchbares Druck Ticket zurück.
ms.assetid: 4aa7b9de-abf2-4781-942e-0b992a6bffed
title: MergeAndValidatePrintTicketThunk2-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeAndValidatePrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: 4a21b9e505e39d64e8e0c696a3b8a6432a012d76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369047"
---
# <a name="mergeandvalidateprintticketthunk2-function"></a>MergeAndValidatePrintTicketThunk2-Funktion

\[Diese Funktion wird nicht unterstützt und wird in zukünftigen Versionen von Windows möglicherweise deaktiviert oder gelöscht. [**Ptmergeandvalidateprintticket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) bietet entsprechende Funktionen und sollte stattdessen verwendet werden.\]

Führt zwei Druck Tickets zusammen und gibt ein gültiges, brauchbares Druck Ticket zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT MergeAndValidatePrintTicketThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pBasePrintTicket,
  _In_      INT         basePrintTicketLength,
  _In_opt_  BYTE        *pDeltaPrintTicket,
  _In_      INT         deltaPrintTicketLength,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppValidatedPrintTicket,
  _Out_     INT         *pValidatedPrintTicketLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprovider* \[ in\]
</dt> <dd>

Ein Handle für einen geöffneten Druck ticketanbieter. Dieses Handle wird von der [**bindptproviderthunk**](bindptproviderthunk.md) -Funktion zurückgegeben.

</dd> <dt>

*pbaseprintticket* \[ in\]
</dt> <dd>

Der Puffer, der die grundlegenden Druck Ticketdaten enthält, wie im [Druck Schema](./printschema.md)beschrieben, in XML ausgedrückt.

</dd> <dt>

*baseprintticketlength* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des Puffers, auf den *pbaseprintticket* verweist.

</dd> <dt>

*pdelta-PrintTicket* \[ in, optional\]
</dt> <dd>

Der Puffer, der das zu Merge Ende Druck Ticket enthält. Die Druck Ticketdaten werden in XML ausgedrückt, wie im [Print-Schema](./printschema.md)beschrieben. Der Wert dieses Parameters kann **null** sein.

</dd> <dt>

*Delta printticketlength* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des Puffers, auf den *pdelta-PrintTicket* verweist.

</dd> <dt>

*Bereich* \[ in\]
</dt> <dd>

Der-Wert, der angibt, ob der Bereich von *pdelta-PrintTicket* und *ppvalidatedprintticket* eine einzelne Seite, ein gesamtes Dokument oder alle Dokumente im Druckauftrag ist. Der Wert dieses Parameters muss ein Member der [**eprintticketscope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) -Enumeration sein, die als **DWORD** umgewandelt wird.

</dd> <dt>

*ppvalidatedprintticket* \[ vorgenommen\]
</dt> <dd>

Die Adresse des Puffers, der das zusammengeführte und validierte Druck Ticket enthält. Diese Funktion Ruft die [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) -Funktion auf, um diesen Puffer zuzuordnen. Wenn der Puffer nicht mehr benötigt wird, muss der Aufrufer ihn durch Aufrufen von [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)freigeben.

</dd> <dt>

*pvalidatedprintticketlength* \[ vorgenommen\]
</dt> <dd>

Die Größe des von *ppvalidatedprintticket* referenzierten Puffers in Bytes.

</dd> <dt>

*pbstrauerrormessage* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die angibt, was, wenn überhaupt, für das Druck Ticket in *pbaseprintticket* oder *pdelta Info Ticket* ungültig ist. Wenn beide gültig sind, ist dieser Wert **null**. Wenn *pbstrauerrormessage* bei Rückgabe der Funktion nicht **null** ist, muss der Aufrufer die Zeichenfolge mit [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)freigeben.

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

[**Ptmergeandvalidateprintticket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)
</dt> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

