---
title: IMsRdpClientAdvancedSettings7 superpanaccelerationfactor-Eigenschaft
description: Gibt einen Wert an, der den superpan-Beschleunigungs Faktor angibt, oder ruft ihn ab. Der superpan-Beschleunigungs Faktor bestimmt, wie schnell der Bildschirm im superpan-Modus ist.
ms.assetid: ce04f109-8a48-48ee-a553-728f12c09dde
ms.tgt_platform: multiple
keywords:
- Superpanaccelerationfactor-Eigenschaft Remotedesktopdienste
- Superpanaccelerationfactor-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, superpanaccelerationfactor-Eigenschaft
- Superpanaccelerationfactor-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, superpanaccelerationfactor-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.put_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.put_SuperPanAccelerationFactor
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0919f3b1920980790203dc265e840e24a9315ae0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957227"
---
# <a name="imsrdpclientadvancedsettings7superpanaccelerationfactor-property"></a>IMsRdpClientAdvancedSettings7:: superpanaccelerationfactor-Eigenschaft

Gibt einen Wert an, der den superpan-Beschleunigungs Faktor angibt, oder ruft ihn ab. Der superpan-Beschleunigungs Faktor bestimmt, wie schnell der Bildschirm im superpan-Modus ist. Der Beschleunigungs Faktor ist die Anzahl der Pixel, die die Bildschirmansicht für jedes Pixel der Mausbewegung durch den Client in eine bestimmte Richtung verschiebt.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SuperPanAccelerationFactor(
  [in]          ULONG uAccelFactor
);

HRESULT get_SuperPanAccelerationFactor(
  [out, retval] ULONG *puAccelFactor
);
```



## <a name="property-value"></a>Eigenschaftswert

Der festzulegende Wert für die übergeordnete Beschleunigung. Der übergeordnete Beschleunigungs Faktor ist die Anzahl der Pixel, die die Bildschirmansicht für jedes Pixel der Mausbewegung in eine bestimmte Richtung verschiebt.

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu superpan finden Sie unter [**enablesuperpan**](imsrdpclientadvancedsettings7-enablesuperpan.md).

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
</dt> <dt>

[**Enablesuperpan**](imsrdpclientadvancedsettings7-enablesuperpan.md)
</dt> </dl>

 

 





