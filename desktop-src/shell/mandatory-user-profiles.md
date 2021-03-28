---
description: Bei einem obligatorischen Benutzerprofil handelt es sich um eine besondere Art von vorkonfiguriertem Roamingbenutzerprofil, mit dem Administratoren Einstellungen für Benutzer angeben können.
title: Verbindliche Benutzerprofile
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09616c7f-1cec-48a0-a953-d4ae35fbd2f6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 744d35e92a279c5d8a8e8b239fa64bb1960e011a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524424"
---
# <a name="mandatory-user-profiles"></a>Verbindliche Benutzerprofile

Bei einem obligatorischen Benutzerprofil handelt es sich um eine besondere Art von vorkonfiguriertem [Roamingbenutzerprofil](roaming-user-profiles.md) , mit dem Administratoren Einstellungen für Benutzer angeben können. Mit obligatorischen Benutzerprofilen kann ein Benutzer seinen Desktop ändern, die Änderungen werden jedoch nicht gespeichert, wenn sich der Benutzer abmeldet. Wenn sich der Benutzer das nächste Mal anmeldet, wird das vom Administrator erstellte obligatorische Benutzerprofil heruntergeladen. Es gibt zwei Arten von obligatorischen Profilen: *normale verbindliche* Profile und *Super verbindliche* Profile.

Benutzerprofile werden zu obligatorischen Profilen, wenn der Administrator die Datei "Ntuser. dat" (die Registrierungs Struktur) auf dem Server in "Ntuser. man" umbenennt. Die. man-Erweiterung bewirkt, dass das Benutzerprofil ein Schreib geschütztes Profil ist.

Benutzerprofile werden äußerst *obligatorisch* , wenn der Ordnername des Profil Pfads in. man; Beispiel: \\ \\ Server \\ Freigabe \\ mandatoryprofile. man \\ .

Super verbindliche Benutzerprofile ähneln normalen obligatorischen Profilen, mit der Ausnahme, dass sich Benutzer, die über Super verbindliche Profile verfügen, nicht anmelden können, wenn der Server, auf dem das obligatorische Profil gespeichert ist, nicht verfügbar ist. Benutzer mit normalen obligatorischen Profilen können sich mit der lokal zwischengespeicherten Kopie des obligatorischen Profils anmelden.

Nur Systemadministratoren können Änderungen an obligatorischen Benutzerprofilen vornehmen.

 

 



