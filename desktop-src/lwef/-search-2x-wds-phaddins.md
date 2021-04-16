---
title: Entwickeln von Protokoll Handler-Add-ins
description: Sie können Microsoft Windows Desktop Search (WDS) erweitern, um neue Datenspeicher einzuschließen, indem Sie einen benutzerdefinierten Protokollhandler implementieren.
ms.assetid: 2447d95f-5832-453c-8857-3b4f4c158177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a8688621f7d2fda653d769c0e1dfdadd240f49
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516787"
---
# <a name="developing-protocol-handler-add-ins"></a>Entwickeln von Protokoll Handler-Add-ins

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .

Sie können Microsoft Windows Desktop Search (WDS) erweitern, um neue Datenspeicher einzuschließen, indem Sie einen benutzerdefinierten Protokollhandler implementieren.

## <a name="indexing-data-stores-with-protocol-handlers"></a>Indizieren von Daten speichern mit Protokoll Handlern

Bei einem Datenspeicher handelt es sich um eine Inhaltsquelle (ein Datenbanksystem, ein Verzeichnis, ein Dateisystem), in der Daten gespeichert und vom WDS-Indexer durchsucht werden können. Der Speicher kann hierarchisch (z. b. eine Datenbank) oder ein Link basiertes (z. b. eine Website) sein. Ein Protokollhandler ermöglicht das Indizieren von Anwendungen wie WDS zum systematischen durchforsten der Knoten eines Datenspeicher, um relevante Informationen zu extrahieren, die in den Index aufgenommen werden sollen. Jeder Protokollhandler wird verwendet, um einen bestimmten Typ von Datenspeicher zu indizieren. WDS wird mit Protokoll Handlern für Dateisystem Speicher und sowohl für Microsoft Outlook-als auch für Microsoft Outlook Express-Datenspeicher (e-Mail-Speicher) ausgeliefert. PST-Dateien usw.). Beim Indizieren von Outlook-e-Mails durchsucht der Protokollhandler z. b. alle Nachrichten in allen Ordnern, die Informationen aus jeder Nachricht und Anlage extrahieren. Diese Informationen werden an den Indexer für die Einbeziehung in den WDS-Katalog übermittelt.

Häufig müssen Benutzer andere Datenspeicher wie Legacy Datenbanken, e-Mail-Speicher oder Datenstrukturen durchsuchen, die nicht von WDS unterstützt werden. Sie können WDS zum durchforsten eines neuen Datenspeicher erweitern, indem Sie verwenden oder einen Protokollhandler speziell für diesen Datenspeicher implementieren. Zuerst sollten Sie zunächst feststellen, ob bereits ein Protokollhandler für Ihren Datenspeicher vorhanden ist, z. b. für die Verwendung mit einer anderen Anwendung wie SharePoint Services. Wenn dies der Fall ist, können Sie diesen Protokollhandler auf dem System installieren. Wenn jedoch kein anderer Protokollhandler vorhanden ist, müssen Sie einen implementieren. WDS-Protokollhandler verwenden die gleichen Designspezifikationen wie SharePoint Services, und Sie können häufig austauschbar verwendet werden.

Außerdem müssen Sie einen Filter implementieren, um auf den Inhalt von Elementen im Speicher zuzugreifen und ihn zu indizieren, wenn der Datenspeicher andere Daten oder andere Dateitypen als einen der von WDS unterstützten 200-Dateitypen enthält. WDS 2. x verwendet den Protokollhandler und die [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)-Technologie, die von SharePoint Services verwendet werden. Wenn Sie bereits Filter für einen bestimmten Speicher und Dateityp auf dem System installiert haben, der indiziert wird, werden die Daten von WDS mithilfe der vorhandenen Schnittstellen indiziert.

 

## <a name="roadmap-to-adding-new-data-stores"></a>Roadmap zum Hinzufügen neuer Datenspeicher

Zum Erweitern von WDS für die durch Forstung neuer Datenspeicher können Sie einen Protokollhandler und mindestens eines der folgenden Add-Ins erstellen: Kontextmenü Handler, Symbol Handler und ein searchprotocoloptions-Add-in.

1.  Erstellen und registrieren Sie einen Multithread-Protokollhandler für den Datenspeicher:
    -   **Isearchprotocol** : Diese Schnittstelle greift auf ein Protokoll zu und ordnet einer iurlaccessor eine URL zu.
    -   **Iurlaccessor** : Dies ist die Hauptschnittstelle, die für den Zugriff auf Elemente aus der Inhaltsquelle und zum Binden des Inhalts an den entsprechenden Filter verwendet wird.
    -   **Iprotocolhandlersite** : Diese Schnittstelle wird verwendet, um zusätzliche Filter anzufordern und zu laden.
    -   **IFilter** : Diese Schnittstelle gibt die URL der einzelnen Elemente in einem Ordner als Wert Eigenschaften für die Verarbeitung zurück.

    > [!Note]
    >
    > Die minimale Add-in-Funktionalität, die benötigt wird, um Suchergebnisse aus einem nicht hierarchischen Datenspeicher zurückzugeben, ist eine Implementierung der Schnittstellen isearchprotocol und iurlaccessor.

     

2.  Implementieren Sie die isearchprotocoloptions-Schnittstelle, um angepasste protokollhandleroptionen wie vordefinierte Startseiten einzuschließen:
    -   **Isearchprotocoloptions** : Diese Schnittstelle definiert Standard-URLs für den Protokollhandler, die verarbeitet werden sollen, bestimmt, welche Anforderungen für einen Protokollhandler gelten, und bestimmt, ob die Anforderungen für ein bestimmtes System erfüllt sind.
3.  Erweitern Sie Shell, indem Sie die folgenden Schnittstellen implementieren, um Benutzeroberflächen Elemente, wie z. b. Kontextmenüs und Datei spezifische Symbole, einzubeziehen:
    -   **IShellFolder** : Diese Schnittstelle, die zum Verwalten von Ordnern verwendet wird, ist erforderlich, um die IContextMenu-und iextracticon-Schnittstellen für eine URL in einem neuen Speicher bereitzustellen.
    -   **Ipersistfolder** : Diese Schnittstelle ist erforderlich, um ein shellordnerobjekt anzuweisen, sich selbst zu initialisieren.
    -   **Ipersistent** : Diese Schnittstelle stellt den Klassen Bezeichner (CLSID) eines Objekts bereit, das im System dauerhaft gespeichert werden kann.
    -   **IContextMenu** : Diese Schnittstelle definiert das Kontextmenü des Rechtsklick für ein Element, auf das von URL verwiesen wird.
    -   **Iextracticon** : Diese Schnittstelle definiert das Symbol, das für ein Element angezeigt wird, auf das von URL verwiesen wird.
4.  Implementieren Sie einen Mechanismus, um den Indexer über Änderungen an Ihrem Datenspeicher zu benachrichtigen:
    -   **Isearchitemschangedsink** : Diese Schnittstelle ermöglicht dem Protokollhandler, den Index von Änderungen an Ihrem Datenspeicher zu benachrichtigen. Dadurch wird die Leistung verbessert, da der Indexer nicht den gesamten Speicher auf inkrementellen Indizes durchsucht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Implementieren eines Protokoll Handlers für WDS](-search-2x-wds-phimplementing.md)
</dt> <dt>

[Hinzufügen von Symbolen, Vorschauen und Kontextmenüs mit Shellerweiterungen](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[Benachrichtigen des Index von Änderungen](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[Installieren und Registrieren von Protokoll Handlern](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 