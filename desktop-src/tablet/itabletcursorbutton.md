---
description: Stellt allgemeine Informationen über eine Schaltfläche auf einem Tablettstiftgerät dar.
ms.assetid: 20c9f8bb-8f8d-4469-baff-b9001c8adb3b
title: Itabletcursor Button-Schnittstelle
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
ms.openlocfilehash: c8f13e46699c1bea42bd8f8a7f78313aeba68aaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346868"
---
# <a name="itabletcursorbutton-interface"></a>Itabletcursor Button-Schnittstelle

Stellt allgemeine Informationen über eine Schaltfläche auf einem Tablettstiftgerät dar.

## <a name="members"></a>Member

Die **itabletcursor Button** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Itabletcursor Button** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die Schnittstelle **itabletcursor Button** verfügt über diese Methoden.



| Methode                                         | BESCHREIBUNG                                                      |
|:-----------------------------------------------|:-----------------------------------------------------------------|
| [**GetGuid**](itabletcursorbutton-getguid.md) | Ruft den eindeutigen Bezeichner der Tablettstiftschaltfläche ab.<br/> |
| [**GetName**](itabletcursorbutton-getname.md) | Ruft den Namen der Tablettstiftschaltfläche ab.<br/>              |



 

## <a name="remarks"></a>Bemerkungen

Entwickler sollten diese Schnittstelle nicht verwenden.

Der folgende Code zeigt, wie die **itabletcursor Button** -Schnittstelle definiert wird.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itabletcursor Button-Schnittstelle**](itabletcursorbutton.md)
</dt> </dl>

 

