---
description: Fordert eine Überprüfung des Benutzers an.
ms.assetid: e8b7155c-3444-4aa8-8a15-3b3624a44a77
title: 'Iscardverify:: Verify-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.Verify
api_type:
- COM
api_location: ''
ms.openlocfilehash: 68f3a97df672d97e635180f41405a75c4cb84661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368730"
---
# <a name="iscardverifyverify-method"></a>Iscardverify:: Verify-Methode

\[Die **Verifizierungs** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **Verify** -Methode fordert eine Überprüfung des Benutzers an.

## <a name="syntax"></a>Syntax


```C++
HRESULT Verify(
  [in] LPBYTEBUFFER pCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcode* \[ in\]
</dt> <dd>

Enthält den Code, der für die [*Smartcard*](../secgloss/s-gly.md) im CHV-Prozess (Karteninhaber Überprüfung) angezeigt werden soll.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Gibt an, ob der Code Global oder lokal ist.

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

**SC \_ FL \_ IHV \_ Global**
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

**SC \_ FL \_ IHV \_ local**
</dt> </dl> </dd> <dt>

*lref* \[ in\]
</dt> <dd>

Smartcardspezifischer Verweis.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die **Verify** -Methode gibt einen der folgenden Werte zurück:



| Rückgabecode                                                                                   | Beschreibung                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Ungültiger Parameter.<br/>                |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Es wurde ein fehlerhafter Zeiger übermittelt.<br/>      |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Bemerkungen

Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardverify**](iscardverify.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscardverify**](iscardverify.md)
</dt> </dl>

 

 
