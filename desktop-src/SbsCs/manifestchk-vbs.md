---
description: Die VBScript-Datei Manifestchk.vbs ist ein Überprüfungs Tool, das im Microsoft Windows Software Development Kit (SDK) zur Validierung von Anwendungs-und assemblymanifestressdateien bereitgestellt wird.
ms.assetid: 8269cb92-bd3f-411f-8395-fe06ed550cc5
title: Manifestchk.vbs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09aff347fbd8b6f44c4e38f123870fa5ee8df572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393594"
---
# <a name="manifestchkvbs"></a>Manifestchk.vbs

Die VBScript-Datei Manifestchk.vbs ist ein Überprüfungs Tool, das im Microsoft Windows Software Development Kit (SDK) zur Validierung von Anwendungs-und assemblymanifestressdateien bereitgestellt wird.

Das Ausführen dieses Beispiels erfordert den Windows Script Host. Weitere Informationen zu Windows Script Host finden Sie im Abschnitt Windows Script Host des Windows SDK. Windows Script Host ist tatsächlich zwei Hosts. CScript.exe ist die Version, mit der Sie Skripts von der Eingabeaufforderung aus ausführen können. CScript.exe stellt Befehls Zeilenschalter für das Festlegen von Skript Eigenschaften bereit.

Das Befehlszeilen Format lautet wie folgt:

**Cscript//nologo manifestchk.vbs/s:** *\[ Laufwerk: \] \[ Pfad \] Schema Dateiname* **/m:** *\[ Laufwerk: \] \[ path \] ManifestFileName* **\[ /q \] /t:** *Option*

Die für Manifestchk.vbs definierten Flags werden in der folgenden Tabelle beschrieben.



| Flag | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /s   | Gibt den Namen der Manifest-Schema Datei an, anhand derer überprüft werden soll. Weitere Informationen finden Sie im Schema unter [Manifest-Datei Schema](manifest-file-schema.md).                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| /m   | Gibt den zu validierenden Manifest-Dateinamen an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| /q   | Unterdrückt die gesamte Ausgabe in der Konsole.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| /t   | Gibt den Typ der Manifest-Datei an. Gültige Werte sind: am Validate das [Manifest-Datei Schema](manifest-file-schema.md) eines Assemblymanifests oder [](assembly-manifests.md) [Anwendungs Manifests](application-manifests.md) .<br/> PC überprüft das [Schema der Verleger Konfigurationsdatei](publisher-configuration-file-schema.md) einer [Verleger Konfigurationsdatei](publisher-configuration-files.md) .<br/> AC überprüft das Anwendungs Konfigurationsdatei-Schema einer [Anwendungs Konfigurationsdatei](application-configuration-files.md).<br/> |



 

Wenn das/q-Flag nicht angegeben ist, zeigt Manifestchk.vbs ausführliche Informationen zum ersten Fehler an, der in der Datei aufgetreten ist, und zeigt eine Meldung an, die angibt, ob der Überprüfungs Vorgang erfolgreich war.

Dieses Hilfsprogramm prüft folgendes:

-   Eine gültige Befehlszeile.
-   MSXML Version 3 ist installiert.
-   Das Manifest verwendet wohl geformtes XML.
-   , Dass das Manifest mit dem bereitgestellten Schema übereinstimmt. Beachten Sie, dass Manifestchk.vbs die Manifestressource nur anhand der Angaben im bereitgestellten Schema überprüft. Ein Beispiel für ein Manifest-Schema finden Sie unter [Manifest-Datei Schema](manifest-file-schema.md).

Cscript.exe gibt den Wert 0 (null) zurück, wenn der Überprüfungsprozess erfolgreich war, und 1, wenn er nicht erfolgreich war. Wenn ein Fehler in einem Befehlszeilenargument vorliegt, wird 2 zurückgegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Parallele assemblyentwicklungtools](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 




