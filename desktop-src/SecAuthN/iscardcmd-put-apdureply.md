---
description: Legt eine neue Antwort-APDU fest.
ms.assetid: 1d058c89-0de9-4809-b008-ae24c62acc5b
title: ISCardCmd::p ut_ApduReply-Methode (Discountddat.h)
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
ms.openlocfilehash: 749c0aee678a036160b52db635f2f096c68e0d20b2295c05387c5b57bbe2befc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481460"
---
# <a name="iscardcmdput_apdureply-method"></a>ISCardCmd::p ut-Methode \_ "ApduReply"

\[Die **\_ put-Methode ApduReply** steht für die Verwendung in den Betriebssystemen zur Verfügung, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **\_ put-Methode ApduReply** legt eine neue [*Antwort-APDU*](../secgloss/r-gly.md)fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ApduReply(
  [in] LPBYTEBUFFER pReplyApdu
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pReplyApdu* \[ In\]
</dt> <dd>

Zeiger auf den Bytepuffer (durch ein **IStream-Objekt** zugeordnet), der die APDU-Wiedergabenachricht bei der Rückgabe enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *pReplyApdu-Parameter* ist ungültig.<br/>  |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Ein ungültiger Zeiger wurde in *pReplyApdu* übergeben.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                            |



 

## <a name="remarks"></a>Hinweise

Rufen Sie [**get \_ ApduReply**](iscardcmd-get-apdureply.md)auf, um ein vorhandenes Antwort-APDU abzurufen.

Eine Liste aller von dieser Schnittstelle bereitgestellten Methoden finden Sie unter [**ISCardCmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Schnittstelle einen Smartcardfehlercode zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie sie eine neue [*Antwort-APDU*](../secgloss/r-gly.md)festlegen. Im Beispiel wird davon ausgegangen, dass pIByteReply ein gültiger Zeiger auf eine Instanz von [**IByteBuffer**](ibytebuffer.md)und pISCardCmd ein gültiger Zeiger auf eine Instanz der [**ISCardCmd-Schnittstelle**](iscardcmd.md) ist.


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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ddat.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Ddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.<br/>            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**get \_ ApduReply**](iscardcmd-get-apdureply.md)
</dt> <dt>

[**get \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
