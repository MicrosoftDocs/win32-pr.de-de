---
description: Erstellt eine Kommunikationsverbindung mit einem Reader unter Verwendung eines angegebenen Anzeigenamens für den Reader.
ms.assetid: 7916896b-c460-47b2-a1db-17d8fc9bdd2e
title: ISCardManage::AttachByIFD-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByIFD
api_type:
- COM
api_location: ''
ms.openlocfilehash: cfc95f8c4318dbc78e3cbd93faf18fd5e8e764ab251096cc0a2c321dedd00002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922865"
---
# <a name="iscardmanageattachbyifd-method"></a>ISCardManage::AttachByIFD-Methode

\[Die **AttachByIFD-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **AttachByIFD-Methode** erstellt eine Kommunikationsverbindung mit einem Reader [*unter*](../secgloss/r-gly.md)Verwendung eines angegebenen Anzeigenamens für den Reader.

## <a name="syntax"></a>Syntax


```C++
HRESULT AttachByIFD(
  [in] BSTR bstrIFDName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrIFDName* \[ In\]
</dt> <dd>

Der Anzeigename des Readers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück:



| Rückgabecode                                                                                   | Beschreibung                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *bstrIFDName-Parameter* ist ungültig.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                            |



 

## <a name="remarks"></a>Hinweise

Um eine Smartcard [*anfügen, rufen*](../secgloss/s-gly.md) [**Sie AttachByHandle auf.**](iscardmanage-attachbyhandle.md)

Um eine Anlage frei zu geben, rufen [**Sie Trennen auf.**](iscardmanage-detach.md)

Um die Verbindung mit der Smartcard ohne Aufruf von [**Detach**](iscardmanage-detach.md) und **AttachByIFD** wiederherzustellen, rufen Sie [**Erneut verbinden auf.**](iscardmanage-reconnect.md)

Eine Liste aller von dieser Schnittstelle definierten Methoden finden Sie unter [**ISCardManage**](iscardmanage.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes gibt diese Schnittstelle möglicherweise einen Smartcardfehlercode zurück, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung zu erfüllen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AttachByHandle**](iscardmanage-attachbyhandle.md)
</dt> <dt>

[**Trennen**](iscardmanage-detach.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**Verbindung wiederherstellen**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
