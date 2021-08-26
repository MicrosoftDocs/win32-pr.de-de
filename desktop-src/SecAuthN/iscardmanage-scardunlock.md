---
description: Gibt die exklusive Verwendung der verbundenen Smartcard frei.
ms.assetid: a236743a-1d12-44db-853d-f757f43a7e8f
title: ISCardManage::SCardUnlock-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardUnlock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1c100d1607cceea95264e9af24ba29b23824dee833c14e492cfb0a1dd7ad396f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013890"
---
# <a name="iscardmanagescardunlock-method"></a>ISCardManage::SCardUnlock-Methode

\[Die **SCardUnlock-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **SCardUnlock-Methode** gibt die exklusive Verwendung der verbundenen [*Smartcard*](../secgloss/s-gly.md)frei.

## <a name="syntax"></a>Syntax


```C++
HRESULT SCardUnlock(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Disposition* \[ In\]
</dt> <dd>

Der Zustand, in dem die Smartcard beim Loslassen der Sperre belassen werden soll.

<dl><span id="LEAVE"></span><span id="leave"></span><dt>

**Verlassen**
</dt><span id="RESET"></span><span id="reset"></span><dt>

**RESET**
</dt><span id="UNPOWER"></span><span id="unpower"></span><dt>

**UNPOWER**
</dt><span id="EJECT"></span><span id="eject"></span><dt>

**Auswerfen**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operation erfolgreich abgeschlossen.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der *Disposition-Parameter* ist ungültig.<br/> |



 

## <a name="remarks"></a>Hinweise

Um die verbundene Smartcard zu sperren, rufen Sie [**SCardLock**](iscardmanage-scardlock.md)auf.

Eine Liste aller von dieser Schnittstelle definierten Methoden finden Sie unter [**ISCardManage**](iscardmanage.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Schnittstelle einen Smartcardfehlercode zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**SCardLock**](iscardmanage-scardlock.md)
</dt> </dl>

 

 
