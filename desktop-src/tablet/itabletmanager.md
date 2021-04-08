---
description: Bietet Zugriff auf alle Tablet-PCs, die mit dem Computer verbunden sind.
ms.assetid: d0fd9a6f-93fe-43d6-97fd-fee45854dfa1
title: Itabletmanager-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 3400d98a832819d1edd640cd78586f1cfb06bdee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050534"
---
# <a name="itabletmanager-interface"></a>Itabletmanager-Schnittstelle

Bietet Zugriff auf alle Tablet-PCs, die mit dem Computer verbunden sind.

## <a name="members"></a>Member

Die **itabletmanager** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Itabletmanager** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itabletmanager** -Schnittstelle verfügt über diese Methoden.



| Methode                                                  | BESCHREIBUNG                                                        |
|:--------------------------------------------------------|:-------------------------------------------------------------------|
| [**Gettablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))           | Ruft das angegebene Tablet-Objekt ab.<br/>                  |
| [**Gettabletcount**](itabletmanager-gettabletcount.md) | Ruft die Anzahl der Tablets ab, die an das System angefügt sind.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Entwickler sollten diese Schnittstelle nicht verwenden.

Der folgende Code zeigt, wie die **itabletmanager** -Schnittstelle implementiert wird.

``` syntax
[
    object,
    uuid(764DE8AA-1867-47C1-8F6A-122445ABD89A),
    pointer_default(unique)
]
interface ITabletManager : IUnknown
{
    HRESULT GetDefaultTablet(
        [out] ITablet **ppTablet);

    HRESULT GetTabletCount(
        [out] ULONG *pcTablets);

    HRESULT GetTablet(
        [in] ULONG iTablet,
        [out] ITablet **ppTablet);

    HRESULT GetTabletContextById(
        [in] TABLET_CONTEXT_ID tcid,
        [out] ITabletContext **ppContext);

    HRESULT GetCursorById(
        [in] CURSOR_ID cid,
        [out] ITabletCursor **ppCursor);
};
        
        
```

[**Cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) mit der Klassen-ID "CLSID \_ tabletmanagers" aufrufen und dann " [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) " aufrufen, um einen Zeiger auf die **itabletmanager-Schnittstelle** zu erhalten. Die GUID "CLSID \_ tabletmanagers" ist wie folgt definiert:

``` syntax
#define CLSID_TabletManagerS uuid(A5B020FD-E04B-4e67-B65A-E7DEED25B2CF)
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

