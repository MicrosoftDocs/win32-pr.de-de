---
description: Fügt das iscard-Objekt an ein geöffnetes und konfiguriertes smartcardhandle an.
ms.assetid: e735d33d-a337-404e-a760-4cf8f19d172a
title: 'Iscard:: attachbyhandle-Methode (scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e72ce215b373ef8bd48921f796083e9bc5e801be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364183"
---
# <a name="iscardattachbyhandle-method"></a>Iscard:: attachbyhandle-Methode

\[Die **attachbyhandle** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **attachbyhandle** -Methode fügt das [**iscard**](iscard.md) -Objekt an ein geöffnetes und konfiguriertes [*smartcardhandle*](../secgloss/s-gly.md) an.

## <a name="syntax"></a>Syntax


```C++
HRESULT AttachByHandle(
  [in] HSCARD hCard
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hCard* \[ in\]
</dt> <dd>

Ein Handle für eine geöffnete Verbindung zu einer Smartcard.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operation erfolgreich abgeschlossen.<br/>   |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der *hCard* -Parameter ist ungültig.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

Wenn Sie die Verwendung des Handles abgeschlossen haben, geben Sie die Anlage frei, indem Sie die [**iscard::D Etach**](iscard-detach.md) -Methode aufrufen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das Anfügen an ein smartcardhandle gezeigt.


```C++
HRESULT  hr;

// hSC is of type HSCARD and has been previously assigned.
// Attach SCard to the smart card using the value in hSC.
hr = pISCard->AttachByHandle(hSC);
if (FAILED(hr))
{
   printf("Failed AttachByHandle\n");
   // Take other error handling action as needed.
}
// Proceed using attached reader.
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

[**Attachbyreader**](iscard-attachbyreader.md)
</dt> <dt>

[**Trennen**](iscard-detach.md)
</dt> <dt>

[**\_cardhandle erhalten**](iscard-get-cardhandle.md)
</dt> <dt>

[**Iscard**](iscard.md)
</dt> <dt>

[**Erneut**](iscard-reattach.md)
</dt> </dl>

 

 
