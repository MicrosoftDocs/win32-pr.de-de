---
description: Ruft das aktuelle Resource Manager-Kontext Handle ab. Diese Methode gibt ( \* pContext) = = NULL zurück, wenn kein Kontext festgelegt wurde.
ms.assetid: c031f53d-4670-4d48-934c-a1550f21c23a
title: 'Iscard:: get_Context-Methode (scardmgr. h)'
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
ms.openlocfilehash: 8b5aba075d755b644a78cca23a827a70966f4ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867851"
---
# <a name="iscardget_context-method"></a>Iscard:: get- \_ Kontext Methode

\[Die **\_ Kontext** Methode "Get" ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **get \_ context** -Methode ruft das aktuelle [*Resource Manager-Kontext*](../secgloss/r-gly.md) Handle ab. Diese Methode gibt ( \* *pContext*) = = **null** zurück, wenn kein Kontext festgelegt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Context(
  [out] HSCARDCONTEXT *pContext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pContext* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den Kontext Handle bei Rückgabe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operation erfolgreich abgeschlossen.<br/>       |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der *pContext* -Parameter ist ungültig.<br/>  |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>    | Ein fehlerhafter Zeiger wurde in *pContext* übergeben.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der Resource Manager-Kontext wird festgelegt, indem die [*smartcardfunktion*](../secgloss/s-gly.md) " [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext)" aufgerufen wird.

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie das aktuelle [*Resource Manager-Kontext*](../secgloss/r-gly.md) Handle abgerufen wird.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scardmgr. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscard ist definiert als 1461aac3-6810-11D0-918f -00aa00c18068<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_ATR erhalten**](iscard-get-atr.md)
</dt> <dt>

[**\_cardhandle erhalten**](iscard-get-cardhandle.md)
</dt> <dt>

[**get- \_ Protokoll**](iscard-get-protocol.md)
</dt> <dt>

[**\_Status erhalten**](iscard-get-status.md)
</dt> <dt>

[**Iscard**](iscard.md)
</dt> <dt>

[**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext)
</dt> </dl>

 

 
