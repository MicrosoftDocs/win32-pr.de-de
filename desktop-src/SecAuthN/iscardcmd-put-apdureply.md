---
description: Legt eine neue Antwort-APDU fest.
ms.assetid: 1d058c89-0de9-4809-b008-ae24c62acc5b
title: Iscardcmd::p ut_ApduReply-Methode (scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0292f3ebd4e5f18638ad496cdf15cd9f5c4320f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862635"
---
# <a name="iscardcmdput_apdureply-method"></a>Iscardcmd::p UT- \_ apdureply-Methode

\[Die **Put \_ apdureply** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Mit der **Put \_ apdureply** -Methode wird eine neue [*Antwort-APDU*](../secgloss/r-gly.md)festgelegt.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ApduReply(
  [in] LPBYTEBUFFER pReplyApdu
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*preplyapdu* \[ in\]
</dt> <dd>

Ein Zeiger auf den Byte Puffer (durch ein **IStream** -Objekt zugeordnet), der bei der Rückgabe die APDU-Wiedergabe Meldung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>         |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *preplyapdu* -Parameter ist ungültig.<br/>  |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in *preplyapdu* übermittelt.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                            |



 

## <a name="remarks"></a>Bemerkungen

Um ein vorhandenes Antwort-APDU abzurufen, nennen [**Sie get \_ apdureply**](iscardcmd-get-apdureply.md).

Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie ein neues [*Antwort-APDU*](../secgloss/r-gly.md)festgelegt wird. In diesem Beispiel wird davon ausgegangen, dass pibytereply ein gültiger Zeiger auf eine Instanz von [**ibytebuffer**](ibytebuffer.md)ist und dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.


```C++
HRESULT    hr;

// Set the reply data.
hr = pISCardCmd->put_ApduReply(pIByteReply);
if (FAILED(hr)) 
{
    printf("Failed put_ApduReply.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scarddat. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_apdureply erhalten**](iscardcmd-get-apdureply.md)
</dt> <dt>

[**\_apdureplylength erhalten**](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[**Iscardcmd**](iscardcmd.md)
</dt> </dl>

 

 
