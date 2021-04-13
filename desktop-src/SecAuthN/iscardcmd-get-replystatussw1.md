---
description: Ruft das Antwort-APDUs SW1 Status Byte ab.
ms.assetid: 5f74d0c9-cf82-4694-bca6-a2655e717a1f
title: 'Iscardcmd:: get_ReplyStatusSW1-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatusSW1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92bcf490a3cb1fc533bcf9a1046642d3c3e55b59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526351"
---
# <a name="iscardcmdget_replystatussw1-method"></a>Iscardcmd:: get \_ ReplyStatusSW1-Methode

\[Die Methode " **get \_ ReplyStatusSW1** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **get \_ ReplyStatusSW1** -Methode ruft das [*Antwort-APDUs*](../secgloss/r-gly.md) SW1 Status Byte ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ReplyStatusSW1(
  [out] LPBYTE pbySW1
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbySW1* \[ vorgenommen\]
</dt> <dd>

Zeiger auf das Byte, das den Wert des SW1 Byte bei der Rückgabe enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>     |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *pbySW1* -Parameter ist ungültig.<br/>  |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | In *pbySW1* wurde ein fehlerhafter Zeiger übermittelt.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                        |



 

## <a name="remarks"></a>Bemerkungen

Das SW1-Status Byte der [*Antwort APDU*](../secgloss/r-gly.md) ist schreibgeschützt.

Rufen [**Sie get \_ ReplyStatusSW2**](iscardcmd-get-replystatussw2.md)auf, um das SW2-Status Byte der Antwort abzurufen.

Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie das SW1-Status Byte der [*Antwort-APDU*](../secgloss/r-gly.md)abgerufen wird. Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.


```C++
BYTE     bySW1;
HRESULT  hr;

// Retrieve the reply status SW1 byte.
hr = pISCardCmd->get_ReplyStatusSW1(&bySW1);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatusSW1\n");
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

[**get \_ ReplyStatusSW2**](iscardcmd-get-replystatussw2.md)
</dt> <dt>

[**\_replystatus erhalten**](iscardcmd-get-replystatus.md)
</dt> <dt>

[**Iscardcmd**](iscardcmd.md)
</dt> </dl>

 

 
