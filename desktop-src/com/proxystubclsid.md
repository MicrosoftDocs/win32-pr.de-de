---
title: ProxyStubClsid
description: Karten eine IID zu einer CLSID in 16-Bit-Proxy-DLLs.
ms.assetid: 07e1e9de-e529-496c-b9f7-e7f799089f02
keywords:
- ProxyStubClsid-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f86db768979a72d2d2f0b8c7a137d6b105f4a52d082ec50c6e78ba271fbca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129992"
---
# <a name="proxystubclsid"></a>ProxyStubClsid

Karten eine IID zu einer CLSID in 16-Bit-Proxy-DLLs.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid = {CLSID}
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ SZ-Wert,** der die CLSID für die IID angibt.

Wenn Sie Schnittstellen hinzufügen, müssen Sie diesen Eintrag verwenden, um sie (16-Bit-Systeme) zu registrieren, damit OLE den entsprechenden Remotingcode finden kann, um eine prozessübergreifende Kommunikation herzustellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schnittstelle**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid32**](proxystubclsid32.md)
</dt> </dl>

 

 




