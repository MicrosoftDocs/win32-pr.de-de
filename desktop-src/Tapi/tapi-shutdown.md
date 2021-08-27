---
description: Das ordnungsgemäße Herunterfahren von Kommunikationssitzungen und einer gesamten Anwendung ist erforderlich, um zu verhindern, dass Ressourcen in Aufrufen oder Anwendungen, die sie nicht mehr benötigen, gebunden bleiben.
ms.assetid: 40694b7f-474b-41aa-be3f-48e4ca517a6f
title: TAPI Herunterfahren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88303d2475a2ce0a21478575483c0fd93e44e96b71efa83790b7973343d6d9f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080440"
---
# <a name="tapi-shutdown"></a>TAPI Herunterfahren

Das ordnungsgemäße Herunterfahren von Kommunikationssitzungen und einer gesamten Anwendung ist erforderlich, um zu verhindern, dass Ressourcen in Aufrufen oder Anwendungen, die sie nicht mehr benötigen, gebunden bleiben.

TAPI bietet eine Reihe von Funktionen und Methoden zur Unterstützung des Prozesses. Natürlich muss die Anwendung auch die Verantwortung für die ordnungsgemäße Freigabe des zugeordneten Speichers übernehmen, sei es in Form von Datenstrukturen oder COM-Verweisen.



| TAPI 2.x-Funktionen                                                            | BESCHREIBUNG                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) | Aufheben der Registrierung der Anwendung als Handler für unterstützte Telefonieaufrufe. |
| [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose)                                       | Trennt die Anwendung als Manager für Aufrufe in der angegebenen Zeile.  |
| [**lineShutdown**](/windows/win32/api/tapi/nf-tapi-lineshutdown)                                 | Beendet die Verwendung der Linienabstraktion durch die Anwendung.            |



 



| TAPI 3.x-Schnittstellen oder -Methoden                                            | BESCHREIBUNG                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**ITTAPI::UnregisterNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-unregisternotifications) | Entfernt alle Ereignisbenachrichtigungsregistrierungen, die von der Anwendung ausgeführt werden. |
| [**ITTAPI::Shutdown**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-shutdown)                               | Trennt die Anwendung als Aufruf-Manager.                             |



 

 

 
