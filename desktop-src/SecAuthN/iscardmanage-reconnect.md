---
description: Ermöglicht es einer Anwendung, erneut eine Verbindung mit einer Smartcard oder einem Reader herzustellen, ohne einen Trenn Befehl, gefolgt von einem attachbyhandle-oder attachbyifd-Rückruf, ausgeben zu müssen.
ms.assetid: 450e817d-2cb2-4752-a86e-50cc8e434723
title: 'Iscardmanage:: Reconnect-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Reconnect
api_type:
- COM
api_location: ''
ms.openlocfilehash: b8b05e6292a92267569eb1f53e10f6143554aba1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864047"
---
# <a name="iscardmanagereconnect-method"></a>Iscardmanage:: Reconnect-Methode

\[Die Methode zum **erneuten Verbinden** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Mit der Methode " **Verbindung Connect** " kann eine Anwendung erneut eine Verbindung mit einer [*Smartcard*](../secgloss/s-gly.md) oder einem [*Reader*](../secgloss/r-gly.md) herstellen, ohne einen [**Trenn**](iscardmanage-detach.md) Befehl, gefolgt von einem [**attachbyhandle**](iscardmanage-attachbyhandle.md) -oder [**attachbyifd-**](iscardmanage-attachbyifd.md) Rückruf, ausgeben zu müssen.

## <a name="syntax"></a>Syntax


```C++
HRESULT Reconnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück:



| Rückgabecode                                                                                   | Beschreibung                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Bemerkungen

So fügen Sie einen smartcardanrufe an [](iscardmanage-attachbyhandle.md) [](iscardmanage-attachbyifd.md)

Um eine Smartcard zu trennen, wenden Sie [**trennen**](iscardmanage-detach.md)an.

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

[**Attachbyhandle**](iscardmanage-attachbyhandle.md)
</dt> <dt>

[**Attachbyifd**](iscardmanage-attachbyifd.md)
</dt> <dt>

[**Trennen**](iscardmanage-detach.md)
</dt> <dt>

[**Iscardmanage**](iscardmanage.md)
</dt> </dl>

 

 
