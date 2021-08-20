---
description: Mit dem Dienst für die Nachverfolgung verteilter Links können Clientanwendungen verschobene Linkquellen nachverfolgen.
ms.assetid: 6f438c72-f23d-4ca4-83bd-fe3bc433ceeb
title: Distributed Link Tracking und Objektbezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6077ec45f99543f42ec8ad61b3763dab4b2a56d6e555832acdc2b3e66feaee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117997662"
---
# <a name="distributed-link-tracking-and-object-identifiers"></a>Distributed Link Tracking und Objektbezeichner

Das Speichern eines Verweises auf eine Datei oder ein Verzeichnis unter Verwendung ihres Pfads und Dateinamens ist nicht zuverlässig. Wenn ein Benutzer eine Datei umbenennt, werden die Links zur Datei unterbrochen. Wenn ein Benutzer das Verzeichnis umbenennt, werden die Links zur Datei sowie alle Dateien und Unterverzeichnisse in der Verzeichnisstruktur unterbrochen.

Mit dem Dienst für die **Nachverfolgung verteilter Links** können Clientanwendungen verschobene Linkquellen nachverfolgen. Clients, die den Linkverfolgungsdienst abonnieren, können die Integrität ihrer Verweise aufrechterhalten, und die Objekte können auf eine Weise nachverfolgt werden, die für den Benutzer transparent ist.

## <a name="object-identifiers"></a>Objektbezeichner

Der Linkverfolgungsdienst behält seinen Link zu einem Objekt mithilfe eines **Objektbezeichners (ID)** bei. Eine Objekt-ID ist ein optionales Attribut, das eine Datei oder ein Verzeichnis auf einem Volume eindeutig identifiziert.

Ein Index aller Objekt-IDs wird auf dem Volume gespeichert. Bei Umbenennungs-, Sicherungs- und Wiederherstellungsvorgängen werden Objekt-IDs beibehalten. Kopiervorgänge behalten objekt-IDs jedoch nicht bei, da dies ihre Eindeutigkeit verletzen würde.

Sie können die folgenden Vorgänge für Objekt-IDs ausführen:

-   Erstellung
-   Löschen
-   Abfrage

Wenn Sie eine Objekt-ID erstellen, richten Sie die Identität der Datei für den Linkverfolgungsdienst ein. Wenn Sie dagegen eine Objekt-ID löschen, beendet der Linkverfolgungsdienst die Verwaltung von Links zur Datei. Eine Liste der Dateisystem-Steuerungscodes, die Vorgänge für Objekt-IDs ausführen, finden Sie unter [Dateiverwaltungs-Steuerungscodes.](file-management-control-codes.md)

Der Distributed Link Tracking-Dienst verfolgt Linkquellen für Shellverknüpfungen und OLE-Links auf NTFS-Dateisystemvolumes nach. Der Linkclient kann einen fehlerhaften Link mit aktualisierten Informationen zum neuen Speicherort der Linkquelle beheben.

## <a name="link-tracking-features"></a>Features für die Linknachverfolgung

Shellverknüpfungen umfassen die heuristische Linknachverfolgung, die einen Struktursuchalgorithmus verwendet, um eine Übereinstimmung für eine verschobene Linkquelle zu finden. Der Suchalgorithmus basiert auf dem letzten bekannten Pfad der Datei- und Dateiinformationen, einschließlich Erstellungsdatum, Dateigröße, Dateiname und Erweiterung.

OLE-Verknüpfung umfasst die gleiche heuristische Linknachverfolgung. Windows enthält auch die gleiche heuristische Linknachverfolgung mit einigen zusätzlichen Verbesserungen bei der Suche nach Namensräumen, um Ergebnisse in einigen gängigen Szenarien zu erzielen. Die Verbesserungen umfassen das folgende Verfahren, das von den von einer Clientanwendung vorgegebenen Zeitlimits abhängt.

**So suchen Sie nach Namensbereichen**

