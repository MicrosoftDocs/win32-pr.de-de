---
title: IMsRdpClient4-Schnittstelle
description: Stellt die Methoden und Eigenschaften bereit, die zum Konfigurieren und Verwenden des Clientsteuerelements erforderlich sind. Wird von der IMsRdpClient3-Schnittstelle abgeleitet.
ms.assetid: c3382a86-f044-4924-b69b-5907f2506eb6
ms.tgt_platform: multiple
keywords:
- IMsRdpClient4-Schnittstelle Remotedesktopdienste
- IMsRdpClient4-Schnittstelle Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClient4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ac9660384e15827b3a1bc6949e448ff2f9ce99c3d034de02c86a3831cc219ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475590"
---
# <a name="imsrdpclient4-interface"></a>IMsRdpClient4-Schnittstelle

Stellt die Methoden und Eigenschaften bereit, die zum Konfigurieren und Verwenden des Clientsteuerelements erforderlich sind. Wird von der [**IMsRdpClient3-Schnittstelle**](imsrdpclient3.md) abgeleitet.

## <a name="members"></a>Member

Die **IMsRdpClient4-Schnittstelle** erbt von [**IMsRdpClient3.**](imsrdpclient3.md) **IMsRdpClient4** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClient4-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                | Zugriffstyp          | Beschreibung                                                                                             |
|:------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings5**](imsrdpclient4-advancedsettings5.md)<br/> | Schreibgeschützt<br/> | Ein [**IMsRdpClientAdvancedSettings4-Schnittstellenzeiger.**](imsrdpclientadvancedsettings4.md)<br/> |



 

## <a name="remarks"></a>Hinweise

Die **IMsRdpClient4-Schnittstelle** wurde durch die folgenden Schnittstellen erweitert, wobei jede neue Schnittstelle alle Methoden und Eigenschaften der vorherigen Schnittstellen erbt:

-   [**IMsRdpClient5**](imsrdpclient5.md)
-   [**IMsRdpClient6**](imsrdpclient6.md)
-   [**IMsRdpClient7**](imsrdpclient7.md)
-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 ist als C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24 definiert.<br/> CLSID \_ MsRdpClient10NotSafeForScripting ist als A0C63C30-F08D-4AB4-907C-34905D770C7D definiert.<br/> CLSID \_ MsRdpClient4 ist als 4EDCB26C-D24C-4E72-AF07-B576699AC0DE definiert.<br/> CLSID \_ MsRdpClient4a ist als 54CE37E0-9834-41AE-9896-4DAB69DC022B definiert.<br/> CLSID \_ MsRdpClient4NotSafeForScripting ist als 6AE29350-321B-42BE-BBE5-12FB5270C0DE definiert.<br/> CLSID \_ MsRdpClient5 ist als 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2 definiert.<br/> CLSID \_ MsRdpClient5NotSafeForScripting ist als 4EB2F086-C818-447E-B32C-C51CE2B30D31 definiert.<br/> CLSID \_ MsRdpClient6 ist als 7390F3D8-0439-4C05-91E3-CF5CB290C3D0 definiert.<br/> CLSID \_ MsRdpClient6NotSafeForScripting ist als D2EA46A7-C2BF-426B-AF24-E19C44456399 definiert.<br/> CLSID \_ MsRdpClient7 ist als A9D7038D-B5ED-472E-9C47-94BEA90A5910 definiert.<br/> CLSID \_ MsRdpClient7NotSafeForScripting ist als 54D38BF7-B1EF-4479-9674-1BD6EA465258 definiert.<br/> CLSID \_ MsRdpClient8 ist als 5F681803-2900-4C43-A1CC-CF405404A676 definiert.<br/> CLSID \_ MsRdpClient8NotSafeForScripting ist als A3BC03A0-041D-42E3-AD22-882B7865C9C5 definiert.<br/> CLSID \_ MsRdpClient9 ist als 301B94BA-5D25-4A12-BFFE-3B6E7A616585 definiert.<br/> CLSID \_ MsRdpClient9NotSafeForScripting ist als 8B918B82-7985-4C24-89DF-C33AD2BBFBCD definiert.<br/> |
| IID<br/>                      | IID \_ IMsRdpClient4 ist als 095E0738-D97D-488b-B9F6-DD0E8D66C0DE definiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[Remotedesktop-Webverbindung-Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





