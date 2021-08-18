---
description: Gibt exklusiven Zugriff auf die Smartcard frei.
ms.assetid: 12256c91-faf2-4a06-9501-f00d0115a069
title: ISCard::UnlockSCard-Methode (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.UnlockSCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6e61811d84520db2d152fdbfdccfaeefafbee3c0a221e19cf56050096e1f5f5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482090"
---
# <a name="iscardunlockscard-method"></a>ISCard::UnlockSCard-Methode

\[Die **UnlockScard-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **UnlockScard-Methode** gibt exklusiven Zugriff auf die [*Smartcard*](../secgloss/s-gly.md)frei.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnlockSCard(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Disposition* \[ In\]
</dt> <dd>

Gibt an, was mit der Karte im verbundenen [*Reader*](../secgloss/r-gly.md)geschehen soll.



| Wert                                                                                                                                      | Bedeutung                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <dt>**Verlassen**</dt> </dl>       | Belässt die Smartcard im aktuellen [*Zustand*](../secgloss/s-gly.md).<br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <dt>**RESET**</dt> </dl>       | Setzt die Smartcard auf einen bekannten Zustand zurück.<br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <dt>**UNPOWER**</dt> </dl> | Entfernt die Stromversorgung von der Smartcard.<br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <dt>**Auswerfen**</dt> </dl>       | Wirft die Smartcard aus, wenn der Reader über auswerfende Funktionen verfügt.<br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operation erfolgreich abgeschlossen.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der *Disposition-Parameter* ist ungültig.<br/> |



 

## <a name="remarks"></a>Hinweise

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Schnittstelle einen Smartcardfehlercode zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die Freigabe des exklusiven Zugriffs auf die Smartcard.


```C++
HRESULT    hr;

// Unlock the smart card.
hr = pISCard->UnlockSCard(LEAVE);
if (FAILED(hr))
{
   printf("Failed UnlockSCard\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCard ist als 1461AAC3-6810-11D0-918F-00AA00C18068 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISCard**](iscard.md)
</dt> <dt>

[**LockSCard**](iscard-lockscard.md)
</dt> </dl>

 

 
