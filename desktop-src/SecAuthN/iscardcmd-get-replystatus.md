---
description: Ruft das Nachrichten Status Wort von APDU ab.
ms.assetid: c8a4b713-4ae9-49f2-a623-6ee305123638
title: 'Iscardcmd:: get_ReplyStatus-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatus
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 021c5395dbca6275161a53cb7e8a0c2247ab9410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129333"
---
# <a name="iscardcmdget_replystatus-method"></a>Iscardcmd:: get \_ replystatus-Methode

\[Die **get \_ replystatus** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **get \_ replystatus** -Methode ruft das Nachrichten Status Wort [*von APDU*](../secgloss/r-gly.md) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ReplyStatus(
  [out] LPWORD pwStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwstatus* \[ vorgenommen\]
</dt> <dd>

Zeiger auf das Wort, das den Status bei der Rückgabe hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>       |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *pwstatus* -Parameter ist ungültig.<br/>  |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in *pwstatus* übergeben.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                          |



 

## <a name="remarks"></a>Bemerkungen

Um das Nachrichten Status Wort für die Antwort APDU festzulegen, wenden Sie [**Put \_ replystatus**](iscardcmd-put-replystatus.md)an.

Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie das Nachrichten Status Wort der [*Antwort-APDU*](../secgloss/r-gly.md)abgerufen wird. Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.


```C++
WORD    wReplyStatus;
HRESULT hr;

// Get reply status.
hr = pISCardCmd->get_ReplyStatus(&wReplyStatus);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatus\n");
  // Take other error handling action as needed.
}
else
{
  if (wReplyStatus != 0x9000)
  {
    printf("APDU failed - Error [0x%x]\n", wReplyStatus);
    // Take other error handling action as needed.
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

[**Iscardcmd**](iscardcmd.md)
</dt> <dt>

[**Put \_ replystatus**](iscardcmd-put-replystatus.md)
</dt> </dl>

 

 
