---
description: Ein obligatorisches Benutzerprofil ist ein spezieller Typ von vorkonfiguriertem Roamingbenutzerprofil, mit dem Administratoren Einstellungen für Benutzer angeben können.
title: Erforderliche Benutzerprofile
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09616c7f-1cec-48a0-a953-d4ae35fbd2f6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 748135affd0b6be399242ff171c88a45da3047911f0603f47eccf0a1f0ba0018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117678144"
---
# <a name="mandatory-user-profiles"></a>Erforderliche Benutzerprofile

Ein obligatorisches Benutzerprofil ist ein spezieller Typ von vorkonfiguriertem [Roamingbenutzerprofil,](roaming-user-profiles.md) mit dem Administratoren Einstellungen für Benutzer angeben können. Mit obligatorischen Benutzerprofilen kann ein Benutzer seinen Desktop ändern, aber die Änderungen werden nicht gespeichert, wenn sich der Benutzer abmeldet. Wenn sich der Benutzer das nächste Mal anmeldet, wird das vom Administrator erstellte erforderliche Benutzerprofil heruntergeladen. Es gibt zwei Arten von obligatorischen Profilen: *normale obligatorische* Profile und *überfällige* Profile.

Benutzerprofile werden zu obligatorischen Profilen, wenn der Administrator die Datei NTuser.dat (die Registrierungsstruktur) auf dem Server in NTuser.man umbenennt. Die MAN-Erweiterung bewirkt, dass das Benutzerprofil ein schreibgeschütztes Profil ist.

Benutzerprofile werden *überschreibend,* wenn der Ordnername des Profilpfads auf .man endet. z. B. \\ \\ die \\ Serverfreigabe \\ mandatoryprofile.man \\ .

Überfällige Benutzerprofile ähneln normalen obligatorischen Profilen, mit der Ausnahme, dass Sich Benutzer mit übermäßig obligatorischen Profilen nicht anmelden können, wenn der Server, auf dem das obligatorische Profil gespeichert wird, nicht verfügbar ist. Benutzer mit normalen obligatorischen Profilen können sich mit der lokal zwischengespeicherten Kopie des obligatorischen Profils anmelden.

Nur Systemadministratoren können Änderungen an obligatorischen Benutzerprofilen vornehmen.

 

 



