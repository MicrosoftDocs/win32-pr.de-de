---
title: Bereitstellen von Benutzerberechtigungen für Mediengeräte
description: Standardmäßig gewähren sowohl Windows Vista als auch Windows Server 2008 Administratoren und Benutzern, die direkt auf dem Computer angemeldet sind (Zwischenbenutzer), Lese-/Schreibzugriff.
ms.assetid: 5bb8c8fc-03b4-45b5-816c-45f6cd580de6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1c5827b960405855ba34880e39750b39d4f934e395167479b7cae7912721af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758561"
---
# <a name="providing-user-permissions-for-media-burning-devices"></a>Bereitstellen von Benutzerberechtigungen für Mediengeräte

Standardmäßig gewähren sowohl Windows Vista als auch Windows Server 2008 Administratoren und Benutzern, die direkt auf dem Computer angemeldet sind (Zwischenbenutzer), Lese-/Schreibzugriff. Allerdings muss ein Administrator Windows XP und Windows Server 2003 diesen Geräten Lese-/Schreibberechtigungen für andere Benutzergruppen erteilen.

Ein Administrator kann bestimmte gerätebezogene Berechtigungen für Energiebenutzer und interaktive Benutzer anpassen.

Um den entsprechenden Gruppenberechtigungsbereich in Windows XP zu erreichen, klicken Sie auf **Start**, klicken Sie auf **Ausführen,** geben Sie **gpedit.msc** ein, und klicken Sie dann **auf OK.** Erweitern Sie Gruppenrichtlinie-Schnittstelle **Computerkonfiguration,** erweitern Sie **Windows Einstellungen,** erweitern Sie **Einstellungen,** erweitern Sie **Lokale** Richtlinien, und doppelklicken Sie **auf Sicherheitsoptionen**.

![Screenshot: Fenster "Gruppenrichtlinie" mit einer Richtlinie, die im Bereich "Richtlinie" ausgewählt ist](images/gpolpanel.jpg)

In diesem Bereich muss ein Administrator die Einstellungen von zwei Geräteoptionen angeben, um die erforderlichen Gruppenberechtigungen anzugeben:

-   Legen Sie "Geräte: Cd-ROM-Zugriff auf nur lokal angemeldete Benutzer beschränken" auf **Aktiviert fest.**
-   Legen Sie "Geräte: Dürfen Wechselmedien formatieren und auswerfen" auf **Administratoren und PowerUser fest.** Es ist auch möglich, Windows Vista-Berechtigungen zu emulieren, indem Sie diese Option auf **Administratoren und interaktive Benutzer festlegen.**

Während in Windows XP oder Windows Server 2003 keine bestimmte Benutzeroberfläche für die Verwendung von [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) oder [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)vorhanden ist, ist es möglich, diese APIs zu verwenden, um benutzerdefinierten Benutzergruppen Geräteberechtigungen zu erteilen. Beispielsweise gewährt ein Aufruf von **SetSecurityInfo** Benutzergruppen Berechtigungen. Berechtigungsänderungen mit dieser API sind temporär und werden während eines Neustarts nicht beibehalten. Durch aufrufen [von SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) werden jedoch die Berechtigungsänderungen in der Registrierung implementiert, die während eines Neustarts beibehalten werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von IMAPI](using-imapi.md)
</dt> <dt>

[**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)
</dt> </dl>

 

 