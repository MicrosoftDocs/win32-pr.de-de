---
description: Kopiert die Anwendungsprotokoll-Dateneinheit (Application Protocol Data Unit, APDU) aus dem IByteBuffer-Objekt (IStream) in die APDU, die in diesem Schnittstellenobjekt umschlossen ist.
ms.assetid: 28dac222-ee7a-40aa-903b-e9c0b7757c9c
title: ISCardCmd::p ut_Apdu-Methode (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: feb9b5230564122ac3bed3c34271f0c608924babbbc2c263e10425931fb62337
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014613"
---
# <a name="iscardcmdput_apdu-method"></a>ISCardCmd::p ut-Apdu-Methode \_

\[Die **\_ put-Apdu-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **\_ put-Apdu-Methode** kopiert die Anwendungsprotokoll-Dateneinheit (Application [*Protocol Data Unit,*](../secgloss/a-gly.md) APDU) aus dem [**IByteBuffer**](ibytebuffer.md) -Objekt **(IStream)** in das APDU, das in diesem Schnittstellenobjekt umschlossen ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Apdu(
  [in] LPBYTEBUFFER pApdu
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pApdu* \[ In\]
</dt> <dd>

Zeiger auf die ISO 7816-4-APDU, die kopiert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *pApdu-Parameter* ist ungültig.<br/>  |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in *pApdu übergeben.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                       |



 

## <a name="remarks"></a>Hinweise

Rufen Sie get Apdu auf, um die unformatierte APDU aus dem Bytepuffer abzurufen, der über einen **IStream** zugeordnet ist, der die APDU-Nachricht [**\_ enthält.**](iscardcmd-get-apdu.md)

Eine Liste aller von dieser Schnittstelle bereitgestellten Methoden finden Sie unter [**ISCardCmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes [](../secgloss/s-gly.md) gibt diese Schnittstelle möglicherweise einen Smartcard-Fehlercode zurück, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung zu erfüllen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie sie eine APDU aus einem [**IByteBuffer**](ibytebuffer.md) -Objekt **(IStream)** in die APDU kopieren, die von einem Schnittstellenobjekt umschlossen ist. Im Beispiel wird davon ausgegangen, dass pIByteApdu ein gültiger Zeiger auf eine Instanz von **IByteBuffer** und pISCardCmd ein gültiger Zeiger auf eine Instanz der [**ISCardCmd-Schnittstelle**](iscardcmd.md) ist.


```C++
HRESULT    hr;


// Set the APDU.
hr = pISCardCmd->put_Apdu(pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed put_Apdu.\n");
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

[**Get \_ Apdu**](iscardcmd-get-apdu.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
