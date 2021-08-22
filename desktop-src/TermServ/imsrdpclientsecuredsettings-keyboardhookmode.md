---
title: IMsRdpClientSecuredSettings-Eigenschaft "KeyboardHookMode"
description: Gibt die Einstellungen für die Tastaturumleitung an, die angeben, wie und wann Windows Tastenkombination (z. B. ALT+TAB) angewendet werden soll.
ms.assetid: 16734580-9be9-476b-b8e7-1eca3ba24d61
ms.tgt_platform: multiple
keywords:
- KeyboardHookMode-Eigenschaft Remotedesktopdienste
- KeyboardHookMode-Eigenschaft Remotedesktopdienste , IMsRdpClientSecuredSettings-Schnittstelle
- IMsRdpClientSecuredSettings-Schnittstelle Remotedesktopdienste , KeyboardHookMode-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.KeyboardHookMode
- IMsRdpClientSecuredSettings.get_KeyboardHookMode
- IMsRdpClientSecuredSettings.put_KeyboardHookMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a291eeb26f8011440b8629ed46e1bb12c8b9cfb7adb937d33f80afe60a4d5cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657590"
---
# <a name="imsrdpclientsecuredsettingskeyboardhookmode-property"></a>IMsRdpClientSecuredSettings::KeyboardHookMode-Eigenschaft

Gibt die Einstellungen für die Tastaturumleitung an, die angeben, wie und wann Windows Tastenkombination (z. B. ALT+TAB) angewendet werden soll.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_KeyboardHookMode(
  [in]  LONG keyboardHookMode
);

HRESULT get_KeyboardHookMode(
  [out] LONG *pkeyboardHookMode
);
```



## <a name="property-value"></a>Eigenschaftswert

Die neuen Einstellungen. Dieser Parameter kann einen der folgenden Werte annehmen.

<dt>

0
</dt> <dd>

Wenden Sie Schlüsselkombinationen nur lokal auf dem Clientcomputer an.

</dd> <dt>

1
</dt> <dd>

Wenden Sie Schlüsselkombinationen auf dem Remoteserver an.

</dd> <dt>

2
</dt> <dd>

Wenden Sie Tastenkombinationen nur dann auf den Remoteserver an, wenn der Client im Vollbildmodus ausgeführt wird. Dies ist der Standardwert.

</dd> </dl>

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Hinweise

Diese Eigenschaften können nicht festgelegt werden, wenn das Steuerelement verbunden ist.

Weitere Informationen finden Sie unter [Bereitstellen der RDP-Clientsicherheit.](providing-for-rdp-client-security.md)

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                 |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ IMsRdpClientSecuredSettings ist als 605befcf-39c1-45cc-a811-068fb7be346d definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





