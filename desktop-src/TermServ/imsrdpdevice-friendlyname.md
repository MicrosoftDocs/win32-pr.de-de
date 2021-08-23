---
title: IMsRdpDevice FriendlyName (Eigenschaft)
description: Ruft den Anzeigenamen für das Gerät ab.
ms.assetid: ed27eacd-1d39-484c-8217-62ed608db050
ms.tgt_platform: multiple
keywords:
- FriendlyName-Remotedesktopdienste
- FriendlyName-Eigenschaft Remotedesktopdienste , IMsRdpDevice-Schnittstelle
- IMsRdpDevice-Schnittstelle Remotedesktopdienste , FriendlyName-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDevice.FriendlyName
- IMsRdpDevice.get_FriendlyName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38d2b9ec817cdfa2a384e2f601da82a7e182b458574a5bb4b29fe639d8e11216
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119334620"
---
# <a name="imsrdpdevicefriendlyname-property"></a>IMsRdpDevice::FriendlyName (Eigenschaft)

Ruft den Anzeigenamen für das Gerät ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_FriendlyName(
  [out] BSTR *pFriendlyName
);
```



## <a name="property-value"></a>Eigenschaftswert

Neuer Anzeigename.

## <a name="error-codes"></a>Fehlercodes

Wenn die Methode erfolgreich ist, **wird S \_ OK** zurückgegeben. Jeder andere **HRESULT-Wert** gibt an, dass der Aufruf fehlgeschlagen ist.

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

 

 





