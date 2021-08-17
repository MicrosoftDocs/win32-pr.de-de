---
title: IMsRdpClientAdvancedSettings8 BandwidthDetection (Eigenschaft)
description: Gibt an, ob Bandbreitenänderungen automatisch erkannt werden.
ms.assetid: 30b2b7b3-9050-4a11-9929-2ad1dbf5ed2d
ms.tgt_platform: multiple
keywords:
- BandwidthDetection-Eigenschaft Remotedesktopdienste
- BandwidthDetection-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , BandwidthDetection -Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ab6fbe8291c0318e378add8041d0e2d2d0f30b6ee1e298c3a43a6a0ccd430c31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138783"
---
# <a name="imsrdpclientadvancedsettings8bandwidthdetection-property"></a>IMsRdpClientAdvancedSettings8::BandwidthDetection (Eigenschaft)

Gibt an, ob Bandbreitenänderungen automatisch erkannt werden.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BandwidthDetection(
  [in]          VARIANT_BOOL fAutodetect
);

HRESULT get_BandwidthDetection(
  [out, retval] VARIANT_BOOL *pfAutodetect
);
```



## <a name="property-value"></a>Eigenschaftswert

**VARIANT \_ TRUE,** wenn Bandbreitenänderungen automatisch erkannt werden, **andernfalls VARIANT \_ FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> </dl>

 

 





