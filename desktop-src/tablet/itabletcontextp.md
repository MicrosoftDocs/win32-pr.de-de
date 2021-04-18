---
description: Stellt den Tablet-Kontext dar.
ms.assetid: d518c42d-c2f6-4776-bea5-fecdfe48e260
title: Itabletcontextp-Schnittstelle
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
ms.openlocfilehash: 5b3b6a69deeaa30c3fa0e16b1b36094dceaff304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351132"
---
# <a name="itabletcontextp-interface"></a>Itabletcontextp-Schnittstelle

Stellt den Tablet-Kontext dar.

## <a name="members"></a>Member

Die **itabletcontextp** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Itabletcontextp** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itabletcontextp** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                           | BESCHREIBUNG                                                                     |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**Istopmosthook**](itabletcontextp-istopmosthook.md)                                           | Gibt an, ob sich der Tablet-Kontext im Top-Hook befindet.<br/>             |
| [**Überlappen**](itabletcontextp-overlap.md)                                                       | Verschiebt einen Tablet-Kontext an die Vorder-oder Rückseite der Eingabe Warteschlange.<br/>      |
| [**Trackinputrect**](itabletcontextp-trackinputrect.md)                                         | Aktualisiert den Tablet-Digitalisierer auf Fenster Speicherort-Mapping-Koordinaten.<br/> |
| [**Usenamedsharedmemorycommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) | Ermöglicht den Zugriff auf Arbeitsspeicher, der für tablettthreads freigegeben<br/>             |
| [**"US-haredmemorycommunications"**](itabletcontextp-usesharedmemorycommunications.md)           | Ermöglicht den Zugriff auf Arbeitsspeicher, der für tablettthreads freigegeben<br/>             |



 

## <a name="remarks"></a>Bemerkungen

Entwickler sollten diese Schnittstelle nicht verwenden.

" [**Usenamedsharedmemorycommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) " ist nur unter Windows Vista und höher verfügbar.

Im folgenden Code wird beschrieben, wie die **itabletcontextp** -Schnittstelle definiert wird.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

