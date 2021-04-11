---
description: Gibt die Anlage auf einer bestimmten Smartcard oder einem Leser frei, der von attachbyhandle bzw. attachbyifd zugeordnet wird.
ms.assetid: 601b35a6-9094-4786-b94c-5cd1283feef5
title: Iscardmanage::D Etach-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Detach
api_type:
- COM
api_location: ''
ms.openlocfilehash: bc5a48f76a643447b3e3d836d61ad7a769c56ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130653"
---
# <a name="iscardmanagedetach-method"></a>Iscardmanage::D Etach-Methode

\[Die **Detach** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **Detach** -Methode gibt die Anlage auf eine bestimmte [*Smartcard*](../secgloss/s-gly.md) oder einen [*Leser*](../secgloss/r-gly.md) frei, der von [**attachbyhandle**](iscardmanage-attachbyhandle.md) bzw. [**attachbyifd**](iscardmanage-attachbyifd.md) zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT Detach();
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

Um erneut eine Verbindung mit der Smartcard herzustellen, ohne **Detach** und [**attachbyhandle**](iscardmanage-attachbyhandle.md)aufzurufen, rufen Sie [**Verbindung**](iscardmanage-reconnect.md)auf.

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

[**Iscardmanage**](iscardmanage.md)
</dt> <dt>

[**Verbindung wiederherstellen**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
