---
description: Ruft eine ATR-Zeichenfolge der Smartcard ab.
ms.assetid: 2021bd0c-6ef8-4679-be6c-9a9fd33d9fd6
title: 'Iscard:: get_Atr-Methode (scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Atr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4f2a5688ee85318003ea366bbce614e8250a131a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373271"
---
# <a name="iscardget_atr-method"></a>Iscard:: get- \_ ATR-Methode

\[Die **get \_ ATR** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **get \_ ATR** -Methode ruft eine [*ATR-Zeichenfolge*](../secgloss/a-gly.md) der [*Smartcard*](../secgloss/s-gly.md)ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Atr(
  [out] LPBYTEBUFFER *ppAtr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppatr* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen Byte Puffer in der Form eines [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) , der die ATR-Zeichenfolge bei der Rückgabe enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>             |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *ppatr* -Parameter ist ungültig.<br/>           |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in *ppatr* übermittelt.<br/>          |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Der Arbeitsspeicher zum erfüllen der Anforderung ist nicht verfügbar.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Sie die ATR-Zeichenfolge von der Smartcard abrufen.


```C++
// Retrieve the ATR.
// pISCard is a pointer to a previously instantiated ISCard.
// pAtr is a pointer to a previously instantiated IByteBuffer.
hr = pISCard->get_Atr(&pAtr);
if (FAILED(hr))
{
    printf("Failed get_Atr\n");
    // Take other error handling action.
}
// Success, you can now use IByteBuffer::Read to access ATR bytes.
BYTE  byAtr[32];
   long  lBytesRead, i;
   // Read the ATR string into a byte array.
   hr = pAtr->Read(byAtr, 32, &lBytesRead);
   // Use the ATR value. (This example merely displays the bytes.)
   for ( i = 0; i < lBytesRead; i++)
       printf("%c", *(byAtr + i));
   printf("\n");
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

[**\_cardhandle erhalten**](iscard-get-cardhandle.md)
</dt> <dt>

[**\_Kontext erhalten**](iscard-get-context.md)
</dt> <dt>

[**get- \_ Protokoll**](iscard-get-protocol.md)
</dt> <dt>

[**\_Status erhalten**](iscard-get-status.md)
</dt> <dt>

[**Iscard**](iscard.md)
</dt> <dt>

[**Ibytebuffer:: Read**](ibytebuffer-read.md)
</dt> </dl>

 

 
