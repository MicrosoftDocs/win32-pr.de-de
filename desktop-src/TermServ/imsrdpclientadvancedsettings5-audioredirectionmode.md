---
title: IMsRdpClientAdvancedSettings5 AudioRedirectionMode (Eigenschaft)
description: Legt den Audioumleitungsmodus und verschiedene Audioumleitungsoptionen fest und ruft sie ab.
ms.assetid: c0f5762b-00fd-40bb-ac97-3351b999f38d
ms.tgt_platform: multiple
keywords:
- AudioRedirectionMode-Remotedesktopdienste
- AudioRedirectionMode-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste , AudioRedirectionMode -Eigenschaft
- AudioRedirectionMode-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , AudioRedirectionMode -Eigenschaft
- AudioRedirectionMode-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , AudioRedirectionMode (Eigenschaft)
- AudioRedirectionMode-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , AudioRedirectionMode -Eigenschaft
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
ms.openlocfilehash: df4216b4babf74e5e5f15994c0d8387e0d5087c4f69e4d0245b59cb5765dfe88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118352512"
---
# <a name="imsrdpclientadvancedsettings5audioredirectionmode-property"></a>IMsRdpClientAdvancedSettings5::AudioRedirectionMode (Eigenschaft)

Legt den Audioumleitungsmodus und verschiedene Audioumleitungsoptionen fest und ruft sie ab.

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

Legt unterschiedliche Werte für den Audioumleitungsmodus fest. Dieser Parameter verfügt über die folgenden möglichen Werte.

<dt>

<span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span>

**AUDIO \_ MODE \_ REDIRECT 0** (Audioumleitung ist aktiviert, und die Option für die Umleitung ist "Bring to this computer". Dies ist der Standardmodus.)


</dt> <dd></dd> <dt>

<span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span>

**AUDIO \_ MODE \_ PLAY ON SERVER \_ \_ 1** (Audioumleitung ist aktiviert, und die Option "Auf Remotecomputer verlassen" ist aktiviert. Die Option "Auf Remotecomputer verlassen" wird nur unterstützt, wenn eine Remoteverbindung mit einem Hostcomputer mit Windows Vista besteht. Wenn die Verbindung mit einem Hostcomputer hergestellt wird, auf dem Windows Server 2008 ausgeführt wird, wird die Option "Auf Remotecomputer verlassen" in "Do not play" geändert.)


</dt> <dd></dd> <dt>

<span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span>

**AUDIO \_ MODE \_ NONE 2** (Audioumleitung ist aktiviert, und der Modus ist "Do not play".)


</dt> <dd></dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                   |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings5 ist als FBA7F64E-6783-4405-DA45-FA4A763DABD0 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





