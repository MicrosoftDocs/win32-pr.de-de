---
description: Stellt ein Tablet dar, das an den Computer angefügt ist.
ms.assetid: 31e11f7d-5610-4c49-9203-2dc322fbef95
title: ITablet-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: a0cb98a74758d701e7ab6322567d2a20606380a58fc43676ad5edb136cec999b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712250"
---
# <a name="itablet-interface"></a>ITablet-Schnittstelle

Stellt ein Tablet dar, das an den Computer angefügt ist.

## <a name="members"></a>Member

Die **ITablet-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITablet** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITablet-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                 | BESCHREIBUNG                                                                           |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**CreateContext**](itablet-createcontext.md)                         | Erstellt ein Kontextobjekt, das das angegebene Tablettgerät beschreibt.<br/>       |
| [**GetCursor**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))                                 | Ruft das angegebene [**ITabletCursor-Objekt**](itabletcursor.md) ab.<br/>     |
| [**GetCursorCount**](itablet-getcursorcount.md)                       | Ruft die Anzahl der Cursorobjekte ab, die dem Tablet zugeordnet sind.<br/>         |
| [**GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md) | Ruft die Standardkontexteinstellungen für das Tablet ab.<br/>                     |
| [**GetHardwareCaps**](itablet-gethardwarecaps.md)                     | Ruft einen Wert ab, der die Funktionen der Tabletthardware darstellt.<br/> |
| [**GetMaxInputRect**](itablet-getmaxinputrect.md)                     | Ruft ein Rechteck ab, das den maximalen Eingabebereich des Tablets darstellt.<br/>    |
| [**GetName**](itablet-getname.md)                                     | Ruft eine Zeichenfolge ab, die den Namen des Tablettgeräts enthält.<br/>               |
| [**GetPlugAndPlayId**](itablet-getplugandplayid.md)                   | Ruft eine Zeichenfolge ab, die die Plug & Play-ID für das Tablettgerät enthält.<br/>  |
| [**GetPropertyMetrics**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))               | Ruft die Metrikdaten für eine angegebene Eigenschaft ab.<br/>                       |



 

## <a name="remarks"></a>Hinweise

Entwickler sollten diese Schnittstelle nicht verwenden.

Der folgende Code beschreibt, wie die **ITablet-Schnittstelle** definiert wird.

``` syntax
[
    object,
   uuid(1CB2EFC3-ABC7-4172-8FCB-3BC9CB93E29F),
    pointer_default(unique)
]
interface ITablet : IUnknown
{
    HRESULT GetDefaultContextSettings(
        [out] TABLET_CONTEXT_SETTINGS **ppTCS);

    HRESULT CreateContext(
        [in] HWND hWnd,
        [in, unique] RECT *prcInput,
        [in] DWORD dwOptions,
        [in, unique] TABLET_CONTEXT_SETTINGS *pTCS,
        [in] CONTEXT_ENABLE_TYPE cet,
        [out] ITabletContext **ppCtx,
        [in, out, unique] TABLET_CONTEXT_ID *pTcid,
        [in, out, unique] PACKET_DESCRIPTION **ppPD,
        [in, unique] ITabletEventSink *pSink);

    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetMaxInputRect(
        [out] RECT *prcInput);

    HRESULT GetHardwareCaps(
        [out] DWORD *pdwCaps);

    HRESULT GetPropertyMetrics(
        [in] REFGUID rguid,
        [out] PROPERTY_METRICS *pPM);

    HRESULT GetPlugAndPlayId(
        [out] LPWSTR *ppwszPPId);

    HRESULT GetCursorCount(
        [out] ULONG *pcCurs);

    HRESULT GetCursor(
        [in] ULONG iCur,
        [out] ITabletCursor **ppCur);
};   
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

