---
description: Stellt den Tablet-Kontext dar.
ms.assetid: d518c42d-c2f6-4776-bea5-fecdfe48e260
title: ITabletContextP-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: da5c26a0a9d7d080a9787fef0b7ba2fdb919e473fd66c989fca478c4ac7d0ac3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883520"
---
# <a name="itabletcontextp-interface"></a>ITabletContextP-Schnittstelle

Stellt den Tablet-Kontext dar.

## <a name="members"></a>Member

Die **ITabletContextP-Schnittstelle erbt** von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITabletContextP** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITabletContextP-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                           | Beschreibung                                                                     |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**IsTopMostHook**](itabletcontextp-istopmosthook.md)                                           | Gibt an, ob sich der Tablet-Kontext im obersten Hook befindet.<br/>             |
| [**Überlappen**](itabletcontextp-overlap.md)                                                       | Verschiebt einen Tablet-Kontext an den Vorder- oder Rückseite der Eingabewarteschlange.<br/>      |
| [**TrackInputRect**](itabletcontextp-trackinputrect.md)                                         | Aktualisiert den Tablettdigitalisierer in Fensterpositionszuordnungskoordinaten.<br/> |
| [**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) | Ermöglicht den Zugriff auf den von Tabletthreads gemeinsam genutzten Arbeitsspeicher.<br/>             |
| [**UseSharedMemoryCommunications**](itabletcontextp-usesharedmemorycommunications.md)           | Ermöglicht den Zugriff auf den von Tabletthreads gemeinsam genutzten Arbeitsspeicher.<br/>             |



 

## <a name="remarks"></a>Hinweise

Entwickler sollten diese Schnittstelle nicht verwenden.

[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) ist nur auf Windows Vista und höher verfügbar.

Der folgende Code beschreibt, wie die **ITabletContextP-Schnittstelle** definiert wird.

``` syntax
[
    object,
    uuid(22F74D0A-694F-4f47-A5CE-AE08A6409AC8),
    pointer_default(unique)
]
interface ITabletContextP : ITabletContext
{

    HRESULT Overlap([in] BOOL bTop, [out] DWORD *pdwtcid);

    HRESULT GetType([out] CONTEXT_TYPE *pct);

    HRESULT TrackInputRect([out] RECT *prcInput);

    HRESULT IsTopMostHook();

    HRESULT GetEventSink(
        [out] ITabletEventSink **ppSink);

    HRESULT UseSharedMemoryCommunications(
        [in]  DWORD pid,
        [out] DWORD *phEventMoreData,
        [out] DWORD *phEventClientReady,
        [out] DWORD *phMutexAccess,
        [out] DWORD *phFileMapping);

    HRESULT UseNamedSharedMemoryCommunications(
        [in] DWORD pid,
        [in, string] LPCTSTR szSid,
        [in, string] LPCTSTR sdIlSid,
        [out] DWORD *pdwEventMoreDataId,
        [out] DWORD *pdwEventClientReadyId,
        [out] DWORD *pdwMutexAccessId,
        [out] DWORD *pdwFileMappingId);
};
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

