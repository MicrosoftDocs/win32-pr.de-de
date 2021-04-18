---
title: IMsRdpClientSecuredSettings2 (Eigenschaft)
description: Gibt die Einstellung für die Vorverbindungs-BLOB (Festplatte) an, die vor der Verbindungs Herstellung mit dem Server verwendet werden soll. | IMsRdpClientSecuredSettings2 (Eigenschaft)
ms.assetid: e2ddd9fd-d868-4fc5-835d-0f4db5da71e3
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Platine-Eigenschaft
- Eigenschaften Remotedesktopdienste der Platine, IMsRdpClientSecuredSettings2-Schnittstelle
- IMsRdpClientSecuredSettings2-Schnittstelle Remotedesktopdienste, Eigenschaft ' PCB '
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings2.PCB
- IMsRdpClientSecuredSettings2.get_PCB
- IMsRdpClientSecuredSettings2.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99b9a04a854f218fcbe1735ec6271aa4a58edba
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365059"
---
# <a name="imsrdpclientsecuredsettings2pcb-property"></a>IMsRdpClientSecuredSettings2::P CB-Eigenschaft

Gibt die Einstellung für die Vorverbindungs-BLOB (Festplatte) an, die vor der Verbindungs Herstellung mit dem Server verwendet werden soll.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *bstrPCB
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Einstellung für die Festplatte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md)
</dt> </dl>

 

 





