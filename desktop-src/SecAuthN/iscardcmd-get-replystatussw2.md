---
description: Ruft das Antwort-APDU-SW2 Status Byte ab.
ms.assetid: 24ad0164-84fc-4a99-b9dd-0f7d789dff92
title: 'Iscardcmd:: get_ReplyStatusSW2-Methode (scarddat. h)'
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
ms.openlocfilehash: 7ff503758a50437b4b7ff974fe4455d4b92ce978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129332"
---
# <a name="iscardcmdget_replystatussw2-method"></a>Iscardcmd:: get \_ ReplyStatusSW2-Methode

\[Die Methode " **get \_ ReplyStatusSW2** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **get \_ ReplyStatusSW2** -Methode ruft die [*Antwort APDU*](../secgloss/r-gly.md) SW2 Status Byte ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ReplyStatusSW2(
  [out] LPBYTE pbySW2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbySW2* \[ vorgenommen\]
</dt> <dd>

Zeiger auf das Byte, das den Wert des SW2 Byte bei der Rückgabe enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>     |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *pbySW2* ist ungültig.<br/>            |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | In *pbySW2* wurde ein fehlerhafter Zeiger übermittelt.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                        |



 

## <a name="remarks"></a>Bemerkungen

Das SW2-Status Byte der Antwort APDU ist schreibgeschützt.

Rufen [**Sie get \_ ReplyStatusSW1**](iscardcmd-get-replystatussw1.md)auf, um das SW1-Status Byte der Antwort abzurufen.

Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie das SW2-Status Byte der [*Antwort-APDU*](../secgloss/r-gly.md)abgerufen wird. Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.


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

[**get \_ ReplyStatusSW1**](iscardcmd-get-replystatussw1.md)
</dt> <dt>

[**\_replystatus erhalten**](iscardcmd-get-replystatus.md)
</dt> <dt>

[**Iscardcmd**](iscardcmd.md)
</dt> </dl>

 

 
