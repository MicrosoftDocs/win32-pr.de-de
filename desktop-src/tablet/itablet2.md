---
description: Erweitert die iTablet-Schnittstelle.
ms.assetid: dd4f3b2e-7f63-4d5b-b50e-64458719c17a
title: ITablet2-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b402695aa278105ad57209f3ff33e66ccaf8c746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363326"
---
# <a name="itablet2-interface"></a>ITablet2-Schnittstelle

Erweitert die [**iTablet-Schnittstelle**](itablet.md).

## <a name="members"></a>Member

Die **ITablet2** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ITablet2** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITablet2** -Schnittstelle verfügt über diese Methoden.



| Methode                                          | BESCHREIBUNG                                                                                              |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**Getdevicekind**](itablet2-getdevicekind.md) | Gibt den Typ des Hardware Geräts zurück, das das Tablet-Objekt darstellt, z. b. Maus, Stift oder Fingereingabe<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle wurde in Windows Vista eingeführt.

Entwickler sollten diese Schnittstelle nicht verwenden.

Im folgenden Code wird beschrieben, wie die **ITablet2** -Schnittstelle definiert wird.

``` syntax
[
    object,
    uuid(C247F616-BBEB-406A-AED3-F75E656599AE),
    pointer_default(unique)
]
interface ITablet2 : IUnknown
{
    HRESULT GetDeviceKind([out] TABLET_DEVICE_KIND *pKind);

    HRESULT GetMatchingScreenRect([out] RECT *prcInput);
};
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

