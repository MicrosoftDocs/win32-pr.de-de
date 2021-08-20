---
title: IMsRdpClientAdvancedSettings7 AudioQualityMode-Eigenschaft
description: Gibt einen Wert an, der die Einstellung des Audioqualitätsmodus für umgeleitetes Audio angibt, oder ruft diesen ab. Standardmäßig ist dies auf 0 festgelegt.
ms.assetid: 9945c524-ca50-41ae-a7cf-1386cd758c0f
ms.tgt_platform: multiple
keywords:
- AudioQualityMode-Eigenschaft Remotedesktopdienste
- AudioQualityMode-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , AudioQualityMode-Eigenschaft
- AudioQualityMode-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , AudioQualityMode-Eigenschaft
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
ms.openlocfilehash: 1635c2ed01144a640b624a014959a4847ae5f746502267444d958a20b959eef9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001308"
---
# <a name="imsrdpclientadvancedsettings7audioqualitymode-property"></a>IMsRdpClientAdvancedSettings7::AudioQualityMode-Eigenschaft

Gibt einen Wert an, der die Einstellung des Audioqualitätsmodus für umgeleitetes Audio angibt, oder ruft diesen ab. Standardmäßig ist dies auf 0 festgelegt.

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

Ein -Wert, der den Audioqualitätsmodus angibt.

Mögliche Werte sind:

<dt>

0
</dt> <dd>

Dynamische Audioqualität. Dies ist die Standardeinstellung für die Audioqualität. Der Server passt die Audioausgabequalität dynamisch als Reaktion auf Netzwerkbedingungen und die Client- und Serverfunktionen an.

</dd> <dt>

1
</dt> <dd>

Mittlere Audioqualität. Der Server verwendet ein festes, aber komprimiertes Format für die Audioausgabe.

</dd> <dt>

2
</dt> <dd>

Hohe Audioqualität. Der Server stellt audio output in uncompressed PCM format with lower processing overhead for latency (Audioausgabe im nicht komprimierten PCM-Format mit geringerem Verarbeitungsaufwand für Latenz) bereit.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                                |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 ist als 26036036-4010-4578-8091-0db9a1edf9c3 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





