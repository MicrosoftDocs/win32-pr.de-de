---
description: Stellt allgemeine Informationen zu einer Schaltfläche auf einem Stiftgerät dar.
ms.assetid: 20c9f8bb-8f8d-4469-baff-b9001c8adb3b
title: ITabletCursorButton-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 76f5e581a4db81d9e260b388cc129d915121a69f3b360441e4220fd58aa0e623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938600"
---
# <a name="itabletcursorbutton-interface"></a>ITabletCursorButton-Schnittstelle

Stellt allgemeine Informationen zu einer Schaltfläche auf einem Stiftgerät dar.

## <a name="members"></a>Member

Die **ITabletCursorButton-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITabletCursorButton** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITabletCursorButton-Schnittstelle** verfügt über diese Methoden.



| Methode                                         | BESCHREIBUNG                                                      |
|:-----------------------------------------------|:-----------------------------------------------------------------|
| [**Getguid**](itabletcursorbutton-getguid.md) | Ruft den eindeutigen Bezeichner der Stiftschaltfläche ab.<br/> |
| [**GetName**](itabletcursorbutton-getname.md) | Ruft den Namen der Stiftschaltfläche ab.<br/>              |



 

## <a name="remarks"></a>Hinweise

Entwickler sollten diese Schnittstelle nicht verwenden.

Der folgende Code zeigt, wie die **ITabletCursorButton-Schnittstelle** definiert ist.

``` syntax
[
    object,
    uuid(997A992E-8B6C-4945-BC17-A1EE563B3AB7),
    pointer_default(unique)
]
interface ITabletCursorButton : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetGuid(
        [out] GUID *pguidBtn);
};
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITabletCursorButton-Schnittstelle**](itabletcursorbutton.md)
</dt> </dl>

 

