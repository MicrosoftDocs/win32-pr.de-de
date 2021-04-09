---
description: Wird von der ieaxisysteminstaller-Schnittstelle aufgerufen, um zu überprüfen, ob ein ActiveX-Objekt installiert werden kann.
ms.assetid: d5cd6263-d07e-4261-9463-b9a06e883f16
title: Ieaxiservicecallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3ad276126548ac6d5fdc2c828f722c90b43ad679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869024"
---
# <a name="ieaxiservicecallback-interface"></a>Ieaxiservicecallback-Schnittstelle

Die **ieaxiservicecallback** -Schnittstelle wird von der [**ieaxisysteminstaller**](ieaxisysteminstaller.md) -Schnittstelle aufgerufen, um zu überprüfen, ob ein ActiveX-Objekt installiert werden kann.

Diese Schnittstelle wird von der [**cieaxiinstallerservice**](cieaxiinstallerservice.md) -Klasse implementiert.

Diese Schnittstelle ist nicht in einem öffentlichen Header deklariert. Anwendungen müssen es selbst definieren. Das folgende IDL-Fragment (Interface Definition Language) beschreibt diese Schnittstelle, einschließlich ihrer IID.

``` syntax
[
    object,
    uuid(1823E7BA-EC36-447a-9B2E-B4912E15AFE7),
    dual,
    nonextensible,
    pointer_default(unique)
]

interface IeAxiServiceCallback : IUnknown
{
    HRESULT VerifyFile(
                       [in] BSTR bstrFileUrl,
                       [out] BSTR * bstrApprovedFileName);
}

```

## <a name="members"></a>Member

Die **ieaxiservicecallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ieaxiservicecallback** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ieaxiservicecallback** -Schnittstelle verfügt über diese Methoden.



| Methode                                                | BESCHREIBUNG                                                                                                                                    |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verifyfile**](ieaxiservicecallback-verifyfile.md) | Führt Sicherheitsüberprüfungen für das angegebene ActiveX-Objekt aus und gibt den Speicherort zurück, an dem die entsprechende CAB-Datei heruntergeladen wurde.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                 |
| IID<br/>                      | IID \_ ieaxiservicecallback ist als 1823e7ba-ec36-447a-9b2e-b4912e15afe7 definiert.<br/>                   |



 

