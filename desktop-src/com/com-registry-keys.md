---
title: COM-Registrierungsschlüssel
description: COM-Registrierungsschlüssel
ms.assetid: 08406092-eb77-4001-a4fa-659ce945e4d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76b85bb84b0a6f2e6ccc233b68af2889f4cb11ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856244"
---
# <a name="com-registry-keys"></a>COM-Registrierungsschlüssel

Die Registrierung enthält eine Fülle von Informationen, die von com verwendet werden. Die wichtigsten Informationen werden in den folgenden Schlüsseln gespeichert.



| Schlüssel                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AppID](appid-key.md)<br/>                                   | Gruppiert die Konfigurationsoptionen (einen Satz benannter Werte) für ein oder mehrere verteilte COM-Objekte zu einem Speicherort in der Registrierung. Unterschlüssel unter diesem Schlüssel werden verwendet, um einen Anwendungs Bezeichner (AppID) einem Remote Servernamen zuzuordnen. Zur Vereinfachung der Verwaltung allgemeiner Sicherheits-und Konfigurationseinstellungen werden verteilte COM-Objekte, die von derselben ausführbaren Datei gehostet werden, zu einer AppID gruppiert.<br/>                                                                                                                                                                                                                                                                                                                      |
| [CLSID](clsid-key-hklm.md)<br/>                              | Ein Klassen Bezeichner (CLSID) ist eine Globally Unique Identifier, die ein com-Klassenobjekt identifiziert. Wenn der Server oder Container das Verknüpfen mit eingebetteten Objekten zulässt, registrieren Sie für jede unterstützte Objektklasse eine CLSID. Der CLSID-Schlüssel enthält Informationen, die vom Standard-com-Handler verwendet werden, um Informationen zu einer Klasse zurückzugeben, wenn Sie sich im Zustand wird ausgeführt befindet.<br/> Um eine CLSID für Ihre Anwendung zu erhalten, verwenden Sie uuidgen.exe, das sich im \\ Verzeichnis "TOOLs" des com-Toolkits befindet, oder verwenden Sie " [**cokreateguid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid)". <br/>                                                                                                                                                                                       |
| [ProgID](-progid--key.md)<br/>                               | Eine programmgesteuerte Kennung (ProgID) ist ein Registrierungs Eintrag, der einer CLSID zugeordnet werden kann. Mit der ProgID-Taste wird eine benutzerfreundliche Zeichenfolge einer CLSID zugeordnet. Wie bei der CLSID identifiziert die ProgID eine Klasse, jedoch mit einer geringeren Genauigkeit. Verwenden Sie eine ProgID in Programmier Situationen, in denen eine CLSID nicht verwendet werden kann. ProgIDs sollten nicht in der Benutzeroberfläche angezeigt werden. ProgIDs sind nicht garantiert eindeutig und können daher nur verwendet werden, wenn keine Namenskollisionen auftreten.<br/>                                                                                                                                                                                                                                                      |
| [VersionIndependentProgId](versionindependentprogid.md)<br/> | Ordnet eine ProgID einer CLSID zu. Es wird verwendet, um die neueste Version einer Objekt Anwendung zu bestimmen. Ebenso wie die ProgID kann die Versions unabhängige ProgID mit einem lesbaren Namen registriert werden. <br/> Anwendungen müssen einen Versions unabhängigen programmatischen Bezeichner unter dem versionindependent dentprogid-Schlüssel registrieren. Die Versions unabhängige ProgID bezieht sich auf die-Klasse der Anwendung und ändert sich nicht von Version zu Version, sondern bleibt in allen Versionen konstant. Sie wird mit Makro Sprachen verwendet und verweist auf die aktuell installierte Version der-Klasse der Anwendung. Die Versions unabhängige ProgID muss mit dem Namen der aktuellen Version der Objekt Anwendung übereinstimmen. <br/> |
| [Datei \_ Erweiterung](-file-extension--key.md)<br/>              | Ordnet eine Dateinamenerweiterung einer ProgID zu.<br/> Die im Dateinamen-Erweiterungs Schlüssel enthaltenen Informationen werden von den System-und [dateimonikern](file-monikers.md)verwendet. [**Getclassfile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) verwendet den Schlüssel für die Dateinamenerweiterung zum Bereitstellen der zugeordneten CLSID. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Interface](interface-key.md)<br/>                           | Registriert neue Schnittstellen durch Zuordnen eines Schnittstellen namens zu einem Schnittstellen Bezeichner (IID). IIDs werden spezifischen Informationen zu einer Schnittstelle zugeordnet. Die Informationen sind hauptsächlich für die Verwendung von Schnittstellen über Prozess Grenzen hinweg erforderlich. <br/> Beim Hinzufügen einer neuen Schnittstelle muss der Schnittstellen Schlüssel für com abgeschlossen werden, damit die neue Schnittstelle registriert wird. Es muss ein IID-Unterschlüssel für jede neue Schnittstelle vorhanden sein. <br/>                                                                                                                                                                                                                                                                                                       |
| [Schieren](hkey-local-machine-software-microsoft-ole.md)<br/>     | Steuert die standardmäßigen Start-und Zugriffsberechtigungen für verteilte COM-Objekte sowie Sicherheitsfunktionen auf Aufrufebene für Anwendungen, die nicht [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)aufrufen. Nur Administratoren haben vollen Zugriff auf diesen Teil der Registrierung. Alle anderen Benutzer verfügen über schreibgeschützten Zugriff. <br/>                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von com-Anwendungen](registering-com-applications.md)
</dt> </dl>

 

 





