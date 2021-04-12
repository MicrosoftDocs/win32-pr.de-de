---
title: IMsRdpClientNonScriptable6 SendLocation3D-Methode
description: Sendet einen breiten-, Längen-und Höhen Wert an den Server, damit der geografische Standort des Clients in der Remote Sitzung wiedergegeben werden kann.
ms.tgt_platform: multiple
keywords:
- SendLocation3D-Methode Remotedesktopdienste
- SendLocation3D-Methode Remotedesktopdienste, IMsRdpClientNonScriptable6-Schnittstelle
- IMsRdpClientNonScriptable6-Schnittstelle Remotedesktopdienste, SendLocation3D-Methode
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation3D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: c63e779b6d6d090544af40a7ee6d9c05f8c49494
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480523"
---
# <a name="imsrdpclientnonscriptable6sendlocation3d-method"></a>IMsRdpClientNonScriptable6:: SendLocation3D-Methode

Sendet einen breiten-, Längen-und Höhen Wert an den Server, damit der geografische Standort des Clients in der Remote Sitzung wiedergegeben werden kann.

## <a name="syntax"></a>Syntax

```C++
HRESULT SendLocation3D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude,
  [in] INT32 altitude
);
```

## <a name="parameters"></a>Parameter

*Breitengrad* \[ in\]

Der Breitengrad eines geografischen Standorts. Der gültige Bereich von breiten Werten liegt zwischen-90,0 und 90,0 Grad.

*Längengrad* \[ in\]

Der Längengrad eines geografischen Standorts. Der gültige Bereich von breiten Werten liegt zwischen-180,0 und 180,0 Grad.

*Höhe* \[ in\]

Die Höhe eines geografischen Standorts in Meter.

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
