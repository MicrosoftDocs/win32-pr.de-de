---
description: Speichert Tablet-Kontextinformationen.
ms.assetid: a9eadc83-c3dc-42ba-bd4c-24a4a95563ff
title: Itabletcontext-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContext
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 14c1b34058ebda76f5fd21c6a5d686aa25ae41f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530038"
---
# <a name="itabletcontext-interface"></a>Itabletcontext-Schnittstelle

Speichert Tablet-Kontextinformationen.

## <a name="members"></a>Member

Die **itabletcontext** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="remarks"></a>Bemerkungen

Der folgende Code definiert die **itabletcontext** -Schnittstelle.

``` syntax
[
    object,
    uuid(45AAAF04-9D6F-41AE-8ED1-ECD6D4B2F17F),
    pointer_default(unique)
]
interface ITabletContext : IUnknown
{
    HRESULT GetId(
        [out] TABLET_CONTEXT_ID *pTcid);

    HRESULT GetWindow(
        [out] HWND *pHwnd);

    HRESULT GetSettings(
        [out] TABLET_CONTEXT_SETTINGS **ppTCS);

    HRESULT GetTablet(
        [out] ITablet **ppTablet);

    HRESULT Enable(
        [in] CONTEXT_ENABLE_TYPE cet);

    HRESULT GetOptions(
        [out] DWORD *pdwOptions);

    HRESULT GetPacketDescription(
        [out] PACKET_DESCRIPTION **ppPD);

    HRESULT GetStatus(
        [out] DWORD *pdwStatus);

    HRESULT GetInputRect(
        [out] RECT *prcInput);

    HRESULT SetInputRect(
        [in, unique] RECT *prcInput);

    HRESULT SetDevInputRect(
        [in, unique] RECT *prcInput);

    HRESULT GetDevInputRect(
        [out] RECT *prcInput);

    HRESULT SetCapture(void);

    HRESULT ReleaseCapture(void);

    HRESULT SetCursorCapture(
        [in] CURSOR_ID cid);

    HRESULT ReleaseCursorCapture(
        [in] CURSOR_ID cid);

    HRESULT GetPackets(
        [in] ULONG nBegin,
        [in] ULONG nEnd,
        [in, out] ULONG *pcPkts,
        [in] ULONG cbPkts,
        [out, size_is(cbPkts)] BYTE *pbPkts, 
        [out] CURSOR_ID *pCid
    );

    HRESULT PeekPackets(
        [in] ULONG nBegin,
        [in] ULONG nEnd,
        [in, out] ULONG *pcPkts,
        [in] ULONG cbPkts,
        [out, size_is(cbPkts)] BYTE *pbPkts,
        [out] CURSOR_ID * pCid
    );

    HRESULT FlushPackets(
        [in] ULONG nBegin,
        [in] ULONG nEnd
    );

    HRESULT FlushQueue(void);

    HRESULT GetPacketCount(
        [in]  ULONG nBegin,
        [in]  ULONG nEnd,
        [out] ULONG *pcPkts
    );

    HRESULT GetPacketQueueInfo(
        [out] ULONG *pnBegin,
        [out] ULONG *pnEnd,
        [out] ULONG *pcPkts
    );


    HRESULT ForwardPackets(
        [in] ULONG nBegin,
        [in] ULONG nEnd
    );

    HRESULT InjectPackets(
        [in] ULONG cPkts,
        [in] ULONG cbPkts,
        [in, size_is(cbPkts)] BYTE *pbPkts,
        [in, size_is(cPkts)] CURSOR_ID *pCids
    );

    HRESULT ModifyPackets(
        [in] ULONG nBegin,
        [in] ULONG nEnd,
        [in] ULONG cbPkts,
        [in, size_is(cbPkts)] BYTE *pbPkts
    );

    HRESULT ConvertToScreenCoordinates(
        [in] ULONG cPkts,
        [in] ULONG cbPkts,
        [in, size_is(cbPkts)] BYTE *pbPkts,
        [out, size_is(cPkts)] POINT *pPointsInScreen
   );
};  
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

