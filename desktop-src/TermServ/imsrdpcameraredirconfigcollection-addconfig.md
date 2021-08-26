---
title: IMsRdpCameraRedirConfigCollection AddConfig-Methode
description: Fügt der Sammlung ein IMsRdpCameraRedirConfig-Objekt hinzu (die entsprechende Kamera muss nicht verbunden sein).
ms.tgt_platform: multiple
keywords:
- AddConfig-Methode Remotedesktopdienste
- AddConfig-Methode Remotedesktopdienste, IMsRdpCameraRedirConfigCollection-Schnittstelle
- IMsRdpCameraRedirConfigCollection-Schnittstelle Remotedesktopdienste, AddConfig-Methode
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
ms.openlocfilehash: 88d4f7952497ca0afd970a979441f98864b2855ed3f36f3e556dc4241ed52769
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033650"
---
# <a name="imsrdpcameraredirconfigcollectionaddconfig-method"></a>IMsRdpCameraRedirConfigCollection::AddConfig-Methode

Fügt der Sammlung ein [IMsRdpCameraRedirConfig-Objekt](imsrdpcameraredirconfig.md) hinzu (die entsprechende Kamera muss nicht verbunden sein).

## <a name="syntax"></a>Syntax

```C++
HRESULT AddConfig(
    [in] BSTR symbolicLink,
    [in] VARIANT_BOOL fRedirected
);
```

## <a name="parameters"></a>Parameter

*symbolicLink* \[ In\]

Die symbolische Verknüpfung für das neue [IMsRdpCameraRedirConfig-Objekt.](imsrdpcameraredirconfig.md)

*fRedirected* \[ In\]

Gibt an, ob die neue Kamera standardmäßig umgeleitet wird.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1803 (Build 17134)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection ist als AE45252B-AAAB-4504-B681-649D6073A37A definiert.          |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>