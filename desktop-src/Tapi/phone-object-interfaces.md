---
description: Das Telefon objekt ist die Entität, die das tatsächliche Telefongerät und alle seine Steuerelemente darstellt.
ms.assetid: 5bc2f595-8e2b-4938-b813-1574a9390084
title: Telefon Objektschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e146910b8184f35057843f20ad663e2be21d2c4844852e7cca3939e1e979d00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873270"
---
# <a name="phone-object-interfaces"></a>Telefon Objektschnittstellen

Das Telefon objekt ist die Entität, die das tatsächliche Telefongerät und alle seine Steuerelemente darstellt.

Die [**Schnittstellen ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) und [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) werden nicht direkt im Telefon-Objekt verfügbar gemacht, sondern sind eng damit verknüpft und werden hier zur Vereinfachung aufgeführt.



| Schnittstelle                                                  | BESCHREIBUNG                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                 | Ermöglicht den Zugriff auf das Telefongerät auf einer Ebene, die mit der mit TAPI 2 verfügbaren vergleichbar ist. *x* C-API.                                      |
| [**ITAutomatedPhoneControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) | Stellt Methoden für die automatisierte Steuerung der Töne und Ringe eines Telefons sowie für die automatisierte Anrufbehandlung basierend auf dem Hookswitch-Zustand eines Telefons zur Seite. |
| [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)                       | Ruft die Beschreibung von Telefonereignissen ab.                                                                                                |
| [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)                           | Enumeriert [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone).                                                                                                    |



 

 

 



