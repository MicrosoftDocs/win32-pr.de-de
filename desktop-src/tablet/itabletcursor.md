---
description: Stellt ein Stiftobjekt dar.
ms.assetid: c55945b7-59df-49b5-b25f-fa96056889fc
title: ITabletCursor-Schnittstelle
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
ms.openlocfilehash: 83a24329b318ec2bb542a3bbb63a28d4db9fce877b99f75aa7091670825fa439
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716938"
---
# <a name="itabletcursor-interface"></a>ITabletCursor-Schnittstelle

Stellt ein Stiftobjekt dar.

## <a name="members"></a>Member

Die **ITabletCursor-Schnittstelle erbt** von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITabletCursor** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITabletCursor-Schnittstelle** verfügt über diese Methoden.



| Methode                                                 | Beschreibung                                                            |
|:-------------------------------------------------------|:-----------------------------------------------------------------------|
| [**GetButton**](itabletcursor-getbutton.md)           | Ruft das angegebene Schaltflächenobjekt von einem Tablettstift ab.<br/> |
| [**GetButtonCount**](itabletcursor-getbuttoncount.md) | Ruft die Anzahl der Schaltflächen auf dem Tablettstift ab.<br/>       |
| [**Getid**](itabletcursor-getid.md)                   | Ruft den Stiftbezeichner ab.<br/>                            |
| [**GetName**](itabletcursor-getname.md)               | Ruft den Namen des Tablettstifts ab.<br/>                    |
| [**IsInverted**](itabletcursor-isinverted.md)         | Gibt an, ob der Stift auf dem Kopf steht.<br/>                     |



 

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Schnittstelle nicht.

Der folgende Code beschreibt, wie die **ITabletCursor-Schnittstelle** definiert wird.

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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

