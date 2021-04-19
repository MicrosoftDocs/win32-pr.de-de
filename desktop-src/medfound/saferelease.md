---
description: Saferelease
ms.assetid: 2e9af7bc-f478-4a9c-b28f-b0a72fa9ec75
title: Saferelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0661b8515c1d8a79c81eef19f49cf8996fcbf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360129"
---
# <a name="saferelease"></a>Saferelease


Viele der Codebeispiele in dieser Dokumentation verwenden die folgende Funktion zum Freigeben von COM-Schnittstellen Zeigern.


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
> Diese Funktion ist nicht in einem SDK-Header definiert. Um diese Funktion verwenden zu können, müssen Sie Sie in Ihrem eigenen Code definieren.

 

Diese Funktion gibt den Zeiger *ppT* frei und legt ihn gleich **null** fest.

Eine andere Möglichkeit ist die Verwendung einer intelligenten Zeiger Klasse, z. b. **CComPtr**, die im Active Template Library (ATL) definiert ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Info über Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)
</dt> </dl>

 

 