1.  Suchen Sie vier Verzeichnisebenen nach unten im letzten Verzeichnis.
2.  Verschieben Sie ein Verzeichnis nach oben, und wiederholen Sie die Schritte 1 und 2 dreimal. Dies kann zu Ergebnissen führen, wenn das Objekt in der Nähe verschoben wurde.
3.  Suchen Sie vier Ebenen nach unten im Desktopstamm. Dies kann Ergebnisse liefern, wenn das Objekt an einen Speicherort auf demselben Desktop verschoben wurde.
4.  Suchen Sie im Stamm auf jedem lokalen Festplattenlaufwerk vier Ebenen nach unten.
5.  Wiederholen Sie die Schritte 1 bis 3 ohne vier Verzeichnislimits.

> [!Note]  
> Diese Verknüpfungsnachverfolgungsschemas sind für den Endbenutzer transparent. Sie liefern jedoch nicht immer positive Ergebnisse und können zeitaufwändig sein.

 

Weitere Informationen zu Shellverknüpfungen finden Sie unter [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka).

Weitere Informationen zu OLE-Links finden Sie unter [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink).

Wenn ein Link zu einer Datei unter NTFS 3.0 oder höher erstellt wird und die Datei auf ein anderes Volume mit NTFS 3.0 oder höher innerhalb derselben Domäne verschoben wird, kann die Datei vom Nachverfolgungsdienst gefunden werden, je nach Zeitaspekten. Darüber hinaus wird die Datei gefunden, wenn sie außerhalb der Domäne oder innerhalb einer Arbeitsgruppe verschoben wird.

Um die NTFS-Version eines Volumes abzurufen, öffnen Sie eine Eingabeaufforderung mit Administratorzugriffsrechten, und führen Sie den folgenden Befehl aus:

**fsutil fsinfo ntfsinfo** *X::**

wobei *X* der Laufwerkbuchstabe des Volumes ist.

Wenn ein Link zu einer Datei erstellt wird, wird die Zieldatei als **Linkquelle** betrachtet, und der Ersteller des Links ist der **Linkclient.** Wenn beispielsweise eine Shellverknüpfung zum Verknüpfen mit einem Textdokument erstellt wird, ist das Textdokument die Linkquelle, und die Shellverknüpfung ist der Linkclient.

Der Dienst für die Nachverfolgung verteilter Links verwaltet Dateilinks für die folgenden Situationen, die innerhalb einer Domäne auftreten:

-   Die Linkquelldatei wird von einem NTFS-Dateisystemvolume in ein anderes innerhalb derselben Domäne verschoben.
-   Der Name des Computers, der die Linkquelle enthält, wird umbenannt.
-   Die Netzwerkfreigaben auf dem Linkquellcomputer werden geändert.
-   Das Volume, das die Linkquelldatei enthält, wird auf einen anderen Computer innerhalb derselben Domäne verschoben.

Der Dienst für die Nachverfolgung verteilter Links versucht auch in den vorherigen Situationen, Links zu verwalten, auch wenn sie nicht innerhalb einer Domäne auftreten, d. h., sie sind domänenübergreifend oder innerhalb einer Arbeitsgruppe. Verknüpfungen können in diesen Situationen immer beibehalten werden, wenn die Netzwerkfreigabe auf dem Linkquellcomputer geändert wird. Sie können auch beibehalten werden, wenn eine Linkquelle innerhalb eines Computers verschoben wird. Links können in der Regel beibehalten werden, wenn die Linkquelle auf einen anderen Computer verschoben wird, aber diese Art der Nachverfolgung ist im Laufe der Zeit weniger zuverlässig.

## <a name="link-tracking-functionality"></a>Linknachverfolgungsfunktionalität

Die Funktion für die Linknachverfolgung wird hauptsächlich in Form der folgenden beiden Systemdienste implementiert:

-   Überwachung verteilter Verknüpfungen (Client)
-   Distributed Link Tracking Server

<dl> <dt>

<span id="Distributed_Link_Tracking_Client"></span><span id="distributed_link_tracking_client"></span><span id="DISTRIBUTED_LINK_TRACKING_CLIENT"></span>Distributed Link Tracking Client
</dt> <dd>

