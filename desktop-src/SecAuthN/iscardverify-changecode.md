---
description: Ersetzt den aktuellen CHV-Code (Karteninhaberüberprüfung) durch neuen CHV-Code.
ms.assetid: 8d47d842-67e8-4948-a63b-49bcfc8a69a1
title: ISCardVerify::ChangeCode-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ChangeCode
api_type:
- COM
api_location: ''
ms.openlocfilehash: 665cf0ec4c06feca9bcc221125daedc9ab8a12dabed0577b1f4bab5a31334804
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013540"
---
# <a name="iscardverifychangecode-method"></a>ISCardVerify::ChangeCode-Methode

\[Die **ChangeCode-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **ChangeCode-Methode** ersetzt den aktuellen CHV-Code (Card Holder Verification) durch neuen CHV-Code.

## <a name="syntax"></a>Syntax


```C++
HRESULT ChangeCode(
  [in] LPBYTEBUFFER pOldCode,
  [in] LPBYTEBUFFER pNewCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOldCode* \[ In\]
</dt> <dd>

Zeiger auf einen [**IByteBuffer,**](ibytebuffer.md) der den aktuellen Code des Benutzers enthält.

</dd> <dt>

*pNewCode* \[ In\]
</dt> <dd>

Zeiger auf einen [**IByteBuffer**](ibytebuffer.md) mit dem neuen Code, der der [*Smartcard*](../secgloss/s-gly.md) während des Änderungsprozesses zur Authentifizierung des Benutzers angezeigt wird.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Gibt an, ob der Code global oder lokal ist und ob der Code aktiviert oder deaktiviert werden soll.

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

**SC \_ FL \_ IHV \_ GLOBAL**
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

**SC \_ FL \_ IHV \_ LOCAL**
</dt><span id="SC_FL_IHV_ENABLE"></span><span id="sc_fl_ihv_enable"></span><dt>

**SC \_ FL \_ IHV \_ ENABLE**
</dt><span id="SC_FL_IHV_DISABLE"></span><span id="sc_fl_ihv_disable"></span><dt>

**SC \_ FL \_ IHV \_ DISABLE**
</dt> </dl> </dd> <dt>

*lRef* \[ In\]
</dt> <dd>

Smartcardspezifische Referenz.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück:



| Rückgabecode                                                                                   | Beschreibung                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ungültiger Parameter.<br/>                |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Ein ungültiger Zeiger wurde übergeben.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Hinweise

Eine Liste aller von dieser Schnittstelle definierten Methoden finden Sie unter [**ISCardVerify.**](iscardverify.md)

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

[**IByteBuffer**](ibytebuffer.md)
</dt> <dt>

[**ISCardVerify**](iscardverify.md)
</dt> <dt>

[Smartcard-Rückgabewerte](authentication-return-values.md)
</dt> </dl>

 

 
