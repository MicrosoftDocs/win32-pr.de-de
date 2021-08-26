---
title: IMsRdpClient7-Schnittstelle
description: Stellt die Methoden und Eigenschaften zur Konfiguration und Verwendung des Clientsteuer steuerelements zur Anwendung. Wird von der IMsRdpClient6-Schnittstelle ableiten.
ms.assetid: f6bc5d50-f16a-44be-8244-5aec13c52066
ms.tgt_platform: multiple
keywords:
- IMsRdpClient7-Remotedesktopdienste
- IMsRdpClient7-Schnittstelle Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClient7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1cdd90e9e05a0220fffa2646ae31cf652bb232283b0dec9c908202f38f950f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990530"
---
# <a name="imsrdpclient7-interface"></a>IMsRdpClient7-Schnittstelle

Stellt die Methoden und Eigenschaften zur Konfiguration und Verwendung des Clientsteuer steuerelements zur Anwendung. Wird von der [**IMsRdpClient6-Schnittstelle**](imsrdpclient6.md) ableiten.

## <a name="members"></a>Member

Die **IMsRdpClient7-Schnittstelle** erbt von [**IMsRdpClient6**](imsrdpclient6.md). **IMsRdpClient7** verfügt auch über diese Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IMsRdpClient7-Schnittstelle** verfügt über diese Methoden.



| Methode                                               | Beschreibung                                                         |
|:-----------------------------------------------------|:--------------------------------------------------------------------|
| [**GetStatusText**](imsrdpclient7-getstatustext.md) | Ruft den Statustext für den angegebenen Statuscode ab.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClient7-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                  | Zugriffstyp          | Beschreibung                                                                                                                |
|:--------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings8**](imsrdpclient7-advancedsettings8.md)<br/>   | Schreibgeschützt<br/> | Ein Objekt, das die [**IMsRdpClientAdvancedSettings7-Schnittstelle**](imsrdpclientadvancedsettings7.md) unterstützt.<br/>   |
| [**RemoteProgram2**](imsrdpclient7-remoteprogram2.md)<br/>         | Schreibgeschützt<br/> | Ein Objekt, das die [**ITSRemoteProgram2-Schnittstelle**](itsremoteprogram2.md) unterstützt.<br/>                           |
| [**SecuredSettings3**](imsrdpclient7-securedsettings3.md)<br/>     | Schreibgeschützt<br/> | Ein Objekt, das die [**IMsRdpClientSecuredSettings2-Schnittstelle**](imsrdpclientsecuredsettings2.md) unterstützt.<br/>     |
| [**TransportSettings3**](imsrdpclient7-transportsettings3.md)<br/> | Schreibgeschützt<br/> | Ein Objekt, das die [**IMsRdpClientTransportSettings3-Schnittstelle**](imsrdpclienttransportsettings3.md) unterstützt.<br/> |



 

## <a name="remarks"></a>Hinweise

Die **IMsRdpClient7-Schnittstelle** wurde durch die folgenden Schnittstellen erweitert, und jede neue Schnittstelle erbt alle Methoden und Eigenschaften der vorherigen Schnittstellen:

-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Requirements for Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 ist als C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24 definiert.<br/> CLSID \_ MsRdpClient10NotSafeForScripting ist als A0C63C30-F08D-4AB4-907C-34905D770C7D definiert.<br/> CLSID \_ MsRdpClient7 ist als A9D7038D-B5ED-472E-9C47-94BEA90A5910 definiert.<br/> CLSID \_ MsRdpClient7NotSafeForScripting ist als 54D38BF7-B1EF-4479-9674-1BD6EA465258 definiert.<br/> CLSID \_ MsRdpClient8 ist als 5F681803-2900-4C43-A1CC-CF405404A676 definiert.<br/> CLSID \_ MsRdpClient8NotSafeForScripting ist als A3BC03A0-041D-42E3-AD22-882B7865C9C5 definiert.<br/> CLSID \_ MsRdpClient9 ist als 301B94BA-5D25-4A12-BFFE-3B6E7A616585 definiert.<br/> CLSID \_ MsRdpClient9NotSafeForScripting ist als 8B918B82-7985-4C24-89DF-C33AD2BBFBCD definiert.<br/> |
| IID<br/>                      | IID \_ IMsRdpClient7 ist als b2a5b5ce-3461-444a-91d4-add26d070638 definiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





