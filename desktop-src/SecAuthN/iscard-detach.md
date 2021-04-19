---
description: Schließt die geöffnete Verbindung mit der Smartcard.
ms.assetid: 7d768945-8d5d-4d29-b5bc-1b2ac5b0e114
title: Iscard::D Etach-Methode (scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Detach
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f9fd2b2a6d9ea2df8e886c6ff9851706c2030a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355346"
---
# <a name="iscarddetach-method"></a>Iscard::D Etach-Methode

\[Die **Detach** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **Detach** -Methode schließt die geöffnete Verbindung mit der [*Smartcard*](../secgloss/s-gly.md).

## <a name="syntax"></a>Syntax


```C++
HRESULT Detach(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Disposition* \[ in\]
</dt> <dd>

Gibt an, was mit der Karte im verbundenen [*Reader*](../secgloss/r-gly.md)geschehen soll.



| Wert                                                                                                                                      | Bedeutung                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <dt>**Lassen Sie**</dt> </dl>       | Verlässt die Smartcard im aktuellen [*Zustand*](../secgloss/s-gly.md).<br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <dt>**Festlegen**</dt> </dl>       | Setzt die Smartcard auf einen bekannten Zustand zurück.<br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <dt>**Nicht mehr**</dt> </dl> | Entfernt die Stromversorgung von der Smartcard.<br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <dt>**Auswerfen**</dt> </dl>       | Fügt die Smartcard ein, wenn der Reader über Auswerfen-Funktionen verfügt.<br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | *Disposition* ist ungültig.<br/>       |



 

## <a name="remarks"></a>Bemerkungen

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das Schließen der Verbindung mit der Smartcard.


```C++
HRESULT    hr;

// Detach the smart card.
hr = pISCard->Detach(LEAVE);
if (FAILED(hr))
{
   printf("Failed Detach\n");
   // Take error handling action as needed.
}
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

[**Attachbyhandle**](iscard-attachbyhandle.md)
</dt> <dt>

[**Attachbyreader**](iscard-attachbyreader.md)
</dt> <dt>

[**Iscard**](iscard.md)
</dt> <dt>

[**Erneut**](iscard-reattach.md)
</dt> </dl>

 

 
