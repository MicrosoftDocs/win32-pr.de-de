---
title: IWMDRMIndividualizationStatus-Schnittstelle
description: Die IWMDRMIndividualizationStatus-Schnittstelle ermöglicht das Abrufen erweiterter Statusinformationen zum Fortschritt der Individualisierung. Diese Schnittstelle wird mit MEWMDRMIndividualizationProgress-Ereignissen bereitgestellt.
ms.assetid: 3a148005-22fa-4495-a47c-d9463db16293
keywords:
- IWMDRMIndividualizationStatus-Schnittstelle windows Media Format
- IWMDRMIndividualizationStatus-Schnittstelle Windows Media Format , beschrieben
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe6242d2c66b165be8c750d71c61020e9a6acc66f68654d73898fd5000ace3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701469"
---
# <a name="iwmdrmindividualizationstatus-interface"></a>IWMDRMIndividualizationStatus-Schnittstelle

Die **IWMDRMIndividualizationStatus-Schnittstelle** ermöglicht das Abrufen erweiterter Statusinformationen zum Fortschritt der Individualisierung.

Diese Schnittstelle wird mit MEWMDRMIndividualizationProgress-Ereignissen bereitgestellt. Viele dieser Ereignisse werden zwischen einem Aufruf von [**IWMDRMSecurity::P erformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) und dem Abschluss des Individualisierungsprozesses generiert, was durch die Generierung eines **MEWMDRMIndividualizationCompleted-Ereignisses** signalisiert wird.

Um einen Zeiger auf eine Instanz der **IWMDRMIndividualizationStatus-Schnittstelle** abzurufen, müssen Sie zunächst die **METHODE "POINTERMediaEvent::GetValue"** des Statusereignisses aufrufen. Der Wert, den Sie aus dem Ereignis abrufen, ist ein Zeiger auf die **IUnknown-Schnittstelle** des Objekts, das die **IWMDRMIndividualizationStatus-Schnittstelle** implementiert.

## <a name="members"></a>Member

Die **IWMDRMIndividualizationStatus-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMIndividualizationStatus** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWMDRMIndividualizationStatus-Schnittstelle** verfügt über diese Methoden.



| Methode                                                       | Beschreibung                                                        |
|:-------------------------------------------------------------|:-------------------------------------------------------------------|
| [**GetStatus**](iwmdrmindividualizationstatus-getstatus.md) | Ruft ausführliche Informationen zur Individualisierung ab.<br/> |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Schnittstellen**](drm-interfaces.md)
</dt> </dl>

 

