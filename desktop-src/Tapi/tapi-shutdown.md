---
description: Das ordnungsgemäße Herunterfahren von Kommunikationssitzungen und einer gesamten Anwendung ist erforderlich, um zu verhindern, dass Ressourcen in aufrufen oder Anwendungen, die Sie nicht mehr benötigen, gebunden bleiben.
ms.assetid: 40694b7f-474b-41aa-be3f-48e4ca517a6f
title: TAPI Herunterfahren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661273a3d72559d965fa1ea6066f1090f8e6b6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357014"
---
# <a name="tapi-shutdown"></a>TAPI Herunterfahren

Das ordnungsgemäße Herunterfahren von Kommunikationssitzungen und einer gesamten Anwendung ist erforderlich, um zu verhindern, dass Ressourcen in aufrufen oder Anwendungen, die Sie nicht mehr benötigen, gebunden bleiben.

TAPI stellt eine Reihe von Funktionen und Methoden bereit, um den Prozess zu unterstützen. Natürlich muss die Anwendung auch die Verantwortung für die ordnungsgemäße Freigabe von zugewiesener Speicher übernehmen, egal ob in Form von Datenstrukturen oder com-verweisen.



| TAPI 2. x-Funktionen                                                            | BESCHREIBUNG                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**lineregisterrequestrecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) | Hebt die Registrierung der Anwendung als Handler für unterstützte telefonieaufrufe auf. |
| [**lineclose**](/windows/win32/api/tapi/nf-tapi-lineclose)                                       | Trennt die Anwendung als Manager für Aufrufe in der angegebenen Zeile.  |
| [**LineShutdown**](/windows/win32/api/tapi/nf-tapi-lineshutdown)                                 | Fährt die Verwendung der Zeilen Abstraktion durch die Anwendung herunter.            |



 



| TAPI 3. x-Schnittstellen oder-Methoden                                            | BESCHREIBUNG                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**Ittapi:: UnregisterNotification**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-unregisternotifications) | Entfernt alle Ereignis Benachrichtigungs Registrierungen, die von der Anwendung ausgeführt werden. |
| [**Ittapi:: Shutdown**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-shutdown)                               | Trennt die Anwendung als einen-Callcenter.                             |



 

 

 
