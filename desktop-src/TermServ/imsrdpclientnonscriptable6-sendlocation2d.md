---
title: IMsRdpClientNonScriptable6 SendLocation2D-Methode
description: Sendet einen breiten-und Längengrad Wert an den Server, damit der geografische Standort des Clients in der Remote Sitzung wiedergegeben werden kann.
ms.tgt_platform: multiple
keywords:
- SendLocation2D-Methode Remotedesktopdienste
- SendLocation2D-Methode Remotedesktopdienste, IMsRdpClientNonScriptable6-Schnittstelle
- IMsRdpClientNonScriptable6-Schnittstelle Remotedesktopdienste, SendLocation2D-Methode
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation2D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: b706fdb35ba8360b294d25021c0c1a18bbe90188
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "103745344"
---
# <a name="imsrdpclientnonscriptable6sendlocation2d-method"></a>IMsRdpClientNonScriptable6:: SendLocation2D-Methode

Sendet einen breiten-und Längengrad Wert an den Server, damit der geografische Standort des Clients in der Remote Sitzung wiedergegeben werden kann.

## <a name="syntax"></a>Syntax

```C++
HRESULT SendLocation2D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude
);
```

## <a name="parameters"></a>Parameter

*Breitengrad* \[ in\]

Der Breitengrad eines geografischen Standorts. Der gültige Bereich von breiten Werten liegt zwischen-90,0 und 90,0 Grad.

*Längengrad* \[ in\]

Der Längengrad eines geografischen Standorts. Der gültige Bereich von breiten Werten liegt zwischen-180,0 und 180,0 Grad.

## <a name="return-value"></a>Rückgabewert

Gibt **\_ OK** zurück, wenn erfolgreich.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1709 (Build 16299)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClientNonScriptable6 ist als 05293249-B28B-4db8-BE64-1b2t496b910e definiert.            |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md)
</dt> </dl>
