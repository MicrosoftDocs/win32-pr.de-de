---
description: Erstellt eine Kommunikations Verknüpfung mit einem Reader unter Verwendung eines angegebenen anzeigen Amens für den Reader.
ms.assetid: 7916896b-c460-47b2-a1db-17d8fc9bdd2e
title: 'Iscardmanage:: attachbyifd-Methode'
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
ms.openlocfilehash: ae0aaae2157331d5d1bae2814c563c89dc73c757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349479"
---
# <a name="iscardmanageattachbyifd-method"></a>Iscardmanage:: attachbyifd-Methode

\[Die **attachbyifd-** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **attachbyifd-** Methode erstellt eine Kommunikations Verknüpfung mit einem [*Reader*](../secgloss/r-gly.md)unter Verwendung eines angegebenen anzeigen Amens für den Reader.

## <a name="syntax"></a>Syntax


```C++
HRESULT AttachByIFD(
  [in] BSTR bstrIFDName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrif-Name* \[ in\]
</dt> <dd>

Der Anzeige Name des Readers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück:



| Rückgabecode                                                                                   | Beschreibung                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>         |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der Parameter " *bstrifdname* " ist ungültig.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                            |



 

## <a name="remarks"></a>Bemerkungen

Zum Anfügen [](../secgloss/s-gly.md) eines smartcardanrufes [**attachbyhandle**](iscardmanage-attachbyhandle.md).

Zum Freigeben eines Anlage Aufrufs [**trennen**](iscardmanage-detach.md).

Um erneut eine Verbindung mit der Smartcard herzustellen, ohne [**Detach**](iscardmanage-detach.md) und **attachbyifd** aufzurufen, rufen Sie [**Verbindung**](iscardmanage-reconnect.md)auf.

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

[**Trennen**](iscardmanage-detach.md)
</dt> <dt>

[**Iscardmanage**](iscardmanage.md)
</dt> <dt>

[**Verbindung wiederherstellen**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
