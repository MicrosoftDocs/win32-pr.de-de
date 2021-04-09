---
description: Implementiert die Schnittstellen iaxiservice und ieaxiservicecallback.
ms.assetid: 39f2ee3a-d4fd-4091-acd6-3d6b715bea75
title: Cieaxiinstallerservice-Objekt
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
ms.openlocfilehash: b5ae7ec2a2c904a523f3388fa08a3bf2e44fec9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959007"
---
# <a name="cieaxiinstallerservice-object"></a>Cieaxiinstallerservice-Objekt

Das **cieaxiinstallerservice** -Objekt implementiert die [**iaxiservice**](ieaxiservice.md) -und [**ieaxiservicecallback**](ieaxiservicecallback.md) -Schnittstellen.

Dieses Objekt ist nicht in einem öffentlichen Header deklariert. Anwendungen müssen es selbst definieren. Das folgende IDL-Fragment (Interface Definition Language) beschreibt dieses Objekt, einschließlich seiner CLSID.

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
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iaxiservice**](ieaxiservice.md)
</dt> <dt>

[**Ieaxiservicecallback**](ieaxiservicecallback.md)
</dt> </dl>

 

 




