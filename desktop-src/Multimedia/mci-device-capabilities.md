---
title: MCI-Gerätefunktionen
description: MCI-Gerätefunktionen
ms.assetid: ac79fbe6-23ea-44ce-ada1-abea1fd07394
keywords:
- Mciwndcanconfig-Makro
- Mciwndcaneject-Makro
- Mciwndcanplay-Makro
- Mciwndcanrecord-Makro
- Mciwndcansave-Makro
- Mciwndcanwindow-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59effd4e00106a2bb0175bf39b7eb07fa8b65d30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037513"
---
# <a name="mci-device-capabilities"></a>MCI-Gerätefunktionen

Mciwnd umfasst die folgenden Makros, damit Sie MCI-Geräte auf ihre Funktionen Abfragen können.



| Makro                                      | Beschreibung                                                                                                                                 |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Mciwndcanconfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) | Bestimmt, ob ein Gerät über ein Konfigurations Dialogfeld verfügt, das mehrere Konfigurationen unterstützt, z. b. das MCIAVI-Gerät.                   |
| [**Mciwndcaneject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)   | Bestimmt, ob ein Gerät über eine softwaregesteuerte Auswerfen-Funktion verfügt.                                                                       |
| [**Mciwndcanplay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)     | Bestimmt, ob ein Gerät den vorhandenen Inhalt wiedergeben kann.                                                                                  |
| [**Mciwndcanrecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) | Bestimmt, ob ein Gerät aufzeichnen kann.                                                                                                     |
| [**Mciwndcansave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)     | Bestimmt, ob ein Gerät Daten speichern kann.                                                                                                 |
| [**Mciwndcanwindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) | Bestimmt, ob ein Gerät MCI-Fenster Befehle unterstützt (z. b. [**Fenster**](window.md), [**Put**](put.md) und [**Where**](where.md)). |



 

Diese Makros geben " **true** " zurück, wenn das Gerät die bestimmte Funktion unterstützt, andernfalls " **false** ".

 

 




