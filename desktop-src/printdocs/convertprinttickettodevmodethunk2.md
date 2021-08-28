---
description: Konvertiert ein Druckticket in eine DEVMODE-Struktur.
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
ms.openlocfilehash: e6325ca61d18d571a3a3b346b18f6191b53e43d2ce96799c34a643477123f20c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112680"
---
# <a name="convertprinttickettodevmodethunk2-function"></a>ConvertPrintTicketToDevModeThunk2-Funktion

\[Diese Funktion wird nicht unterstützt und kann in zukünftigen Versionen von Windows deaktiviert oder gelöscht werden. [**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) bietet entsprechende Funktionen und sollte stattdessen verwendet werden.\]

Konvertiert ein Druckticket in eine [**DEVMODE-Struktur.**](/windows/win32/api/wingdi/ns-wingdi-devmodea)

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

*hProvider* \[ In\]
</dt> <dd>

Ein Handle für einen offenen Druckticketanbieter. Dieses Handle wird von der [**BindPTProviderThunk-Funktion**](bindptproviderthunk.md) zurückgegeben.

</dd> <dt>

*pPrintTicket* \[ In\]
</dt> <dd>

Der Puffer, der das zu konvertierende Druckticket enthält.

</dd> <dt>

*cbSize* \[ In\]
</dt> <dd>

Die Größe des in *pPrintTicket* übergebenen Puffers in Bytes.

</dd> <dt>

*baseType* \[ In\]
</dt> <dd>

Ein -Wert, der angibt, ob der [**DEVMODE-Standard**](/windows/win32/api/wingdi/ns-wingdi-devmodea) des Benutzers oder der **DEVMODE-Standard** für die Druckwarteschlange verwendet wird, um Werte für die **DevMODE-Ausgabe** bereitzustellen, wenn *pPrintTicket* nicht jede mögliche Einstellung für einen **DEVMODE** angibt. Der Wert dieses Parameters muss ein Member der [**EDefaultDevmodeType-Enumeration**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) sein, der als **INT-Typ** definiert wird.

</dd> <dt>

*Bereich* \[ In\]
</dt> <dd>

Ein -Wert, der den Bereich von *pPrintTicket* angibt. Dieser Wert kann eine einzelne Seite, ein gesamtes Dokument oder alle Dokumente im Druckauftrag angeben. Der Wert dieses Parameters muss ein Member der [**EPrintTicketScope-Enumeration**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) sein, der in **ein DWORD-Element** umformt wird.

</dd> <dt>

*ppDevmode* \[ out\]
</dt> <dd>

Die Adresse des neu erstellten [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea). Diese Funktion ruft [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) auf, um diesen Puffer zuzuordnen. Wenn der Puffer nicht mehr benötigt wird, muss der Aufrufer ihn durch Aufrufen von [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)freigeben.

</dd> <dt>

*pwDevModeLength* \[ out\]
</dt> <dd>

Die Größe des in *ppDevmode* zurückgegebenen [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) in Bytes.

</dd> <dt>

*errMsg* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die angibt, was , wenn überhaupt, für das Druckticket in *pPrintTicket* ungültig ist. Wenn sie gültig ist, ist dies **NULL.** Wenn *errMsg* nicht **NULL** ist, wenn die Funktion zurückgegeben wird, muss der Aufrufer die Zeichenfolge mit [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)freigeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben. Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung.](../com/error-handling-in-com.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Druckschema](./printschema.md)
</dt> <dt>

[**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)
</dt> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

