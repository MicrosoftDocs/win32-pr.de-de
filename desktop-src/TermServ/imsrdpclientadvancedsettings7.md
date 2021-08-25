---
title: IMsRdpClientAdvancedSettings7-Schnittstelle
description: Macht Methoden und Eigenschaften verfügbar, die erweiterte Einstellungen des ActiveX-Steuerelements verwalten.
ms.assetid: 2d6848b4-2ce6-4624-b46e-65e7daf2d0f1
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5df2990a257d8f7fa544c24e33dba6a2422d2db8bea878f2487ca131e5bd607
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866560"
---
# <a name="imsrdpclientadvancedsettings7-interface"></a>IMsRdpClientAdvancedSettings7-Schnittstelle

Macht Methoden und Eigenschaften verfügbar, die erweiterte Einstellungen des ActiveX-Steuerelements verwalten.

Um eine Instanz dieser Schnittstelle abzurufen, verwenden Sie die [**IMsTscAx::AdvancedSettings-Eigenschaft,**](imstscax-advancedsettings.md) um einen [**IMsTscAdvancedSettings-Schnittstellenzeiger**](imstscadvancedsettings-interface.md) abzurufen. Rufen Sie dann [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den **IMsTscAdvancedSettings-Zeiger** auf, und übergeben Sie **IID \_ IMsRdpClientAdvancedSettings7** an **QueryInterface**.

## <a name="members"></a>Member

Die **IMsRdpClientAdvancedSettings7-Schnittstelle** erbt von **IMsRdpClientAdvancedSettings6.** **IMsRdpClientAdvancedSettings7** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientAdvancedSettings7-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                                    | Zugriffstyp           | BESCHREIBUNG                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AudioCaptureRedirectionMode**](imsrdpclientadvancedsettings7-audiocaptureredirectionmode.md)<br/> | Lesen/Schreiben<br/> | Gibt einen Wert an, der angibt, ob das Standardaudioeingabegerät vom Client zur Remotesitzung umgeleitet wird, oder ruft diesen ab.<br/> |
| [**AudioQualityMode**](imsrdpclientadvancedsettings7-audioqualitymode.md)<br/>                       | Lesen/Schreiben<br/> | Gibt einen Wert an, der die Einstellung des Audioqualitätsmodus für umgeleitetes Audio angibt, oder ruft diesen ab.<br/>                                        |
| [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md)<br/>                           | Lesen/Schreiben<br/> | Gibt einen Wert an, der angibt, ob SuperPan aktiviert oder deaktiviert ist, oder ruft diesen ab.<br/>                                                    |
| [**NetworkConnectionType**](imsrdpclientadvancedsettings7-networkconnectiontype.md)<br/>             | Lesen/Schreiben<br/> | Gibt einen Wert an, der den Netzwerkverbindungstyp angibt, oder ruft diesen ab.<br/>                                                                |
| [**RedirectDirectX**](imsrdpclientadvancedsettings7-redirectdirectx.md)<br/>                         | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht verwendet.<br/>                                                                                                                |
| [**SuperPanAccelerationFactor**](imsrdpclientadvancedsettings7-superpanaccelerationfactor.md)<br/>   | Lesen/Schreiben<br/> | Gibt einen Wert an, der den SuperPan-Beschleunigungsfaktor angibt, oder ruft diesen ab.<br/>                                                           |
| [**VideoPlaybackMode**](imsrdpclientadvancedsettings7-videoplaybackmode.md)<br/>                     | Lesen/Schreiben<br/> | Gibt einen Wert an, der den Videowiedergabemodus angibt, oder ruft diesen ab.<br/>                                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                                |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 ist als 26036036-4010-4578-8091-0db9a1edf9c3 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

