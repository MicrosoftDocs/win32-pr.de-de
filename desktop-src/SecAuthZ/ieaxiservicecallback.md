---
description: Wird von der IeAxiSystemInstaller-Schnittstelle aufgerufen, um zu überprüfen, ob ein ActiveX-Objekt installiert werden kann.
ms.assetid: d5cd6263-d07e-4261-9463-b9a06e883f16
title: IeAxiServiceCallback-Schnittstelle
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
ms.openlocfilehash: 3313a1744a1fb9a3b34549ca32bb9b0c7cf18977c7785075900c4a11425b5949
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908350"
---
# <a name="ieaxiservicecallback-interface"></a>IeAxiServiceCallback-Schnittstelle

Die **IeAxiServiceCallback-Schnittstelle** wird von der [**IeAxiSystemInstaller-Schnittstelle**](ieaxisysteminstaller.md) aufgerufen, um zu überprüfen, ob ein ActiveX-Objekt installiert werden kann.

Die [**CIeAxiInstallerService-Klasse**](cieaxiinstallerservice.md) implementiert diese Schnittstelle.

Diese Schnittstelle wird nicht in einem öffentlichen Header deklariert. Anwendungen müssen sie selbst definieren. Das folgende IDL-Fragment (Interface Definition Language) beschreibt diese Schnittstelle, einschließlich ihrer IID.

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

Die **IeAxiServiceCallback-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IeAxiServiceCallback** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IeAxiServiceCallback-Schnittstelle** verfügt über diese Methoden.



| Methode                                                | BESCHREIBUNG                                                                                                                                    |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**VerifyFile**](ieaxiservicecallback-verifyfile.md) | Führt Sicherheitsüberprüfungen für das angegebene ActiveX-Objekt aus und gibt den Speicherort zurück, an den die entsprechende .cab-Datei heruntergeladen wurde.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Business, Windows Vista Enterprise, nur Windows Vista \[ Ultimate-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiServiceCallback ist als 1823E7BA-EC36-447a-9B2E-B4912E15AFE7 definiert.<br/>                   |



 

