---
title: Imstscnonscriptable-Schnittstelle
description: Enthält Eigenschaften und Methoden, die sich auf die Anwendung eines Kennworts für das Remotedesktop ActiveX-Steuerelement beziehen.
ms.assetid: b4a68e02-cce6-4fbe-98b4-0627c10f3f37
ms.tgt_platform: multiple
keywords:
- Imstscnonscriptable-Schnittstelle Remotedesktopdienste
- Imstscnonscriptable-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsTscNonScriptable
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92372f7ea9479f7fcdd632546a0bd7dd2f0b465e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340978"
---
# <a name="imstscnonscriptable-interface"></a>Imstscnonscriptable-Schnittstelle

Enthält Eigenschaften und Methoden, die sich auf die Anwendung eines Kennworts für das Remotedesktop ActiveX-Steuerelement beziehen.

Die **imstscnonscriptable** -Schnittstelle wird hauptsächlich verwendet, um den automatischen Anmelde Zugriff auf Remotedesktop-Sitzungshost (RD-Sitzungshost)-Servern in Szenarios zu konfigurieren, in denen das Remotedesktop ActiveX-Steuerelement in einem benutzerdefinierten Container gehostet wird. Wenn die automatische Anmeldung konfiguriert ist, erhält der Benutzer beim Verbindungs Zeitpunkt nicht das Windows-Anmelde Dialogfeld.

Auf einigen Plattformen können die Methoden der **imstscnonscriptable** -Schnittstelle verwendet werden, um Kenn Wörter in einem von drei unterstützten Formaten anzugeben:

-   Klartext
-   Portabel codiert
-   Binäre (nicht portabel) codiert

Beachten Sie, dass ein Kennwort in einem codierten Format aus zwei Teilen besteht:

-   Codiertes Kenn Wort Part.
-   Salt-Wert Teil.

Beide Teile sind erforderlich, um ein codiertes Kennwort festzulegen. Weder der Teil des codierten Kennworts noch der Salt-Wert muss als sicher verschlüsselt angesehen werden.

Der Skript fähige-Zugriff auf Klartext-Kenn Wörter ist über die [**cleartextpassword**](imsrdpclientadvancedsettings-cleartextpassword.md) -Eigenschaft der Skript fähige-Schnittstelle [**imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md)verfügbar.

Auf die **imstscnonscriptable** -Schnittstelle kann nur über die Vtable zugegriffen werden.

## <a name="members"></a>Member

Die **imstscnonscriptable** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Imstscnonscriptable** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **imstscnonscriptable** -Schnittstelle verfügt über diese Methoden.



| Methode                                                     | BESCHREIBUNG                                           |
|:-----------------------------------------------------------|:------------------------------------------------------|
| [**ResetPassword**](imstscnonscriptable-resetpassword.md) | Setzt alle Kenn Wort Zustände im-Steuerelement zurück.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **imstscnonscriptable** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                      | Zugriffstyp           | BESCHREIBUNG                                                                  |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------|
| [**Binarypassword**](imstscnonscriptable-binarypassword.md)<br/>       | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht unterstützt.<br/>                                   |
| [**Binarysalt**](imstscnonscriptable-binarysalt.md)<br/>               | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht unterstützt.<br/>                                   |
| [**Cleartextpassword**](imstscnonscriptable-cleartextpassword.md)<br/> | Lesegeschützt<br/> | Das Remotedesktop ActiveX-Steuerelement Kennwort im nur-Text-Format.<br/> |
| [**Portablepassword**](imstscnonscriptable-portablepassword.md)<br/>   | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht unterstützt.<br/>                                   |
| [**Portablesalt**](imstscnonscriptable-portablesalt.md)<br/>           | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht unterstützt.<br/>                                   |



 

## <a name="remarks"></a>Bemerkungen

Die Angabe eines Kennworts für das Remotedesktop ActiveX-Steuerelement ist optional. Wenn Sie ein Kennwort für das-Steuerelement angeben, sollten Sie nur eines der vorangehenden drei Formate auf das-Steuerelement anwenden, bevor Sie die Verbindung mit einem Rückruf der [**Connect**](imstscax-connect.md) -Methode initiieren.

