---
title: IMsRdpDevice RedirectionState-Eigenschaft
description: Gibt den Umleitungsstatus des Geräts an.
ms.assetid: 967734c9-64d8-4604-a133-4649279f4475
ms.tgt_platform: multiple
keywords:
- RedirectionState-Eigenschaft Remotedesktopdienste
- RedirectionState-Eigenschaft Remotedesktopdienste , IMsRdpDevice-Schnittstelle
- IMsRdpDevice-Schnittstelle Remotedesktopdienste , RedirectionState-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDevice.RedirectionState
- IMsRdpDevice.get_RedirectionState
- IMsRdpDevice.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8609c682a7a31d293e6e8a9606c8ae445b0487da0d95399fb4e00d779914bfd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606682"
---
# <a name="imsrdpdeviceredirectionstate-property"></a>IMsRdpDevice::RedirectionState-Eigenschaft

Gibt den Umleitungsstatus des Geräts an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a>Eigenschaftswert

Legen Sie diesen Parameter auf **VARIANT \_ FALSE** fest, um die Umleitung zu deaktivieren, oder **VARIANT \_ TRUE,** um die Umleitung zu aktivieren.

## <a name="error-codes"></a>Fehlercodes

Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Jeder andere **HRESULT-Wert** gibt an, dass der Aufruf fehlgeschlagen ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDevice ist als 60c3b9c8-9e92-4f5e-a3e7-604a912093ea definiert.<br/>        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpDevice**](imsrdpdevice.md)
</dt> </dl>

 

 





