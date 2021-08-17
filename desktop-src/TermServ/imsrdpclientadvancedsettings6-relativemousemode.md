---
title: IMsRdpClientAdvancedSettings6 RelativeMouseMode-Eigenschaft
description: Gibt an, ob die Maus den relativen Modus verwenden soll.
ms.assetid: 29ae9575-ce60-4999-9601-18413ae739e6
ms.tgt_platform: multiple
keywords:
- RelativeMouseMode-Eigenschaft Remotedesktopdienste
- RelativeMouseMode-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , RelativeMouseMode-Eigenschaft
- RelativeMouseMode-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , RelativeMouseMode-Eigenschaft
- RelativeMouseMode-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , RelativeMouseMode-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.RelativeMouseMode
- IMsRdpClientAdvancedSettings6.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings6.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.RelativeMouseMode
- IMsRdpClientAdvancedSettings7.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.RelativeMouseMode
- IMsRdpClientAdvancedSettings8.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.put_RelativeMouseMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cfe0551cf02f94f3494fde5ebf49ffb60c2bd4a966db1efb5f0dfeb3bd9e4bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138813"
---
# <a name="imsrdpclientadvancedsettings6relativemousemode-property"></a>IMsRdpClientAdvancedSettings6::RelativeMouseMode-Eigenschaft

Gibt an, ob die Maus den relativen Modus verwenden soll. Enthält **VARIANT \_ TRUE,** wenn sich die Maus im relativen Modus befindet, oder **VARIANT \_ FALSE,** wenn sich die Maus im absoluten Modus befindet.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RelativeMouseMode(
  [in]          VARIANT_BOOL fRelativeMouseMode
);

HRESULT get_RelativeMouseMode(
  [out, retval] VARIANT_BOOL *pfRelativeMouseMode
);
```



## <a name="property-value"></a>Eigenschaftswert

Enthält den neuen Eigenschaftswert.

## <a name="remarks"></a>Hinweise

Der Mausmodus gibt an, wie das ActiveX-Steuerelement die Mauskoordinaten berechnet, die es an den Remotedesktop-Sitzungshost -Server (RD-Sitzungshost) sendet. Wenn sich die Maus im relativen Modus befindet, berechnet das ActiveX-Steuerelement Mauskoordinaten relativ zur letzten Position der Maus. Wenn sich die Maus im absoluten Modus befindet, berechnet das ActiveX-Steuerelement Mauskoordinaten relativ zum Desktop des RD-Sitzungshost-Servers.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista mit SP1<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                   |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 ist als 222c4b5d-45d9-4df0-a7c6-60cf9089d285 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