> [!Note]  
> Sie können auch die automatische Anmeldung auf dem Server mit dem Remotedesktopdienste-Konfigurationstool (TSCC. msc) aktivieren. ein Administrator kann dieses Tool verwenden, um eine Verbindung in einer Situation, in der eine automatisierte Anmeldung erforderlich ist, einem bestimmten Kennwort zuzuweisen.

 

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

Die **imstscnonscriptable** -Schnittstelle wurde durch die folgenden Schnittstellen erweitert, wobei jede neue Schnittstelle alle Methoden und Eigenschaften der vorherigen Schnittstellen erbt:

-   [**Imsrdpclientnonscriptable**](imsrdpclientnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
-   [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
-   [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
-   [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| CLSID<br/>                    | CLSID \_ MsRdpClient ist als 791fa017-2de3-492e-acc5-53c67a2b94d0 definiert.<br/> CLSID- \_ MsRdpClient10 ist als C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24 definiert.<br/> CLSID- \_ MsRdpClient10NotSafeForScripting ist als A0C63C30-F08D-4AB4-907C-34905D770C7D definiert.<br/> Die CLSID- \_ MsRdpClient2 ist als 9059-Datei mit dem Namen "" definiert.<br/> CLSID \_ MsRdpClient2a ist als 971127bb-259f-48c2-bd75-5f97a3331551 definiert<br/> CLSID \_ MsRdpClient2NotSafeForScripting ist als 3523c2b-4031-44e4-9a3b-f 1e94986ee7f definiert.<br/> CLSID \_ MsRdpClient3 ist als 7584c670-2274-4efb-B00B-d6aaba6d3850 definiert.<br/> CLSID \_ MsRdpClient3a ist als 6a6f 4B83-45c5-4ca9-bdd9-0d81c12295e4 definiert.<br/> CLSID \_ MsRdpClient3NotSafeForScripting ist als ACE575FD-1F-4074-9401-EBAB990FA9DE definiert.<br/> CLSID \_ MsRdpClient4 ist als 4edcb26c-d24c-4e72-af07-b576699ac0de definiert.<br/> CLSID \_ MsRdpClient4a ist als 54ce37e0-9834-41ae-9896-4dab69dc022b definiert.<br/> CLSID \_ MsRdpClient4NotSafeForScripting ist als 6ae29350-321b-42be-bbe5-12b5270c0de definiert.<br/> CLSID \_ MsRdpClient5 ist als 4eb89ff4-7f78-4a0f-8b8d-2bf02e94e4b2 definiert.<br/> CLSID \_ MsRdpClient5NotSafeForScripting ist als 4eb2f 086-C818-447e-b32c-c51ce2b30d31 definiert.<br/> CLSID \_ MsRdpClient6 ist als 7390f3d8-0439-4c05-91E3-cf5cb290c3d0 definiert.<br/> CLSID- \_ MsRdpClient6NotSafeForScripting ist als D2EA46A7-C2BF-426B-AF24-E19C44456399 definiert.<br/> CLSID- \_ MsRdpClient7 ist als A9D7038D-B5ED-472E-9C47-94BEA90A5910 definiert.<br/> CLSID \_ MsRdpClient7NotSafeForScripting ist als 54d38bf 7-b1ef-4479-9674-1bd6ea465258 definiert.<br/> CLSID \_ MsRdpClient8 ist als 5f681803-2900-4c43-a1cc-cf405404a676 definiert.<br/> CLSID- \_ MsRdpClient8NotSafeForScripting ist als A3BC03A0-041D-42E3-AD22-882B7865C9C5 definiert.<br/> CLSID \_ MsRdpClient9 ist als 301b94ba-5d25-4a12-bffe-3b6e7a616585 definiert<br/> CLSID \_ MsRdpClient9NotSafeForScripting ist als 8b918b82-7985-4c24-89df-c33ad2bbfbcd definiert.<br/> Die CLSID \_ msrdpclientnozafeforscripting ist als 7cacbd7b-0d99-468f-ac33-22e495c0afe5 definiert.<br/> CLSID \_ mstscax ist als 1sb464c8-09bb-4017-A2F5-EB742F04392F definiert.<br/> CLSID \_ mstscaxnozafeforscripting ist als A41A4187-5A86-4E26-B40A-856F9035D9CB definiert.<br/> |
| IID<br/>                      | IID \_ imstscnonscriptable ist als C1E6743A-41C1-4A74-832A-0DD06C1C7A0E definiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**Imstscax:: Connect**](imstscax-connect.md)
</dt> </dl>

 

