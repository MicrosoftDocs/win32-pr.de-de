---
title: Imsrdpdevice redirectionstate (Eigenschaft)
description: Gibt den Umleitungs Status des Geräts an.
ms.assetid: 967734c9-64d8-4604-a133-4649279f4475
ms.tgt_platform: multiple
keywords:
- Redirectionstate-Eigenschaft Remotedesktopdienste
- Redirectionstate-Eigenschaft Remotedesktopdienste, imsrdpdevice-Schnittstelle
- Imsrdpdevice-Schnittstelle Remotedesktopdienste, redirectionstate-Eigenschaft
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
ms.openlocfilehash: be0f6fb5781700daa8a65443d2713253e97f73bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476452"
---
# <a name="imsrdpdeviceredirectionstate-property"></a>Imsrdpdevice:: redirectionstate-Eigenschaft

Gibt den Umleitungs Status des Geräts an.

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

Legen Sie diesen Parameter auf **Variant \_ false** fest, um die Umleitung zu deaktivieren oder **Variant \_ true** zu aktivieren

## <a name="error-codes"></a>Fehlercodes

Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ imsrdpdevice ist als 60c3b9c8-9E92-4fi5e-a3e7-604a912093ea definiert.<br/>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpdevice**](imsrdpdevice.md)
</dt> </dl>

 

 





