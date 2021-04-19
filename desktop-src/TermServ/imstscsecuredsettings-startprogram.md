---
title: Imstscsecuredsettings-Start Programm (Eigenschaft)
description: Gibt das Programm an, das auf dem Remote Server bei der Verbindung gestartet werden soll.
ms.assetid: bd2a5ced-468b-48db-ad51-9940577a0310
ms.tgt_platform: multiple
keywords:
- StartProgram-Eigenschaft Remotedesktopdienste
- StartProgram-Eigenschaft Remotedesktopdienste, imstscsecuredsettings-Schnittstelle
- Imstscsecuredsettings-Schnittstelle Remotedesktopdienste, StartProgram-Eigenschaft
- StartProgram-Eigenschaft Remotedesktopdienste, imsrdpclientsecuredsettings-Schnittstelle
- Imsrdpclientsecuredsettings-Schnittstelle Remotedesktopdienste, StartProgram-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.StartProgram
- IMsTscSecuredSettings.get_StartProgram
- IMsTscSecuredSettings.put_StartProgram
- IMsRdpClientSecuredSettings.StartProgram
- IMsRdpClientSecuredSettings.get_StartProgram
- IMsRdpClientSecuredSettings.put_StartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e79612855117f48e629e9a06246f3fad922d37f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346338"
---
# <a name="imstscsecuredsettingsstartprogram-property"></a>Imstscsecuredsettings:: StartProgram-Eigenschaft

Gibt das Programm an, das auf dem Remote Server bei der Verbindung gestartet werden soll.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_StartProgram(
  [in]  BSTR newVal
);

HRESULT get_StartProgram(
  [out] BSTR *pStartProgram
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Name des neuen Start Programms. Die maximale Länge dieser Zeichenfolge beträgt **Max. \_ Pfad**-1 Zeichen.

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der Wert dieser Eigenschaft nicht festgelegt ist, wird der Shellbefehl des Sitzungs Benutzers ausgeführt. Der Shellbefehl wird aus dem folgenden Registrierungs Wert auf dem Server gelesen:

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **Shell**

Weitere Informationen finden Sie unter [Bereitstellen der RDP-Client Sicherheit](providing-for-rdp-client-security.md) .

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ imstscsecuredsettings ist als c9d65442-a0f9-45b2-8f73-d61d2db8cbb6 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpclientsecuredsettings**](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[**Imstscsecuredsettings**](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





