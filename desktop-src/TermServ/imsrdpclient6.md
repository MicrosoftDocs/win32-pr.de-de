---
title: IMsRdpClient6-Schnittstelle
description: Stellt die Methoden und Eigenschaften zur Konfiguration und Verwendung des Clientsteuer steuerelements zur Anwendung. Wird von der IMsRdpClient5-Schnittstelle ableiten.
ms.assetid: 97ec885f-1c55-4293-84d0-2d1d804a9df8
ms.tgt_platform: multiple
keywords:
- IMsRdpClient6-Remotedesktopdienste
- IMsRdpClient6-Schnittstelle Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClient6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4bbf8fb9cc532b1968b8fba99b62e49feaf4538fd618018666d0338736cc04d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138913"
---
# <a name="imsrdpclient6-interface"></a>IMsRdpClient6-Schnittstelle

Stellt die Methoden und Eigenschaften zur Konfiguration und Verwendung des Clientsteuer steuerelements zur Anwendung. Wird von der [**IMsRdpClient5-Schnittstelle**](imsrdpclient5.md) ableiten.

## <a name="members"></a>Member

Die **IMsRdpClient6-Schnittstelle** erbt von [**IMsRdpClient5**](imsrdpclient5.md). **IMsRdpClient6** verfügt auch über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClient6-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                  | Zugriffstyp          | Beschreibung                                                                                           |
|:--------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings7**](imsrdpclient6-advancedsettings7.md)<br/>   | Schreibgeschützt<br/> | Die Schnittstelle zu [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md).<br/>   |
| [**TransportSettings2**](imsrdpclient6-transportsettings2.md)<br/> | Schreibgeschützt<br/> | Die Schnittstelle zu [**IMsRdpClientTransportSettings2.**](imsrdpclienttransportsettings2.md)<br/> |



 

## <a name="remarks"></a>Hinweise

Die **IMsRdpClient6-Schnittstelle** wurde durch die folgenden Schnittstellen erweitert, und jede neue Schnittstelle erbt alle Methoden und Eigenschaften der vorherigen Schnittstellen:

-   [**IMsRdpClient7**](imsrdpclient7.md)
-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Requirements for Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista mit SP1<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 ist als C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24 definiert.<br/> CLSID \_ MsRdpClient10NotSafeForScripting ist als A0C63C30-F08D-4AB4-907C-34905D770C7D definiert.<br/> CLSID \_ MsRdpClient6 ist als 7390F3D8-0439-4C05-91E3-CF5CB290C3D0 definiert.<br/> CLSID \_ MsRdpClient6NotSafeForScripting ist als D2EA46A7-C2BF-426B-AF24-E19C44456399 definiert.<br/> CLSID \_ MsRdpClient7 ist als A9D7038D-B5ED-472E-9C47-94BEA90A5910 definiert.<br/> CLSID \_ MsRdpClient7NotSafeForScripting ist als 54D38BF7-B1EF-4479-9674-1BD6EA465258 definiert.<br/> CLSID \_ MsRdpClient8 ist als 5F681803-2900-4C43-A1CC-CF405404A676 definiert.<br/> CLSID \_ MsRdpClient8NotSafeForScripting ist als A3BC03A0-041D-42E3-AD22-882B7865C9C5 definiert.<br/> CLSID \_ MsRdpClient9 ist als 301B94BA-5D25-4A12-BFFE-3B6E7A616585 definiert.<br/> CLSID \_ MsRdpClient9NotSafeForScripting ist als 8B918B82-7985-4C24-89DF-C33AD2BBFBCD definiert.<br/> |
| IID<br/>                      | IID \_ IMsRdpClient6 ist als d43b7d80-8517-4b6d-9eac-96ad6800d7f2 definiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

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

 

 





