---
title: IMsRdpClientAdvancedSettings5 audioredirectionmode-Eigenschaft
description: Legt den audioumleitungs Modus und andere audioumleitungs Optionen fest und ruft ihn ab.
ms.assetid: c0f5762b-00fd-40bb-ac97-3351b999f38d
ms.tgt_platform: multiple
keywords:
- Audioredirectionmode-Eigenschaft Remotedesktopdienste
- Audioredirectionmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, audioredirectionmode-Eigenschaft
- Audioredirectionmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, audioredirectionmode-Eigenschaft
- Audioredirectionmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, audioredirectionmode-Eigenschaft
- Audioredirectionmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, audioredirectionmode-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.AudioRedirectionMode
- IMsRdpClientAdvancedSettings5.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings5.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40be8b8e63f210d060c0f585c9fe31328ac6ed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340527"
---
# <a name="imsrdpclientadvancedsettings5audioredirectionmode-property"></a>IMsRdpClientAdvancedSettings5:: audioredirectionmode-Eigenschaft

Legt den audioumleitungs Modus und andere audioumleitungs Optionen fest und ruft ihn ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AudioRedirectionMode(
  [in]  UINT uiAudioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] UINT *puiAudioRedirectionMode
);
```



## <a name="property-value"></a>Eigenschaftswert

Legt verschiedene Werte für den audioumleitungs Modus fest. Dieser Parameter verfügt über die folgenden möglichen Werte.

<dt>

<span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span>

**Audiodatei \_ \_Modusumleitung 0** (die Audioumleitung ist aktiviert, und die Option für die Umleitung lautet "an diesen Computer übertragen". Dies ist der Standardmodus.)


</dt> <dd></dd> <dt>

<span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span>

**Audiodatei \_ Der Modus wird \_ \_ auf \_ Server 1 abgespielt** (die Audioumleitung ist aktiviert, und die Option ist "auf Remote Computer verlassen". Die Option "Remote Computer verlassen" wird nur unterstützt, wenn eine Remote Verbindung mit einem Host Computer hergestellt wird, auf dem Windows Vista ausgeführt wird. Wenn die Verbindung mit einem Host Computer hergestellt wird, auf dem Windows Server 2008 ausgeführt wird, wird die Option "auf Remote Computer verlassen" in "nicht wiedergeben" geändert.)


</dt> <dd></dd> <dt>

<span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span>

**Audiodatei \_ Modus \_ None 2** (Audioumleitung ist aktiviert, und der Modus ist nicht wiedergeben).


</dt> <dd></dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                   |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings5 ist als FBA7F64E-6783-4405-DA45-FA4A763DABD0 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





