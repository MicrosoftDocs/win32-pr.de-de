---
title: IMsRdpClientAdvancedSettings6 Connect-Administrator Server Eigenschaft
description: Ruft ab oder legt fest, ob das ActiveX-Steuerelement versuchen soll, eine Verbindung mit dem Server zu Verwaltungszwecken herzustellen.
ms.assetid: b98f9b9b-a3e7-4a3c-a7e3-e388ce53c5c9
ms.tgt_platform: multiple
keywords:
- Connect-Administrator Server-Eigenschaft Remotedesktopdienste
- ConnectRemotedesktopdienste Administration Server-Eigenschaft, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste, connecttadministration-Server Eigenschaft
- ConnectRemotedesktopdienste Administration Server-Eigenschaft, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste, connecttadministration-Server Eigenschaft
- ConnectRemotedesktopdienste Administration Server-Eigenschaft, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste, connecttadministration-Server Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.put_ConnectToAdministerServer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9cad8d50e2e0a4c1ec18fbd33733dc394101a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040614"
---
# <a name="imsrdpclientadvancedsettings6connecttoadministerserver-property"></a>IMsRdpClientAdvancedSettings6:: ConnectTo Administration Server-Eigenschaft

Ruft ab oder legt fest, ob das ActiveX-Steuerelement versuchen soll, eine Verbindung mit dem Server zu Verwaltungszwecken herzustellen.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ConnectToAdministerServer(
  [in]  VARIANT_BOOL connectToAdministerServer
);

HRESULT get_ConnectToAdministerServer(
  [out] VARIANT_BOOL *pConnectToAdministerServer
);
```



## <a name="property-value"></a>Eigenschaftswert

**Variant \_ TRUE** , wenn das ActiveX-Steuerelement versucht, zu Verwaltungszwecken eine Verbindung mit dem Server herzustellen. Andernfalls ist der Wert **\_ false**. Der Standardwert ist **Variant \_ false**.

## <a name="remarks"></a>Bemerkungen

Zum Verwenden von **connectdeadministration Server** muss Remotedesktopverbindung (RDC)-Client Version 6,1 oder höher ausgeführt werden.

> [!Note]  
> Die RDC-Version 6,1 (6.0.6001) unterstützt Remotedesktopprotokoll 6,1. RDC 6,1 ist in Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) enthalten.

 

**Verbindungs Server Server** stellt eine Verbindung mit einer Sitzung her, die für administrative Zwecke auf dem Remote Server verwendet wird. Wenn der Remotedesktop-Sitzungshost (RD-Sitzungshost)-Rollen Dienst auf dem Remote Server installiert ist, führt **connectdeadministration** folgende Aktionen aus:

-   Deaktiviert die Remotedesktopdienste Client Zugriffs Lizenzierung für die Sitzung.
-   Deaktiviert die Zeit Zonen Umleitung für die Sitzung.
-   Deaktiviert die Umleitung von Remotedesktopverbindung Broker (RD-Verbindungsbroker) für die Sitzung.
-   Deaktiviert Plug & Play Geräte Umleitung für die Sitzung.
-   Ändert das Remote Sitzungs Design in Windows Classic für die Sitzung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                   |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 ist als 222c4b5d-45d9-4df0-a7c6-60cf9089d285 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





