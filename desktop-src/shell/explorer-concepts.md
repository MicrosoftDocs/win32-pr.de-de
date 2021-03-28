---
description: Der Shell-Namespace organisiert das Dateisystem und andere Objekte, die von der Shell verwaltet werden, in einer einzigen Struktur strukturierten Hierarchie. Konzeptionell handelt es sich um eine größere und inklusiver Version des Dateisystems.
title: Allgemeine explorerkonzepte
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 78136c36-bd3c-4114-8b69-fef4e307566d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d5ea7d154ef0455576d91f99eb53dccd93c25339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554000"
---
# <a name="common-explorer-concepts"></a>Allgemeine explorerkonzepte

Der Shell- *Namespace* organisiert das Dateisystem und andere Objekte, die von der Shell verwaltet werden, in einer einzigen Struktur strukturierten Hierarchie. Konzeptionell handelt es sich um eine größere und inklusiver Version des Dateisystems.

-   [Introduction (Einführung)](#introduction)
-   [Identifizieren von Namespace Objekten](#identifying-namespace-objects)
    -   [Element-IDs](#item-ids)
    -   [Liste der Element-IDs](#item-id-lists)
    -   [PIDLs](#pidls)
    -   [Zuordnen von pidls](#allocating-pidls)

## <a name="introduction"></a>Einführung

Eine der Hauptaufgaben der Shell besteht darin, den Zugriff auf die Vielzahl von Objekten zu verwalten und bereitzustellen, aus denen das System besteht. Die häufigsten und vertrauten Objekte sind die Ordner und Dateien, die sich auf Computer Laufwerken befinden. Die Shell verwaltet jedoch auch eine Reihe von nicht Dateisystemen oder *virtuellen* Objekten. Beispiele hierfür sind:

-   Netzwerkdrucker
-   Andere vernetzte Computer
-   System Steuerungsanwendungen
-   Der Papierkorb

Einige virtuelle Objekte umfassen überhaupt keinen physischen Speicher. Das Drucker Objekt enthält beispielsweise eine Auflistung von Links zu vernetzten Druckern. Andere virtuelle Objekte (z. b. der Papierkorb) enthalten möglicherweise Daten, die auf einem Laufwerk gespeichert sind, müssen jedoch anders behandelt werden als normale Dateien. Beispielsweise kann ein virtuelles-Objekt verwendet werden, um in einer Datenbank gespeicherte Daten darzustellen. Im Hinblick auf den-Namespace können die verschiedenen Elemente in der Datenbank als separate Objekte im Windows-Explorer angezeigt werden, obwohl Sie alle in einer einzigen Datenträger Datei gespeichert sind.

Virtuelle Objekte befinden sich möglicherweise sogar auf Remote Computern. Beispielsweise können die Dokument Dateien eines Benutzers auf einem Server gespeichert werden, um das Roaming zu vereinfachen. Um Benutzern den Zugriff auf Ihre Dateien über mehrere Desktop-PCs zu gestatten, verweist der Ordner "eigene Dateien" auf dem Desktop-PC, den Sie zurzeit verwenden, auf den Server, nicht auf die Festplatte des Desktop-PCs. Der Pfad enthält entweder ein zugeordnetes Netzwerklaufwerk oder einen UNC-Pfadnamen.

Wie das Dateisystem enthält der-Namespace zwei grundlegende Typen von Objekten: Ordner und Dateien. Ordner Objekte sind die *Knoten* der Struktur. Dabei handelt es sich um Container für Datei Objekte und andere Ordner. Datei Objekte sind die *Blätter* der Struktur. Sie sind entweder normale Datenträger Dateien oder virtuelle Objekte, wie z. b. Drucker Verknüpfungen. Ordner, die nicht Teil des Dateisystems sind, werden manchmal auch als *virtuelle Ordner* bezeichnet.

Wie bei Dateisystem Ordnern variiert die Sammlung virtueller Ordner in der Regel von System zu System. Es gibt drei Klassen von virtuellen Ordnern:

-   Standard mäßige virtuelle Ordner, z. b. der Papierkorb, die auf allen Systemen gefunden werden.
-   Optionale virtuelle Ordner mit Standardnamen und-Funktionen, die jedoch möglicherweise nicht auf allen Systemen vorhanden sind.
-   Nicht standardmäßige Ordner, die vom Benutzer installiert werden.

Im Unterschied zu Dateisystem Ordnern können Benutzer keine neuen virtuellen Ordner selbst erstellen. Sie können nur diejenigen installieren, die von nicht-Microsoft-Entwicklern erstellt wurden. Die Anzahl der virtuellen Ordner ist daher normalerweise weitaus geringer als die Anzahl der Dateisystem Ordner. Eine Erläuterung zum Implementieren virtueller Ordner finden Sie unter [Namespace Erweiterungen](nse-works.md).

Sie können sehen, wie der Namespace in der Explorer-Leiste von Windows-Explorer strukturiert ist. Der folgende Screenshot von Windows Explorer zeigt z. b. einen relativ einfachen Namespace.

![Screenshot, der eine Ansicht des Shell-Namespace anzeigt](images/prog1.png)

Der ultimative Stamm der Namespace Hierarchie ist der Desktop. Direkt unterhalb des Stamms befinden sich mehrere virtuelle Ordner (z. b. Arbeitsplatz und der Papierkorb).

Die Dateisysteme der verschiedenen Laufwerke können als Teilmengen der größeren Namespace Hierarchie angesehen werden. Die Stämme dieser Dateisysteme sind Unterordner des Ordners Arbeitsplatz. Arbeitsplatz umfasst auch die Stämme aller zugeordneten Netzlaufwerke. Andere Knoten in der Struktur, z. b. "eigene Dokumente", sind virtuelle Ordner.

## <a name="identifying-namespace-objects"></a>Identifizieren von Namespace Objekten

Bevor Sie ein Namespace Objekt verwenden können, müssen Sie zunächst eine Möglichkeit haben, es zu identifizieren. Ein Objekt im Dateisystem könnte einen Namen haben, z. b. MyFile.htm. Da es möglicherweise andere Dateien mit diesem Namen an anderer Stelle im System gibt, ist für eine eindeutige Identifizierung einer Datei oder eines Ordners ein voll qualifizierter Pfad erforderlich, z. b. "C: \\ MyDocs \\MyFile.htm". Bei diesem Pfad handelt es sich im Grunde um eine geordnete Liste aller Ordner in einem Pfad aus dem Dateisystem Stamm "C:" \\ , die mit der Datei endet.

Im Kontext des-Namespace sind Pfade nach wie vor sehr nützlich für das Identifizieren von Objekten, die sich im Dateisystem Teil des-Namespace befinden. Sie können jedoch nicht für virtuelle Objekte verwendet werden. Stattdessen bietet die Shell eine Alternative Identifikationsmethode, die mit jedem Namespace Objekt verwendet werden kann.

### <a name="item-ids"></a>Element-IDs

In einem Ordner hat jedes Objekt eine *Element-ID*, die die funktionale Entsprechung eines Datei-oder Ordner namens ist. Die Element-ID ist tatsächlich eine [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Struktur:


```
typedef struct _SHITEMID { 
    USHORT cb; 
    BYTE   abID[1]; 
} SHITEMID, * LPSHITEMID;
```



Der **Abid** -Member ist der Bezeichner des Objekts. Die Länge von **Abid** ist nicht definiert, und ihr Wert wird durch den Ordner bestimmt, der das-Objekt enthält. Da es keine Standard Definition gibt, wie **Abid** -Werte von Ordnern zugewiesen werden, sind Sie nur für das zugeordnete Ordner Objekt von Bedeutung. Anwendungen sollten Sie einfach als Token behandeln, das ein Objekt in einem bestimmten Ordner identifiziert. Da die Länge der **Abid** variiert, enthält das **CB** -Element die Größe der [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Struktur in Bytes.

Da Element-IDs zu Anzeige Zwecken nicht nützlich sind, weist der Ordner, der das Objekt enthält, normalerweise einen anzeigen Amen zu. Dies ist der Name, der von Windows Explorer beim Anzeigen des Inhalts eines Ordners verwendet wird. Weitere Informationen zur Behandlung von anzeigen Amen finden Sie unter [erhalten von Informationen aus einem Ordner](folder-info.md).

### <a name="item-id-lists"></a>Liste der Element-IDs

Die Element-ID wird nur selten von sich selbst verwendet. Normalerweise ist Sie Teil einer Element-ID-Liste, die den gleichen Zweck wie ein Dateisystempfad hat. Anstelle der für Pfade verwendeten Zeichenfolge ist eine Element-ID-Liste jedoch eine [**itemittel List**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) -Struktur. Diese Struktur ist eine geordnete Sequenz aus einer oder mehreren Element-IDs, die mit einem 2-Byte- **null**-Wert beendet wird. Jede Element-ID in der Liste der Element-IDs entspricht einem Namespace Objekt. Ihre Reihenfolge definiert einen Pfad im Namespace, ähnlich wie ein Dateisystempfad.

Die folgende Abbildung zeigt eine Schema förmige Darstellung der [**itemittlerlist**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) -Struktur, die C: \\ MyDocs \\MyFile.htm entspricht. Der Anzeige Name der einzelnen Element-IDs wird oberhalb des anzeigen Amens angezeigt. Die unterschiedlichen Breiten der **Abid** -Elemente sind willkürlich. Sie veranschaulichen die Tatsache, dass die Größe dieses Members variieren kann.

![eine Schema grafische Darstellung einer PIDL](images/shell2.png)

### <a name="pidls"></a>PIDLs

Für die Shell-API werden Namespace Objekte normalerweise durch einen Zeiger auf Ihre [**itemittellist**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) -Struktur oder einen Zeiger auf eine Element Bezeichner-Liste (PIDL) identifiziert. Der praktische Hinweis ist, dass der Begriff PIDL in dieser Dokumentation im Allgemeinen auf die Struktur selbst und nicht auf den Zeiger verweist.

Die in der vorangehenden Abbildung gezeigte PIDL wird als *vollständige* oder *absolute* PIDL bezeichnet. Eine vollständige PIDL startet vom Desktop und enthält die Element-IDs aller zwischen Ordner im Pfad. Er endet mit der Element-ID des Objekts, gefolgt von einem abschließenden zwei Byte **null**. Eine vollständige PIDL ähnelt einem voll qualifizierten Pfad und identifiziert das Objekt im Shellnamespace eindeutig.

Vollständige pidls werden nur selten verwendet. Viele Funktionen und Methoden erwarten eine *relative PIDL*. Der Stamm einer relativen PIDL ist ein Ordner, nicht der Desktop. Wie bei relativen Pfaden definiert die Reihe von Element-IDs, die die Struktur bilden, einen Pfad im Namespace zwischen zwei Objekten. Obwohl Sie das Objekt nicht eindeutig identifizieren, sind Sie in der Regel kleiner als eine vollständige PIDL und sind für viele Zwecke ausreichend.

Die am häufigsten verwendeten relativen pidls, *Einstufige pidls*, sind relativ zum übergeordneten Ordner des Objekts. Sie enthalten nur die Element-ID des Objekts und einen abschließenden **null**-Wert. Mehrstufige pidls werden auch für viele Zwecke verwendet. Sie enthalten mindestens zwei Element-IDs und definieren in der Regel einen Pfad von einem übergeordneten Ordner zu einem Objekt durch eine Reihe von mindestens einem Unterordner. Beachten Sie, dass eine PIDL einer einzelnen Ebene immer noch eine voll qualifizierte PIDL sein kann. Insbesondere Desktop Objekte sind untergeordnete Elemente des Desktops, sodass Ihre voll qualifizierten pidls nur eine Element-ID enthalten.

Wie unter Abrufen [einer Ordner-ID](folder-id.md)erläutert, bietet die Shell-API eine Reihe von Möglichkeiten zum Abrufen der PIDL eines Objekts. Wenn Sie es haben, verwenden Sie es im Allgemeinen nur, um das Objekt zu identifizieren, wenn Sie andere shellapi-Funktionen und-Methoden aufzurufen. In diesem Kontext sind die internen Inhalte einer PIDL undurchsichtig und irrelevant. Stellen Sie sich für die Zwecke dieser Diskussion pidls als Token vor, die bestimmte Namespace Objekte darstellen, und konzentrieren Sie sich darauf, wie Sie Sie für häufige Aufgaben verwenden können.

### <a name="allocating-pidls"></a>Zuordnen von pidls

Obwohl pidls eine gewisse Ähnlichkeit mit Pfaden aufweisen, erfordert die Verwendung einen etwas anderen Ansatz. Der Hauptunterschied besteht darin, wie Sie Arbeitsspeicher zuordnen und deren Speicherplatz zuweisen.

Wie die für einen Pfad verwendete Zeichenfolge muss Arbeitsspeicher für eine PIDL zugeordnet werden. Wenn eine Anwendung eine PIDL erstellt, muss Sie ausreichend Arbeitsspeicher für die [**itemittel List**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) -Struktur zuordnen. In den meisten Fällen, die hier erläutert werden, erstellt die Shell die PIDL und verarbeitet die Speicher Belegung. Unabhängig davon, welche Zuweisung der PIDL erfolgt ist, ist die Anwendung in der Regel für die Aufhebung der Zuordnung der PIDL verantwortlich, wenn Sie nicht mehr benötigt wird.

Verwenden Sie die [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) -Funktion, um die PIDL zuzuordnen, und die [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) -Funktion, um Sie freizugeben.

 

 
