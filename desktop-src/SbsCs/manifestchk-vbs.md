---
description: Die VBScript-Datei Manifestchk.vbs ist ein Validierungstool, das im Microsoft Windows Software Development Kit (SDK) zur Überprüfung von Anwendungs- und Assemblymanifestdateien bereitgestellt wird.
ms.assetid: 8269cb92-bd3f-411f-8395-fe06ed550cc5
title: Manifestchk.vbs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686843d1b4ab099d44a33b715f65564a12834f54ed6e8f62310df0aedbe53de1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142053"
---
# <a name="manifestchkvbs"></a>Manifestchk.vbs

Die VBScript-Datei Manifestchk.vbs ist ein Validierungstool, das im Microsoft Windows Software Development Kit (SDK) zur Überprüfung von Anwendungs- und Assemblymanifestdateien bereitgestellt wird.

Zum Ausführen dieses Beispiels ist Windows Skripthost erforderlich. Weitere Informationen zu Windows Script Host finden Sie im Abschnitt Windows Script Host des Windows SDK. Windows Der Skripthost ist eigentlich zwei Hosts. CScript.exe ist die Version, mit der Sie Skripts über die Eingabeaufforderung ausführen können. CScript.exe bietet Befehlszeilenschalter zum Festlegen von Skripteigenschaften.

Das Befehlszeilenformat sieht wie folgt aus:

**Cscript :nologo manifestchk.vbs /s:** *\[ Laufwerk: \] \[ \] Pfadschemadateiname* **/m:** *\[ Laufwerk: \] \[ \] Pfadmanifestdateiname* **\[ /q \] /t:** *Option*

Die für Manifestchk.vbs definierten Flags werden in der folgenden Tabelle beschrieben.



| Flag | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /s   | Gibt den Namen der Manifestschemadatei an, anhand derer Manifeste überprüft werden sollen. Informationen zum Schema finden Sie unter [Manifestdateischema.](manifest-file-schema.md)                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| /m   | Gibt den zu überprüfenden Manifestdateinamen an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| /q   | Unterdrückt die gesamte Ausgabe an die Konsole.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| /t   | Gibt den Typ der Manifestdatei an. Die gültigen Werte sind: AM Überprüft das [Manifestdateischema](manifest-file-schema.md) eines [Assemblymanifests](assembly-manifests.md) oder [Anwendungsmanifests.](application-manifests.md)<br/> PC Überprüfen des Schemas der [Herausgeberkonfigurationsdatei](publisher-configuration-file-schema.md) einer [Herausgeberkonfigurationsdatei](publisher-configuration-files.md)<br/> AC Überprüft das Anwendungskonfigurationsdateischema einer [Anwendungskonfigurationsdatei.](application-configuration-files.md)<br/> |



 

Wenn das /q-Flag nicht angegeben ist, zeigt Manifestchk.vbs ausführliche Informationen zum ersten Fehler in der Datei an und zeigt eine Meldung an, die angibt, ob der Überprüfungsprozess erfolgreich war.

Dieses Hilfsprogramm überprüft Folgendes:

-   Eine gültige Befehlszeile.
-   Diese MSXML Version 3 ist installiert.
-   Das Manifest verwendet wohlgeformten XML-Code.
-   Das Manifest stimmt mit dem bereitgestellten Schema überein. Beachten Sie, dass Manifestchk.vbs die Manifestdatei nur basierend auf dem überprüft, was im bereitgestellten Schema angegeben ist. Ein Beispiel für ein Manifestschema finden Sie unter [Manifestdateischema.](manifest-file-schema.md)

Cscript.exe gibt den Wert 0 zurück, wenn der Überprüfungsprozess erfolgreich war, und 1, wenn er nicht erfolgreich war. Wenn ein Befehlszeilenargument einen Fehler enthält, wird 2 zurückgegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwicklungstools für die side-by-Side-Assembly](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 




