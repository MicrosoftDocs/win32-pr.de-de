---
description: Erfahren Sie mehr über den Shellnamespace und seine Datenquellenobjekte. Dieser Namespace bietet Erweiterbarkeitsoptionen in der Windows Shell-Benutzeroberfläche.
ms.assetid: 539c4455-e1c7-45a0-b3c3-781f2b7a1617
title: Einführung in den Shellnamespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c758f95934e70abdb525547fda3940cd75ebc9b455fbca2cfdbd38ff962c3b0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219900"
---
# <a name="introduction-to-the-shell-namespace"></a>Einführung in den Shellnamespace

Der *Shell-Namespace* organisiert das Dateisystem und andere objekte, die von der Shell verwaltet werden, in einer einzelnen strukturstrukturierten Hierarchie. Konzeptionell handelt es sich um eine größere und inklusivere Version des Dateisystems.

-   [Introduction (Einführung)](#introduction)
-   [Identifizieren von Namespaceobjekten](#identifying-namespace-objects)
    -   [Element-IDs](#item-ids)
    -   [Element-ID-Listen](#item-id-lists)
    -   [PIDLs](#pidls)
    -   [Zuordnen von PIDLs](#allocating-pidls)

## <a name="introduction"></a>Einführung

Eine der Hauptaufgaben der Shell ist das Verwalten und Bereitstellen des Zugriffs auf die vielzahl von Objekten, aus denen das System besteht. Die zahlreichen und vertrautsten dieser Objekte sind die Ordner und Dateien, die sich auf Computerdatenträgern befinden. Die Shell verwaltet jedoch auch eine Reihe von Nichtdateisystem- oder *virtuellen* Objekten. Beispiele hierfür sind:

-   Netzwerkdrucker
-   Andere Netzwerkcomputer
-   Systemsteuerung von Anwendungen
-   Die Papierkorb

Einige virtuelle Objekte enthalten überhaupt keinen physischen Speicher. Das Druckerobjekt enthält beispielsweise eine Sammlung von Links zu Druckern im Netzwerk. Andere virtuelle Objekte, z. B. die Papierkorb, können Daten enthalten, die auf einem Laufwerk gespeichert sind, aber anders als normale Dateien behandelt werden müssen. Beispielsweise kann ein virtuelles Objekt verwendet werden, um in einer Datenbank gespeicherte Daten zu darstellen. Im Hinblick auf den Namespace können die verschiedenen Elemente in der Datenbank im Windows-Explorer als separate Objekte angezeigt werden, obwohl sie alle in einer einzelnen Datenträgerdatei gespeichert sind.

Virtuelle Objekte können sich sogar auf Remotecomputern befinden. Um beispielsweise das Roaming zu erleichtern, können die Dokumentdateien eines Benutzers auf einem Server gespeichert werden. Damit Benutzer von mehreren Desktop-PCs aus auf ihre Dateien zugreifen können, wird der ordner Eigene Dokumente auf dem Desktop-PC, den sie derzeit verwenden, auf den Server und nicht auf die Festplatte des Desktop-PCs verweisen. Der Pfad enthält entweder ein zugeordnetes Netzwerklaufwerk oder einen UNC-Pfadnamen.

Wie das Dateisystem enthält der Namespace zwei grundlegende Objekttypen: Ordner und Dateien. Ordnerobjekte sind die *Knoten* der Struktur. sie sind Container für Dateiobjekte und andere Ordner. Dateiobjekte sind die *Blätter* der Struktur. sie sind entweder normale Datenträgerdateien oder virtuelle Objekte, z. B. Druckerverbindungen. Ordner, die nicht Teil des Dateisystems sind, werden manchmal als virtuelle *Ordner bezeichnet.*

Wie Dateisystemordner variiert auch die Sammlung virtueller Ordner in der Regel von System zu System. Es gibt drei Klassen virtueller Ordner:

-   Virtuelle Standardordner, z. B. Papierkorb, die sich auf allen Systemen befinden.
-   Optionale virtuelle Ordner, die Standardnamen und -funktionen haben, aber möglicherweise nicht auf allen Systemen vorhanden sind.
-   Nicht standardmäßige Ordner, die vom Benutzer installiert werden.

Im Gegensatz zu Dateisystemordnern können Benutzer selbst keine neuen virtuellen Ordner erstellen. Sie können nur Diejenigen installieren, die von Nicht-Microsoft-Entwicklern erstellt wurden. Die Anzahl der virtuellen Ordner ist daher normalerweise deutlich geringer als die Anzahl der Dateisystemordner. Eine Erörterung der Implementierung virtueller Ordner finden Sie unter [Namespaceerweiterungen](nse-works.md).

Eine visuelle Darstellung der Struktur des Namespaces wird in der Explorer-Leiste des Windows angezeigt. Der folgende Screenshot von Windows Explorer zeigt beispielsweise einen relativ einfachen Namespace.

![eine Ansicht des Shellnamespace](images/prog1.png)

Der endgültige Stamm der Namespacehierarchie ist der Desktop. Direkt unterhalb des Stammordners befinden sich mehrere virtuelle Ordner wie Arbeitsplatz und Papierkorb.

Die Dateisysteme der verschiedenen Laufwerke können als Teilmengen der größeren Namespacehierarchie angesehen werden. Die Stämme dieser Dateisysteme sind Unterordner des Arbeitsplatz Ordners. Arbeitsplatz enthält auch die Stämme aller zugeordneten Netzwerklaufwerke. Andere Knoten in der Struktur, z. B. Eigene Dokumente, sind virtuelle Ordner.

## <a name="identifying-namespace-objects"></a>Identifizieren von Namespaceobjekten

Bevor Sie ein Namespaceobjekt verwenden können, müssen Sie es zunächst identifizieren können. Ein Objekt im Dateisystem kann einen Namen haben, z. B. MyFile.htm. Da es möglicherweise andere Dateien mit diesem Namen an anderer Stelle im System gibt, erfordert die eindeutige Identifizierung einer Datei oder eines Ordners einen vollqualifizierten Pfad wie "C: \\ MyDocs \\MyFile.htm". Dieser Pfad ist im Grunde eine geordnete Liste aller Ordner in einem Pfad aus dem Dateisystemstamm C: \\ , der mit der Datei endet.

Im Kontext des Namespace sind Pfade immer noch sehr nützlich, um Objekte zu identifizieren, die sich im Dateisystemteil des Namespace befinden. Sie können jedoch nicht für virtuelle Objekte verwendet werden. Stattdessen bietet die Shell eine alternative Möglichkeit zur Identifizierung, die mit jedem Namespaceobjekt verwendet werden kann.

### <a name="item-ids"></a>Element-IDs

Innerhalb eines Ordners verfügt jedes Objekt über eine *Element-ID,* die der funktionalen Entsprechung eines Datei- oder Ordnernamens entspricht. Die Element-ID ist tatsächlich eine [**SHITEMID-Struktur:**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid)


```
typedef struct _SHITEMID { 
    USHORT cb; 
    BYTE   abID[1]; 
} SHITEMID, * LPSHITEMID; 
```



Der **abID-Member** ist der Bezeichner des Objekts. Die Länge von **abID** ist nicht definiert, und der Wert wird durch den Ordner bestimmt, der das -Objekt enthält. Da es keine Standarddefinition dafür gibt, **wie abID-Werte** von Ordnern zugewiesen werden, sind sie nur für das zugeordnete Ordnerobjekt aussagekräftig. Anwendungen sollten sie einfach als Token behandeln, das ein Objekt in einem bestimmten Ordner identifiziert. Da die Länge von **abID** variiert, enthält **der cb-Member** die Größe der [**SHITEMID-Struktur**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) in Bytes.

Da Element-IDs nicht zu Anzeigezwecken nützlich sind, weist der Ordner, der das Objekt enthält, normalerweise einen Anzeigenamen zu. Dies ist der Name, der vom Windows Explorer verwendet wird, wenn der Inhalt eines Ordners angezeigt wird. Weitere Informationen zur Handhabung von Anzeigenamen finden Sie unter [Abrufen von Informationen aus einem Ordner.](folder-info.md)

### <a name="item-id-lists"></a>Element-ID-Listen

Die Element-ID wird nur selten allein verwendet. Normalerweise ist sie Teil einer Element-ID-Liste, die denselben Zweck wie ein Dateisystempfad erfüllt. Anstelle der für Pfade verwendeten Zeichenfolge ist eine Element-ID-Liste jedoch eine [**ITEMIDLIST-Struktur.**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) Diese Struktur ist eine geordnete Sequenz von einer oder mehr Element-IDs, die mit einem Zwei-Byte-NULL-Wert **beendet wird.** Jede Element-ID in der Element-ID-Liste entspricht einem Namespaceobjekt. Ihre Reihenfolge definiert einen Pfad im Namespace, ähnlich wie ein Dateisystempfad.

Die folgende Abbildung zeigt eine schematische Darstellung der [**ITEMIDLIST-Struktur,**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) die C: \\ MyDocs \\MyFile.htm. Der Anzeigename jeder Element-ID wird darüber angezeigt. Die unterschiedlichen Breiten der **abID-Member** sind willkürlich. Sie veranschaulichen die Tatsache, dass die Größe dieses Mitglieds variieren kann.

![eine schematische Abbildung einer Pidl](images/shell2.png)

### <a name="pidls"></a>PIDLs

Für die Shell-API werden Namespaceobjekte in der Regel durch einen Zeiger auf ihre [**ITEMIDLIST-Struktur**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) oder einen Zeiger auf eine Elementbezeichnerliste (ITEM Identifier List, PIDL) identifiziert. Der Einfachheit halber bezieht sich der Begriff PIDL in dieser Dokumentation im Allgemeinen auf die Struktur selbst und nicht auf den Zeiger darauf.

Die in der obigen Abbildung gezeigte PIDL wird als vollständige *oder* *absolute* PIDL bezeichnet. Eine vollständige PIDL beginnt auf dem Desktop und enthält die Element-IDs aller Zwischenordner im Pfad. Er endet mit der Element-ID des Objekts, gefolgt von einem beendenden **Zwei-Byte-NULL-Wert.** Eine vollständige PIDL ähnelt einem vollqualifizierten Pfad und identifiziert das Objekt eindeutig im Shellnamespace.

Vollständige PIDLs werden selten verwendet. Viele Funktionen und Methoden erwarten eine *relative PIDL.* Der Stamm einer relativen PIDL ist ein Ordner, nicht der Desktop. Wie bei relativen Pfaden definiert die Reihe von Element-IDs, aus denen die Struktur aufgebaut ist, einen Pfad im Namespace zwischen zwei Objekten. Obwohl sie das Objekt nicht eindeutig identifizieren, sind sie in der Regel kleiner als eine vollständige PIDL und für viele Zwecke ausreichend.

Die am häufigsten verwendeten relativen PIDLs, *PIDLs* auf einer Ebene, sind relativ zum übergeordneten Ordner des Objekts. Sie enthalten nur die Element-ID des Objekts und einen beendenden **NULL-Wert.** PiDLs mit mehreren Ebene werden auch für viele Zwecke verwendet. Sie enthalten mindestens zwei Element-IDs und definieren in der Regel einen Pfad von einem übergeordneten Ordner zu einem Objekt über eine Reihe von Unterordnern. Beachten Sie, dass eine PIDL auf einer ebene weiterhin eine vollqualifizierte PIDL sein kann. Insbesondere Desktopobjekte sind dem Desktop unteren Elemente, sodass ihre vollqualifizierten PIDLs nur eine Element-ID enthalten.

Wie unter [Abrufen der ORDNER-ID](folder-id.md)erläutert, bietet die Shell-API eine Reihe von Möglichkeiten zum Abrufen der PIDL eines Objekts. Sobald Sie es haben, verwenden Sie es in der Regel nur, um das Objekt zu identifizieren, wenn Sie andere Shell-API-Funktionen und -Methoden aufrufen. In diesem Kontext sind die internen Inhalte einer PIDL nicht transparent und irrelevant. Stellen Sie sich für diese Diskussion PIDLs als Token vor, die bestimmte Namespaceobjekte darstellen, und konzentrieren Sie sich darauf, wie sie für allgemeine Aufgaben verwendet werden.

### <a name="allocating-pidls"></a>Zuordnen von PIDLs

Obwohl PIDLs mit Pfaden vergleichbar sind, erfordert deren Verwendung einen etwas anderen Ansatz. Der Hauptunterschied besteht darin, wie Speicher zugeordnet und freigegeben wird.

Wie die zeichenfolge, die für einen Pfad verwendet wird, muss Arbeitsspeicher für eine PIDL zugeordnet werden. Wenn eine Anwendung eine PIDL erstellt, muss sie ausreichend Arbeitsspeicher für die [**ITEMIDLIST-Struktur**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) zuordnen. In den meisten der hier beschriebenen Fälle erstellt die Shell die PIDL und verarbeitet die Speicherbelegung. Unabhängig davon, was der PIDL zugeordnet ist, ist die Anwendung in der Regel für die Zuordnung der PIDL verantwortlich, wenn sie nicht mehr benötigt wird.

Verwenden Sie die [**CoTaskMemAlloc-Funktion,**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) um die PIDL zuzuordnen, und die [**CoTaskMemFree-Funktion,**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) um die Zuordnung freizugeben.

 

 
