---
description: Ruft die Unformatierung der Anwendungsprotokoll-Dateneinheit (APDU) ab.
ms.assetid: d8b326db-de54-4ef8-becb-fd905414c45c
title: ISCardCmd::get_Apdu-Methode (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 773185563db798877d38d3fb877fe1b4459468e4eeb4d45aed922203bd813418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015090"
---
# <a name="iscardcmdget_apdu-method"></a>ISCardCmd::get \_ Apdu-Methode

\[Die **\_ Get-Apdu-Methode** steht für die Verwendung in den betriebssystemen zur Verfügung, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **\_ Get-Apdu-Methode** ruft die Unformatierung der [*Anwendungsprotokoll-Dateneinheit*](../secgloss/a-gly.md) (APDU) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Apdu(
  [out] LPBYTEBUFFER *ppApdu
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppApdu* \[ out\]
</dt> <dd>

Zeiger auf den Bytepuffer, der über ein **IStream-Objekt** zugeordnet ist, das die APDU-Nachricht bei der Rückgabe enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *ppApdu-Parameter* ist ungültig.<br/>  |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in *ppApdu übergeben.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                        |



 

## <a name="remarks"></a>Hinweise

Rufen Sie put Apdu auf, um die APDU aus einem [**IByteBuffer**](ibytebuffer.md) -Objekt (**IStream**) in das APDU zu kopieren, das in diesem Schnittstellenobjekt [**\_ umschlossen ist.**](iscardcmd-put-apdu.md)

Rufen Sie get [**\_ ApduLength**](iscardcmd-get-apdulength.md)auf, um die Länge des APDU zu bestimmen.

Eine Liste aller methoden, die von der [**ISCardCmd-Schnittstelle**](iscardcmd.md) bereitgestellt werden, finden Sie unter [**ISCardCmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes [](../secgloss/s-gly.md) gibt diese Schnittstelle möglicherweise einen Smartcard-Fehlercode zurück, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung zu erfüllen. Informationen zu Smartcard-Fehlercodes finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Sie die Unformatierung der [*Anwendungsprotokoll-Dateneinheit*](../secgloss/a-gly.md) (APDU) abrufen. Im Beispiel wird davon ausgegangen, dass pISCardCmd ein gültiger Zeiger auf die [**ISCardCmd-Schnittstelle**](iscardcmd.md) und pIByteApdu ein gültiger Zeiger auf eine Instanz der [**IByteBuffer-Schnittstelle**](ibytebuffer.md) ist.


```C++
HRESULT    hr;

hr = pISCardCmd->get_Apdu(&pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed get_Apdu.\n");
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

[**get \_ ApduLength**](iscardcmd-get-apdulength.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ Apdu**](iscardcmd-put-apdu.md)
</dt> </dl>

 

 
