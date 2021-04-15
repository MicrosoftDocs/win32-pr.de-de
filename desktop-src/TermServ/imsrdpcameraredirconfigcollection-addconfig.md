---
title: IMsRdpCameraRedirConfigCollection AddConfig-Methode
description: Fügt der Auflistung ein imsrdpcameraredirconfig-Objekt hinzu (die entsprechende Kamera muss nicht verbunden sein).
ms.tgt_platform: multiple
keywords:
- AddConfig-Methode Remotedesktopdienste
- AddConfig-Methode Remotedesktopdienste, imsrdpcameraredirconfigcollection-Schnittstelle
- Imsrdpcameraredirconfigcollection-Schnittstelle Remotedesktopdienste, AddConfig-Methode
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.AddConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e8c954b710c3f35bca9685d461e478104dac9039
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104520304"
---
# <a name="imsrdpcameraredirconfigcollectionaddconfig-method"></a>Imsrdpcameraredirconfigcollection:: AddConfig-Methode

Fügt der Auflistung ein [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt hinzu (die entsprechende Kamera muss nicht verbunden sein).

## <a name="syntax"></a>Syntax

```C++
HRESULT AddConfig(
    [in] BSTR symbolicLink,
    [in] VARIANT_BOOL fRedirected
);
```

## <a name="parameters"></a>Parameter

*SymbolicLink* \[ in\]

Die symbolische Verknüpfung für das neue [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt.

*frei geleitet* \[ in\]

Gibt an, ob die neue Kamera standardmäßig umgeleitet wird.

## <a name="return-value"></a>Rückgabewert

Gibt **\_ OK** zurück, wenn erfolgreich.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1803 (Build 17134)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ imsrdpcameraredirconfigcollection ist als AE45252B-aaab-4504-B681-649d6073a37a definiert.          |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>