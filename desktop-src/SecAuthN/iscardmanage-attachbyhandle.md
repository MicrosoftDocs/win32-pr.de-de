---
description: Erstellt mithilfe eines vom Smartcard-Ressourcen-Manager zurückgegebenen Handles eine Kommunikationsverbindung mit einer Smartcard (CARD).
ms.assetid: dfd05dce-4416-4881-92ca-c85baccf3b86
title: ISCardManage::AttachByHandle-Methode
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
ms.openlocfilehash: c464f2d514a59754b5dc4d9d98f745a4802843c3cfafa3df16057c53456221c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014160"
---
# <a name="iscardmanageattachbyhandle-method"></a>ISCardManage::AttachByHandle-Methode

\[Die **AttachByHandle-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **AttachByHandle-Methode** erstellt mithilfe eines handle, das vom Smartcard-Ressourcen-Manager zurückgegeben wird, eine Kommunikationsverbindung mit einer [*Smartcard*](../secgloss/r-gly.md) [*(CARD).*](../secgloss/s-gly.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT AttachByHandle(
  [in] HSCARD hICC
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hICC* \[ In\]
</dt> <dd>

Ein Handle für eine Smartcard.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück:



| Rückgabecode                                                                                   | Beschreibung                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *hICC-Parameter* ist ungültig.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                     |



 

## <a name="remarks"></a>Hinweise

Um einen Reader [*anfügen,*](../secgloss/r-gly.md) rufen [**Sie AttachByIFD auf.**](iscardmanage-attachbyifd.md)

Um eine Anlage frei zu geben, rufen [**Sie Trennen auf.**](iscardmanage-detach.md)

Um die Verbindung mit der Smartcard ohne Aufruf von [**Detach**](iscardmanage-detach.md) und **AttachByHandle** wiederherzustellen, rufen Sie [**Erneut verbinden auf.**](iscardmanage-reconnect.md)

Eine Liste aller methoden, die von der [**ISCardManage-Schnittstelle**](iscardmanage.md) definiert werden, finden Sie unter [**ISCardManage**](iscardmanage.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes gibt diese Schnittstelle möglicherweise einen Smartcard-Fehlercode zurück, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung zu erfüllen. Informationen zu Smartcard-Fehlercodes finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AttachByIFD**](iscardmanage-attachbyifd.md)
</dt> <dt>

[**Trennen**](iscardmanage-detach.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**Verbindung wiederherstellen**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