Der Client für die verteilte Linknachverfolgung wird auf allen Computern ausgeführt und verwaltet die Linknachverfolgungsaktivitäten für diesen Computer. Zu diesen Aktivitäten gehören das Suchen nach Linkquellen und das Verarbeiten von Verschiebungen von Linkquellen. Wenn eine Linkquelle verschoben wird, übergibt der Dienst Informationen an den Server für die verteilte Linknachverfolgung, der auf Domänencontrollern ausgeführt wird.

</dd> <dt>

<span id="Distributed_Link_Tracking_Server"></span><span id="distributed_link_tracking_server"></span><span id="DISTRIBUTED_LINK_TRACKING_SERVER"></span>Distributed Link Tracking Server
</dt> <dd>

Der Server für die Nachverfolgung verteilter Links wird auf jedem Domänencontroller in einer Domäne ausgeführt. Der Dienst akzeptiert Benachrichtigungen über Datei- und Volumebewegungen vom Überwachungsdienst auf einem Computer und ermöglicht es dem Client für die verteilte Linknachverfolgung, den aktuellen Speicherort einer Linkquelle abzufragen.

Dieser Serverdienst verwaltet Informationen zu verschobenen Volumes und Dateien auf den Domänencontrollern. Die Informationen zu Verschiebungen können eine bestimmte Größe nicht überschreitet, und sie werden automatisch entfernt, wenn sie nicht mehr benötigt werden.

</dd> </dl>

Die Linkverfolgungsdienste werden von den [**Schnittstellen IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka) und [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink) verfügbar gemacht. Daher werden sie von Shellverknüpfungen verwendet. Wenn die [**IShellLink::Resolve-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) aufgerufen wird und die Referenzdatei nicht gefunden werden kann, z. B. wenn der Benutzer eine Shellverknüpfung aktiviert, wird der Nachverfolgungsdienst automatisch aufgerufen, um die Datei zu finden. Wenn die [**IOleLink-Implementierung**](/windows/win32/api/oleidl/nn-oleidl-iolelink) beispielsweise in ihrer [**BindToSource-Methode**](/windows/desktop/api/oleidl/nf-oleidl-iolelink-bindtosource) keine Datei finden kann, wird automatisch für den Überwachungsdienst aufgerufen.

## <a name="link-tracking-limitations"></a>Einschränkungen der Linknachverfolgung

Die Distributed Link Tracking-Dienste sind nur im NTFS-Dateisystem und nur für Linkquellen unter NTFS 3.0 oder höher verfügbar. Wenn also eine Linkquelle auf ein FAT-Dateisystemvolume verschoben wird, geht die Nachverfolgungsinformation verloren. Wenn eine Linkquelle zwischen NTFS 3.0 oder höher verschoben wird, aber auf dem Computer, der die Verschiebung ausführt, eine frühere Version von Windows ausgeführt wird, gehen die Informationen zur Linknachverfolgung verloren. Wenn die Informationen zur Linknachverfolgung verloren gegangen sind, wird der Linkquelldatei selbst kein Schaden zugefügt. Sie können von den Distributed Link Tracking Services einfach nicht nachverfolgt werden.

Um die NTFS-Version eines Volumes abzurufen, öffnen Sie eine Eingabeaufforderung mit Administratorzugriffsrechten, und führen Sie den folgenden Befehl aus:

**fsutil fsinfo ntfsinfo** *X::**

wobei *X* der Laufwerkbuchstabe des Volumes ist.

Links zu Dateien auf Wechselmedien werden nicht beibehalten. Außerdem erkennt der Überwachungsdienst ein neues NTFS-Dateisystemvolume erst, wenn das System neu gestartet wird. Ein neues Volume kann verfügbar werden, weil ein FAT-Dateisystemvolume neu an das NTFS-Dateisystem neu partitioniert oder ein neues externes Laufwerk verbunden wird.

 

 
