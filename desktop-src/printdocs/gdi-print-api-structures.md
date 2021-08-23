---
description: GDI-Druck-API-Strukturen
ms.assetid: 7753a54d-5136-4e46-a5ba-024bcfb961dc
title: GDI-Druck-API-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5af0087ed47123b29d6712df2c842a7f05c0d77997df7c3049cc42e0677a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971469"
---
# <a name="gdi-print-api-structures"></a>GDI-Druck-API-Strukturen

## <a name="in-this-section"></a>In diesem Abschnitt



| Struktur                                                      | Beschreibung                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)<br/>                          | Die [**DEVMODE-Datenstruktur**](/windows/win32/api/wingdi/ns-wingdi-devmodea) enthält Informationen zur Initialisierung und Umgebung eines Druckers oder Anzeigegeräts. <br/>                                                                                                              |
| [**DOCINFO**](/windows/desktop/api/Wingdi/ns-wingdi-docinfoa)<br/>                          | Die [**DOCINFO-Struktur**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) enthält die Eingabe- und Ausgabedateinamen sowie andere Informationen, die von der [**StartDoc-Funktion verwendet**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) werden.<br/>                                                                                                  |
| [**DRAWPATRECT**](/windows/desktop/api/Wingdi/ns-wingdi-drawpatrect)<br/>                  | Die [**DRAWPATRECT-Struktur**](/windows/desktop/api/wingdi/ns-wingdi-drawpatrect) definiert ein zu erstellende Rechteck.<br/>                                                                                                                                                                         |
| [**PSFEATURE \_ CUSTPAPER**](/windows/desktop/api/Wingdi/ns-wingdi-psfeature_custpaper)<br/> | Die [**PSFEATURE \_ CUSTPAPER-Struktur**](/windows/desktop/api/wingdi/ns-wingdi-psfeature_custpaper) enthält Informationen zu einer benutzerdefinierten Papiergröße für einen PostScript Treiber. Diese Struktur wird mit der [**Get \_ PS \_ FEATURESETTING-Drucker-Escapefunktion**](/previous-versions/windows/desktop/legacy/dd144954(v=vs.85)) verwendet.<br/> |
| [**PSFEATURE-AUSGABE \_**](/windows/desktop/api/Wingdi/ns-wingdi-psfeature_output)<br/>       | Die [**PSFEATURE \_ OUTPUT-Struktur**](/windows/desktop/api/wingdi/ns-wingdi-psfeature_output) enthält Informationen zu PostScript Treiberausgabeoptionen. Diese Struktur wird mit der [**Get \_ PS \_ FEATURESETTING-Drucker-Escapefunktion**](/previous-versions/windows/desktop/legacy/dd144954(v=vs.85)) verwendet.<br/>                  |
| [**PSINJECTDATA**](/windows/desktop/api/Wingdi/ns-wingdi-psinjectdata)<br/>                | Die [**PSINJECTDATA-Struktur**](/windows/desktop/api/wingdi/ns-wingdi-psinjectdata) ist ein Header für den Eingabepuffer, der mit der [**POSTSCRIPT INJECTION-Drucker-Escapefunktion \_**](/previous-versions/windows/desktop/legacy/dd162830(v=vs.85)) verwendet wird.<br/>                                                                            |



 

 

