---
title: IMsRdpClientNonScriptable2-Schnittstelle
description: Bietet Zugriff auf die nicht Skript fähigen Eigenschaften der Remote Sitzung eines Clients auf dem Remotedesktop ActiveX-Steuerelement. Wird von der imsrdpclientnonscriptable-Schnittstelle abgeleitet.
ms.assetid: 06a5ffc9-3c9e-44d6-a5b5-9ccb7488deff
ms.tgt_platform: multiple
keywords:
- IMsRdpClientNonScriptable2-Schnittstelle Remotedesktopdienste
- IMsRdpClientNonScriptable2 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f840b506ee0aa738a63df888b64c6384d4def1ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345933"
---
# <a name="imsrdpclientnonscriptable2-interface"></a>IMsRdpClientNonScriptable2-Schnittstelle

Bietet Zugriff auf die nicht Skript fähigen Eigenschaften der Remote Sitzung eines Clients auf dem Remotedesktop ActiveX-Steuerelement. Wird von der [**imsrdpclientnonscriptable**](imsrdpclientnonscriptable-interface.md) -Schnittstelle abgeleitet. Auf Methoden dieser Schnittstelle kann nur über die Vtable zugegriffen werden. Sie sind nicht zur Verwendung mit Skript fähigen Clients verfügbar.

## <a name="members"></a>Member

Die **IMsRdpClientNonScriptable2** -Schnittstelle erbt von [**imsrdpclientnonscriptable**](imsrdpclientnonscriptable-interface.md). **IMsRdpClientNonScriptable2** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientNonScriptable2** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                                   | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Uianentwindowhandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)<br/> | Lesen/Schreiben<br/> | Das Fenster Handle, das das übergeordnete Fenster für das-Steuerelement sein soll. Dadurch können alle Fenster, die vom Steuerelement angezeigt werden, in Bezug auf alle Fenster, die von der übergeordneten Anwendung angezeigt werden, ordnungsgemäß modal sein.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle wurde durch die folgenden Schnittstellen erweitert, wobei jede neue Schnittstelle alle Methoden und Eigenschaften der vorherigen Schnittstellen erbt:

-   [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
-   [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
-   [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008, Windows Server 2008 mit SP1<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| CLSID<br/>                    | CLSID- \_ MsRdpClient10 ist als C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24 definiert.<br/> CLSID- \_ MsRdpClient10NotSafeForScripting ist als A0C63C30-F08D-4AB4-907C-34905D770C7D definiert.<br/> CLSID \_ MsRdpClient4 ist als 4edcb26c-d24c-4e72-af07-b576699ac0de definiert.<br/> CLSID \_ MsRdpClient4a ist als 54ce37e0-9834-41ae-9896-4dab69dc022b definiert.<br/> CLSID \_ MsRdpClient4NotSafeForScripting ist als 6ae29350-321b-42be-bbe5-12b5270c0de definiert.<br/> CLSID \_ MsRdpClient5 ist als 4eb89ff4-7f78-4a0f-8b8d-2bf02e94e4b2 definiert.<br/> CLSID \_ MsRdpClient5NotSafeForScripting ist als 4eb2f 086-C818-447e-b32c-c51ce2b30d31 definiert.<br/> CLSID \_ MsRdpClient6 ist als 7390f3d8-0439-4c05-91E3-cf5cb290c3d0 definiert.<br/> CLSID- \_ MsRdpClient6NotSafeForScripting ist als D2EA46A7-C2BF-426B-AF24-E19C44456399 definiert.<br/> CLSID- \_ MsRdpClient7 ist als A9D7038D-B5ED-472E-9C47-94BEA90A5910 definiert.<br/> CLSID \_ MsRdpClient7NotSafeForScripting ist als 54d38bf 7-b1ef-4479-9674-1bd6ea465258 definiert.<br/> CLSID \_ MsRdpClient8 ist als 5f681803-2900-4c43-a1cc-cf405404a676 definiert.<br/> CLSID- \_ MsRdpClient8NotSafeForScripting ist als A3BC03A0-041D-42E3-AD22-882B7865C9C5 definiert.<br/> CLSID \_ MsRdpClient9 ist als 301b94ba-5d25-4a12-bffe-3b6e7a616585 definiert<br/> CLSID \_ MsRdpClient9NotSafeForScripting ist als 8b918b82-7985-4c24-89df-c33ad2bbfbcd definiert.<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable2 ist als 17a5e535-4072-4fa4-af32-c8d0d47345e9 definiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpclientnonscriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**Imstscnonscriptable**](imstscnonscriptable-interface.md)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





