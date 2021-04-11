---
description: Ruft die Rohdaten-app (Application Protocol Data Unit, APDU) ab.
ms.assetid: d8b326db-de54-4ef8-becb-fd905414c45c
title: 'Iscardcmd:: get_Apdu-Methode (scarddat. h)'
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
ms.openlocfilehash: fb943d7ade48f6684cdc10cb4b1ad7e48f87e65c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041750"
---
# <a name="iscardcmdget_apdu-method"></a>Iscardcmd:: get \_ APDU-Methode

\[Die **get \_ APDU** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **get \_ APDU** -Methode ruft die RAW-APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Apdu(
  [out] LPBYTEBUFFER *ppApdu
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppapdu* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den Byte Puffer, der über ein **IStream** -Objekt zugeordnet ist, das die APDU-Nachricht bei der Rückgabe enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>     |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *ppapdu* -Parameter ist ungültig.<br/>  |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in *ppapdu* übermittelt.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                        |



 

## <a name="remarks"></a>Bemerkungen

Um das APDU aus einem [**ibytebuffer**](ibytebuffer.md) (**IStream**)-Objekt in das APDU zu kopieren, das in diesem Schnittstellen Objekt enthalten ist, wenden Sie [**Put \_ APDU**](iscardcmd-put-apdu.md)an.

Um die Länge des APDU zu ermitteln, wenden [**Sie get \_ apdulength**](iscardcmd-get-apdulength.md)an.

Eine Liste aller Methoden, die von der [**iscardcmd**](iscardcmd.md) -Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Informationen zu smartcardfehlercodes finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie die RAW [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) abgerufen wird. Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf die [**iscardcmd**](iscardcmd.md) -Schnittstelle ist, und dass "pibyteapdu" ein gültiger Zeiger auf eine Instanz der [**ibytebuffer**](ibytebuffer.md) -Schnittstelle ist.


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

[**\_apdulength erhalten**](iscardcmd-get-apdulength.md)
</dt> <dt>

[**Iscardcmd**](iscardcmd.md)
</dt> <dt>

[**\_APDU platzieren**](iscardcmd-put-apdu.md)
</dt> </dl>

 

 
