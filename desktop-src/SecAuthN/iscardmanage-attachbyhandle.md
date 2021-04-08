---
description: Erstellt mithilfe eines Handles, das von der Smartcard-Ressourcen-Manager zurückgegeben wird, einen Kommunikationslink zu einer Smartcard (ICC).
ms.assetid: dfd05dce-4416-4881-92ca-c85baccf3b86
title: 'Iscardmanage:: attachbyhandle-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByHandle
api_type:
- COM
api_location: ''
ms.openlocfilehash: 266b6a0d2a4027fe85f1f5539b970a44fc21bbee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866012"
---
# <a name="iscardmanageattachbyhandle-method"></a>Iscardmanage:: attachbyhandle-Methode

\[Die **attachbyhandle** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **attachbyhandle** -Methode erstellt mithilfe eines Handles, das von der Smartcard- [*Ressourcen-Manager*](../secgloss/r-gly.md)zurückgegeben wird, einen Kommunikationslink zu einer [*Smartcard*](../secgloss/s-gly.md) (ICC).

## <a name="syntax"></a>Syntax


```C++
HRESULT AttachByHandle(
  [in] HSCARD hICC
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hicc* \[ in\]
</dt> <dd>

Ein Handle für eine Smartcard.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück:



| Rückgabecode                                                                                   | Beschreibung                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>  |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *hicc* -Parameter ist ungültig.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Zum Anfügen eines [*Reader*](../secgloss/r-gly.md) -Anfügens [**attachbyifd**](iscardmanage-attachbyifd.md).

Zum Freigeben eines Anlage Aufrufs [**trennen**](iscardmanage-detach.md).

Um erneut eine Verbindung mit der Smartcard herzustellen, ohne [**Detach**](iscardmanage-detach.md) und **attachbyhandle** aufzurufen, rufen Sie [**Verbindung**](iscardmanage-reconnect.md)auf.

Eine Liste aller Methoden, die von der [**iscardmanage**](iscardmanage.md) -Schnittstelle definiert werden, finden Sie unter [**iscardmanage**](iscardmanage.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Informationen zu smartcardfehlercodes finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attachbyifd**](iscardmanage-attachbyifd.md)
</dt> <dt>

[**Trennen**](iscardmanage-detach.md)
</dt> <dt>

[**Iscardmanage**](iscardmanage.md)
</dt> <dt>

[**Verbindung wiederherstellen**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
