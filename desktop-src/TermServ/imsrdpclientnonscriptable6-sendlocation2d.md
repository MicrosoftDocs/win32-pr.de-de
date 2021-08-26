---
title: IMsRdpClientNonScriptable6 SendLocation2D-Methode
description: Sendet einen Breiten- und Längengradwert an den Server, damit der geografische Standort des Clients in der Remotesitzung widergespiegelt werden kann.
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
ms.openlocfilehash: 2e2e252f86249531c61922cf02f308bfaf2b76c2518ff9b420f5ec3fd80d9d88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990140"
---
# <a name="imsrdpclientnonscriptable6sendlocation2d-method"></a>IMsRdpClientNonScriptable6::SendLocation2D-Methode

Sendet einen Breiten- und Längengradwert an den Server, damit der geografische Standort des Clients in der Remotesitzung widergespiegelt werden kann.

## <a name="syntax"></a>Syntax

```C++
HRESULT SendLocation2D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude
);
```

## <a name="parameters"></a>Parameter

*Breitengrad* \[ In\]

Der Breitengrad eines geografischen Standorts. Der gültige Breitengradbereich liegt zwischen -90,0 und 90,0 Grad.

*Längengrad* \[ In\]

Der Längengrad eines geografischen Standorts. Der gültige Breitengradbereich liegt zwischen -180,0 und 180,0 Grad.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1709 (Build 16299)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClientNonScriptable6 ist als 05293249-B28B-4DB8-BE64-1B2F496B910E definiert.            |

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md)
</dt> </dl>
