---
title: IMsRdpClientAdvancedSettings6 relativemousmode (Eigenschaft)
description: Gibt an, ob die Maus den relativen Modus verwenden soll.
ms.assetid: 29ae9575-ce60-4999-9601-18413ae739e6
ms.tgt_platform: multiple
keywords:
- Relativemousmode-Eigenschaft Remotedesktopdienste
- Relativemousmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, relativemousmode (Eigenschaft)
- Relativemousmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, relativemousmode (Eigenschaft)
- Relativemousmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, relativemousmode (Eigenschaft)
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
ms.openlocfilehash: 31c575acefbfef54dc4c858f465f0cdde2ce8bc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346726"
---
# <a name="imsrdpclientadvancedsettings6relativemousemode-property"></a>IMsRdpClientAdvancedSettings6:: relativemousmode (Eigenschaft)

Gibt an, ob die Maus den relativen Modus verwenden soll. Enthält **Variant \_ true** , wenn sich der Mauszeiger im relativen Modus befindet, oder **Variant \_ false** , wenn sich der Mauszeiger im absoluten Modus befindet.

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

Enthält den neuen Eigenschafts Wert.

## <a name="remarks"></a>Bemerkungen

Der Mausmodus gibt an, wie das ActiveX-Steuerelement die Maus Koordinaten berechnet, die es an den Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) sendet. Wenn sich der Mauszeiger im relativen Modus befindet, berechnet das ActiveX-Steuerelement Maus Koordinaten in Bezug auf die letzte Position der Maus. Wenn sich der Mauszeiger im absoluten Modus befindet, berechnet das ActiveX-Steuerelement die Maus Koordinaten relativ zum Desktop des RD-Sitzungshost Servers.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista mit SP1<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                   |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 ist als 222c4b5d-45d9-4df0-a7c6-60cf9089d285 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





