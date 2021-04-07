---
title: Iwmdrmnonsilentlicenseaquisition-Schnittstelle
description: Die iwmdrmnonsilentlicenseaquisition-Schnittstelle stellt Methoden bereit, die den Erwerb von Lizenzen ermöglichen, die einen Benutzereingriff erfordern. Diese Schnittstelle kann durch die Ausführung eines nicht automatischen Lizenz Erwerbs abgerufen werden.
ms.assetid: 57dc3daa-d457-49b0-b589-a72ba180e75e
keywords:
- Iwmdrmnonsilentlicenseaquisition-Schnittstelle Windows Media-Format
- Iwmdrmnonsilentlicenseaquisition Interface Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89fce7764b755231812c761778131c159ddd860b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728712"
---
# <a name="iwmdrmnonsilentlicenseaquisition-interface"></a>Iwmdrmnonsilentlicenseaquisition-Schnittstelle

Die **iwmdrmnonsilentlicenseaquisition** -Schnittstelle stellt Methoden bereit, die den Erwerb von Lizenzen ermöglichen, die einen Benutzereingriff erfordern.

Diese Schnittstelle kann durch die Ausführung eines nicht automatischen Lizenz Erwerbs abgerufen werden. Nachdem Sie [**iwmdrmlicensmanagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) aufgerufen haben, wird ein **mewmdrmlicenabacquisitionabgeschlossene** -Ereignis generiert. Aufrufen der **imfmediaevent:: GetValue** -Methode des Ereignisses zum Abrufen eines Zeigers auf eine **IUnknown** -Schnittstelle, die für einen Zeiger auf eine Instanz dieser Schnittstelle abgefragt werden kann.

## <a name="members"></a>Member

Die **iwmdrmnonsilentlicenseaquisition** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwmdrmnonsilentlicenseaquisition** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwmdrmnonsilentlicenseaquisition** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                | BESCHREIBUNG                                                                             |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**Getchallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) | Ruft die Lizenz Herausforderung ab, die auf dem Lizenzserver gesendet werden soll.<br/> |
| [**GetURL**](iwmdrmnonsilentlicenseaquisition-geturl.md)             | Ruft die URL ab, an die die Lizenz Aufforderung gepostet werden soll.<br/>           |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen**](drm-interfaces.md)
</dt> <dt>

[**Nicht automatische Lizenz Beschaffung**](non-silent-license-acquisition.md)
</dt> </dl>

 

