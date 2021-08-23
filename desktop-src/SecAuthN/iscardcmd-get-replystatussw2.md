---
description: Ruft das Antwort-APDU SW2-Status byte ab.
ms.assetid: 24ad0164-84fc-4a99-b9dd-0f7d789dff92
title: ISCardCmd::get_ReplyStatusSW2-Methode (Ddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatusSW2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 60004c56d9d6dec8aa7b5afc9c77e3c5af813020db387172b06a0c802bd9fd8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481540"
---
# <a name="iscardcmdget_replystatussw2-method"></a>ISCardCmd::get \_ ReplyStatusSW2-Methode

\[Die **\_ methode get ReplyStatusSW2** steht für die Verwendung in den Betriebssystemen zur Verfügung, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **\_ get ReplyStatusSW2-Methode** ruft das [*Antwort-APDU*](../secgloss/r-gly.md) SW2-Status-Byte ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ReplyStatusSW2(
  [out] LPBYTE pbySW2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbySW2* \[ out\]
</dt> <dd>

Zeiger auf das Byte, das bei der Rückgabe den Wert des SW2-Byte enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *PbySW2* ist ungültig.<br/>            |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Ein ungültiger Zeiger wurde in *pbySW2* übergeben.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                        |



 

## <a name="remarks"></a>Hinweise

Das SW2-Status-Byte des Antwort-APDU ist schreibgeschützt.

Rufen Sie [**get \_ ReplyStatusSW1**](iscardcmd-get-replystatussw1.md)auf, um das Sw1-Status byte der Antwort-APDU abzurufen.

Eine Liste aller von dieser Schnittstelle bereitgestellten Methoden finden Sie unter [**ISCardCmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Schnittstelle einen [*Smartcardfehlercode*](../secgloss/s-gly.md) zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie das SW2-Status-Byte der [*Antwort-APDU*](../secgloss/r-gly.md)abgerufen wird. Im Beispiel wird davon ausgegangen, dass pISCardCmd ein gültiger Zeiger auf eine Instanz der [**ISCardCmd-Schnittstelle**](iscardcmd.md) ist.


```C++
BYTE     bySW2;
HRESULT  hr;

// Retrieve the reply status SW2 byte.
hr = pISCardCmd->get_ReplyStatusSW2(&bySW2);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatusSW2\n");
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

[**get \_ ReplyStatusSW1**](iscardcmd-get-replystatussw1.md)
</dt> <dt>

[**get \_ ReplyStatus**](iscardcmd-get-replystatus.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
