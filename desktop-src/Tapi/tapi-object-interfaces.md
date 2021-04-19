---
description: Das TAPI-Objekt ist das Hauptobjekt für TAPI 3.
ms.assetid: 046f2646-6043-4d68-a42a-8750c016b3c8
title: TAPI-Objekt Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906bda205f0d00a54cdb14cf408431cc45cad124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363640"
---
# <a name="tapi-object-interfaces"></a>TAPI-Objekt Schnittstellen

Das [TAPI-Objekt](tapi-object.md) ist das Hauptobjekt für TAPI 3.

Die [**ittapiobjectevent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) -Schnittstelle wird nicht direkt für das TAPI-Objekt verfügbar gemacht, ist jedoch eng mit ihr verknüpft und wird hier zur Verfügung gestellt.



| Schnittstellen                                                 | BESCHREIBUNG                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ittapi**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi)                                   | Primäre TAPI 3-Schnittstelle.                                                                                                                              |
| [**ITTAPI2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2)                                 | Wird von [**ittapi**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi)abgeleitet. bietet zusätzliche Methoden zur Unterstützung von Telefongeräten.                                                         |
| [**Ittapieventnotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) | Ausgehende Schnittstelle, mit der asynchrone Informationen zu TAPI 3-Ereignissen empfangen werden.                                                                       |
| [**Ittapicallcenter**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter)               | Stellt eine Einstiegs Schnittstelle in callcentersteuerelemente bereit.                                                                                                 |
| [**Ittapiobjectevent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | Stellt Methoden zum Abrufen von Informationen zu TAPI-Objekt Ereignissen bereit.                                                                                |
| [**ITTAPIObjectEvent2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | Erweitert [**ittapiobjectevent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent); stellt eine Methode zum Abrufen eines Zeigers auf das Telefon Objekt bereit, das das TAPI-Objekt Ereignis verursacht hat. |



 

 

 
