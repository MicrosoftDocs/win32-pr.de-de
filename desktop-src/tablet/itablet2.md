---
description: Erweitert die ITablet-Schnittstelle.
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
ms.openlocfilehash: 0df1114f5808e5fd08a1a2dbe00ccfb451eaa7096c978d3f4d454e508c0a2fcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717349"
---
# <a name="itablet2-interface"></a>ITablet2-Schnittstelle

Erweitert die [**ITablet-Schnittstelle**](itablet.md).

## <a name="members"></a>Member

Die **ITablet2-Schnittstelle erbt** von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITablet2** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITablet2-Schnittstelle** verfügt über diese Methoden.



| Methode                                          | Beschreibung                                                                                              |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**GetDeviceKind**](itablet2-getdevicekind.md) | Gibt den Typ des Hardwaregeräts zurück, das das Tablettobjekt darstellt, z. B. Maus, Stift oder Fingereingabe.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Schnittstelle wurde in Windows Vista eingeführt.

Entwickler sollten diese Schnittstelle nicht verwenden.

Der folgende Code beschreibt, wie die **ITablet2-Schnittstelle** definiert wird.

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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

