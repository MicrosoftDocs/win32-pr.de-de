---
title: Imsrdpclientsecuredsettings keyboardhuokmode (Eigenschaft)
description: Gibt die Einstellungen der Tastatur Umleitung an, die angeben, wie und wann die Windows-Tastenkombination angewendet werden soll (z. b. Alt + Tab).
ms.assetid: 16734580-9be9-476b-b8e7-1eca3ba24d61
ms.tgt_platform: multiple
keywords:
- Keyboardhuokmode-Eigenschaft Remotedesktopdienste
- Keyboardhuokmode-Eigenschaft Remotedesktopdienste, imsrdpclientsecuredsettings-Schnittstelle
- Imsrdpclientsecuredsettings-Schnittstelle Remotedesktopdienste, keyboardhuokmode-Eigenschaft
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
ms.openlocfilehash: 948069b689d8799a98805148017a204b719d7645
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391730"
---
# <a name="imsrdpclientsecuredsettingskeyboardhookmode-property"></a>Imsrdpclientsecuredsettings:: keyboardhuokmode-Eigenschaft

Gibt die Einstellungen der Tastatur Umleitung an, die angeben, wie und wann die Windows-Tastenkombination angewendet werden soll (z. b. Alt + Tab).

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

Anwenden von Tastenkombinationen nur lokal auf dem Client Computer.

</dd> <dt>

1
</dt> <dd>

Anwenden von Tastenkombinationen auf dem Remote Server.

</dd> <dt>

2
</dt> <dd>

Anwenden von Tastenkombinationen auf den Remote Server, wenn der Client im Vollbildmodus ausgeführt wird. Dies ist der Standardwert.

</dd> </dl>

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften können nicht festgelegt werden, wenn das Steuerelement verbunden ist.

Weitere Informationen finden Sie unter [Bereitstellen der RDP-Client Sicherheit](providing-for-rdp-client-security.md) .

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                 |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ imsrdpclientsecuredsettings ist als 605befcf-39c1-45cc-a811-068fb7be346d definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpclientsecuredsettings**](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





