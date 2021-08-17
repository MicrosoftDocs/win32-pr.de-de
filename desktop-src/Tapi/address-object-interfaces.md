---
description: Adressobjekte sind Entitäten, die Aufrufe tätigen oder empfangen können. Die zugehörigen Schnittstellen und Methoden ermöglichen einer Anwendung das Erhalten und Festlegen von Informationen zu einer Adresse, z. B. ob die Adresse Überrufer-ID-Unterstützung hat.
ms.assetid: 6e347e4c-aec3-4bbd-95f3-a68e6e136e11
title: Adressobjektschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2254ba47e81ebd40f5ce95a1c870c363d09243c69cec0c4ec358cf3ee5604de7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949176"
---
# <a name="address-object-interfaces"></a>Adressobjektschnittstellen

[Adressobjekte sind](address-object.md) Entitäten, die Aufrufe tätigen oder empfangen können. Die zugehörigen Schnittstellen und Methoden ermöglichen einer Anwendung das Erhalten und Festlegen von Informationen zu einer Adresse, z. B. ob die Adresse Überrufer-ID-Unterstützung hat.

Die [**Schnittstellen ITAddressEvent,**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) [**ITAddressTranslationInfo,**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo) [**ITCallingCard,**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard) [**ITForwardInformation,**](/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation) [**ITLocationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo)und [**IEnumAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress) werden nicht direkt im Adressobjekt verfügbar gemacht, sondern sind eng damit verknüpft und werden hier zur Referenzfreundlichkeit aufgeführt.



| Schnittstelle                                                            | BESCHREIBUNG                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)                                       | Fungiert als Basisschnittstelle für das Address-Objekt.                                                                                                  |
| [**ITAddress2**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress2)                                     | Leitet sich von [**ITAddress ab.**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress) stellt zusätzliche Methoden zur Unterstützung von Telefongeräten zur Verfügung.                                            |
| [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities)               | Ruft Informationen zu den Funktionen einer Adresse ab.                                                                                          |
| [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent)                             | Stellt Informationen zu Adressereignissen zur Verfügung.                                                                                                 |
| [**ITAddressTranslation**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation)                 | Führt eine Adressübersetzung aus.                                                                                                                   |
| [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo)         | Ruft Informationen zur Adressübersetzung ab.                                                                                                           |
| [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard)                               | Stellt Methoden zum Abrufen von Anrufkarteninformationen zur Verfügung.                                                                                          |
| [**ITForwardInformation**](/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation)                 | Stellt Methoden zum Einrichten und Implementieren der Aufrufweiterleitung zur Anwendung.                                                                               |
| [**ITLegacyAddressMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol)   | Unterstützt Ältere Anwendungen, die direkten Zugriff auf ein Gerät und dessen Konfiguration erfordern.                                                      |
| [**ITLegacyAddressMediaControl2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itlegacyaddressmediacontrol2) | Erweitert [**ITLegacyAddressMediaControl,**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol) indem die Konfiguration von Parametern im Zusammenhang mit Liniengeräten ermöglicht wird. |
| [**ITLocationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo)                             | Ruft Informationen ab, die sich auf den Speicherort der aufrufenden Partei bezieht.                                                                                  |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                             | Ruft Informationen zu den Medienunterstützungsfunktionen einer Adresse ab.                                                                            |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)                       | Ruft Informationen zu verfügbaren Terminals ab und stellt eine Methode zum Erstellen zusätzlicher Terminals bereit.                                                   |
| [**IEnumAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress)                                 | Enumeriert [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress).                                                                                                      |
| [**IEnumCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallingcard)                         | Enumeriert [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard).                                                                                              |



 

Wenn die Adresse eine [Wave-MSP-Adresse](wave-msp.md) ist, wird die [**ITLegacyWaveSupport-Schnittstelle**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacywavesupport) auch für das Address-Objekt verfügbar gemacht.

 

 
