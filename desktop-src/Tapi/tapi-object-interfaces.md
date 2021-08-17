---
description: Das TAPI-Objekt ist das Hauptobjekt für TAPI 3.
ms.assetid: 046f2646-6043-4d68-a42a-8750c016b3c8
title: TAPI-Objektschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada1e49fe83a75c802b06ded953f309a157365d482d22d06c6bbedf97a5b8ac7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139853"
---
# <a name="tapi-object-interfaces"></a>TAPI-Objektschnittstellen

Das [TAPI-Objekt](tapi-object.md) ist das Hauptobjekt für TAPI 3.

Die [**ITTAPIObjectEvent-Schnittstelle**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) wird nicht direkt für das TAPI-Objekt verfügbar gemacht, ist aber eng damit verknüpft und wird hier zur Referenzfreundlichkeit aufgeführt.



| Schnittstellen                                                 | Beschreibung                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi)                                   | Primäre TAPI 3-Schnittstelle.                                                                                                                              |
| [**ITTAPI2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2)                                 | Leitet sich von [**ITTAPI ab.**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi) stellt zusätzliche Methoden zur Unterstützung von Telefongeräten zur Verfügung.                                                         |
| [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) | Ausgehende Schnittstelle, die zum Empfangen asynchroner Informationen zu TAPI 3-Ereignissen verwendet wird.                                                                       |
| [**ITTAPICallCenter**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter)               | Stellt eine Einstiegsschnittstelle in Callcenter-Steuerelemente bereit.                                                                                                 |
| [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | Stellt Methoden zum Abrufen von Informationen zu TAPI-Objektereignissen zur Verfügung.                                                                                |
| [**ITTAPIObjectEvent2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | Erweitert [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent); stellt eine Methode zum Abrufen eines Zeigers auf das Phone-Objekt, das das TAPI-Objektereignis verursacht hat, zur |



 

 

 
