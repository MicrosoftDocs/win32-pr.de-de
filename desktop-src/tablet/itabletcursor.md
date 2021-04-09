---
description: Stellt ein tablettstiftobjekt dar.
ms.assetid: c55945b7-59df-49b5-b25f-fa96056889fc
title: Itabletcursor-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: eecbebc7090fb57d3794f3d056c24fba61fa5c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868683"
---
# <a name="itabletcursor-interface"></a>Itabletcursor-Schnittstelle

Stellt ein tablettstiftobjekt dar.

## <a name="members"></a>Member

Die **itabletcursor** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Itabletcursor** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itabletcursor** -Schnittstelle verfügt über diese Methoden.



| Methode                                                 | BESCHREIBUNG                                                            |
|:-------------------------------------------------------|:-----------------------------------------------------------------------|
| [**Getbutton**](itabletcursor-getbutton.md)           | Ruft das angegebene Schaltflächen Objekt aus einem Tablet Tablettstift ab.<br/> |
| [**Getbuttoncount**](itabletcursor-getbuttoncount.md) | Ruft die Anzahl der Schaltflächen auf dem Tablettstift ab.<br/>       |
| [**GetId**](itabletcursor-getid.md)                   | Ruft den tablettstiftbezeichner ab.<br/>                            |
| [**GetName**](itabletcursor-getname.md)               | Ruft den Namen des Tablettstifts ab.<br/>                    |
| [**Isinvertierte**](itabletcursor-isinverted.md)         | Gibt an, ob der Tablettstift aufwärts unten ist.<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Schnittstelle nicht.

Im folgenden Code wird beschrieben, wie die **itabletcursor** -Schnittstelle definiert wird.

``` syntax
[
    object,
    uuid(EF9953C6-B472-4B02-9D22-D0E247ADE0E8,
    pointer_default(unique)
]
interface ITabletCursor : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT IsInverted();

    HRESULT GetId(
        [out] CURSOR_ID *pCid);

    HRESULT GetTablet(
        [out] ITablet **ppTablet);

    HRESULT GetButtonCount(
        [out] ULONG *pcButtons);

    HRESULT GetButton(
        [in] ULONG iButton,
        [out] ITabletCursorButton **ppButton);
};

     
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

