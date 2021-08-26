---
title: SendMessage-Methode der Win32_VirtualDesktopSession-Klasse
description: Senden Sie eine Nachricht an den Benutzer über die Sitzung für virtuelle Desktops.
ms.assetid: 4bb9183e-c016-48f2-8e8c-0d5fb395c435
ms.tgt_platform: multiple
keywords:
- SendMessage-Remotedesktopdienste
- SendMessage-methode Remotedesktopdienste , Win32_VirtualDesktopSession-Klasse
- Win32_VirtualDesktopSession klasse Remotedesktopdienste , SendMessage-Methode
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
ms.openlocfilehash: a159d9c8b4e8c4b5086fff9c4fc6c67c0a6e33464eeefee77d15a620b157bd55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988150"
---
# <a name="sendmessage-method-of-the-win32_virtualdesktopsession-class"></a>SendMessage-Methode der Win32 \_ VirtualDesktopSession-Klasse

Senden Sie eine Nachricht an den Benutzer über die Sitzung für virtuelle Desktops.

## <a name="syntax"></a>Syntax


```mof
uint32 SendMessage(
  [in] string Title,
  [in] string Message
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Titel* \[ In\]
</dt> <dd>

Der Titel des Unordnungsgefecks.

</dd> <dt>

*Nachricht* \[ In\]
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
| Namespace<br/>                | \\Stamm-CIMv2-Rdms \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ VirtualDesktopSession**](win32-virtualdesktopsession.md)
</dt> </dl>

 

 





