---
title: Imsrdpdrive-Name (Eigenschaft)
description: Ruft den Namen des Laufwerks ab.
ms.assetid: 5aabb7df-fd46-48aa-ad1d-51da45495782
ms.tgt_platform: multiple
keywords:
- Name-Eigenschaft Remotedesktopdienste
- Name-Eigenschaft Remotedesktopdienste, imsrdpdrive-Schnittstelle
- Imsrdpdrive-Schnittstelle Remotedesktopdienste, Name-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDrive.Name
- IMsRdpDrive.get_Name
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38eeb0f6112983f508bb43ba69d721aeb52c314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477739"
---
# <a name="imsrdpdrivename-property"></a>Imsrdpdrive:: Name-Eigenschaft

Ruft den Namen des Laufwerks ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Name(
  [out] BSTR *pName
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Name des Laufwerks.

## <a name="error-codes"></a>Fehlercodes

Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ imsrdpdrive ist als d28b5458-f694-47a8-8e61-40356a767e46 definiert.<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpdrive**](imsrdpdrive.md)
</dt> </dl>

 

 





