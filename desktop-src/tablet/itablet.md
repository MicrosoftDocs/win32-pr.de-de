---
description: Stellt ein Tablet dar, das mit dem Computer verbunden ist.
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
ms.openlocfilehash: 76fa7baea2713e5a2e5eaae562b6dac29e002fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356289"
---
# <a name="itablet-interface"></a>ITablet-Schnittstelle

Stellt ein Tablet dar, das mit dem Computer verbunden ist.

## <a name="members"></a>Member

Die **iTablet** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Außerdem gibt** es die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iTablet** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                 | BESCHREIBUNG                                                                           |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**CreateContext**](itablet-createcontext.md)                         | Erstellt ein Kontext Objekt, das das angegebene Tablet-Gerät beschreibt.<br/>       |
| [**GetCursor**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))                                 | Ruft das angegebene [**itabletcursor**](itabletcursor.md) -Objekt ab.<br/>     |
| [**Getcurrsorcount**](itablet-getcursorcount.md)                       | Ruft die Anzahl der dem Tablet zugeordneten Cursor Objekte ab.<br/>         |
| [**Getdefaultcontextsettings**](itablet-getdefaultcontextsettings.md) | Ruft die Standardkontext Einstellungen für das Tablet ab.<br/>                     |
| [**Gethardwarecaps**](itablet-gethardwarecaps.md)                     | Ruft einen Wert ab, der die Funktionen der Tablet-Hardware darstellt.<br/> |
| [**Getmaxinputrect**](itablet-getmaxinputrect.md)                     | Ruft ein Rechteck ab, das den maximalen Eingabebereich des Tablets darstellt.<br/>    |
| [**GetName**](itablet-getname.md)                                     | Ruft eine Zeichenfolge ab, die den Namen des Tablettgeräts enthält.<br/>               |
| [**Getplugandplayid**](itablet-getplugandplayid.md)                   | Ruft eine Zeichenfolge ab, die die Plug & Play ID für das Tablet-Gerät enthält.<br/>  |
| [**GetPropertyMetrics**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))               | Ruft die Metrikdaten für eine angegebene Eigenschaft ab.<br/>                       |



 

## <a name="remarks"></a>Bemerkungen

Entwickler sollten diese Schnittstelle nicht verwenden.

Im folgenden Code wird beschrieben, wie die **iTablet** -Schnittstelle definiert wird.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

