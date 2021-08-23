---
title: IMsRdpClient3-Schnittstelle
description: Stellt die Methoden und Eigenschaften bereit, die zum Konfigurieren und Verwenden des Clientsteuerelements erforderlich sind. Wird von der IMsRdpClient2-Schnittstelle abgeleitet.
ms.assetid: 31e52de1-1fb0-47ef-aad5-fd06621f2b3c
ms.tgt_platform: multiple
keywords:
- IMsRdpClient3-Schnittstelle Remotedesktopdienste
- IMsRdpClient3-Schnittstelle Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClient3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 444f022c2f4db57c1c62f1405b30625bf7fed291674255ed6287026c9451e825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059008"
---
# <a name="imsrdpclient3-interface"></a>IMsRdpClient3-Schnittstelle

Stellt die Methoden und Eigenschaften bereit, die zum Konfigurieren und Verwenden des Clientsteuerelements erforderlich sind. Wird von der [**IMsRdpClient2-Schnittstelle**](imsrdpclient2.md) abgeleitet.

## <a name="members"></a>Member

Die **IMsRdpClient3-Schnittstelle** erbt von [**IMsRdpClient2.**](imsrdpclient2.md) **IMsRdpClient3** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClient3-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                | Zugriffstyp          | Beschreibung                                                                                                                                                       |
|:------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/> | Schreibgeschützt<br/> | Zeiger auf die [**IMsRdpClientAdvancedSettings3-Schnittstelle,**](imsrdpclientadvancedsettings3.md) die zum Festlegen erweiterter Einstellungen für das Clientsteuerelement verwendet wird.<br/> |



 

## <a name="remarks"></a>Hinweise

Die **IMsRdpClient3-Schnittstelle** wurde durch die folgenden Schnittstellen erweitert, wobei jede neue Schnittstelle alle Methoden und Eigenschaften der vorherigen Schnittstellen erbt:

-   [**IMsRdpClient4**](imsrdpclient4.md)
-   [**IMsRdpClient5**](imsrdpclient5.md)
-   [**IMsRdpClient6**](imsrdpclient6.md)
-   [**IMsRdpClient7**](imsrdpclient7.md)
-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 ist als C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24 definiert.<br/> CLSID \_ MsRdpClient10NotSafeForScripting ist als A0C63C30-F08D-4AB4-907C-34905D770C7D definiert.<br/> CLSID \_ MsRdpClient3 ist als 7584C670-2274-4EFB-B00B-D6AABA6D3850 definiert.<br/> CLSID \_ MsRdpClient3a ist als 6A6F4B83-45C5-4CA9-BDD9-0D81C12295E4 definiert.<br/> CLSID \_ MsRdpClient3NotSafeForScripting ist als ACE575FD-1FCF-4074-9401-EBAB990FA9DE definiert.<br/> CLSID \_ MsRdpClient4 ist als 4EDCB26C-D24C-4E72-AF07-B576699AC0DE definiert.<br/> CLSID \_ MsRdpClient4a ist als 54CE37E0-9834-41AE-9896-4DAB69DC022B definiert.<br/> CLSID \_ MsRdpClient4NotSafeForScripting ist als 6AE29350-321B-42BE-BBE5-12FB5270C0DE definiert.<br/> CLSID \_ MsRdpClient5 ist als 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2 definiert.<br/> CLSID \_ MsRdpClient5NotSafeForScripting ist als 4EB2F086-C818-447E-B32C-C51CE2B30D31 definiert.<br/> CLSID \_ MsRdpClient6 ist als 7390F3D8-0439-4C05-91E3-CF5CB290C3D0 definiert.<br/> CLSID \_ MsRdpClient6NotSafeForScripting ist als D2EA46A7-C2BF-426B-AF24-E19C44456399 definiert.<br/> CLSID \_ MsRdpClient7 ist als A9D7038D-B5ED-472E-9C47-94BEA90A5910 definiert.<br/> CLSID \_ MsRdpClient7NotSafeForScripting ist als 54D38BF7-B1EF-4479-9674-1BD6EA465258 definiert.<br/> CLSID \_ MsRdpClient8 ist als 5F681803-2900-4C43-A1CC-CF405404A676 definiert.<br/> CLSID \_ MsRdpClient8NotSafeForScripting ist als A3BC03A0-041D-42E3-AD22-882B7865C9C5 definiert.<br/> CLSID \_ MsRdpClient9 ist als 301B94BA-5D25-4A12-BFFE-3B6E7A616585 definiert.<br/> CLSID \_ MsRdpClient9NotSafeForScripting ist als 8B918B82-7985-4C24-89DF-C33AD2BBFBCD definiert.<br/> |
| IID<br/>                      | IID \_ IMsRdpClient3 ist als 91b7cbc5-a72e-4fa0-9300-d647d7e897ff definiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[Remotedesktop-Webverbindung-Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





