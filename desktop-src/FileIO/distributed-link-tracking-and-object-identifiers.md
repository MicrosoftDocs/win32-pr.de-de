---
description: Der Dienst für die verteilte Link Überwachung ermöglicht Client Anwendungen das Nachverfolgen von Verknüpfungs Quellen, die verschoben wurden.
ms.assetid: 6f438c72-f23d-4ca4-83bd-fe3bc433ceeb
title: Nachverfolgung verteilter Links und Objekt Bezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d28e151c21fd5320a41950be7647c1e8e0a88b
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "106350653"
---
# <a name="distributed-link-tracking-and-object-identifiers"></a>Nachverfolgung verteilter Links und Objekt Bezeichner

Das Speichern eines Verweises auf eine Datei oder ein Verzeichnis mithilfe des Pfads und des Datei namens ist nicht zuverlässig. Wenn ein Benutzer eine Datei umbenennt, werden die Verknüpfungen zur Datei unterbrochen. Wenn ein Benutzer das Verzeichnis umbenennt, werden die Links zur Datei und alle Dateien und Unterverzeichnisse in der Verzeichnisstruktur unterbrochen.

Der **Dienst für die verteilte Link Überwachung** ermöglicht Client Anwendungen das Nachverfolgen von Verknüpfungs Quellen, die verschoben wurden. Clients, die den Link Überwachungsdienst abonnieren, können die Integrität ihrer Verweise beibehalten, und die Objekte können auf eine Weise verfolgt werden, die für den Benutzer transparent ist.

## <a name="object-identifiers"></a>Objektbezeichner

Der Link Überwachungsdienst verwaltet seinen Link zu einem Objekt mithilfe eines **Objekt Bezeichners (ID)**. Eine Objekt-ID ist ein optionales Attribut, das eine Datei oder ein Verzeichnis auf einem Volume eindeutig identifiziert.

Ein Index aller Objekt-IDs wird auf dem Volume gespeichert. Umbenennungs-, Sicherungs-und Wiederherstellungs Vorgänge erhalten Objekt-IDs. Bei Kopier Vorgängen werden Objekt-IDs jedoch nicht beibehalten, da dies die Eindeutigkeit verletzen würde.

Sie können die folgenden Vorgänge für Objekt-IDs ausführen:

-   Erstellung
-   Löschen
-   Abfrage

Wenn Sie eine Objekt-ID erstellen, legen Sie die Identität der Datei für den Link Überwachungsdienst fest. Wenn Sie hingegen eine Objekt-ID löschen, beendet der Link Überwachungsdienst die Beibehaltung von Links zur Datei. Eine Liste der Dateisystem-Steuerungs Codes, die Vorgänge für Objekt-IDs ausführen, finden Sie unter [File Management Control Codes](file-management-control-codes.md).

Der Dienst für die verteilte Link Überwachung verfolgt Link Quellen für Shellverknüpfungen und OLE-Links innerhalb von NTFS-Dateisystemvolumes. Der Link Client kann eine fehlerhafte Verknüpfung mit aktualisierten Informationen am neuen Speicherort der Verknüpfungs Quelle beheben.

## <a name="link-tracking-features"></a>Features zur Verbindungsverfolgung

Shellverknüpfungen enthalten eine heuristische Link Verfolgung, bei der ein Struktur Suchalgorithmus verwendet wird, um eine Entsprechung für eine verschodelte Verknüpfungs Quelle zu finden. Der Suchalgorithmus basiert auf dem letzten bekannten Pfad der Datei und der Dateiinformationen, die das Erstellungsdatum, die Dateigröße und den Dateinamen und die Erweiterung enthalten.

Die OLE-Verknüpfung umfasst die gleiche heuristische Link Verfolgung. Windows umfasst auch die gleiche heuristische Link Verfolgung mit einigen zusätzlichen Verbesserungen für die Suche nach Namespaces, um Ergebnisse in einigen gängigen Szenarien zu erzielen. Die Verbesserungen umfassen das folgende Verfahren, das von Zeitlimits abhängig ist, die von einer Client Anwendung erhoben werden.

**So suchen Sie nach Namespaces**

