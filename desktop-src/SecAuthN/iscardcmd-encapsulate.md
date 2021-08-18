---
description: Die Encapsulate-Methode kapselt den angegebenen Befehl Application Protocol Data Unit (APDU) in eine andere Befehls-APDU für die Übertragung an eine Smartcard.
ms.assetid: dfffad09-046b-46cb-b6fd-286a4bbf1066
title: ISCardCmd::Encapsulate-Methode (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.Encapsulate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f531d0d5f55bea1fe63875a9feb508eb8b4c0e830705bfad2603cc52664c6f44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015120"
---
# <a name="iscardcmdencapsulate-method"></a>ISCardCmd::Encapsulate-Methode

\[Die **Encapsulate-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **Encapsulate-Methode** kapselt den angegebenen Befehl [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) in einen anderen Befehls-APDU für die Übertragung an eine [*Smartcard.*](../secgloss/s-gly.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT Encapsulate(
  [in] LPBYTEBUFFER  pApdu,
  [in] ISO_APDU_TYPE ApduType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pApdu* \[ In\]
</dt> <dd>

Zeiger auf das APDU, das gekapselt werden soll.

</dd> <dt>

*ApduType* \[ In\]
</dt> <dd>

ISO 7816-4-Case für [*T=0-Übertragungen.*](../secgloss/t-gly.md)

<dl><span id="ISO_CASE_1"></span><span id="iso_case_1"></span><dt>

**ISO \_ CASE \_ 1**
</dt><span id="ISO_CASE_2"></span><span id="iso_case_2"></span><dt>

**ISO \_ CASE \_ 2**
</dt><span id="ISO_CASE_3"></span><span id="iso_case_3"></span><dt>

**ISO \_ CASE \_ 3**
</dt><span id="ISO_CASE_4"></span><span id="iso_case_4"></span><dt>

**ISO \_ CASE \_ 4**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ungültiger Parameter.<br/>                   |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in *pApdu übergeben.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                       |



 

## <a name="remarks"></a>Hinweise

Rufen Sie [**BuildCmd**](iscardcmd-buildcmd.md)auf, um eine Befehls-APDU zu erstellen.

Eine Liste aller von dieser Schnittstelle bereitgestellten Methoden finden Sie unter [**ISCardCmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes gibt diese Schnittstelle möglicherweise einen Smartcard-Fehlercode zurück, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung zu erfüllen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie eine Befehls-APDU gekapselt wird. Im Beispiel wird davon ausgegangen, dass pIByteApdu ein gültiger Zeiger auf eine Instanz der [**IByteBuffer-Schnittstelle**](ibytebuffer.md) ist.


```C++
HRESULT    hr;

// pIByteApdu is a pointer to an instance of IByteBuffer.
// Encapsulate the APDU.
hr = pISCardCmd->Encapsulate(pIByteApdu, ISO_CASE_1);
if (FAILED(hr)) 
{
    printf("Failed Encapsulate.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.<br/>            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**BuildCmd**](iscardcmd-buildcmd.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
