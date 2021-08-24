---
title: IMsTscNonScriptable-Schnittstelle
description: Enthält Eigenschaften und Methoden, die sich auf die Anwendung eines Kennworts auf das Remotedesktop ActiveX-Steuerelement beziehen.
ms.assetid: b4a68e02-cce6-4fbe-98b4-0627c10f3f37
ms.tgt_platform: multiple
keywords:
- IMsTscNonScriptable-Schnittstelle Remotedesktopdienste
- IMsTscNonScriptable-Schnittstelle Remotedesktopdienste beschrieben
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
ms.openlocfilehash: 86ce3b1e921635850e9ffa713c55a812a806ac4e757e772569e7db817410ad3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770650"
---
# <a name="imstscnonscriptable-interface"></a>IMsTscNonScriptable-Schnittstelle

Enthält Eigenschaften und Methoden, die sich auf die Anwendung eines Kennworts auf das Remotedesktop ActiveX-Steuerelement beziehen.

Die **IMsTscNonScriptable-Schnittstelle** wird hauptsächlich verwendet, um den automatischen Kennwortanmeldezugriff auf Remotedesktop-Sitzungshost -Server (RD-Sitzungshost) in Szenarien zu konfigurieren, in denen das Remotedesktop ActiveX-Steuerelement in einem benutzerdefinierten Container gehostet wird. Wenn die automatische Anmeldung konfiguriert ist, empfängt der Benutzer zum Zeitpunkt der Verbindung nicht das Dialogfeld Windows Anmeldung.

Auf einigen Plattformen können die Methoden der **IMsTscNonScriptable-Schnittstelle** verwendet werden, um Kennwörter in einem von drei unterstützten Formaten anzugeben:

-   Klartext
-   Portierbar codiert
-   Binär (nicht portierbar) codiert

Beachten Sie, dass ein Kennwort in einem codierten Format aus zwei Teilen besteht:

-   Codierter Kennwortteil.
-   Salt-Wertteil.

Beide Teile sind erforderlich, um ein codiertes Kennwort festzulegen. Weder der codierte Kennwortteil noch der Salt-Wertteil sollten als sicher verschlüsselt betrachtet werden.

Skriptfähiger Zugriff auf Klartextkennwörter ist über die [**ClearTextPassword-Eigenschaft**](imsrdpclientadvancedsettings-cleartextpassword.md) der skriptfähigen Schnittstelle [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)verfügbar.

Auf **die IMsTscNonScriptable-Schnittstelle** kann nur über die vtable zugegriffen werden.

## <a name="members"></a>Member

Die **IMsTscNonScriptable-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMsTscNonScriptable** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IMsTscNonScriptable-Schnittstelle** verfügt über diese Methoden.



| Methode                                                     | Beschreibung                                           |
|:-----------------------------------------------------------|:------------------------------------------------------|
| [**Resetpassword**](imstscnonscriptable-resetpassword.md) | Setzt alle Kennwortzustände im Steuerelement zurück.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **IMsTscNonScriptable-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                      | Zugriffstyp           | Beschreibung                                                                  |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------|
| [**BinaryPassword**](imstscnonscriptable-binarypassword.md)<br/>       | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht unterstützt.<br/>                                   |
| [**BinarySalt**](imstscnonscriptable-binarysalt.md)<br/>               | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht unterstützt.<br/>                                   |
| [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md)<br/> | Lesegeschützt<br/> | Der Remotedesktop ActiveX Steuerelementkennwort im Klartextformat.<br/> |
| [**PortablePassword**](imstscnonscriptable-portablepassword.md)<br/>   | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht unterstützt.<br/>                                   |
| [**PortableSalt**](imstscnonscriptable-portablesalt.md)<br/>           | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht unterstützt.<br/>                                   |



 

## <a name="remarks"></a>Hinweise

Die Angabe eines Kennworts für das Remotedesktop ActiveX-Steuerelement ist optional. Wenn Sie ein Kennwort für das Steuerelement angeben, sollten Sie nur eines der vorherigen drei Formate auf das Steuerelement anwenden, bevor Sie die Verbindung mit einem Aufruf der [**Verbinden-Methode**](imstscax-connect.md) initiieren.

