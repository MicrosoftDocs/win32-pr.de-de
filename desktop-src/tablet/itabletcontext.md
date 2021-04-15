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
# <a name="itabletcontext-interface"></a><span data-ttu-id="a90a6-103">Itabletcontext-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a90a6-103">ITabletContext interface</span></span>

<span data-ttu-id="a90a6-104">Speichert Tablet-Kontextinformationen.</span><span class="sxs-lookup"><span data-stu-id="a90a6-104">Stores tablet context information.</span></span>

## <a name="members"></a><span data-ttu-id="a90a6-105">Member</span><span class="sxs-lookup"><span data-stu-id="a90a6-105">Members</span></span>

<span data-ttu-id="a90a6-106">Die **itabletcontext** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="a90a6-106">The **ITabletContext** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="a90a6-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a90a6-107">Remarks</span></span>

<span data-ttu-id="a90a6-108">Der folgende Code definiert die **itabletcontext** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a90a6-108">The following code defines the **ITabletContext** interface.</span></span>

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

## <a name="requirements"></a><span data-ttu-id="a90a6-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a90a6-109">Requirements</span></span>



| <span data-ttu-id="a90a6-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a90a6-110">Requirement</span></span> | <span data-ttu-id="a90a6-111">Wert</span><span class="sxs-lookup"><span data-stu-id="a90a6-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a90a6-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a90a6-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a90a6-113">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a90a6-113">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a90a6-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a90a6-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a90a6-115">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a90a6-115">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a90a6-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a90a6-116">Library</span></span><br/>                  | <dl> <span data-ttu-id="a90a6-117"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a90a6-117"><dt>Wisptis.exe</dt></span></span> </dl> |



 

