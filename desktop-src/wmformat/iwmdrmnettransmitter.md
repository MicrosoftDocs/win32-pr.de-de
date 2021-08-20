---
title: IWMDRMNetTransmitter-Schnittstelle
description: Die IWMDRMNetTransmitter-Schnittstelle stellt Methoden bereit, die erforderlich sind, um Windows Medien-DRM für Netzwerkgeräte als Sender zu verwenden. Rufen Sie IWMDRMProvider CreateObject auf, um eine Instanz dieser Schnittstelle abzurufen. Übergeben Sie IID \_ IWMDRMNetTransmitter als riid-Parameter.
ms.assetid: e93db52a-8829-4d16-b839-824e34b3e582
keywords:
- IWMDRMNetTransmitter-Schnittstelle windows Media Format
- IWMDRMNetTransmitter-Schnittstelle windows Media Format , beschrieben
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b7526ad349403abdb74f1e5684356af1b51b91f99b40e8e26a3b04932d4e5cf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027558"
---
# <a name="iwmdrmnettransmitter-interface"></a>IWMDRMNetTransmitter-Schnittstelle

Die **IWMDRMNetTransmitter-Schnittstelle** stellt Methoden bereit, die erforderlich sind, um Windows Medien-DRM für Netzwerkgeräte als Sender zu verwenden.

Rufen Sie [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md)auf, um eine Instanz dieser Schnittstelle abzurufen. Übergeben Sie **IID \_ IWMDRMNetTransmitter** als *riid-Parameter.*

## <a name="members"></a>Member

Die **IWMDRMNetTransmitter-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMNetTransmitter** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWMDRMNetTransmitter-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                        | BESCHREIBUNG                                                                                                 |
|:------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) | Generiert eine Antwortnachricht für die Blattlizenz.<br/>                                                       |
| [**GetRootLicenseResponse**](iwmdrmnettransmitter-getrootlicenseresponse.md) | Generiert eine Antwortnachricht für die Stammlizenz.<br/>                                                        |
| [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md)       | Verarbeitet eine Lizenzaufgabe, die von einem Microsoft Windows-Medien-DRM für den Empfänger von Netzwerkgeräten gesendet wird<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMNetReceiver-Schnittstelle**](iwmdrmnetreceiver.md)
</dt> </dl>

 

