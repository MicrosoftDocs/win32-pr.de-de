---
description: Gibt die exklusive Verwendung der verbundenen Smartcard frei.
ms.assetid: a236743a-1d12-44db-853d-f757f43a7e8f
title: 'Iscardmanage:: scardunlock-Methode'
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
ms.openlocfilehash: 90c6b10d407992ae8147998d2d420989cc91e970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215465"
---
# <a name="iscardmanagescardunlock-method"></a>Iscardmanage:: scardunlock-Methode

\[Die Methode " **scardunlock** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **scardunlock** -Methode gibt die exklusive Verwendung der verbundenen [*Smartcard*](../secgloss/s-gly.md)frei.

## <a name="syntax"></a>Syntax


```C++
HRESULT SCardUnlock(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Disposition* \[ in\]
</dt> <dd>

Der Zustand, in dem die Smartcard bei der Freigabe der Sperre belassen werden soll.

<dl><span id="LEAVE"></span><span id="leave"></span><dt>

**Lassen Sie**
</dt><span id="RESET"></span><span id="reset"></span><dt>

**RESET**
</dt><span id="UNPOWER"></span><span id="unpower"></span><dt>

**Nicht mehr**
</dt><span id="EJECT"></span><span id="eject"></span><dt>

**Auswerfen**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operation erfolgreich abgeschlossen.<br/>         |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der *Disposition* -Parameter ist ungültig.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Um die verbundene Smartcard zu sperren, nennen Sie [**scardlock**](iscardmanage-scardlock.md).

Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardmanage**](iscardmanage.md).

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

[**Iscardmanage**](iscardmanage.md)
</dt> <dt>

[**Scardlock**](iscardmanage-scardlock.md)
</dt> </dl>

 

 
