---
title: IMsRdpClient3-Schnittstelle
description: Stellt die Methoden und Eigenschaften bereit, die zum Konfigurieren und Verwenden des Client Steuer Elements erforderlich sind. Wird von der IMsRdpClient2-Schnittstelle abgeleitet.
ms.assetid: 31e52de1-1fb0-47ef-aad5-fd06621f2b3c
ms.tgt_platform: multiple
keywords:
- IMsRdpClient3-Schnittstelle Remotedesktopdienste
- IMsRdpClient3 Interface Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: 6911f839a26aae67fbc1e57494e5a75291721663
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479113"
---
# <a name="imsrdpclient3-interface"></a>IMsRdpClient3-Schnittstelle

Stellt die Methoden und Eigenschaften bereit, die zum Konfigurieren und Verwenden des Client Steuer Elements erforderlich sind. Wird von der [**IMsRdpClient2**](imsrdpclient2.md) -Schnittstelle abgeleitet.

## <a name="members"></a>Member

Die **IMsRdpClient3** -Schnittstelle erbt von [**IMsRdpClient2**](imsrdpclient2.md). **IMsRdpClient3** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClient3** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                       |
|:------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/> | Schreibgeschützt<br/> | Zeiger auf die [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) -Schnittstelle, die verwendet wird, um erweiterte Einstellungen für das Client Steuerelement festzulegen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die **IMsRdpClient3** -Schnittstelle wurde durch die folgenden Schnittstellen erweitert, wobei jede neue Schnittstelle alle Methoden und Eigenschaften der vorherigen Schnittstellen erbt:

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
| CLSID<br/>                    | CLSID- \_ MsRdpClient10 ist als C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24 definiert.<br/> CLSID- \_ MsRdpClient10NotSafeForScripting ist als A0C63C30-F08D-4AB4-907C-34905D770C7D definiert.<br/> CLSID \_ MsRdpClient3 ist als 7584c670-2274-4efb-B00B-d6aaba6d3850 definiert.<br/> CLSID \_ MsRdpClient3a ist als 6a6f 4B83-45c5-4ca9-bdd9-0d81c12295e4 definiert.<br/> CLSID \_ MsRdpClient3NotSafeForScripting ist als ACE575FD-1F-4074-9401-EBAB990FA9DE definiert.<br/> CLSID \_ MsRdpClient4 ist als 4edcb26c-d24c-4e72-af07-b576699ac0de definiert.<br/> CLSID \_ MsRdpClient4a ist als 54ce37e0-9834-41ae-9896-4dab69dc022b definiert.<br/> CLSID \_ MsRdpClient4NotSafeForScripting ist als 6ae29350-321b-42be-bbe5-12b5270c0de definiert.<br/> CLSID \_ MsRdpClient5 ist als 4eb89ff4-7f78-4a0f-8b8d-2bf02e94e4b2 definiert.<br/> CLSID \_ MsRdpClient5NotSafeForScripting ist als 4eb2f 086-C818-447e-b32c-c51ce2b30d31 definiert.<br/> CLSID \_ MsRdpClient6 ist als 7390f3d8-0439-4c05-91E3-cf5cb290c3d0 definiert.<br/> CLSID- \_ MsRdpClient6NotSafeForScripting ist als D2EA46A7-C2BF-426B-AF24-E19C44456399 definiert.<br/> CLSID- \_ MsRdpClient7 ist als A9D7038D-B5ED-472E-9C47-94BEA90A5910 definiert.<br/> CLSID \_ MsRdpClient7NotSafeForScripting ist als 54d38bf 7-b1ef-4479-9674-1bd6ea465258 definiert.<br/> CLSID \_ MsRdpClient8 ist als 5f681803-2900-4c43-a1cc-cf405404a676 definiert.<br/> CLSID- \_ MsRdpClient8NotSafeForScripting ist als A3BC03A0-041D-42E3-AD22-882B7865C9C5 definiert.<br/> CLSID \_ MsRdpClient9 ist als 301b94ba-5d25-4a12-bffe-3b6e7a616585 definiert<br/> CLSID \_ MsRdpClient9NotSafeForScripting ist als 8b918b82-7985-4c24-89df-c33ad2bbfbcd definiert.<br/> |
| IID<br/>                      | IID \_ IMsRdpClient3 ist als 91b7cbc5-a72e-4fa0-9300-d647d7e897ff definiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**Imsrdpclient**](imsrdpclient-interface.md)
</dt> <dt>

[**Imstscax**](imstscax-interface.md)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





