---
title: Proxystubclsid
description: Ordnet eine IID einer CLSID in 16-Bit-Proxy-DLLs zu.
ms.assetid: 07e1e9de-e529-496c-b9f7-e7f799089f02
keywords:
- Proxystubclsid-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adfbe319903b2e278be342d169a2e523c952693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037367"
---
# <a name="proxystubclsid"></a>Proxystubclsid

Ordnet eine IID einer CLSID in 16-Bit-Proxy-DLLs zu.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid = {CLSID}
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ SZ** -Wert, der die CLSID für die IID angibt.

Wenn Sie Schnittstellen hinzufügen, müssen Sie diesen Eintrag verwenden, um Sie zu registrieren (16-Bit-Systeme), damit OLE den entsprechenden remotingcode finden kann, um prozessübergreifende Kommunikation herzustellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schnittstelle**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid32**](proxystubclsid32.md)
</dt> </dl>

 

 




