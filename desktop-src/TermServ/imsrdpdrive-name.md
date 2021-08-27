---
title: IMsRdpDrive Name (Eigenschaft)
description: Ruft den Namen des Laufwerks ab.
ms.assetid: 5aabb7df-fd46-48aa-ad1d-51da45495782
ms.tgt_platform: multiple
keywords:
- Name-Remotedesktopdienste
- Name-Eigenschaft Remotedesktopdienste , IMsRdpDrive-Schnittstelle
- IMsRdpDrive-Schnittstelle Remotedesktopdienste , Name-Eigenschaft
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
ms.openlocfilehash: bde69814f38c39315a02a76bd52b8c3c38baffc2c0a92601ef383cb60b0bc492
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125640"
---
# <a name="imsrdpdrivename-property"></a>IMsRdpDrive::Name (Eigenschaft)

Ruft den Namen des Laufwerks ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Name(
  [out] BSTR *pName
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Laufwerkname.

## <a name="error-codes"></a>Fehlercodes

Wenn die Methode erfolgreich ist, **wird S \_ OK** zurückgegeben. Jeder andere **HRESULT-Wert** gibt an, dass der Aufruf fehlgeschlagen ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDrive ist als d28b5458-f694-47a8-8e61-40356a767e46 definiert.<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpDrive**](imsrdpdrive.md)
</dt> </dl>

 

 





