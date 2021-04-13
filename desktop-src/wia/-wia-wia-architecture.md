---
description: WIA wird als Component Object Model (com) out-of-Process-Server implementiert, um den robusten Betrieb von Client Anwendungen zu gewährleisten.
ms.assetid: 9f3d1848-36ab-4e0f-a7f4-312bc85ecc00
title: WIA-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09652258ee249fb3c68e65472e863ccd35154ee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560671"
---
# <a name="wia-architecture"></a>WIA-Architektur

WIA wird als Component Object Model (com) out-of-Process-Server implementiert, um den robusten Betrieb von Client Anwendungen zu gewährleisten. Im Gegensatz zu den meisten Prozess Server Anwendungen vermeidet die Windows-Abbild Beschaffung (WIA) während der Abbild Datenübertragung durch die Bereitstellung eines eigenen Datenübertragungsmechanismus ( [**iwiadatatransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer)) Leistungseinbußen. Diese Hochleistungs Schnittstelle verwendet ein frei gegebenes Speicherfenster zum Übertragen von Daten an den Client.

WIA umfasst drei Hauptkomponenten: eine Device Manager, eine Minidriver-Dienst Bibliothek und ein Geräte-Mini Treiber.

-   Der Device Manager listet Abbild Erstellungs Geräte auf, ruft Geräteeigenschaften ab, richtet Ereignisse für Geräte ein und erstellt Geräte Objekte.
-   Die Minidriver-Dienst Bibliothek implementiert alle Dienste, die Geräte unabhängig sind.
-   Der Geräte-Mini Treiber ordnet einem bestimmten Gerät WIA-Eigenschaften und-Befehle zu.

Das folgende Diagramm veranschaulicht die WIA-Architektur:

![WIA-Architektur](images/wiarch.gif)

 

 



