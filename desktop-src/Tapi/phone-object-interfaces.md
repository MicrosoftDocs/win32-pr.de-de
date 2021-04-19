---
description: Das Telefon Objekt ist die Entität, die das eigentliche Telefongerät und alle seine Steuerelemente darstellt.
ms.assetid: 5bc2f595-8e2b-4938-b813-1574a9390084
title: Telefon Objekt Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f39b163e895a512e7adc7be5c2fb848c5849361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359186"
---
# <a name="phone-object-interfaces"></a>Telefon Objekt Schnittstellen

Das Telefon Objekt ist die Entität, die das eigentliche Telefongerät und alle seine Steuerelemente darstellt.

Die [**itphoneevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) -und [**ienumphone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) -Schnittstellen werden nicht direkt auf dem Phone-Objekt verfügbar gemacht, sind jedoch eng damit verknüpft und werden hier als praktische Referenz aufgeführt.



| Schnittstelle                                                  | BESCHREIBUNG                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                 | Ermöglicht den Zugriff auf das Telefongerät auf einer Ebene, die mit der von TAPI 2 verfügbaren vergleichbar ist. *x* -C-API.                                      |
| [**Itautomatedphonecontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) | Stellt Methoden für die automatisierte Steuerung der Töne und Ringe eines Telefons sowie für die automatisierte Anruf Behandlung auf der Grundlage des Status eines Telefonanschlusses bereit. |
| [**Itphoneevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)                       | Ruft die Beschreibung der Telefon Ereignisse ab.                                                                                                |
| [**Ienumphone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)                           | Listet das [**itphone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)auf.                                                                                                    |



 

 

 



