---
title: Imsrdpdrive redirectionstate (Eigenschaft)
description: Gibt den Umleitungs Status des Laufwerks an.
ms.assetid: 05333671-460d-4c07-8b7e-fbb7bc215353
ms.tgt_platform: multiple
keywords:
- Redirectionstate-Eigenschaft Remotedesktopdienste
- Redirectionstate-Eigenschaft Remotedesktopdienste, imsrdpdrive-Schnittstelle
- Imsrdpdrive-Schnittstelle Remotedesktopdienste, redirectionstate-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDrive.RedirectionState
- IMsRdpDrive.get_RedirectionState
- IMsRdpDrive.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561190e976e0b8190553376f5e9f7a5b2de2550
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392075"
---
# <a name="imsrdpdriveredirectionstate-property"></a>Imsrdpdrive:: redirectionstate-Eigenschaft

Gibt den Umleitungs Status des Laufwerks an.

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

Legen Sie diesen Parameter auf **Variant \_ false** fest. , wenn Umleitung oder **Variant \_ true** deaktiviert werden soll. , um die Umleitung zu aktivieren.

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

 

 





