---
title: COM-Registrierungsschlüssel
description: COM-Registrierungsschlüssel
ms.assetid: 08406092-eb77-4001-a4fa-659ce945e4d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80800bda0123823fec85a514c19031d485b17baca729969b4e74e5f08516eecd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048498"
---
# <a name="com-registry-keys"></a>COM-Registrierungsschlüssel

Die Registrierung enthält eine Vielzahl von Informationen, die von COM verwendet werden. Die wichtigsten Informationen werden in den folgenden Schlüsseln gespeichert.



| Key                                                                 | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AppID](appid-key.md)<br/>                                   | Unterteilt die Konfigurationsoptionen (einen Satz benannter Werte) für ein oder mehrere verteilte COM-Objekte an einem Speicherort in der Registrierung. Unterschlüssel unter diesem Schlüssel werden verwendet, um einen Anwendungsbezeichner (AppID) einem Remoteservernamen zu zuordnen. Um die Verwaltung gemeinsamer Sicherheits- und Konfigurationseinstellungen zu vereinfachen, werden verteilte COM-Objekte, die von derselben ausführbaren Datei gehostet werden, in einer AppID gruppiert.<br/>                                                                                                                                                                                                                                                                                                                      |
| [Clsid](clsid-key-hklm.md)<br/>                              | Ein Klassenbezeichner (CLSID) ist ein global eindeutiger Bezeichner, der ein COM-Klassenobjekt identifiziert. Wenn der Server oder Container das Verknüpfen mit eingebetteten Objekten zulässt, registrieren Sie eine CLSID für jede unterstützte Klasse von Objekten. Der CLSID-Schlüssel enthält Informationen, die vom COM-Standardhandler verwendet werden, um Informationen zu einer Klasse zurück zu geben, wenn sie sich im Ausführungszustand befindet.<br/> Um eine CLSID für Ihre Anwendung zu erhalten, verwenden Sie uuidgen.exe im VERZEICHNIS TOOLs des \\ COM-Toolkits, oder verwenden Sie [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid). <br/>                                                                                                                                                                                       |
| [ProgID](-progid--key.md)<br/>                               | Ein programmgesteuerter Bezeichner (ProgID) ist ein Registrierungseintrag, der einer CLSID zugeordnet werden kann. Der ProgID-Schlüssel ordnet einer CLSID eine benutzerfreundliche Zeichenfolge zu. Wie die CLSID identifiziert die ProgID eine Klasse, jedoch mit weniger Genauigkeit. Verwenden Sie eine ProgID in Programmiersituationen, in denen es nicht möglich ist, eine CLSID zu verwenden. ProgIDs sollten nicht auf der Benutzeroberfläche angezeigt werden. ProgIDs sind nicht garantiert eindeutig, sodass sie nur verwendet werden können, wenn keine Namenskollisionen auftreten.<br/>                                                                                                                                                                                                                                                      |
| [VersionIndependentProgID](versionindependentprogid.md)<br/> | Ordnet eine ProgID einer CLSID zu. Sie wird verwendet, um die neueste Version einer Objektanwendung zu bestimmen. Wie die ProgID kann auch die versionsunabhängige ProgID mit einem für Menschen lesbaren Namen registriert werden. <br/> Anwendungen müssen einen versionsunabhängigen programmgesteuerten Bezeichner unter dem Schlüssel VersionIndependentProgID registrieren. Die versionsunabhängige ProgID bezieht sich auf die -Klasse der Anwendung und ändert sich nicht von Version zu Version, sondern bleibt in allen Versionen konstant. Sie wird mit Makrosprachen verwendet und verweist auf die derzeit installierte Version der -Klasse der Anwendung. Die versionsunabhängige ProgID muss dem Namen der neuesten Version der Objektanwendung entsprechen. <br/> |
| [\_Dateierweiterung](-file-extension--key.md)<br/>              | Ordnet eine Dateierweiterung einer ProgID zu.<br/> Informationen, die im Dateierweiterungsschlüssel enthalten sind, werden sowohl vom Systemmoniker als auch vom [Dateimoniker verwendet.](file-monikers.md) [**GetClassFile verwendet**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) den Dateinamenerweiterungsschlüssel, um die zugeordnete CLSID zu geben. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Interface](interface-key.md)<br/>                           | Registriert neue Schnittstellen durch Zuordnen eines Schnittstellennamens zu einem Schnittstellenbezeichner (IID). Sie ordnet IIDs spezifischen Informationen zu einer Schnittstelle zu. Die Informationen sind hauptsächlich für die Verwendung von Schnittstellen über Prozessgrenzen hinweg erforderlich. <br/> Beim Hinzufügen einer neuen Schnittstelle muss der Schnittstellenschlüssel abgeschlossen werden, damit COM die neue Schnittstelle registrieren kann. Es muss einen IID-Unterschlüssel für jede neue Schnittstelle geben. <br/>                                                                                                                                                                                                                                                                                                       |
| [Ole](hkey-local-machine-software-microsoft-ole.md)<br/>     | Steuert standardmäßige Start- und Zugriffsberechtigungen für verteilte COM-Objekte sowie Sicherheitsfunktionen auf Aufrufebene für Anwendungen, die [**CoInitializeSecurity nicht aufrufen.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) Nur Administratoren haben Vollzugriff auf diesen Teil der Registrierung. Alle anderen Benutzer haben schreibgeschützten Zugriff. <br/>                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von COM-Anwendungen](registering-com-applications.md)
</dt> </dl>

 

 





