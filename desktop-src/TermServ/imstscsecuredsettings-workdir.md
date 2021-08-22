---
title: IMsTscSecuredSettings WorkDir-Eigenschaft
description: Gibt das Arbeitsverzeichnis des Startprogramms an.
ms.assetid: e67f7274-be47-42c4-9267-a05bb93e6725
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der WorkDir-Eigenschaft
- WorkDir-Eigenschaft Remotedesktopdienste , IMsTscSecuredSettings-Schnittstelle
- IMsTscSecuredSettings-Schnittstelle Remotedesktopdienste , WorkDir-Eigenschaft
- WorkDir-Eigenschaft Remotedesktopdienste , IMsRdpClientSecuredSettings-Schnittstelle
- IMsRdpClientSecuredSettings-Schnittstelle Remotedesktopdienste , WorkDir-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.WorkDir
- IMsTscSecuredSettings.get_WorkDir
- IMsTscSecuredSettings.put_WorkDir
- IMsRdpClientSecuredSettings.WorkDir
- IMsRdpClientSecuredSettings.get_WorkDir
- IMsRdpClientSecuredSettings.put_WorkDir
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cc6bd8ffe1e2d2f5b835090ee1dec5e3420a8bfb2d5801b3f5f903b3436bf66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118853142"
---
# <a name="imstscsecuredsettingsworkdir-property"></a>IMsTscSecuredSettings::WorkDir-Eigenschaft

Gibt das Arbeitsverzeichnis des Startprogramms an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_WorkDir(
  [in]  BSTR newVal
);

HRESULT get_WorkDir(
  [out] BSTR *pWorkDir
);
```



## <a name="property-value"></a>Eigenschaftswert

Das neue Arbeitsverzeichnis. Die maximale Länge dieser Zeichenfolge beträgt **MAX \_ PATH**-1 Zeichen.

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Hinweise

Weitere Informationen finden Sie unter [Bereitstellen der RDP-Clientsicherheit.](providing-for-rdp-client-security.md)

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsTscSecuredSettings ist als c9d65442-a0f9-45b2-8f73-d61d2db8cbb6 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





