---
description: Sperrt eine verbundene Smartcard für die exklusive Verwendung.
ms.assetid: c39a7cfe-04b6-4298-927a-4280664cf769
title: 'Iscardmanage:: scardlock-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardLock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2198f512fde90d1c79173f5151fc4f759944500a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215467"
---
# <a name="iscardmanagescardlock-method"></a>Iscardmanage:: scardlock-Methode

\[Die **scardlock** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **scardlock** -Methode sperrt eine verbundene [*Smartcard*](../secgloss/s-gly.md) für die exklusive Verwendung.

## <a name="syntax"></a>Syntax


```C++
HRESULT SCardLock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück:



| Rückgabecode                                                                            | Beschreibung                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Der Vorgang konnte nicht beendet werden.<br/>     |



 

## <a name="remarks"></a>Bemerkungen

Um die exklusive Verwendung der verbundenen Smartcard freizusetzen, nennen Sie [**scardunlock**](iscardmanage-scardunlock.md).

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

[**Scardunlock**](iscardmanage-scardunlock.md)
</dt> </dl>

 

 
