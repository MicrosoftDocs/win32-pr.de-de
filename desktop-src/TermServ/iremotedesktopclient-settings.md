---
title: Iremotedesktopclient Settings-Eigenschaft
description: Ruft das Einstellungs Objekt für den Remotedesktopprotokoll (RDP)-app-Container Client ab.
ms.assetid: 59999489-9ad0-4b85-9643-3b8355b817c2
ms.tgt_platform: multiple
keywords:
- Einstellungs Eigenschaft Remotedesktopdienste
- Einstellungs Eigenschaft Remotedesktopdienste, iremotedesktopclient-Schnittstelle
- Iremotedesktopclient-Schnittstelle Remotedesktopdienste, Einstellungs Eigenschaft
topic_type:
- apiref
api_name:
- IRemoteDesktopClient.Settings
- IRemoteDesktopClient.get_Settings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e84324eaa12610d7ab898cbcb181e7712bc021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956752"
---
# <a name="iremotedesktopclientsettings-property"></a>Iremotedesktopclient:: Settings-Eigenschaft

Ruft das Einstellungs Objekt für den Remotedesktopprotokoll (RDP)-app-Container Client ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Settings(
  [out, retval] IRemoteDesktopClientSettings **Settings
);
```



## <a name="property-value"></a>Eigenschaftswert

Das Einstellungs Objekt für den RDP-Client.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                          |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>  |
| IID<br/>                      | IID \_ iremotedesktopclient ist als 57d25668-625A-4905-BE4E-304caa13f 89c definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iremotedesktopclient**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
</dt> </dl>

 

