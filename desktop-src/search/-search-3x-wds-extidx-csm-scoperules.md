---
description: Mit dem Crawl Scope Manager (CSM) können Sie Bereichs Regeln definieren, die URLs aus dem Windows Search-Crawl Bereich einschließen oder ausschließen.
ms.assetid: 132a55f9-680d-438e-b983-f5ce4cf66a41
title: Verwalten von Bereichs Regeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20d45199726cfe36dc1c4936e9ac7699a288c3ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128613"
---
# <a name="managing-scope-rules"></a>Verwalten von Bereichs Regeln

Mit dem Crawl Scope Manager (CSM) können Sie Bereichs Regeln definieren, die URLs aus dem Windows Search-Crawl Bereich einschließen oder ausschließen.

Mit dem CSM können Sie folgende Aufgaben ausführen:

-   Neue Bereichs Regeln zum Arbeits Regelsatz hinzufügen
-   Entfernen vorhandener Bereichs Regeln
-   Standard Bereichs Regeln aufzählen
-   Ermitteln, ob eine bestimmte URL im Crawl Bereich enthalten oder ausgeschlossen ist oder ob eine über-oder untergeordnete Bereichs Regel vorhanden ist

 

Dieses Thema enthält die folgenden Themen:

-   [Informationen zu Bereichs Regeln](#about-scope-rules)
-   [Vorbereitungen](#before-you-begin)
-   [Hinzufügen von Bereichs Regeln](#adding-scope-rules)
    -   [Hinweise zu Benutzerregeln](#notes-on-user-rules)
-   [Entfernen von Bereichs Regeln](#removing-scope-rules)
-   [Zurücksetzen auf Standardregeln](#reverting-to-default-rules)
-   [Auflisten von Bereichs Regeln](#enumerating-scope-rules)
-   [Ablauf Verfolgungs Bereichs Regeln](#tracing-scope-rules)
-   [Zugehörige Themen](#related-topics)

## <a name="about-scope-rules"></a>Informationen zu Bereichs Regeln

Eine Bereichs Regel ist eine Regel, die URLs innerhalb eines Suchstamms von der durch forchten und Indizierung enthält oder ausschließt. Einschluss Regeln bewirken, dass der Indexer diese URL in den aussperrungs Bereich einschließt, und Ausschluss Regeln bewirken, dass der Indexer diese URL (und seine untergeordneten Elemente) aus dem Crawl Bereich ausschließt.

Nehmen Sie beispielsweise an, Sie haben eine neue Anwendung installiert, deren Datendateien sich im Ordner workteama \\ ProjectFiles auf einem lokalen Computer befinden. Angenommen, Sie möchten, dass alles im Ordner "ProjectFiles" indiziert ist, ausgenommen Elemente in den Unterordner Prototypen. In dieser Situation benötigen Sie eine Inklusions Regel für myPH:///C: \\ workteama \\ ProjectFiles \\ und eine Ausschlussregel für myPH:///C: \\ workteama \\ ProjectFiles- \\ Prototypen \\ .

Es gibt drei Arten von Regeln mit der folgenden Rangfolge:

1.  Gruppenrichtlinie Regeln werden von Administratoren festgelegt und können alle anderen Regeln überschreiben.
2.  Benutzerregeln werden von Benutzern festgelegt, die den Bereich in der Benutzeroberfläche der Windows-Suchoptionen ändern. Benutzer oder andere Anwendungen können alle Benutzerregeln entfernen und zu Standardregeln zurückkehren.
3.  Standardregeln werden in der Regel von einer Anwendung festgelegt, um einen Standardbereich zu definieren. Standardregeln können z. b. festgelegt werden, wenn dem System ein neuer Protokollhandler oder Container hinzugefügt wird.

Zusammen bilden diese Regel Typen den *Arbeits Regelsatz* , von dem aus der CSM (Crawl Scope Manager) die vollständige Liste der zu durch forckenden URLs generiert. Obwohl Standardregeln von Gruppenrichtlinien Regeln und Benutzerregeln überschrieben werden können, werden Sie in Ihrem eigenen Standard Regelsatz verwaltet, auf den Sie jederzeit zurückgreifen können. Der Indexer durchsucht die URLs aus dem Arbeits Regelsatz und fügt dem Katalog Elemente, Eigenschaften und Inhalt hinzu.

> [!Note]  
> Benutzer mit Zugriff auf die Systemsteuerung können die Regeln über diese Schnittstelle ändern. Daher sollten Anwendungen, die die Bereichs Verwaltung anbieten, die Regeln immer direkt aus dem CSM erhalten, indem Sie die Enumerationsmethoden verwenden, anstatt sich auf eine gespeicherte Kopie von Benutzerregeln zu verlassen.

 

Ausschluss Regeln können Muster-URLs mit dem Platzhalter Zeichen ' \* ' definieren, z. b.: file:///C: \\ ProjectA \\ \* \\ . Eine Ausschlussregel, die dieses Muster verwendet, verhindert, dass der Indexer Ordner unter dem Verzeichnis "ProjectA" durchsucht. Ein komplizierteres Beispiel ist, dass es eine Inklusions Regel für file:///C: \\ ProjectA \\ und eine Ausschluss Muster Regel für file:///C: \\ ProjectA- \\ \* \\ Daten gibt \\ \* . In diesem Fall würde der Indexer Elemente in durchforsten:

-   C: \\ ProjectA\\
-   C: \\ ProjectA \\ **Version1** \\ testfiles\\
-   C: \\ ProjectA \\ **Version1 \\** temporäre \\ Daten\\

Der Indexer würde Elemente in jedoch nicht durchforsten:

-   C: \\ ProjectA \\ **Version1** \\ Daten\\

 

## <a name="before-you-begin"></a>Vorbereitungen

Bevor Sie eine der Schnittstellen für den Crawl Bereich-Manager verwenden, müssen Sie die folgenden Schritte ausführen:

1.  Erstellen des **csearchmanager** -Objekts und Abrufen der **isearchmanager** -Schnittstelle
2.  Rufen Sie **isearchmanager:: getCatalog** für "SystemIndex" auf, um eine Instanz der **isearchcatalogmanager** -Schnittstelle zu erhalten.
3.  Rufen Sie **isearchcatalogmanager:: getcrawlscopemanager** auf, um eine Instanz der **isearchcrawlscopemanager** -Schnittstelle zu erhalten.

Nachdem Sie die Änderungen an dem Crawl Bereich-Manager vorgenommen haben, müssen Sie die [**isearchcrawlscopemanager:: SaveAll**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall) -Methode aufzurufen. Diese Methode nimmt keine Parameter an und gibt \_ bei Erfolg S OK zurück.

 

## <a name="adding-scope-rules"></a>Hinzufügen von Bereichs Regeln

Die für das CSM festgelegten Arbeitsregeln enthalten Benutzer-und Standardregeln sowie alle Regeln, die von der Gruppenrichtlinie erzwungen werden. Benutzerregeln werden von Benutzern auf einer Benutzeroberfläche eingerichtet, und Standardregeln können wie folgt festgelegt werden:

-   Von einem Systemadministrator implementierte Gruppenrichtlinien (diese verwenden nicht die [**isearchcrawlscopemanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) -Schnittstelle.)
-   Installation oder Aktualisierung einer Anwendung wie Windows Search oder eines Protokoll Handlers
-   Eine Setup Anwendung für das Hinzufügen eines neuen Datenspeicher oder Containers

[**Isearchcrawlscopemanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) bietet zwei Methoden zum Hinzufügen neuer Bereichs Regeln, wie in der folgenden Tabelle beschrieben. Pfade für Inklusions Regeln für das Dateisystem müssen mit einem umgekehrten Schrägstrich \\ (z. b. file:///C: \\ Files \\ ) enden, und Pfade für Ausschluss Regeln müssen mit einem Sternchen enden (z. b. file:///c: \\ Files \\ \* ). Nur Ausschluss Regeln können Muster-URLs enthalten. Außerdem wird empfohlen, die Sicherheits-IDs (SIDs) der Benutzer in Pfade zu einschließen, um die Sicherheit zu verbessern. Pro-Benutzer-Pfade sind sicherer, da Abfragen dann in einem benutzerspezifischen Prozess ausgeführt werden. Dadurch wird sichergestellt, dass ein Benutzer die Elemente nicht sehen kann, die beispielsweise aus dem Posteingang eines anderen Benutzers indiziert wurden.

In der folgenden Tabelle werden die Methoden der isearchcrawlscopemanager-Schnittstelle beschrieben, die zum Hinzufügen neuer Bereichs Regeln verwendet wird.



| Methode                                                                              | BESCHREIBUNG                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Adduserscoperule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-adduserscoperule)       | Fügt eine Regel für eine URL hinzu, wie vom Benutzer angegeben. Diese Regeln überschreiben Standardregeln. Verwenden Sie diese Methode, wenn Sie eine Benutzeroberfläche implementiert haben, mit der Benutzer ihre eigenen Bereichs Regeln und URLs verwalten können.                         |
| [**Adddefaultscoperule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-adddefaultscoperule) | Fügt eine Regel für eine URL hinzu, wie von einer anderen Anwendung angegeben, wie z. b. einem Protokollhandler. Verwenden Sie diese Methode, wenn Sie einen neuen Protokollhandler implementiert oder einen neuen Datenspeicher hinzugefügt haben. Diese Regeln können durch Benutzerregeln überschrieben werden. |



 

Jede Methode übernimmt eine URL zu einem indizierbaren Speicherort und Flags, die bestimmen, ob die URL eingeschlossen oder ausgeschlossen werden soll. Der *ffollowflags* -Parameter ist für die zukünftige Verwendung reserviert. Wenn Sie eine neue Bereichs Regel hinzufügen und der Crawl Bereichs-Manager feststellt, dass die Regel bereits vorhanden ist (basierend auf der URL oder dem angegebenen Muster), wird der Arbeits Regelsatz so aktualisiert, dass (1) die alte Regel durch die neue Regel ersetzt wird, und (2) alle Benutzerregeln, die ihm widersprechen, werden entfernt.

**Tipp:** Während der file://root standardmäßig im Crawl Bereich enthalten ist, werden Programmdateien nicht standardmäßig indiziert. Daher müssen Anwendungen mit Daten, die in Ihrem Programmdatei Verzeichnis gespeichert werden, ihren Speicherort als Standardregel hinzufügen.

### <a name="notes-on-user-rules"></a>Hinweise zu Benutzerregeln

Wenn eine neue Benutzer Regel mit einer vorhandenen Standardregel identisch ist, überschreibt die neue Benutzer Regel die Standardregel im Arbeits Regelsatz. Wenn die neue Benutzer Regel mit einer vorhandenen Benutzer Regel identisch ist, wird die alte Benutzer Regel ersetzt.

Das Festlegen des Flags " *foverridächildren* " hat im Arbeits Regelsatz die folgenden Ergebnisse:

-   " **True** " führt zum Entfernen aller untergeordneten Regeln aus dem Arbeits Regelsatz (sowohl Benutzerregeln als auch Standardregeln).
-   FALSE führt zum erneuten Hinzufügen der Arbeitsregeln alle Standardregeln aus, die untergeordnete Elemente der neuen Benutzer Regel sind. Wenn eine untergeordnete Standardregel eine Einfügung ist und die neue Benutzer Regel ein Ausschluss ist, wird die Standardregel in eine Inklusions Benutzer Regel geändert.

 

## <a name="removing-scope-rules"></a>Entfernen von Bereichs Regeln

Sie können die [**isearchcrawlscopemanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) -Schnittstelle verwenden, um eine Bereichs Regel aus dem Arbeits Regelsatz zu entfernen. Diese Schnittstelle stellt die folgenden beiden Methoden zum Entfernen von Bereichs Regeln bereit.



| Methode                                                                                    | BESCHREIBUNG                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Removescoperule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removescoperule)               | Entfernt eine Benutzer Regel für eine angegebene URL aus dem Arbeits Regelsatz. Wenn die Benutzer Regel ein Duplikat von ist oder eine Standardregel überschreibt, verbleibt die Standardregel im Arbeits Regelsatz.                  |
| [**Removedefaultscoperule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removedefaultscoperule) | Entfernt eine Standardregel für eine angegebene URL aus dem Arbeits Regelsatz und dem Standardregel Satz. Nachdem Sie diese Methode aufgerufen haben, können Sie mit reverttodefaultscopes nicht mehr auf diese Standardregel zurückgreifen. |



 

Jede Methode übernimmt eine URL und ein Flag, das angibt, ob die zu entfernende Regel eine Inklusions-oder Ausschlussregel ist. Diese Methoden gibt einen Fehler zurück, wenn eine Regel mit dieser URL und dem Einschluss-/ausschlusflag nicht gefunden wurde.

**Tipp:** Wenn Sie einen Bereich vollständig aus dem Crawl Bereich entfernen möchten, verwenden Sie die [**removeroot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) -Methode, mit der der Suchstamm und alle zugehörigen Bereichs Regeln entfernt werden. Dies wird beispielsweise beim Deinstallieren von als bewährte Vorgehensweise angesehen.

Es ist auch möglich, alle Benutzer Satz Überschreibungen eines Suchstamms zu entfernen und die ursprünglichen Such Stamm-und Standard Bereichs Regeln wiederherzustellen. Weitere Informationen finden Sie im nächsten Abschnitt.

> [!Note]  
> Wenn Benutzer unter Windows Vista über Benutzerprofile in der Systemsteuerung entfernt werden, entfernt CSM alle Regeln und Stämme, die ihre SID enthalten, und entfernt ihre indizierten Elemente aus dem Katalog. Unter Windows XP müssen Sie die Stamm Elemente und Regeln der Benutzer manuell entfernen.

 

 

## <a name="reverting-to-default-rules"></a>Zurücksetzen auf Standardregeln

Durch das Zurücksetzen auf Standardregeln werden alle Benutzerregeln für eine URL oder einen Stamm entfernt und alle Standardregeln für den Arbeits Regelsatz wieder hergestellt. Regeln, die von der Gruppenrichtlinie festgelegt wurden, werden jedoch nicht entfernt. Die [**reverttodefaultscopes**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-reverttodefaultscopes) -Methode nimmt keine Parameter an und gibt einen Fehlercode zurück, wenn die Standardregeln nicht wieder hergestellt werden können.

 

## <a name="enumerating-scope-rules"></a>Auflisten von Bereichs Regeln

Der CSM listet Bereichs Regeln mithilfe einer standardmäßigen Enumeratorschnittstelle im com-Stil, [**ienumsearchscoperules**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules) , auf. Sie können diese Schnittstelle verwenden, um Bereichs Regeln für verschiedene Zwecke aufzuzählen. Beispielsweise können Sie den gesamten Arbeits Regelsatz auf einer Benutzeroberfläche anzeigen oder ermitteln, ob eine Regel oder das untergeordnete Element einer Regel bereits im Crawl Bereich vorhanden ist.

 

## <a name="tracing-scope-rules"></a>Ablauf Verfolgungs Bereichs Regeln

Mit dem CSM können Sie auch bestimmen, ob eine angegebene URL im Durchforstungs Bereich enthalten ist und ob Sie über eine über-oder untergeordnete Bereichs Regel verfügt. Sie können auch herausfinden, warum eine URL im Crawl Bereich enthalten oder ausgeschlossen ist. Diese Methoden sind nicht für die Verwendung mit Muster-URLs vorgesehen.

In der folgenden Tabelle werden die Methoden von [**isearchcrawlscopemanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) beschrieben, die zum Hinzufügen neuer Bereichs Regeln verwendet werden.



| Methode                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetParser-scopeversionid**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-getparentscopeversionid) | Ruft die Versions-ID der übergeordneten Inklusions-URL ab. Mit dieser Methode können Sie festzustellen, ob sich der übergeordnete Bereich seit der letzten Überprüfung geändert hat.<br/> Beispiel: Wenn eine e-Mail-Anwendung vom Anbieter verwaltete Benachrichtigungen verwendet, erhält Sie möglicherweise die übergeordnete Bereichs Version, bevor Sie geschlossen wird, und überprüft die Version erneut, wenn Sie geöffnet wird. Anschließend kann die Anwendung ermitteln, ob Sie einen neuen Benachrichtigungs Satz an den Indexer überbringen muss.<br/> |
| [**Haschildscoperule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-haschildscoperule)             | Gibt **true** zurück, wenn die angegebene URL eine untergeordnete Regel aufweist (eine Regel, die auf ein untergeordnetes Element auf jeder Ebene innerhalb der URL-Hierarchie angewendet wird) <br/> Beispiel: Wenn die URL file:///C: \\ Folder lautet \\ , gibt diese Methode **true** zurück, wenn das CSM eine Bereichs Regel speziell für den \\ Unterordner file:///C: Folder enthält \\ \\ .<br/>                                                                                                                                              |
| [**Hasparameentscoperule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-hasparentscoperule)           | Gibt **true** zurück, wenn die angegebene URL über eine übergeordnete Regel verfügt (eine Regel, die auf ein übergeordnetes Element in der URL-Hierarchie angewendet wird).<br/> Beispiel: Wenn die URL file:///C: \\ Folder- \\ Unterordner ist, gibt diese Methode **true** zurück, wenn das CSM eine Bereichs Regel speziell für file:///C: \\ Folder aufweist \\ .<br/>                                                                                                                                                   |
| [**Includidincrawlscope**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope)       | Gibt **true** zurück, wenn die angegebene URL im Crawl Bereich enthalten ist.                                                                                                                                                                                                                                                                                                                                                                                  |
| [**Incluentdincrawlscopeex**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex)   | Gibt einen Wert aus der [**clusion \_ reason**](/windows/win32/api/searchapi/ne-searchapi-clusion_reason) -Enumeration zurück, der erklärt, warum die URL in den Crawl Bereich eingeschlossen oder davon ausgeschlossen wird, und ruft den Wert **true** ab, wenn die URL in den Crawl Bereich eingefügt wird. Diese Methode kann Ihnen helfen, Konflikte in Ihrem Arbeits Regelsatz zu identifizieren.                                                                                                                                       |



 

 

> [!Note]  
> Die Methoden " [**includedincrawlscope**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope) " und " [**includedincrawlscopeex**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex) " bestimmen, ob die URL nur basierend auf den Regeln im CSM durchsucht wird. Es kann andere Gründe geben, dass eine URL nicht durchsucht wird, z. b. wenn das Fanci-Bit festgelegt wird (d. h., ein Benutzer hat die schnelle Indizierung im Eigenschaften Dialogfeld des Ordners nicht zugelassen).

 

Wenn Sie der Meinung sind, dass ein Dateipfad ausgeschlossen werden soll, er aber als eingeschlossen aufgeführt ist, stellen Sie sicher, dass die Ausschluss Regeln mit " <path> \\ \* " enden. Wenn Sie der Meinung sind, dass ein Datei-oder Dateipfad eingeschlossen werden soll, dies aber nicht der Fall ist, überprüfen Sie die Einstellung "Fanci-Bit" auf die Datei oder den Pfad. Klicken Sie hierzu mit der rechten Maustaste auf die Datei oder den Dateipfad, und wählen Sie **Eigenschaften** aus. Stellen Sie dann sicher, dass das Kontrollkästchen **für die schnelle Suche, dass der Indizierungs Dienst das Indizieren dieser Ordner zulässt** Wenn die Datei oder der Dateipfad hier nicht für die Indizierung markiert ist, wird er nicht indiziert, auch wenn er sich in einer Inklusions Regel befindet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**Isearchcrawlscopemanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
</dt> <dt>

[**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2)
</dt> <dt>

[**Isearchscoperule**](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)
</dt> <dt>

[**Ienumsearchscoperules**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules)
</dt> <dt>

**Licher**
</dt> <dt>

[Verwalten von Such Stämmen](-search-3x-wds-extidx-csm-searchroots.md)
</dt> </dl>

 

 




