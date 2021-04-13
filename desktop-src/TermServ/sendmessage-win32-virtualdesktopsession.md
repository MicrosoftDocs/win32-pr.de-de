---
title: SendMessage-Methode der Win32_VirtualDesktopSession-Klasse
description: Senden Sie eine Nachricht über die virtuelle Desktop Sitzung an den Benutzer.
ms.assetid: 4bb9183e-c016-48f2-8e8c-0d5fb395c435
ms.tgt_platform: multiple
keywords:
- SendMessage-Methode Remotedesktopdienste
- SendMessage-Methode Remotedesktopdienste, Win32_VirtualDesktopSession-Klasse
- Win32_VirtualDesktopSession-Klasse Remotedesktopdienste, SendMessage-Methode
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession.SendMessage
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1e3e72f5c401b8cbb0e5e5de45f594d61af6275
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391869"
---
# <a name="sendmessage-method-of-the-win32_virtualdesktopsession-class"></a>SendMessage-Methode der Win32 \_ virtualdesktopsession-Klasse

Senden Sie eine Nachricht über die virtuelle Desktop Sitzung an den Benutzer.

## <a name="syntax"></a>Syntax


```mof
uint32 SendMessage(
  [in] string Title,
  [in] string Message
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Titel* \[ in\]
</dt> <dd>

Der Titel der Messung.

</dd> <dt>

*Nachricht* \[ in\]
</dt> <dd>

Der Inhalt der Nachricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | Root \\ CIMv2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ virtualdesktopsession**](win32-virtualdesktopsession.md)
</dt> </dl>

 

 





