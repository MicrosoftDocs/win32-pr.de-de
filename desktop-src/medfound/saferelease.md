---
description: SafeRelease
ms.assetid: 2e9af7bc-f478-4a9c-b28f-b0a72fa9ec75
title: SafeRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46359821dd1f7741f6038ddb2f33cec591aacdf1bf9fc7fd3e6004e9d7601e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034868"
---
# <a name="saferelease"></a>SafeRelease


Viele der Codebeispiele in dieser Dokumentation verwenden die folgende Funktion, um COM-Schnittstellenze0er frei zu geben.


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



> [!Note]  
> Diese Funktion ist nicht in einem SDK-Header definiert. Um diese Funktion zu verwenden, müssen Sie sie in Ihrem eigenen Code definieren.

 

Diese Funktion gibt den Zeiger *ppT frei* und legt ihn auf **NULL fest.**

Eine weitere Möglichkeit besteht in der Verwendung einer intelligenten Zeigerklasse, z. B. **CComPtr,** die im Active Template Library (ATL) definiert ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Info über Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)
</dt> </dl>

 

 
