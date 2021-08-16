---
title: ProxyStubClsid32
description: Karten eine IID zu einer CLSID in 32-Bit-Proxy-DLLs.
ms.assetid: 8d63d2b1-c8ba-4fe8-8025-e7ceee422ee7
keywords:
- ProxyStubClsid32-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9098ffc7771d3f900489292694ade462a2214e733294a1ed18e6ddb9817692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309896"
---
# <a name="proxystubclsid32"></a>ProxyStubClsid32

Karten eine IID zu einer CLSID in 32-Bit-Proxy-DLLs.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid32 = {CLSID}
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ SZ-Wert,** der die CLSID für die IID angibt.

Dies ist ein erforderlicher Eintrag, da sich die IID-zu-CLSID-Zuordnung bei 16-Bit- und 32-Bit-Schnittstellen unterscheiden kann. Die IID-zu-CLSID-Zuordnung hängt davon ab, wie die Schnittstellenproxys in einen Satz von Proxy-DLLs gepackt werden.

Wenn Sie Schnittstellen hinzufügen, müssen Sie diesen Eintrag verwenden, um sie (32-Bit-Systeme) zu registrieren, damit OLE den entsprechenden Remotingcode finden kann, um eine prozessübergreifende Kommunikation herzustellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)
</dt> <dt>

[**Schnittstelle**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid**](proxystubclsid.md)
</dt> </dl>

 

 