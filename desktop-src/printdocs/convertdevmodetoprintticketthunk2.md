---
description: Konvertiert eine DEVMODE-Struktur in ein Druckticket.
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
ms.openlocfilehash: d5aea99e54a43eb35f76c719da885f8d7ae0352d47ecff62b7df38de30410025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950390"
---
# <a name="convertdevmodetoprintticketthunk2-function"></a>ConvertDevModeToPrintTicketThunk2-Funktion

\[Diese Funktion wird nicht unterstützt und kann in zukünftigen Versionen von Windows deaktiviert oder gelöscht werden. [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) bietet entsprechende Funktionen und sollte stattdessen verwendet werden.\]

Konvertiert eine [**DEVMODE-Struktur**](/windows/win32/api/wingdi/ns-wingdi-devmodea) in ein Druckticket.

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

*hProvider* \[ In\]
</dt> <dd>

Ein Handle für einen offenen Druckticketanbieter. Dieses Handle wird von der [**BindPTProviderThunk-Funktion**](bindptproviderthunk.md) zurückgegeben.

</dd> <dt>

*pDevmode* \[ In\]
</dt> <dd>

Ein Zeiger auf den zu konvertierende [**DEVMODE.**](/windows/win32/api/wingdi/ns-wingdi-devmodea)

</dd> <dt>

*cbSize* \[ In\]
</dt> <dd>

Die Größe des in *pDevmode* übergebenen [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) in Bytes.

</dd> <dt>

*Bereich* \[ In\]
</dt> <dd>

Ein -Wert, der den Bereich von *ppPrintTicket* angibt. Dieser Wert kann eine einzelne Seite, ein gesamtes Dokument oder alle Dokumente im Druckauftrag angeben. Der Wert dieses Parameters muss ein Member der [**EPrintTicketScope-Enumeration**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) sein, der in **ein DWORD-Element** umformt wird.

</dd> <dt>

*ppPrintTicket* \[ out\]
</dt> <dd>

Die Adresse des Puffers, der ein Druckticket enthält, das den in *pDevmode* übergebenen [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) darstellt. Diese Funktion ruft [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) auf, um diesen Puffer zuzuordnen. Wenn der Puffer nicht mehr benötigt wird, muss der Aufrufer ihn durch Aufrufen von [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)freigeben.

</dd> <dt>

*printTicketLength* \[ out\]
</dt> <dd>

Die Größe des in *ppPrintTicket* zurückgegebenen Drucktickets in Bytes.

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

[**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)
</dt> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

