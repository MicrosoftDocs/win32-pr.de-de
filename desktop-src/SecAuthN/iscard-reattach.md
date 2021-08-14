---
description: Die ReAttach-Methode setzt die Smartcard zurück oder initialisiert sie erneut.
ms.assetid: c9cd9cd7-5ee6-48dc-8460-deb9c827fcc4
title: ISCard::ReAttach-Methode (Scardmgr.h)
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
ms.openlocfilehash: f28caee7a40574bf7f31fdc4fb55ddd81ea9e22cca12f1664950c96922d50902
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482110"
---
# <a name="iscardreattach-method"></a>ISCard::ReAttach-Methode

\[Die **ReAttach-Methode** ist für die Verwendung in den Im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **ReAttach-Methode** setzt die Smartcard zurück oder [*initialisiert sie erneut.*](../secgloss/s-gly.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT ReAttach(
  [in] SCARD_SHARE_MODES  ShareMode,
  [in] SCARD_DISPOSITIONS InitState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ShareMode* \[ In\]
</dt> <dd>

Modus, in dem die Verbindung mit der Smartcard gemeinsam verwendet oder ausschließlich derEntste ist.



| Wert                                                                                                                                            | Bedeutung                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**Exklusive**</dt> </dl> | Diese Verbindung mit der Smartcard wird von niemand anderem verwendet.<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**geteilt**</dt> </dl>          | Andere Anwendungen können diese Verbindung verwenden.<br/>        |



 

</dd> <dt>

*InitState* \[ In\]
</dt> <dd>

Gibt an, was mit der Karte zu tun ist.



| Wert                                                                                                                                      | Bedeutung                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <dt>**Verlassen**</dt> </dl>       | Belässt die Smartcard im aktuellen [*Zustand*](../secgloss/s-gly.md).<br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <dt>**RESET**</dt> </dl>       | Setzt die Smartcard auf einen bekannten Zustand zurück.<br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <dt>**UNPOWER**</dt> </dl> | Entfernt die Stromversorgung von der Smartcard.<br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <dt>**Auswerfen**</dt> </dl>       | Wirft die Smartcard aus, wenn der Reader über Auswerfenfunktionen verfügt.<br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operation erfolgreich abgeschlossen.<br/>                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Es liegt ein Fehler mit einem oder mehr parametern vor, die an die Funktion übergeben werden.<br/> |



 

## <a name="remarks"></a>Hinweise

Zusätzlich zu den oben aufgeführten COM-Fehlercodes gibt diese Schnittstelle möglicherweise einen Smartcardfehlercode zurück, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung zu erfüllen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das neu initialisieren der Smartcard.


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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCard ist als 1461AAC3-6810-11D0-918F-00AA00C18068 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AttachByHandle**](iscard-attachbyhandle.md)
</dt> <dt>

[**AttachByReader**](iscard-attachbyreader.md)
</dt> <dt>

[**Trennen**](iscard-detach.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> </dl>

 

 
