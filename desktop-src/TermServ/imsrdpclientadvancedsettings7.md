---
title: IMsRdpClientAdvancedSettings7-Schnittstelle
description: Macht Methoden und Eigenschaften verfügbar, die erweiterte Einstellungen des ActiveX-Steuer Elements verwalten.
ms.assetid: 2d6848b4-2ce6-4624-b46e-65e7daf2d0f1
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: eed28c5d26ecf280507ce3cce835a6d0a71fc3bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342189"
---
# <a name="imsrdpclientadvancedsettings7-interface"></a>IMsRdpClientAdvancedSettings7-Schnittstelle

Macht Methoden und Eigenschaften verfügbar, die erweiterte Einstellungen des ActiveX-Steuer Elements verwalten.

Um eine Instanz dieser Schnittstelle abzurufen, verwenden Sie die [**imstscax:: advancedsettings**](imstscax-advancedsettings.md) -Eigenschaft, um einen [**imstscadvancedsettings**](imstscadvancedsettings-interface.md) -Schnittstellen Zeiger zu erhalten. Nennen Sie dann [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den **imstscadvancedsettings** -Zeiger, und übergeben Sie **IID \_ IMsRdpClientAdvancedSettings7** an **QueryInterface**.

## <a name="members"></a>Member

Die **IMsRdpClientAdvancedSettings7** -Schnittstelle erbt von **IMsRdpClientAdvancedSettings6**. **IMsRdpClientAdvancedSettings7** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientAdvancedSettings7** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                                                    | Zugriffstyp           | BESCHREIBUNG                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Audiocaptureredirectionmode**](imsrdpclientadvancedsettings7-audiocaptureredirectionmode.md)<br/> | Lesen/Schreiben<br/> | Gibt einen Wert an, der angibt, ob das standardmäßige Audioeingabegerät vom Client an die Remote Sitzung umgeleitet wird, oder ruft diesen Wert ab.<br/> |
| [**Audioqualitymode**](imsrdpclientadvancedsettings7-audioqualitymode.md)<br/>                       | Lesen/Schreiben<br/> | Gibt einen Wert an oder ruft ihn ab, der die Einstellung für den audioqualitätsmodus für umgeleitete Audiodaten angibt<br/>                                        |
| [**Enablesuperpan**](imsrdpclientadvancedsettings7-enablesuperpan.md)<br/>                           | Lesen/Schreiben<br/> | Gibt einen Wert an, der angibt, ob superpan aktiviert oder deaktiviert ist, oder ruft ihn ab.<br/>                                                    |
| [**Networkconnectiontype**](imsrdpclientadvancedsettings7-networkconnectiontype.md)<br/>             | Lesen/Schreiben<br/> | Gibt einen Wert an, der den Netzwerk Verbindungstyp angibt, oder ruft ihn ab.<br/>                                                                |
| [**Redirectdirectx**](imsrdpclientadvancedsettings7-redirectdirectx.md)<br/>                         | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht verwendet.<br/>                                                                                                                |
| [**Superpanaccelerationfactor**](imsrdpclientadvancedsettings7-superpanaccelerationfactor.md)<br/>   | Lesen/Schreiben<br/> | Gibt einen Wert an, der den superpan-Beschleunigungs Faktor angibt, oder ruft ihn ab.<br/>                                                           |
| [**Videoplaybackmode**](imsrdpclientadvancedsettings7-videoplaybackmode.md)<br/>                     | Lesen/Schreiben<br/> | Gibt einen Wert an, der den Videowiedergabe Modus angibt, oder ruft ihn ab.<br/>                                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                                |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 wird als 26036036-4010-4578-8091-0db9a1edf-C3 definiert.<br/> |



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

[**Imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**Imstscadvancedsettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

