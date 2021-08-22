---
title: IWMDRMNonSilentLicenseAquisition-Schnittstelle
description: Die IWMDRMNonSilentLicenseAquisition-Schnittstelle stellt Methoden bereit, die den Lizenzerwerb ermöglichen, der einen Benutzereingriff erfordert. Diese Schnittstelle kann durch den nicht automatischen Lizenzerwerb erworben werden.
ms.assetid: 57dc3daa-d457-49b0-b589-a72ba180e75e
keywords:
- IWMDRMNonSilentLicenseAquisition-Schnittstelle Windows Media Format
- IWMDRMNonSilentLicenseAquisition-Schnittstelle Windows Media Format , beschrieben
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c953588cb457e8afb21cca38e9daed08b2387ab9fb7871ecd6b17dae9dca152f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110350"
---
# <a name="iwmdrmnonsilentlicenseaquisition-interface"></a>IWMDRMNonSilentLicenseAquisition-Schnittstelle

Die **IWMDRMNonSilentLicenseAquisition-Schnittstelle** stellt Methoden bereit, die den Lizenzerwerb ermöglichen, der einen Benutzereingriff erfordert.

Diese Schnittstelle kann durch den nicht automatischen Lizenzerwerb erworben werden. Nach dem Aufruf [**von IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) wird ein **MEWMDRMLicenseAcquisitionCompleted-Ereignis** generiert. Rufen Sie **die METHODE FÜR DASMEDIAEvent::GetValue** des Ereignisses auf, um einen Zeiger auf eine **IUnknown-Schnittstelle** zu erhalten, die nach einem Zeiger auf eine Instanz dieser Schnittstelle abgefragt werden kann.

## <a name="members"></a>Member

Die **IWMDRMNonSilentLicenseAquisition-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMNonSilentLicenseAquisition** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWMDRMNonSilentLicenseAquisition-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                | Beschreibung                                                                             |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**GetChallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) | Ruft die Lizenzausforderung ab, die an den Lizenzserver gesendet werden soll.<br/> |
| [**Geturl**](iwmdrmnonsilentlicenseaquisition-geturl.md)             | Ruft die URL ab, an die die Lizenzausforderung gesendet werden soll.<br/>           |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen**](drm-interfaces.md)
</dt> <dt>

[**Nicht automatischer Lizenzerwerb**](non-silent-license-acquisition.md)
</dt> </dl>

 

