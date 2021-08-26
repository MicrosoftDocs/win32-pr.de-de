---
description: Ermöglicht einer Anwendung das erneute Herstellen einer Verbindung mit einer Smartcard oder einem Reader, ohne einen Detach-Aufruf gefolgt von einem AttachByHandle- bzw. AttachByIFD-Aufruf aus geben zu müssen.
ms.assetid: 450e817d-2cb2-4752-a86e-50cc8e434723
title: ISCardManage::Reconnect-Methode
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
ms.openlocfilehash: 9c0359a062f62e49b52b92623714e6d94aff015e53a71afa45d4a433c31f28c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013980"
---
# <a name="iscardmanagereconnect-method"></a>ISCardManage::Reconnect-Methode

\[Die **Reconnect-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Mit **der Reconnect-Methode** kann eine Anwendung [](../secgloss/r-gly.md) erneut eine Verbindung [](iscardmanage-detach.md) mit einer Smartcard oder einem Reader herstellen, ohne einen Detach-Aufruf gefolgt von einem [**AttachByHandle-**](iscardmanage-attachbyhandle.md) bzw. [**AttachByIFD-Aufruf**](iscardmanage-attachbyifd.md) aus geben zu müssen. [](../secgloss/s-gly.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT Reconnect();
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

Um eine Smartcard anfügen, rufen [**Sie AttachByHandle**](iscardmanage-attachbyhandle.md) oder [**AttachByIFD auf.**](iscardmanage-attachbyifd.md)

Um eine Smartcard zu trennen, rufen Sie [**Trennen auf.**](iscardmanage-detach.md)

Eine Liste aller von dieser Schnittstelle definierten Methoden finden Sie unter [**ISCardManage**](iscardmanage.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes gibt diese Schnittstelle möglicherweise einen Smartcard-Fehlercode zurück, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung zu erfüllen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AttachByHandle**](iscardmanage-attachbyhandle.md)
</dt> <dt>

[**AttachByIFD**](iscardmanage-attachbyifd.md)
</dt> <dt>

[**Trennen**](iscardmanage-detach.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> </dl>

 

 
