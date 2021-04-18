---
title: Imsrdpclient-Schnittstelle
description: Stellt die Methoden und Eigenschaften bereit, die zum Konfigurieren und Verwenden des Client Steuer Elements erforderlich sind. Wird von der imstscax-Schnittstelle abgeleitet.
ms.assetid: 6698c1d7-94d2-453c-96db-366113b95dd4
ms.tgt_platform: multiple
keywords:
- Imsrdpclient-Schnittstelle Remotedesktopdienste
- Imsrdpclient-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc6d3a1de6a6cd18004ff957ea0f8c4d7c23b14d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337491"
---
# <a name="imsrdpclient-interface"></a>Imsrdpclient-Schnittstelle

Stellt die Methoden und Eigenschaften bereit, die zum Konfigurieren und Verwenden des Client Steuer Elements erforderlich sind. Wird von der [**imstscax**](imstscax-interface.md) -Schnittstelle abgeleitet.

## <a name="members"></a>Member

Die **imsrdpclient** -Schnittstelle erbt von [**imstscax**](imstscax-interface.md). **Imsrdpclient** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **imsrdpclient** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                    | BESCHREIBUNG                                                         |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [**Getvirtualchanneloptions**](imsrdpclient-getvirtualchanneloptions.md) | Ruft die Optionen ab, die für einen virtuellen Kanal festgelegt wurden.<br/>         |
| [**RequestClose**](imsrdpclient-requestclose.md)                         | Fordert ein ordnungsgemäßes Herunterfahren des Client Steuer Elements an.<br/>      |
| [**Setvirtualchanneloptions**](imsrdpclient-setvirtualchanneloptions.md) | Legt die Optionen des virtuellen Kanals für das Client Steuerelement fest.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **imsrdpclient** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                             | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                               |
|:-------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Schreibgeschützt<br/>  | Ein Zeiger auf die [**imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md) -Schnittstelle, die verwendet wird, um erweiterte Einstellungen für das Client Steuerelement festzulegen.<br/> |
| [**ColorDepth**](imsrdpclient-colordepth.md)<br/>                             | Lesen/Schreiben<br/> | Farbtiefe des aktuellen Steuer Elements.<br/>                                                                                                                            |
| [**Extendeddisconnecverrat**](imsrdpclient-extendeddisconnectreason.md)<br/> | Schreibgeschützt<br/>  | Erweiterte Informationen über den Grund für das Trennen der Verbindung des Client Steuer Elements.<br/>                                                                                      |
| [**FullScreen**](imsrdpclient-fullscreen.md)<br/>                             | Lesen/Schreiben<br/> | Gibt an, ob sich das Steuerelement im Vollbildmodus befindet.<br/>                                                                                                          |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Schreibgeschützt<br/>  | Ein Zeiger auf die [**imsrdpclientsecuredsettings**](imsrdpclientsecuredsettings-interface.md) -Schnittstelle, die verwendet wird, um gesicherte Einstellungen für das Client Steuerelement festzulegen.<br/>    |



 

## <a name="remarks"></a>Bemerkungen

Die **imsrdpclient** -Schnittstelle wurde durch die folgenden Schnittstellen erweitert, wobei jede neue Schnittstelle alle Methoden und Eigenschaften der vorherigen Schnittstellen erbt:

-   [**IMsRdpClient2**](imsrdpclient2.md)
-   [**IMsRdpClient3**](imsrdpclient3.md)
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
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| CLSID<br/>                    | CLSID \_ MsRdpClient ist als 791fa017-2de3-492e-acc5-53c67a2b94d0 definiert.<br/> CLSID- \_ MsRdpClient10 ist als C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24 definiert.<br/> CLSID- \_ MsRdpClient10NotSafeForScripting ist als A0C63C30-F08D-4AB4-907C-34905D770C7D definiert.<br/> Die CLSID- \_ MsRdpClient2 ist als 9059-Datei mit dem Namen "" definiert.<br/> CLSID \_ MsRdpClient2a ist als 971127bb-259f-48c2-bd75-5f97a3331551 definiert<br/> CLSID \_ MsRdpClient2NotSafeForScripting ist als 3523c2b-4031-44e4-9a3b-f 1e94986ee7f definiert.<br/> CLSID \_ MsRdpClient3 ist als 7584c670-2274-4efb-B00B-d6aaba6d3850 definiert.<br/> CLSID \_ MsRdpClient3a ist als 6a6f 4B83-45c5-4ca9-bdd9-0d81c12295e4 definiert.<br/> CLSID \_ MsRdpClient3NotSafeForScripting ist als ACE575FD-1F-4074-9401-EBAB990FA9DE definiert.<br/> CLSID \_ MsRdpClient4 ist als 4edcb26c-d24c-4e72-af07-b576699ac0de definiert.<br/> CLSID \_ MsRdpClient4a ist als 54ce37e0-9834-41ae-9896-4dab69dc022b definiert.<br/> CLSID \_ MsRdpClient4NotSafeForScripting ist als 6ae29350-321b-42be-bbe5-12b5270c0de definiert.<br/> CLSID \_ MsRdpClient5 ist als 4eb89ff4-7f78-4a0f-8b8d-2bf02e94e4b2 definiert.<br/> CLSID \_ MsRdpClient5NotSafeForScripting ist als 4eb2f 086-C818-447e-b32c-c51ce2b30d31 definiert.<br/> CLSID \_ MsRdpClient6 ist als 7390f3d8-0439-4c05-91E3-cf5cb290c3d0 definiert.<br/> CLSID- \_ MsRdpClient6NotSafeForScripting ist als D2EA46A7-C2BF-426B-AF24-E19C44456399 definiert.<br/> CLSID- \_ MsRdpClient7 ist als A9D7038D-B5ED-472E-9C47-94BEA90A5910 definiert.<br/> CLSID \_ MsRdpClient7NotSafeForScripting ist als 54d38bf 7-b1ef-4479-9674-1bd6ea465258 definiert.<br/> CLSID \_ MsRdpClient8 ist als 5f681803-2900-4c43-a1cc-cf405404a676 definiert.<br/> CLSID- \_ MsRdpClient8NotSafeForScripting ist als A3BC03A0-041D-42E3-AD22-882B7865C9C5 definiert.<br/> CLSID \_ MsRdpClient9 ist als 301b94ba-5d25-4a12-bffe-3b6e7a616585 definiert<br/> CLSID \_ MsRdpClient9NotSafeForScripting ist als 8b918b82-7985-4c24-89df-c33ad2bbfbcd definiert.<br/> Die CLSID \_ msrdpclientnozafeforscripting ist als 7cacbd7b-0d99-468f-ac33-22e495c0afe5 definiert.<br/> CLSID \_ mstscax ist als 1sb464c8-09bb-4017-A2F5-EB742F04392F definiert.<br/> CLSID \_ mstscaxnozafeforscripting ist als A41A4187-5A86-4E26-B40A-856F9035D9CB definiert.<br/> |
| IID<br/>                      | IID \_ imsrdpclient ist als 92b4a539-7115-4b7c-a5a9-e5d9efc2780a definiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imstscax**](imstscax-interface.md)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





