---
description: Ruft die Knotenadresse ab, die von der Smartcard in der Antwortnachricht verwendet wird.
ms.assetid: bf4f281c-d378-4abd-8f2e-e23c2f4e87a4
title: ISCardCmd::get_ReplyNad-Methode (Ddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyNad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 22460acc80aae359b3d31a7e4bf592514dd5c559feb68117d7547a0cdbedf144
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577540"
---
# <a name="iscardcmdget_replynad-method"></a>ISCardCmd::get \_ ReplyNad-Methode

\[Die **\_ methode get ReplyNad** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **\_ get ReplyNad-Methode** ruft die Knotenadresse (Soll) ab, die von der [*Smartcard*](../secgloss/s-gly.md) in der Antwortnachricht verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ReplyNad(
  [out] BYTE *pbNad
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbNad* \[ out\]
</dt> <dd>

Zeiger auf das Byte, das bei der Rückgabe den von der Antwortnachricht verwendeten Erneuten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                    | Beschreibung                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang wurde erfolgreich abgeschlossen.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | Der *pbNad-Parameter* ist ungültig.<br/>                     |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Interne Aufrufe konnten keine Informationen abrufen.<br/> |



 

## <a name="remarks"></a>Hinweise

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Methode einen Smartcardfehlercode zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie sie die Knotenadresse (Knotenadresse) abruft, die von der [*Smartcard*](../secgloss/s-gly.md) in der Antwortnachricht verwendet wird. Im Beispiel wird davon ausgegangen, dass pISCardCmd ein gültiger Zeiger auf eine Instanz der [**ISCardCmd-Schnittstelle**](iscardcmd.md) ist.


```C++
BYTE    byNad;
HRESULT hr;

// Get reply Nad.
hr = pISCardCmd->get_ReplyNad(&byNad);
if (FAILED(hr))
{
  printf("Failed get_ReplyNad\n");
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
