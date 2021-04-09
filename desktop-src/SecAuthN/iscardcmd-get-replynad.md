---
description: Ruft die von der Smartcard verwendete Knotenadresse (nad) in der Antwortnachricht ab.
ms.assetid: bf4f281c-d378-4abd-8f2e-e23c2f4e87a4
title: 'Iscardcmd:: get_ReplyNad-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyNad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2088aa208a97511fd53eecec5a8cdc473b612bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129336"
---
# <a name="iscardcmdget_replynad-method"></a>Iscardcmd:: get \_ replynad-Methode

\[Die **get \_ replynad** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **get \_ replynad** -Methode ruft die von der [*Smartcard*](../secgloss/s-gly.md) verwendete Knotenadresse (nad) in der Antwortnachricht ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ReplyNad(
  [out] BYTE *pbNad
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbnad* \[ vorgenommen\]
</dt> <dd>

Zeiger auf das Byte, das das von der Antwortnachricht verwendete nad bei der Rückgabe enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                    | Beschreibung                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang wurde erfolgreich abgeschlossen.<br/>                   |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>   | Der *pbnad* -Parameter ist ungültig.<br/>                     |
| <dl> <dt>**E \_ AccessDenied**</dt> </dl> | Bei internen aufrufen konnten die nad-Informationen nicht abgerufen werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Methode möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie die von der [*Smartcard*](../secgloss/s-gly.md) verwendete Knotenadresse (nad) in der Antwortnachricht abgerufen wird. Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.


```C++
BYTE    byNad;
HRESULT hr;

// Get reply Nad.
hr = pISCardCmd->get_ReplyNad(&byNad);
if (FAILED(hr))
{
  printf("Failed get_ReplyNad\n");
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

[**Iscardcmd**](iscardcmd.md)
</dt> </dl>

 

 
