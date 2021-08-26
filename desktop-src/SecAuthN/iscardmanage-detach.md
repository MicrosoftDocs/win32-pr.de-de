---
description: Gibt die Anlage an eine bestimmte Smartcard oder einen reader frei, die bzw. der von AttachByHandle bzw. AttachByIFD zugeordnet wird.
ms.assetid: 601b35a6-9094-4786-b94c-5cd1283feef5
title: ISCardManage::D etach-Methode
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
ms.openlocfilehash: 067c8e9f3e8cee607281d5f0a80ca813e91b425e63c15d3c1d47661acbbd04d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014090"
---
# <a name="iscardmanagedetach-method"></a>ISCardManage::D etach-Methode

\[Die **Detach-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **Detach-Methode** gibt die Anlage an eine bestimmte [*Smartcard*](../secgloss/s-gly.md) oder einen [*bestimmten Reader*](../secgloss/r-gly.md) frei, die bzw. der von [**AttachByHandle**](iscardmanage-attachbyhandle.md) bzw. [**AttachByIFD**](iscardmanage-attachbyifd.md) zugeordnet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Detach();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück:



| Rückgabecode                                                                                   | Beschreibung                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Hinweise

Um eine Smartcard anzufügen, rufen [**Sie AttachByHandle**](iscardmanage-attachbyhandle.md) oder [**AttachByIFD auf.**](iscardmanage-attachbyifd.md)

Um erneut eine Verbindung mit der Smartcard herzustellen, ohne **Detach** und [**AttachByHandle**](iscardmanage-attachbyhandle.md)aufzurufen, rufen [**Sie Erneut verbinden**](iscardmanage-reconnect.md)auf.

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

[**AttachByHandle**](iscardmanage-attachbyhandle.md)
</dt> <dt>

[**AttachByIFD**](iscardmanage-attachbyifd.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**Verbindung wiederherstellen**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
