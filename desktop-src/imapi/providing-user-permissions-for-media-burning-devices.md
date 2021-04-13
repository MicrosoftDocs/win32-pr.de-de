---
title: Bereitstellen von Benutzerberechtigungen für Medien brennende Geräte
description: Standardmäßig gewähren sowohl Windows Vista als auch Windows Server 2008 Administratoren und Benutzern, die direkt auf dem Computer angemeldet sind (zwischen Benutzern), Lese-/Schreibzugriff.
ms.assetid: 5bb8c8fc-03b4-45b5-816c-45f6cd580de6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613eb1bba9a18cfb08e1eee3e6b86c34235ab8e9
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "104218919"
---
# <a name="providing-user-permissions-for-media-burning-devices"></a>Bereitstellen von Benutzerberechtigungen für Medien brennende Geräte

Standardmäßig gewähren sowohl Windows Vista als auch Windows Server 2008 Administratoren und Benutzern, die direkt auf dem Computer angemeldet sind (zwischen Benutzern), Lese-/Schreibzugriff. In Windows XP und Windows Server 2003 muss ein Administrator diesen Geräten jedoch Lese-/Schreibberechtigungen für andere Benutzergruppen erteilen.

Ein Administrator kann bestimmte gerätebezogene Berechtigungen für Poweruser und interaktive Benutzer anpassen.

Um den entsprechenden Bereich für Gruppenberechtigungen in Windows XP zu erreichen, klicken Sie auf **Start**, klicken Sie auf **Ausführen**, geben Sie **gpeer dit. msc** ein, und klicken Sie dann auf **OK**. Erweitern Sie in der Gruppenrichtlinie-Schnittstelle **Computer Konfiguration**, erweitern Sie **Windows-Einstellungen**, erweitern Sie **Sicherheitseinstellungen**, erweitern Sie **lokale Richtlinien**, und doppelklicken Sie auf **Sicherheitsoptionen**.

![Screenshot, der das Fenster "Gruppenrichtlinie" mit einer Richtlinie anzeigt, die im Bereich "Richtlinie" ausgewählt ist.](images/gpolpanel.jpg)

In diesem Bereich muss ein Administrator die Einstellungen der beiden Geräteoptionen angeben, um die erforderlichen Gruppenberechtigungen bereitzustellen:

-   Legen Sie "Geräte: Beschränken des CD-ROM-Zugriffs auf lokal angemeldete Benutzer" auf " **aktiviert** " fest.
-   Legen Sie für **Administratoren und Hauptbenutzer** den Wert "Geräte: erlaubt zum Formatieren und Auswerfen von Wechselmedien" fest. Es ist auch möglich, Windows Vista-Berechtigungen zu emulieren, indem Sie diese Option auf **Administratoren und interaktive Benutzer** festlegen.

Obwohl eine bestimmte Benutzeroberfläche in Windows XP oder Windows Server 2003 für die Verwendung von [**setsecurityinfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) oder [setupdisetdeviceregistryproperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)nicht vorhanden ist, können diese APIs verwendet werden, um benutzerdefinierten Benutzergruppen Geräte Berechtigungen zu erteilen. Beispielsweise wird durch einen Aufrufen von **setsecurityinfo** Berechtigungen für Benutzergruppen erteilt. Berechtigungs Änderungen mit dieser API sind temporär und werden nicht über einen Neustart hinweg beibehalten. Durch Aufrufen von [setupdisetdeviceregistryproperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) werden jedoch die Berechtigungs Änderungen in der Registrierung implementiert, die bei einem Neustart beibehalten werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von IMAPI](using-imapi.md)
</dt> <dt>

[**Setsecurityinfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[Setupdisetdeviceregistryproperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)
</dt> </dl>

 

 