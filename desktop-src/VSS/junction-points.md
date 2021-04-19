---
description: In Windows Vista und Windows Server 2008 haben sich die Standard Speicherorte für Benutzerdaten und Systemdaten geändert.
ms.assetid: 78679851-91f5-447f-8580-12cbf0323fb8
title: Verknüpfungs Punkte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57f1823c67e2c6b95ae366b7604054b47305062e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360204"
---
# <a name="junction-points"></a>Verknüpfungs Punkte

In Windows Vista und Windows Server 2008 haben sich die Standard Speicherorte für Benutzerdaten und Systemdaten geändert. Beispielsweise werden Benutzerdaten, die zuvor im Verzeichnis "% System Drive% \\ Documents and Settings" gespeichert waren, jetzt im Verzeichnis "% System Drive% Users" gespeichert \\ . Aus Gründen der Abwärtskompatibilität haben die alten Standorte Verbindungspunkte, die auf die neuen Speicherorte verweisen. Beispiel: "c: \\ Dokumente und Einstellungen" ist jetzt ein Verknüpfungs Punkt, der auf "c: Users" zeigt \\ . Sicherungs Anwendungen müssen in der Lage sein, Verknüpfungs Punkte zu sichern und wiederherzustellen.

Diese Verknüpfungs Punkte können wie folgt identifiziert werden:

-   Die Attribute "File Attribute Analyse \_ \_ Point", " \_ file \_ Attribute Hidden" und "File Attribute \_ System File" sind \_ \_ festgelegt.
-   Außerdem haben Sie Zugriffs Steuerungs Listen (ACLs) festgelegt, um allen Benutzern den Lesezugriff zu verweigern.

Anwendungen, die einen bestimmten Pfad aufzurufen, können diese Verknüpfungs Punkte durchlaufen, wenn Sie über die erforderlichen Berechtigungen verfügen. Allerdings führt der Versuch, den Inhalt der Verknüpfungs Punkte aufzulisten, zu Fehlern. Aus zwei Gründen ist es wichtig, dass Sicherungs Anwendungen diese Verknüpfungs Punkte nicht durchlaufen oder versuchen, Daten darunter zu sichern:

-   Dies kann dazu führen, dass die Sicherungs Anwendung die gleichen Daten mehrmals sichert.
-   Sie kann auch zu Zyklen (Zirkel Verweise) führen.

## <a name="per-user-junctions-and-system-junctions"></a>Per-User-und System Anschlüsse

Die Verknüpfungs Punkte, die zur Bereitstellung von Datei-und Registrierungsvirtualisierung in Windows Vista und Windows Server 2008 verwendet werden, können in zwei Klassen unterteilt werden: pro Benutzer-und System Anschlüsse.

Pro-Benutzer-Verbindungen werden im Profil jedes einzelnen Benutzers erstellt, um die Abwärtskompatibilität für Benutzer Anwendungen zu gewährleisten. Der Verknüpfungs Punkt bei c: \\ Benutzer \\ *Benutzername* \\ meine Dokumente, die auf c: \\ Benutzer \\ *Benutzername* \\ Dokumente zeigt, ist ein Beispiel für eine benutzerspezifische Verknüpfung. Benutzerspezifische Verbindungen werden vom Profil Dienst erstellt, wenn das Profil des Benutzers erstellt wird.

Die anderen Verbindungen sind System Knotenpunkte, die sich nicht unter dem Benutzer \\ *Namen* Verzeichnis des Benutzers befinden. Zu den System Knotenpunkten zählen beispielsweise folgende:

-   Dokumente und Einstellungen
-   Verbindungen in den Benutzerprofilen "alle Benutzer", "öffentlich" und "Standard"

System Anschlüsse werden von userenv.dll erstellt, wenn Sie von der Windows-Willkommensseite aufgerufen wird (auch als "Machine out-of-Box-do" bezeichnet oder "MOOBE" bezeichnet).

> [!Note]  
> Wenn der Benutzer die Systemsprache in eine andere Sprache als Englisch ändert, werden die Verknüpfungs Punkte pro Benutzer und System mit lokalisierten Namen erstellt.

 

 

 



