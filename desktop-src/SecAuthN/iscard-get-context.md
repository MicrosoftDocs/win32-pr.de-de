---
description: Ruft das aktuelle Resource Manager-Kontexthandle ab. Diese Methode gibt ( \* pContext) == NULL zurück, wenn kein Kontext eingerichtet wurde.
ms.assetid: c031f53d-4670-4d48-934c-a1550f21c23a
title: ISCard::get_Context-Methode (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Context
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 82094d51912031655585cacde0b156451107276bc08ca1be6dc6d82bdbb3229d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015630"
---
# <a name="iscardget_context-method"></a>ISCard::get \_ Context-Methode

\[Die **get \_ Context-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **get \_ Context-Methode** ruft das aktuelle [*Resource Manager-Kontexthandle*](../secgloss/r-gly.md) ab. Diese Methode gibt ( \* *pContext*) == **NULL** zurück, wenn kein Kontext eingerichtet wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Context(
  [out] HSCARDCONTEXT *pContext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pContext* \[ out\]
</dt> <dd>

Zeiger auf das Kontexthandle bei rückgabe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operation erfolgreich abgeschlossen.<br/>       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der *pContext-Parameter* ist ungültig.<br/>  |
| <dl> <dt>**E \_ POINTER**</dt> </dl>    | Ein ungültiger Zeiger wurde in *pContext* übergeben.<br/> |



 

## <a name="remarks"></a>Hinweise

Der Ressourcen-Manager-Kontext wird durch Aufrufen der [*Smartcardfunktion*](../secgloss/s-gly.md) [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext)festgelegt.

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Schnittstelle einen Smartcardfehlercode zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das Abrufen des aktuellen [*Resource Manager-Kontexthandle.*](../secgloss/r-gly.md)


```C++
HSCARDCONTEXT  hCtx;
HRESULT        hr;

// Retrieve the smart card context.
hr = pISCard->get_Context(&hCtx);
if (FAILED(hr))
{
   printf("Failed get_Context\n");
   // Take other error handling action as needed.
}
// Use smart card context as needed.
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCard ist als 1461AAC3-6810-11D0-918F-00AA00C18068 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**get \_ Atr**](iscard-get-atr.md)
</dt> <dt>

[**get \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**get \_ Protocol**](iscard-get-protocol.md)
</dt> <dt>

[**\_Get Status**](iscard-get-status.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> <dt>

[**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext)
</dt> </dl>

 

 