> [!Note]  
> Sie können die automatische Anmeldung auf dem Server auch mit dem Remotedesktopdienste-Konfigurationstool (Tscc.msc. ) aktivieren. Ein Administrator kann dieses Tool verwenden, um einer Verbindung in situationen, in denen eine automatisierte Anmeldung erforderlich ist, ein bestimmtes Kennwort zuzuweisen.

 

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

Die **IMsTscNonScriptable-Schnittstelle** wurde durch die folgenden Schnittstellen erweitert, wobei jede neue Schnittstelle alle Methoden und Eigenschaften der vorherigen Schnittstellen erbt:

-   [**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
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
| CLSID<br/>                    | CLSID \_ MsRdpClient ist als 791fa017-2de3-492e-acc5-53c67a2b94d0 definiert.<br/> CLSID \_ MsRdpClient10 ist als C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24 definiert.<br/> CLSID \_ MsRdpClient10NotSafeForScripting ist als A0C63C30-F08D-4AB4-907C-34905D770C7D definiert.<br/> CLSID \_ MsRdpClient2 ist als 9059F30F-4EB1-4BD2-9FDC-36F43A218F4A definiert.<br/> CLSID \_ MsRdpClient2a ist als 971127BB-259F-48C2-BD75-5F97A3331551 definiert.<br/> CLSID \_ MsRdpClient2NotSafeForScripting ist als 3523C2FB-4031-44E4-9A3B-F1E94986EE7F definiert.<br/> CLSID \_ MsRdpClient3 ist als 7584C670-2274-4EFB-B00B-D6AABA6D3850 definiert.<br/> CLSID \_ MsRdpClient3a ist als 6A6F4B83-45C5-4CA9-BDD9-0D81C12295E4 definiert.<br/> CLSID \_ MsRdpClient3NotSafeForScripting ist als ACE575FD-1FCF-4074-9401-EBAB990FA9DE definiert.<br/> CLSID \_ MsRdpClient4 ist als 4EDCB26C-D24C-4E72-AF07-B576699AC0DE definiert.<br/> CLSID \_ MsRdpClient4a ist als 54CE37E0-9834-41AE-9896-4DAB69DC022B definiert.<br/> CLSID \_ MsRdpClient4NotSafeForScripting ist als 6AE29350-321B-42BE-BBE5-12FB5270C0DE definiert.<br/> CLSID \_ MsRdpClient5 ist als 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2 definiert.<br/> CLSID \_ MsRdpClient5NotSafeForScripting ist als 4EB2F086-C818-447E-B32C-C51CE2B30D31 definiert.<br/> CLSID \_ MsRdpClient6 ist als 7390F3D8-0439-4C05-91E3-CF5CB290C3D0 definiert.<br/> CLSID \_ MsRdpClient6NotSafeForScripting ist als D2EA46A7-C2BF-426B-AF24-E19C44456399 definiert.<br/> CLSID \_ MsRdpClient7 ist als A9D7038D-B5ED-472E-9C47-94BEA90A5910 definiert.<br/> CLSID \_ MsRdpClient7NotSafeForScripting ist als 54D38BF7-B1EF-4479-9674-1BD6EA465258 definiert.<br/> CLSID \_ MsRdpClient8 ist als 5F681803-2900-4C43-A1CC-CF405404A676 definiert.<br/> CLSID \_ MsRdpClient8NotSafeForScripting ist als A3BC03A0-041D-42E3-AD22-882B7865C9C5 definiert.<br/> CLSID \_ MsRdpClient9 ist als 301B94BA-5D25-4A12-BFFE-3B6E7A616585 definiert.<br/> CLSID \_ MsRdpClient9NotSafeForScripting ist als 8B918B82-7985-4C24-89DF-C33AD2BBFBCD definiert.<br/> CLSID \_ MsRdpClientNotSafeForScripting ist als 7CACBD7B-0D99-468F-AC33-22E495C0AFE5 definiert.<br/> CLSID \_ MsTscAx ist als 1FB464C8-09BB-4017-A2F5-EB742F04392F definiert.<br/> CLSID \_ MsTscAxNotSafeForScripting ist als A41A4187-5A86-4E26-B40A-856F9035D9CB definiert.<br/> |
| IID<br/>                      | \_IID-IMsTscNonScriptable ist als C1E6743A-41C1-4A74-832A-0DD06C1C7A0E definiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotedesktop-Webverbindung-Referenz](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsTscAx::Verbinden**](imstscax-connect.md)
</dt> </dl>

 

