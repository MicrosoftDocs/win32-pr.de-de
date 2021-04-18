---
description: Adress Objekte sind Entitäten, die Aufrufe erstellen oder empfangen können. Die zugehörigen Schnittstellen und Methoden ermöglichen es einer Anwendung, Informationen zu einer Adresse zu erhalten und festzulegen, z. b. ob die Adresse eine Aufruferkennung unterstützt.
ms.assetid: 6e347e4c-aec3-4bbd-95f3-a68e6e136e11
title: Adress Objekt Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef19db02123e10e839906a00931ef246d19d2c0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347684"
---
# <a name="address-object-interfaces"></a>Adress Objekt Schnittstellen

[Adress Objekte](address-object.md) sind Entitäten, die Aufrufe erstellen oder empfangen können. Die zugehörigen Schnittstellen und Methoden ermöglichen es einer Anwendung, Informationen zu einer Adresse zu erhalten und festzulegen, z. b. ob die Adresse eine Aufruferkennung unterstützt.

Die Schnittstellen [**itadressevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent), [**itadresstranslationinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo), [**itcallingcard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard), [**itforwardinformation**](/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation), [**itlocationinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo)und [**ienumaddress**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress) werden nicht direkt für das Adress Objekt verfügbar gemacht, sind jedoch eng damit verknüpft und werden hier zur Verfügung gestellt.



| Schnittstelle                                                            | BESCHREIBUNG                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Itaddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)                                       | Fungiert als Basisschnittstelle für das Address-Objekt.                                                                                                  |
| [**ITAddress2**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress2)                                     | Abgeleitet von " [**itaddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress);" bietet zusätzliche Methoden zur Unterstützung von Telefongeräten.                                            |
| [**Itaddress-Funktionen**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities)               | Ruft Informationen zu den Funktionen einer Adresse ab.                                                                                          |
| [**Itadressssevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent)                             | Stellt Informationen zu Adress Ereignissen bereit.                                                                                                 |
| [**Itadresssstranslations**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation)                 | Führt die Adressübersetzung aus.                                                                                                                   |
| [**Itadresssstranslationinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo)         | Ruft Informationen zur Adressübersetzung ab.                                                                                                           |
| [**Itcallingcard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard)                               | Stellt Methoden zum Abrufen von Aufruf Karteninformationen bereit.                                                                                          |
| [**Itforwardinformation**](/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation)                 | Stellt Methoden zum Einrichten und Implementieren der aufrufweiterleitung bereit.                                                                               |
| [**Itlegacyaddressmediacontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol)   | Unterstützt Legacy Anwendungen, die einen direkten Zugriff auf ein Gerät und seine Konfiguration erfordern.                                                      |
| [**ITLegacyAddressMediaControl2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itlegacyaddressmediacontrol2) | Erweitert [**itlegacyaddressmediacontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol) durch das Zulassen der Konfiguration von Parametern, die sich auf Linien Geräte beziehen. |
| [**Itlocationinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo)                             | Ruft Informationen im Zusammenhang mit dem Speicherort der aufrufenden Partei ab.                                                                                  |
| [**Itmediasupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                             | Ruft Informationen zu den Medien Unterstützungsfunktionen einer Adresse ab.                                                                            |
| [**Itterminalsupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)                       | Ruft Informationen zu verfügbaren Terminals ab und stellt eine Methode zum Erstellen zusätzlicher Terminals bereit.                                                   |
| [**Iendumaddress**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress)                                 | Listet [**itaddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)auf.                                                                                                      |
| [**Ienumcallingcard**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallingcard)                         | Listet [**itcallingcard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard)auf.                                                                                              |



 

Wenn es sich bei der Adresse um eine [Wave-MSP](wave-msp.md) -Adresse handelt, wird auch die [**itlegacywavesupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacywavesupport) -Schnittstelle für das Adress Objekt verfügbar gemacht.

 

 
