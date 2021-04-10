---
description: Durch die Methode zum erneuten Anfügen wird die Smartcard zurückgesetzt oder erneut initialisiert.
ms.assetid: c9cd9cd7-5ee6-48dc-8460-deb9c827fcc4
title: 'Iscard:: reattach-Methode (scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.ReAttach
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3f5ff4cd46b2b523b0031e1389b96d9c2c3973a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215111"
---
# <a name="iscardreattach-method"></a>Iscard:: reattach-Methode

\[Die Methode zum **erneuten Anfügen** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Durch die Methode zum **erneuten Anfügen** wird die [*Smartcard*](../secgloss/s-gly.md)zurückgesetzt oder erneut initialisiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReAttach(
  [in] SCARD_SHARE_MODES  ShareMode,
  [in] SCARD_DISPOSITIONS InitState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Share Mode* \[ in\]
</dt> <dd>

Der Modus, in dem die Verbindung mit der Smartcard gemeinsam genutzt oder exklusiv ist.



| Wert                                                                                                                                            | Bedeutung                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**Ausschließliche**</dt> </dl> | Diese Verbindung wird von keiner anderen Person mit der Smartcard verwendet.<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**Genu**</dt> </dl>          | Diese Verbindung kann von anderen Anwendungen verwendet werden.<br/>        |



 

</dd> <dt>

*Initstate* \[ in\]
</dt> <dd>

Gibt an, was mit der Karte zu tun ist.



| Wert                                                                                                                                      | Bedeutung                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <dt>**Lassen Sie**</dt> </dl>       | Verlässt die Smartcard im aktuellen [*Zustand*](../secgloss/s-gly.md).<br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <dt>**Festlegen**</dt> </dl>       | Setzt die Smartcard auf einen bekannten Zustand zurück.<br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <dt>**Nicht mehr**</dt> </dl> | Entfernt die Stromversorgung von der Smartcard.<br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <dt>**Auswerfen**</dt> </dl>       | Fügt die Smartcard ein, wenn der Reader über Auswerfen-Funktionen verfügt.<br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operation erfolgreich abgeschlossen.<br/>                                                     |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Bei einem oder mehreren Parametern, die an die Funktion weitergegeben wurden, ist ein Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie die Smartcard erneut initialisiert wird.


```C++
HRESULT    hr;

// Reattach the smart card.
hr = pISCard->ReAttach(SHARED, LEAVE);
if (FAILED(hr))
{
   printf("Failed ReAttach\n");
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

[**Trennen**](iscard-detach.md)
</dt> <dt>

[**Iscard**](iscard.md)
</dt> </dl>

 

 
