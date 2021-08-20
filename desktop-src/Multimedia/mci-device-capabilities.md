---
title: MCI-Gerätefunktionen
description: MCI-Gerätefunktionen
ms.assetid: ac79fbe6-23ea-44ce-ada1-abea1fd07394
keywords:
- MCIWndCanConfig-Makro
- MCIWndCanEject-Makro
- MCIWndCanPlay-Makro
- MCIWndCanRecord-Makro
- MCIWndCanSave-Makro
- MCIWndCanWindow-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f6dbc6b9d1e7bbfc1c1e3651edd40c0f5953989dee6d2462e065d5c2109b5b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117986698"
---
# <a name="mci-device-capabilities"></a>MCI-Gerätefunktionen

MCIWnd enthält die folgenden Makros, mit derenHilfe Sie MCI-Geräte nach ihren Funktionen abfragen können.



| Makro                                      | Beschreibung                                                                                                                                 |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) | Bestimmt, ob ein Gerät über ein Konfigurationsdialogfeld zur Unterstützung mehrerer Konfigurationen verfügt, z. B. das MCIAVI-Gerät.                   |
| [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)   | Bestimmt, ob ein Gerät über eine softwaregesteuerte Auswerfenfunktion verfügt.                                                                       |
| [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)     | Bestimmt, ob ein Gerät den vorhandenen Inhalt wieder geben kann.                                                                                  |
| [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) | Bestimmt, ob ein Gerät aufzeichnen kann.                                                                                                     |
| [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)     | Bestimmt, ob ein Gerät Daten speichern kann.                                                                                                 |
| [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) | Bestimmt, ob ein Gerät MCI-Fensterbefehle unterstützt (z. B. [**fenster**](window.md), [**put**](put.md) und [**where**](where.md)). |



 

Diese Makros geben **TRUE zurück,** wenn das Gerät die spezifische Funktion unterstützt, andernfalls **FALSE.**

 

 




