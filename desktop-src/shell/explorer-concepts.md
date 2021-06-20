---
description: Machen Sie sich mit allgemeinen Konzepten vertraut, wenn Sie Windows-Explorer erweitern möchten. Dies ist eine von vielen Erweiterungsoptionen auf der Windows Shell-Benutzeroberfläche.
title: Allgemeine Explorer-Konzepte
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 78136c36-bd3c-4114-8b69-fef4e307566d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: db9b46bf944992a16b6a1b8a9bcad581ec7d661b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404933"
---
# <a name="common-explorer-concepts"></a>Allgemeine Explorer-Konzepte

Der *Shell-Namespace* organisiert das Dateisystem und andere objekte, die von der Shell verwaltet werden, in einer einzelnen strukturstrukturierten Hierarchie. Konzeptionell handelt es sich um eine größere und inklusive version des Dateisystems.

-   [Introduction (Einführung)](#introduction)
-   [Identifizieren von Namespaceobjekten](#identifying-namespace-objects)
    -   [Element-IDs](#item-ids)
    -   [Element-ID-Listen](#item-id-lists)
    -   [PIDLs](#pidls)
    -   [Zuordnen von PIDLs](#allocating-pidls)

## <a name="introduction"></a>Einführung

Eine der Hauptaufgaben der Shell ist die Verwaltung und Bereitstellung des Zugriffs auf die vielzahl von Objekten, aus denen das System besteht. Die zahlreichsten und vertrautsten dieser Objekte sind die Ordner und Dateien, die sich auf Computerdatenträgern befinden. Die Shell verwaltet jedoch auch eine Reihe von Nichtdatei-Systemen oder *virtuellen* Objekten. Beispiele hierfür sind:

-   Netzwerkdrucker
-   Andere Netzwerkcomputer
-   Systemsteuerung Anwendungen
-   Die Papierkorb

Einige virtuelle Objekte enthalten keinen physischen Speicher. Das Druckerobjekt enthält z. B. eine Auflistung von Links zu netzwerkgebundenen Druckern. Andere virtuelle Objekte, z. B. die Papierkorb, können Daten enthalten, die auf einem Laufwerk gespeichert sind, aber anders behandelt werden müssen als normale Dateien. Beispielsweise kann ein virtuelles Objekt verwendet werden, um in einer Datenbank gespeicherte Daten darzustellen. Im Hinblick auf den Namespace können die verschiedenen Elemente in der Datenbank im Windows-Explorer als separate Objekte angezeigt werden, obwohl sie alle in einer einzelnen Datenträgerdatei gespeichert sind.

Virtuelle Objekte können sich sogar auf Remotecomputern befinden. Um beispielsweise das Roaming zu vereinfachen, können die Dokumentdateien eines Benutzers auf einem Server gespeichert werden. Um Benutzern Zugriff auf ihre Dateien von mehreren Desktop-PCs zu gewähren, verweist der ordner Eigene Dokumente auf dem Desktop-PC, den sie derzeit verwenden, auf den Server, nicht auf die Festplatte des Desktop-PCs. Der Pfad enthält entweder ein zugeordnetes Netzwerklaufwerk oder einen UNC-Pfadnamen.

Wie das Dateisystem enthält der Namespace zwei grundlegende Objekttypen: Ordner und Dateien. Ordnerobjekte sind die *Knoten* der Struktur. sie sind Container für Dateiobjekte und andere Ordner. Dateiobjekte sind die *Blätter* der Struktur. Dabei handelt es sich entweder um normale Datenträgerdateien oder virtuelle Objekte, z. B. Druckerlinks. Ordner, die nicht Teil des Dateisystems sind, werden manchmal als *virtuelle Ordner* bezeichnet.

Wie Dateisystemordner variiert die Sammlung virtueller Ordner im Allgemeinen von System zu System. Es gibt drei Klassen von virtuellen Ordnern:

-   Virtuelle Standardordner, z. B. die Papierkorb, die sich auf allen Systemen befinden.
-   Optionale virtuelle Ordner, die Standardnamen und -funktionen aufweisen, aber möglicherweise nicht auf allen Systemen vorhanden sind.
-   Nicht standardmäßige Ordner, die vom Benutzer installiert werden.

Im Gegensatz zu Dateisystemordnern können Benutzer keine neuen virtuellen Ordner selbst erstellen. Sie können nur solche installieren, die von Nicht-Microsoft-Entwicklern erstellt wurden. Die Anzahl virtueller Ordner ist daher normalerweise deutlich geringer als die Anzahl der Dateisystemordner. Eine Erläuterung zur Implementierung virtueller Ordner finden Sie unter [Namespaceerweiterungen.](nse-works.md)

Sie können eine visuelle Darstellung der Struktur des Namespace in der Explorer-Leiste des Windows-Explorer sehen. Der folgende Screenshot von Windows-Explorer zeigt beispielsweise einen relativ einfachen Namespace.

![Screenshot mit einer Ansicht des Shellnamespace](images/prog1.png)

Der endgültige Stamm der Namespacehierarchie ist der Desktop. Direkt unterhalb des Stammverzeichnisses befinden sich mehrere virtuelle Ordner, z. B. Arbeitsplatz und die Papierkorb.

Die Dateisysteme der verschiedenen Datenträgerlaufwerke können als Teilmengen der größeren Namespacehierarchie betrachtet werden. Die Stammordner dieser Dateisysteme sind Unterordner des Ordners Arbeitsplatz. Arbeitsplatz enthält auch die Stammdateien aller zugeordneten Netzlaufwerke. Andere Knoten in der Struktur, z. B. Eigene Dokumente, sind virtuelle Ordner.

## <a name="identifying-namespace-objects"></a>Identifizieren von Namespaceobjekten

Bevor Sie ein Namespaceobjekt verwenden können, müssen Sie es zunächst identifizieren können. Ein Objekt im Dateisystem kann einen Namen wie MyFile.htm haben. Da es möglicherweise andere Dateien mit diesem Namen an anderer Stelle im System gibt, erfordert die eindeutige Identifizierung einer Datei oder eines Ordners einen vollqualifizierten Pfad wie "C: \\ MyDocs \\MyFile.htm". Dieser Pfad ist im Grunde eine sortierte Liste aller Ordner in einem Pfad aus dem Dateisystemstamm C: \\ , der mit der Datei endet.

Im Kontext des -Namespaces sind Pfade immer noch sehr nützlich, um Objekte zu identifizieren, die sich im Dateisystemteil des Namespace befinden. Sie können jedoch nicht für virtuelle Objekte verwendet werden. Stattdessen stellt die Shell eine alternative Möglichkeit zur Identifikation bereit, die mit jedem Namespaceobjekt verwendet werden kann.

### <a name="item-ids"></a>Element-IDs

Innerhalb eines Ordners verfügt jedes Objekt über eine *Element-ID.* Dies ist die funktionale Entsprechung eines Datei- oder Ordnernamens. Die Element-ID ist eigentlich eine [**SHITEMID-Struktur:**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid)


```
typedef struct _SHITEMID { 
    USHORT cb; 
    BYTE   abID[1]; 
} SHITEMID, * LPSHITEMID;
```



Der **abID-Member** ist der Bezeichner des Objekts. Die Länge von **abID** ist nicht definiert, und ihr Wert wird durch den Ordner bestimmt, der das -Objekt enthält. Da es keine Standarddefinition gibt, wie **abID-Werte** von Ordnern zugewiesen werden, sind sie nur für das zugeordnete Ordnerobjekt sinnvoll. Anwendungen sollten sie einfach als Token behandeln, das ein Objekt in einem bestimmten Ordner identifiziert. Da die Länge von **abID** variiert, enthält der **cb-Member** die Größe der [**SHITEMID-Struktur**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) in Bytes.

Da Element-IDs für Anzeigezwecke nicht nützlich sind, weist der Ordner, der das Objekt enthält, normalerweise einen Anzeigenamen zu. Dies ist der Name, der von Windows-Explorer verwendet wird, wenn der Inhalt eines Ordners angezeigt wird. Weitere Informationen zur Behandlung von Anzeigenamen finden Sie unter [Abrufen von Informationen aus einem Ordner.](folder-info.md)

### <a name="item-id-lists"></a>Element-ID-Listen

Die Element-ID wird nur selten allein verwendet. Normalerweise ist sie Teil einer Element-ID-Liste, die demselben Zweck dient wie ein Dateisystempfad. Anstelle der für Pfade verwendeten Zeichenfolge ist eine Element-ID-Liste jedoch eine [**ITEMIDLIST-Struktur.**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) Diese Struktur ist eine geordnete Sequenz von mindestens einer Element-IDs, die mit einem 2-Byte **NULL** beendet wird. Jede Element-ID in der Element-ID-Liste entspricht einem Namespaceobjekt. Ihre Reihenfolge definiert einen Pfad im Namespace, ähnlich wie ein Dateisystempfad.

Die folgende Abbildung zeigt eine schematische Darstellung der [**ITEMIDLIST-Struktur,**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) die C: \\ MyDocsMyFile.htm \\ entspricht. Der Anzeigename jeder Element-ID wird darüber angezeigt. Die unterschiedlichen Breiten der **abID-Member** sind willkürlich. sie veranschaulichen die Tatsache, dass die Größe dieses Members variieren kann.

![Eine schematische Abbildung einer Pidl](images/shell2.png)

### <a name="pidls"></a>PIDLs

Für die Shell-API werden Namespaceobjekte in der Regel durch einen Zeiger auf ihre [**ITEMIDLIST-Struktur**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) oder einen Zeiger auf eine Elementbezeichnerliste (PIDL) identifiziert. Der Einfachheit halber verweist der Begriff PIDL in dieser Dokumentation im Allgemeinen auf die Struktur selbst und nicht auf den Zeiger darauf.

Die in der obigen Abbildung dargestellte PIDL wird als *vollständige* oder *absolute* PIDL bezeichnet. Eine vollständige PIDL beginnt mit dem Desktop und enthält die Element-IDs aller Zwischenordner im Pfad. Sie endet mit der Element-ID des Objekts, gefolgt von einem abschließenden 2-Byte-NULL-Wert. Eine vollständige PIDL ähnelt einem vollqualifizierten Pfad und identifiziert das Objekt im Shellnamespace eindeutig.

Vollständige PIDLs werden selten verwendet. Viele Funktionen und Methoden erwarten eine *relative PIDL.* Der Stamm einer relativen PIDL ist ein Ordner, nicht der Desktop. Wie bei relativen Pfaden definiert die Reihe von Element-IDs, aus denen die Struktur besteht, einen Pfad im Namespace zwischen zwei Objekten. Obwohl sie das Objekt nicht eindeutig identifizieren, sind sie in der Regel kleiner als eine vollständige PIDL und für viele Zwecke ausreichend.

Die am häufigsten verwendeten relativen PIDLs( *SINGLE-Level PIDLs*) sind relativ zum übergeordneten Ordner des Objekts. Sie enthalten nur die Element-ID des Objekts und einen abschließenden **NULL-Wert.** PiDLs mit mehreren Ebenen werden auch für viele Zwecke verwendet. Sie enthalten mindestens zwei Element-IDs und definieren in der Regel über eine Reihe von Unterordnern einen Pfad von einem übergeordneten Ordner zu einem Objekt. Beachten Sie, dass eine PIDL auf einer einzelnen Ebene weiterhin eine vollqualifizierte PIDL sein kann. Desktopobjekte sind insbesondere untergeordnete Elemente des Desktops, sodass ihre vollqualifizierten PIDLs nur eine Element-ID enthalten.

Wie unter [Abrufen der ORDNER-ID](folder-id.md)erläutert, bietet die Shell-API eine Reihe von Möglichkeiten zum Abrufen der PIDL eines Objekts. Sobald Sie es haben, verwenden Sie es häufig nur, um das Objekt zu identifizieren, wenn Sie andere Shell-API-Funktionen und -Methoden aufrufen. In diesem Kontext sind die internen Inhalte einer PIDL nicht transparent und irrelevant. Stellen Sie sich für diese Diskussion PIDLs als Token vor, die bestimmte Namespaceobjekte darstellen, und konzentrieren Sie sich darauf, wie sie für allgemeine Aufgaben verwendet werden.

### <a name="allocating-pidls"></a>Zuordnen von PIDLs

Obwohl PIDLs mit Pfaden vergleichbar sind, erfordert deren Verwendung einen etwas anderen Ansatz. Der Hauptunterschied besteht darin, wie Speicher zugeordnet und freigegeben wird.

Wie die zeichenfolge, die für einen Pfad verwendet wird, muss Arbeitsspeicher für eine PIDL zugeordnet werden. Wenn eine Anwendung eine PIDL erstellt, muss sie ausreichend Arbeitsspeicher für die [**ITEMIDLIST-Struktur**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) zuordnen. In den meisten der hier beschriebenen Fälle erstellt die Shell die PIDL und verarbeitet die Speicherbelegung. Unabhängig davon, was der PIDL zugeordnet ist, ist die Anwendung in der Regel für die Zuordnung der PIDL verantwortlich, wenn sie nicht mehr benötigt wird.

Verwenden Sie die [**CoTaskMemAlloc-Funktion,**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) um die PIDL zuzuordnen, und die [**CoTaskMemFree-Funktion,**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) um die Zuordnung freizugeben.

 

 
