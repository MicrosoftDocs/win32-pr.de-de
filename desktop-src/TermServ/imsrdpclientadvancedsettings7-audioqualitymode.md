---
title: IMsRdpClientAdvancedSettings7 audioqualitymode (Eigenschaft)
description: Gibt einen Wert an oder ruft ihn ab, der die Einstellung für den audioqualitätsmodus für umgeleitete Audiodaten angibt Standardmäßig ist dieser Wert auf 0 festgelegt.
ms.assetid: 9945c524-ca50-41ae-a7cf-1386cd758c0f
ms.tgt_platform: multiple
keywords:
- Audioqualitymode-Eigenschaft Remotedesktopdienste
- Audioqualitymode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, audioqualitymode-Eigenschaft
- Audioqualitymode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, audioqualitymode-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioQualityMode
- IMsRdpClientAdvancedSettings7.get_AudioQualityMode
- IMsRdpClientAdvancedSettings7.put_AudioQualityMode
- IMsRdpClientAdvancedSettings8.AudioQualityMode
- IMsRdpClientAdvancedSettings8.get_AudioQualityMode
- IMsRdpClientAdvancedSettings8.put_AudioQualityMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fdfc19176e03f8979e5adb25bf0c9eaf4ceed9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345905"
---
# <a name="imsrdpclientadvancedsettings7audioqualitymode-property"></a>IMsRdpClientAdvancedSettings7:: audioqualitymode (Eigenschaft)

Gibt einen Wert an oder ruft ihn ab, der die Einstellung für den audioqualitätsmodus für umgeleitete Audiodaten angibt Standardmäßig ist dieser Wert auf 0 festgelegt.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AudioQualityMode(
  [in]          UINT audioQualityMode
);

HRESULT get_AudioQualityMode(
  [out, retval] UINT *pAudioQualityMode
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein-Wert, der den audioqualitätsmodus angibt.

Mögliche Werte sind:

<dt>

0
</dt> <dd>

Dynamische Audioqualität. Dies ist die Standardeinstellung für die Audioqualität. Der Server passt die Qualität der Audioausgabe in Reaktion auf die Netzwerkbedingungen und die Client-und Serverfunktionen dynamisch an.

</dd> <dt>

1
</dt> <dd>

Mittlere Audioqualität. Der Server verwendet ein festes, aber komprimiertes Format für die Audioausgabe.

</dd> <dt>

2
</dt> <dd>

Hohe Audioqualität. Der Server stellt Audioausgaben im nicht komprimierten PCM-Format bereit, wobei der Verarbeitungsaufwand für die Latenz geringer ist.

</dd> </dl>

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

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





