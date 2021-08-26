---
title: IWMDRMNetReceiver-Schnittstelle
description: Die IWMDRMNetReceiver-Schnittstelle stellt Methoden bereit, die erforderlich sind, um Microsoft Windows Media DRM für Netzwerkgeräte als Empfänger zu verwenden. Rufen Sie IWMDRMProvider CreateObject auf, um eine Instanz dieser Schnittstelle abzurufen. Übergeben Sie IID \_ IWMDRMNetReceiver als riid-Parameter.
ms.assetid: 29966260-c0aa-4e7e-b827-a872c7429333
keywords:
- IWMDRMNetReceiver-Schnittstelle windows Medienformat
- IWMDRMNetReceiver-Schnittstelle windows Media Format , beschrieben
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cb917d7d229b81a6792461c506b2a6b50aaee2af3bd5f133e44273077924f86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930110"
---
# <a name="iwmdrmnetreceiver-interface"></a>IWMDRMNetReceiver-Schnittstelle

Die **IWMDRMNetReceiver-Schnittstelle** stellt Methoden bereit, die erforderlich sind, um Microsoft Windows Media DRM für Netzwerkgeräte als Empfänger zu verwenden.

Rufen Sie [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md)auf, um eine Instanz dieser Schnittstelle abzurufen. Übergeben Sie **IID \_ IWMDRMNetReceiver** als *riid-Parameter.*

## <a name="members"></a>Member

Die **IWMDRMNetReceiver-Schnittstelle** erbt von [**IWMDRMEventGenerator.**](iwmdrmeventgenerator.md) **IWMDRMNetReceiver** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWMDRMNetReceiver-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                               | BESCHREIBUNG                                                                                                                     |
|:-------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**GetLicenseChallenge**](iwmdrmnetreceiver-getlicensechallenge.md)                 | Generiert eine Lizenzaufforderung, die beim Anfordern geschützter Inhalte an den Sender gesendet wird.<br/>                     |
| [**GetRegistrationChallenge**](iwmdrmnetreceiver-getregistrationchallenge.md)       | Generiert eine Registrierungsaufforderung, die an den Sender gesendet wird, wenn der Empfänger registriert oder erneut validiert wird.<br/> |
| [**ProcessLicenseResponse**](iwmdrmnetreceiver-processlicenseresponse.md)           | Verarbeitet die Lizenzantwort, die vom Sender als Antwort auf eine Lizenzaufforderung gesendet wird.<br/>                              |
| [**ProcessRegistrationResponse**](iwmdrmnetreceiver-processregistrationresponse.md) | Verarbeitet die Registrierungsantwort, die vom Sender als Antwort auf eine Registrierungsaufforderung gesendet wird.<br/>                    |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> <dt>

[**IWMDRMNetTransmitter-Schnittstelle**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





