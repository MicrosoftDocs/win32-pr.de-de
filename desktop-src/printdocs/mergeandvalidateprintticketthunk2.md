---
description: Führt zwei Drucktickets zusammen und gibt ein gültiges, funktionsfähiges Druckticket zurück.
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
ms.openlocfilehash: 156a242d9aa017cc67106a39db6d86809e0ac6f464566205ead09f69fe1b3b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471673"
---
# <a name="mergeandvalidateprintticketthunk2-function"></a>MergeAndValidatePrintTicketThunk2-Funktion

\[Diese Funktion wird nicht unterstützt und kann in zukünftigen Versionen von Windows deaktiviert oder gelöscht werden. [**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) bietet entsprechende Funktionen und sollte stattdessen verwendet werden.\]

Führt zwei Drucktickets zusammen und gibt ein gültiges, funktionsfähiges Druckticket zurück.

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

*hProvider* \[ In\]
</dt> <dd>

Ein Handle für einen offenen Druckticketanbieter. Dieses Handle wird von der [**BindPTProviderThunk-Funktion**](bindptproviderthunk.md) zurückgegeben.

</dd> <dt>

*pBasePrintTicket* \[ In\]
</dt> <dd>

Der Puffer, der die Basisdaten des Drucktickets enthält, ausgedrückt in XML, wie im [Druckschema](./printschema.md)beschrieben.

</dd> <dt>

*basePrintTicketLength* \[ In\]
</dt> <dd>

Die Größe des Puffers in Bytes, auf den *von pBasePrintTicket* verwiesen wird.

</dd> <dt>

*pDeltaPrintTicket* \[ in, optional\]
</dt> <dd>

Der Puffer, der das zusammenzuführende Druckticket enthält. Die Druckticketdaten werden in XML ausgedrückt, wie im [Druckschema](./printschema.md)beschrieben. Der Wert dieses Parameters kann **NULL** sein.

</dd> <dt>

*deltaPrintTicketLength* \[ In\]
</dt> <dd>

Die Größe des Puffers in Bytes, auf den *pDeltaPrintTicket* verweist.

</dd> <dt>

*Bereich* \[ In\]
</dt> <dd>

Der Wert, der angibt, ob der Bereich von *pDeltaPrintTicket* und *ppValidatedPrintTicket* eine einzelne Seite, ein gesamtes Dokument oder alle Dokumente im Druckauftrag ist. Der Wert dieses Parameters muss ein Member der [**EPrintTicketScope-Enumeration**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) sein, der in **ein DWORD-Element** umformt wird.

</dd> <dt>

*ppValidatedPrintTicket* \[ out\]
</dt> <dd>

Die Adresse des Puffers, der das zusammengeführte und überprüfte Druckticket enthält. Diese Funktion ruft [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) auf, um diesen Puffer zuzuordnen. Wenn der Puffer nicht mehr benötigt wird, muss der Aufrufer ihn durch Aufrufen von [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)freigeben.

</dd> <dt>

*pValidatedPrintTicketLength* \[ out\]
</dt> <dd>

Die Größe des Puffers in Bytes, auf den *ppValidatedPrintTicket* verweist.

</dd> <dt>

*pbstrErrorMessage* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die angibt, was für das Druckticket in *pBasePrintTicket* oder *pDeltaPrintTicket* ungültig ist. Wenn beide gültig sind, ist dieser Wert **NULL.** Wenn *pbstrErrorMessage* nicht **NULL** ist, wenn die Funktion zurückgegeben wird, muss der Aufrufer die Zeichenfolge mit [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)freigeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben. Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung.](../com/error-handling-in-com.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Druckschema](./printschema.md)
</dt> <dt>

[**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)
</dt> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

