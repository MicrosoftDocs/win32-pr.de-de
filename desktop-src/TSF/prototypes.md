---
title: Prototypen
description: Prototypen
ms.assetid: 2b31c01b-d52b-4df5-9cb0-a35286febd3a
keywords:
- Textdienstframework (TSF), Prototypen
- TSF (Textdienstframework),Prototypes
- TSF-Referenz,Prototypen
- Referenz zu TSF,Prototypen
- Textdienste,Prototypen
- TSF-fähige Anwendungen,Prototypen
- Prototypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417ea7a87e989cd66ae98ecaeae552699a7cead592278a3f156638dac769b02b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117951649"
---
# <a name="prototypes"></a>Prototypen

[ITfContextRenderingMarkup,](/windows/desktop/TSF/itfcontextrenderingmarkup) [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup)und [TF \_ RENDERINGMARKUP,](/windows/desktop/TSF/tf-renderingmarkup) die in diesem Verweis beschrieben werden, sind in IDL- oder Headerdateien nicht definiert. Die folgenden Prototypen müssen vom MIDL-Compiler kompiliert werden, um die Headerdatei zu erhalten.


```C++
typedef struct
{
    ITfRange *pRange;
    TF_DISPLAYATTRIBUTE tfDisplayAttr;
} TF_RENDERINGMARKUP;

// 
// IEnumTfRenderingMarkup 
// 
[
  object,
  uuid(8c03d21b-95a7-4ba0-ae1b-7fce12a72930),
  pointer_default(unique)
]
interface IEnumTfRenderingMarkup : IUnknown
{
    HRESULT Clone([out] IEnumTfRenderingMarkup **ppClone);

    HRESULT Next([in] ULONG ulCount,
                 [out, size_is(ulCount), length_is(*pcFetched)] TF_RENDERINGMARKUP *rgMarkup,
                 [out] ULONG *pcFetched);

    HRESULT Reset();

    HRESULT Skip([in] ULONG ulCount);
};

// 
// ITfContextRenderingMarkup 
// 
[
  object,
  uuid(a305b1c0-c776-4523-bda0-7c5a2e0fef10),
  pointer_default(unique)
]
interface ITfContextRenderingMarkup : IUnknown
{
    const DWORD TF_GRM_INCLUDE_PROPERTY = 0x1;

    HRESULT GetRenderingMarkup([in] TfEditCookie ec,
                               [in] DWORD dwFlags,
                               [in] ITfRange *pRangeCover,
                               [out] IEnumTfRenderingMarkup **ppEnum);
                                                           
    HRESULT FindNextRenderingMarkup([in] TfEditCookie ec,
                                    [in] DWORD dwFlags,
                                    [in] ITfRange *pRangeQuery,
                                    [in] TfAnchor tfAnchorQuery,
                                    [out] ITfRange **ppRangeFound,
                                    [out] TF_RENDERINGMARKUP *ptfRenderingMarkup);
};
```



 

 