1.  Suchen Sie im letzten Verzeichnis vier Verzeichnis Ebenen nach unten.
2.  Verschieben Sie ein Verzeichnis nach oben, und wiederholen Sie die Schritte 1 und 2 drei Mal, was Ergebnisse zur Folge haben kann, wenn sich das Objekt in der Nähe bewegt
3.  Durchsuchen Sie vier Ebenen nach unten vom Desktop Stammverzeichnis, das Ergebnisse erzielen kann, wenn das Objekt an einen Speicherort auf demselben Desktop verschoben wurde.
4.  Suchen Sie auf jedem lokalen Festplattenlaufwerk vier Ebenen nach unten.
5.  Wiederholen Sie die Schritte 1-3 ohne das Limit von vier Verzeichnissen.

> [!Note]  
> Diese Link nach Verfolgungs Schemas sind für den Endbenutzer transparent. Allerdings erzielen Sie nicht immer positive Ergebnisse und können zeitaufwändig sein.

 

Weitere Informationen zu Shellverknüpfungen finden Sie unter [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka).

Weitere Informationen zu OLE-Links finden Sie unter [**iolelink**](/windows/win32/api/oleidl/nn-oleidl-iolelink).

Wenn eine Verknüpfung zu einer Datei auf NTFS 3,0 oder höher hergestellt wird und die Datei in ein beliebiges anderes Volume mit NTFS 3,0 oder höher innerhalb derselben Domäne verschoben wird, kann die Datei vom Überwachungsdienst gefunden werden, sofern diese Überlegungen zur Zeit vorhanden ist. Wenn die Datei außerhalb der Domäne oder in einer Arbeitsgruppe verschoben wird, wird Sie außerdem gefunden.

Wenn Sie die NTFS-Version eines Volumes abrufen möchten, öffnen Sie eine Eingabeaufforderung mit Administrator Rechten, und führen Sie den folgenden Befehl aus:

f & # f: f & gt; **NTF-Info** *X * * *:**

Dabei ist *X* der Laufwerk Buchstabe des Volumes.

Wenn eine Verknüpfung zu einer Datei erstellt wird, wird die Zieldatei als Verknüpfungs **Quelle** betrachtet, und der Ersteller der Verknüpfung ist der **Link Client**. Wenn z. b. eine Shellverknüpfung erstellt wird, um einen Link zu einem Textdokument zu erstellen, ist das Textdokument die Verknüpfungs Quelle, und die Shellverknüpfung ist der Link Client.

Der Dienst für die verteilte Link Überwachung verwaltet Datei Verknüpfungen für die folgenden Situationen, die in einer Domäne auftreten:

-   Die Link Quelldatei wird in derselben Domäne von einem NTFS-Dateisystem Volume in ein anderes verschoben.
-   Der Name des Computers, auf dem sich die Verknüpfungs Quelle befindet, wurde umbenannt.
-   Die Netzwerkfreigaben auf dem Link Quellcomputer werden geändert.
-   Das Volume, das die Link Quelldatei enthält, wird auf einen anderen Computer innerhalb derselben Domäne verschoben.

Der Dienst für die verteilte Link Überwachung versucht auch, Links in den vorangegangenen Situationen beizubehalten, auch wenn Sie nicht innerhalb einer Domäne auftreten, d. h., Sie sind Domänen übergreifend oder innerhalb einer Arbeitsgruppe. Links können immer in diesen Situationen beibehalten werden, wenn die Netzwerkfreigabe auf dem Link Quellcomputer geändert wird. Sie können auch beibehalten werden, wenn eine Verknüpfungs Quelle innerhalb eines Computers verschoben wird. Links können normalerweise beibehalten werden, wenn die Verknüpfungs Quelle auf einen anderen Computer verschoben wird. diese Art der Nachverfolgung ist im Lauf der Zeit jedoch weniger zuverlässig.

## <a name="link-tracking-functionality"></a>Funktionen zur Verbindungs Nachverfolgung

Die Funktion zur Verbindungs Nachverfolgung wird in erster Linie in Form der folgenden beiden Systemdienste implementiert:

-   Überwachung verteilter Verknüpfungen (Client)
-   Verteilter Link Verfolgungs Server

<dl> <dt>

<span id="Distributed_Link_Tracking_Client"></span><span id="distributed_link_tracking_client"></span><span id="DISTRIBUTED_LINK_TRACKING_CLIENT"></span>Verteilter Link nach Verfolgungs Client
</dt> <dd>

