---
description: Die Clear-Methode löscht die APDU (Application Protocol Data Unit)-und Antwort-APDU-Nachrichten Puffer.
ms.assetid: 5fd3ebb9-b492-4668-9dd8-3ffbcfceb12c
title: 'Iscardcmd:: Clear-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.Clear
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0701906c38764ed1b4817f40430dde9b48bfb12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129353"
---
# <a name="iscardcmdclear-method"></a>Iscardcmd:: Clear-Methode

\[Die **Clear** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **Clear** -Methode löscht die APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) )-und [*Antwort-APDU*](../secgloss/r-gly.md) -Nachrichten Puffer.

## <a name="syntax"></a>Syntax


```C++
HRESULT Clear();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                             | Beschreibung                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**S \_ false**</dt> </dl> | Unbekannter Fehler.<br/>                    |



 

## <a name="remarks"></a>Bemerkungen

Zum Erstellen eines Befehls-APDU rufe Sie [**buildcmd**](iscardcmd-buildcmd.md)auf.

Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie die APDU-Nachrichten Puffer für APDU und Reply gelöscht werden.


```C++
HRESULT  hr;

hr = pISCardCmd->Clear();
if (FAILED(hr))
{
    printf("Failed ISCardCmd::Clear\n");
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

[**Iscardcmd:: buildcmd**](iscardcmd-buildcmd.md)
</dt> <dt>

[**Iscardcmd**](iscardcmd.md)
</dt> </dl>

 

 
