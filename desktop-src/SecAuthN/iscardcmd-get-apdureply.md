---
description: Ruft die Antwort-APDU ab und platziert Sie in einem bestimmten Byte Puffer.
ms.assetid: ab349e7a-350f-4e72-98b4-4c6431b6e380
title: 'Iscardcmd:: get_ApduReply-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2ce11ec2d3d8202574ab23074531c393c9fecb98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050564"
---
# <a name="iscardcmdget_apdureply-method"></a>Iscardcmd:: get \_ apdureply-Methode

\[Die Methode " **get \_ apdureply** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **get \_ apdureply** -Methode ruft die [*Antwort-APDU*](../secgloss/r-gly.md)ab und platziert Sie in einem bestimmten Byte Puffer. Die Antwort kann **null** sein, wenn keine [*Transaktion*](../secgloss/t-gly.md) für den Befehl APDU ausgeführt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ApduReply(
  [out] LPBYTEBUFFER *ppReplyApdu
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppreplyapdu* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den Byte Puffer (durch ein **IStream** -Objekt zugeordnet), der die APDU-Antwortnachricht bei Rückgabe enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>          |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *ppreplyapdu* -Parameter ist ungültig.<br/>  |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in " *ppreplyapdu*" übergeben.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                             |



 

## <a name="remarks"></a>Bemerkungen

Um die Länge der APDU-Antwort zu ermitteln, wenden [**Sie sich an get \_ apdureplylength**](iscardcmd-get-apdureplylength.md).

Um einen neuen Antwort-APDU festzulegen, wenden Sie [**Put \_ apdureply**](iscardcmd-put-apdureply.md)an.

Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie Antwortdaten abgerufen werden. Im Beispiel wird davon ausgegangen, dass lLe eine Variable vom Typ **Long** ist, deren Wert durch einen vorherigen Aufrufen der [**iscardcmd:: get \_ apdureplylength**](iscardcmd-get-apdureplylength.md) -Methode festgelegt wurde, dass pibytereply ein gültiger Zeiger auf eine Instanz der [**ibytebuffer**](ibytebuffer.md) -Schnittstelle ist und dass der Wert von piscardcmd ein gültiger Zeiger auf eine Instanz der [**iscardc**](iscardcmd.md)


```C++
HRESULT      hr;

if (lLe > 0)
{
    // Get reply data if available.
    hr = pISCardCmd->get_ApduReply(&pIByteReply);
    if (FAILED(hr)) 
    {
        printf("Failed ISCardCmd::get_ApduReply.\n");
        // Take other error handling action as needed.
    }
    else
    {
        BYTE byReplyBytes[256];
        LONG lBytesRead;

        hr = pIByteReply->Read(byReplyBytes, lLe, &lBytesRead);
        if (FAILED(hr))
        {
            printf("Failed IByteBuffer::Read.\n");
            // Take other error handling action as needed.
        }
        // Use the bytes in byReplyBytes as needed.
    }
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

[**\_apdureplylength erhalten**](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[**Iscardcmd**](iscardcmd.md)
</dt> <dt>

[**\_apdureply einfügen**](iscardcmd-put-apdureply.md)
</dt> </dl>

 

 