Der Client für die verteilte Link Überwachung wird auf allen Computern ausgeführt und verwaltet die Verknüpfungs nach Verfolgungs Aktivitäten für diesen Computer. Diese Aktivitäten umfassen das Suchen nach Verknüpfungs Quellen und das Verarbeiten von Verknüpfungs Quellen Verschiebungen. Wenn eine Verknüpfungs Quelle verschoben wird, übergibt der Dienst Informationen an den verteilten Verbindungs Verfolgungs Server, der auf Domänen Controllern ausgeführt wird.

</dd> <dt>

<span id="Distributed_Link_Tracking_Server"></span><span id="distributed_link_tracking_server"></span><span id="DISTRIBUTED_LINK_TRACKING_SERVER"></span>Verteilter Link Verfolgungs Server
</dt> <dd>

Der Server für die verteilte Link Verfolgung wird auf jedem Domänen Controller in einer Domäne ausgeführt. Der Dienst akzeptiert Benachrichtigungen von Datei-und volumeverschiebungen vom Überwachungsdienst auf einem Computer und ermöglicht es dem Client für die verteilte Link Verfolgung, den aktuellen Speicherort einer Verknüpfungs Quelle abzufragen.

Dieser Server Dienst verwaltet Informationen in den Domänen Controllern über Volumes und Dateien, die verschoben wurden. Die Informationen zu Verschiebungen können nicht über eine bestimmte Größe hinaus zunehmen und werden automatisch entfernt, wenn dies unnötig ist.

</dd> </dl>

Die Link Überwachungsdienste werden von den [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka) -und [**iolelink**](/windows/win32/api/oleidl/nn-oleidl-iolelink) -Schnittstellen verfügbar gemacht. Daher werden Sie von Shellverknüpfungen verwendet. Wenn die [**IShellLink:: Resolve**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) -Methode aufgerufen wird und die Referenzdatei nicht gefunden werden kann, z. b. wenn der Benutzer eine Shellverknüpfung aktiviert, wird der Überwachungsdienst automatisch aufgerufen, um die Datei zu suchen. Ebenso, wenn die [**iolelink**](/windows/win32/api/oleidl/nn-oleidl-iolelink) -Implementierung eine Datei nicht finden kann, z. b. in der [**bindungsource**](/windows/desktop/api/oleidl/nf-oleidl-iolelink-bindtosource) -Methode, ruft Sie automatisch für den Überwachungsdienst auf.

## <a name="link-tracking-limitations"></a>Einschränkungen bei der Link Verfolgung

Die Überwachungsdienste für verteilte Verbindungen sind nur im NTFS-Dateisystem verfügbar und nur für Link Quellen auf NTFS 3,0 oder höher verfügbar. Wenn also eine Verknüpfungs Quelle in ein FAT-Dateisystem Volume verschoben wird, gehen die nach Verfolgungs Informationen verloren. Wenn darüber hinaus eine Verknüpfungs Quelle zwischen NTFS 3,0 oder höher verschoben wird, der Computer, auf dem der Verschiebe Vorgang ausgeführt wird, jedoch eine frühere Version von Windows ausführt, gehen die Informationen zur Verbindungs Nachverfolgung verloren. Wenn die Informationen zur Verbindungs Nachverfolgung verloren gehen, erfolgt keine Beschädigung der Verknüpfungs Quelldatei selbst, Sie kann nicht von den Diensten für die verteilte Verbindungsverfolgung verfolgt werden.

Wenn Sie die NTFS-Version eines Volumes abrufen möchten, öffnen Sie eine Eingabeaufforderung mit Administrator Rechten, und führen Sie den folgenden Befehl aus:

f & # f: f & gt; **NTF-Info** *X * * *:**

Dabei ist *X* der Laufwerk Buchstabe des Volumes.

Links zu Dateien auf Wechselmedien werden nicht beibehalten. Außerdem erkennt der Überwachungsdienst ein neues NTFS-Dateisystem Volume erst, wenn das System neu gestartet wird. Ein neues Volume kann aufgrund der erneuten Partitionierung, dem erneuten Formatieren eines FAT-Dateisystem Volumes in das NTFS-Dateisystem oder dem Verbinden eines neuen externen Laufwerks verfügbar werden.

 

 
