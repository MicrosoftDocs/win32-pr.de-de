---
description: Implementiert die Schnittstellen IAxiService und IeAxiServiceCallback.
ms.assetid: 39f2ee3a-d4fd-4091-acd6-3d6b715bea75
title: CIeAxiInstallerService-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIeAxiInstallerService
api_type:
- COM
api_location: ''
ms.openlocfilehash: d8e96600762db414fa93316098d5ba87dabfbc3138f516d3d69f1740d0d33d2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783086"
---
# <a name="cieaxiinstallerservice-object"></a>CIeAxiInstallerService-Objekt

Das **CIeAxiInstallerService-Objekt** implementiert die [**Schnittstellen IAxiService**](ieaxiservice.md) und [**IeAxiServiceCallback.**](ieaxiservicecallback.md)

Dieses Objekt wird nicht in einem öffentlichen Header deklariert. Anwendungen müssen sie selbst definieren. Das folgende IDL-Fragment (Interface Definition Language) beschreibt dieses Objekt, einschließlich seiner CLSID.

``` syntax
[
        uuid(90F18417-F0F1-484E-9D3C-59DCEEE5DBD8)
]
    coclass CIeAxiInstallerService
    {
        [default] interface IeAxiService;
        interface IeAxiServiceCallback;
    }

```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Business, Windows Vista Enterprise, nur Windows Vista \[ Ultimate-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAxiService**](ieaxiservice.md)
</dt> <dt>

[**IeAxiServiceCallback**](ieaxiservicecallback.md)
</dt> </dl>

 

 




