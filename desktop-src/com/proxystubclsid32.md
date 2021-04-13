---
title: ProxyStubClsid32
description: Ordnet eine IID einer CLSID in 32-Bit-Proxy-DLLs zu.
ms.assetid: 8d63d2b1-c8ba-4fe8-8025-e7ceee422ee7
keywords:
- ProxyStubClsid32 Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d1d70ad2deb4f747ecf57fd12f0707ac8b2b9d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316556"
---
# <a name="proxystubclsid32"></a>ProxyStubClsid32

Ordnet eine IID einer CLSID in 32-Bit-Proxy-DLLs zu.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid32 = {CLSID}
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ SZ** -Wert, der die CLSID für die IID angibt.

Dies ist ein erforderlicher Eintrag, da die Zuordnung zwischen IID und CLSID für 16-Bit-und 32-Bit-Schnittstellen unterschiedlich sein kann. Die Zuordnung zwischen IID und CLSID hängt davon ab, wie die Schnittstellen Proxys in einen Satz von Proxy-DLLs gepackt werden.

Wenn Sie Schnittstellen hinzufügen, müssen Sie diesen Eintrag verwenden, um Sie zu registrieren (32-Bit-Systeme), damit OLE den entsprechenden remotingcode finden kann, um prozessübergreifende Kommunikation herzustellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Von IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)
</dt> <dt>

[**Schnittstelle**](interface-key.md)
</dt> <dt>

[**Proxystubclsid**](proxystubclsid.md)
</dt> </dl>

 

 