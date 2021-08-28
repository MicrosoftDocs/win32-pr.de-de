---
description: Mit Durchforstungsbereich-Manager (CSM) können Sie Bereichsregeln definieren, die URLs in den Durchforstungsbereich der Windows ein- oder ausschließen.
ms.assetid: 132a55f9-680d-438e-b983-f5ce4cf66a41
title: Verwalten von Bereichsregeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134e4241e9dcd66e468935ae56a4029a51a96c37
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880214"
---
# <a name="managing-scope-rules"></a>Verwalten von Bereichsregeln

Mit Durchforstungsbereich-Manager (CSM) können Sie Bereichsregeln definieren, die URLs in den Durchforstungsbereich der Windows ein- oder ausschließen.

Mit dem CSM können Sie Folgendes tun:

-   Hinzufügen neuer Bereichsregeln zum Arbeitsregelsatz
-   Entfernen vorhandener Bereichsregeln
-   Aufzählen von Standardbereichsregeln
-   Bestimmen, ob eine bestimmte URL in den Durchforstungsbereich eingeschlossen oder daraus ausgeschlossen wird oder ob sie über eine übergeordnete oder untergeordnete Bereichsregel verfügt

 

Dieses Thema enthält die folgenden Themen:

-   [Informationen zu Bereichsregeln](#about-scope-rules)
-   [Vorbereitungen](#before-you-begin)
-   [Hinzufügen von Bereichsregeln](#adding-scope-rules)
    -   [Hinweise zu Benutzerregeln](#notes-on-user-rules)
-   [Entfernen von Bereichsregeln](#removing-scope-rules)
-   [Zurücksetzen auf Standardregeln](#reverting-to-default-rules)
-   [Aufzählen von Bereichsregeln](#enumerating-scope-rules)
-   [Ablaufverfolgungsbereichsregeln](#tracing-scope-rules)
-   [Zugehörige Themen](#related-topics)

## <a name="about-scope-rules"></a>Informationen zu Bereichsregeln

Eine Bereichsregel ist eine Regel, die URLs innerhalb eines Suchstamms einschließt oder davon ausschließt, durchforstung und indiziert zu werden. Einschlussregeln bewirken, dass der Indexer diese URL in den Scrawl-Bereich einschließt, und Ausschlussregeln bewirken, dass der Indexer diese URL (und seine unteren Bereiche) aus dem Durchforstungsbereich ausschließt.

Angenommen, Sie haben eine neue Anwendung installiert, deren Datendateien sich im Ordner WorkteamA \\ ProjectFiles auf einem lokalen Computer befinden. Angenommen, Sie möchten, dass alles im Ordner ProjectFiles indiziert wird, mit Ausnahme der Elemente im Unterordner Prototypes. In diesem Fall benötigen Sie eine Einschlussregel für myPH:///C: \\ WorkteamA ProjectFiles und eine Ausschlussregel für \\ \\ myPH:///C: \\ WorkteamA \\ \\ ProjectFiles Prototypes \\ .

Es gibt drei Arten von Regeln mit der folgenden Rangfolge:

1.  Gruppenrichtlinie Regeln werden von Administratoren festgelegt und können alle anderen Regeln außer Kraft setzen.
2.  Benutzerregeln werden von Benutzern festgelegt, die den Bereich auf der Benutzeroberfläche Windows Suchoptionen ändern. Benutzer oder andere Anwendungen können alle Benutzerregeln entfernen und auf Standardregeln zurücksetzen.
3.  Standardregeln werden in der Regel von einer Anwendung festgelegt, um einen Standardbereich zu definieren. Beispielsweise können Standardregeln festgelegt werden, wenn dem System ein neuer Protokollhandler oder Container hinzugefügt wird.

Zusammen bilden diese Regeltypen  den Arbeitsregelsatz, aus dem der Durchforstungsbereich-Manager (CSM) die vollständige Liste der zu durchforstenden URLs generiert. Standardregeln können zwar durch Gruppenrichtlinienregeln und Benutzerregeln außer Kraft gesetzt werden, sie werden jedoch in einem eigenen Standardregelsatz verwaltet, auf den Sie jederzeit zurücksetzen können. Der Indexer durchforscht die URLs aus dem Arbeitsregelsatz und fügt dem Katalog Elemente, Eigenschaften und Inhalte hinzu.

> [!Note]  
> Benutzer mit Zugriff auf Systemsteuerung können die Regeln über diese Schnittstelle ändern. Daher sollten Anwendungen, die die Bereichsverwaltung anbieten, die Regeln immer direkt aus dem CSM erhalten, indem sie die Enumerationsmethoden verwenden, anstatt sich auf eine gespeicherte Kopie von Benutzerregeln zu verlassen.

 

Ausschlussregeln können Muster-URLs mit dem Platzhalterzeichen " " \* definieren. Beispiel: file:///C: \\ ProjectA \\ \* \\ . Eine Ausschlussregel, die dieses Muster verwendet, verhindert, dass der Indexer Ordner im Verzeichnis ProjectA durchforstung. Angenommen, für ein komplizierteres Beispiel gibt es eine Einschlussregel für file:///C: ProjectA und eine Ausschlussmusterregel für \\ \\ file:///C: \\ \\ \* \\ ProjectA-Daten. \\ \* In diesem Fall durchforstung der Indexer Elemente in:

-   C: \\ ProjectA\\
-   C: \\ ProjectA \\ **version1** \\ testfiles\\
-   C: \\ Temporäre Daten zu ProjectA \\ **Version1 \\** \\\\

Der Indexer durchforste jedoch keine Elemente in:

-   C: \\ ProjectA \\ **version1-Daten** \\\\

 

## <a name="before-you-begin"></a>Vorbereitungen

Bevor Sie eine der Schnittstellen Durchforstungsbereich-Manager verwenden, müssen Sie die folgenden erforderlichen Schritte ausführen:

1.  Erstellen Sie das **CSearchManager-Objekt,** und erhalten Sie **dessen ISearchManager-Schnittstelle.**
2.  Rufen **Sie ISearchManager::GetCatalog** für "SystemIndex" auf, um eine Instanz der **ISearchCatalogManager-Schnittstelle abzurufen.**
3.  Rufen **Sie ISearchCatalogManager::GetCrawlScopeManager** auf, um eine Instanz der **ISearchCrawlScopeManager-Schnittstelle abzurufen.**

Nachdem Sie Änderungen am -Durchforstungsbereich-Manager vorgenommen haben, müssen Sie die [**ISearchCrawlScopeManager::SaveAll-Methode**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall) aufrufen. Diese Methode nimmt keine Parameter an und gibt bei Erfolg S \_ OK zurück.

 

## <a name="adding-scope-rules"></a>Hinzufügen von Bereichsregeln

Die für die CSM festgelegten Arbeitsregeln umfassen Benutzer- und Standardregeln sowie alle Regeln, die durch Gruppenrichtlinien erzwungen werden. Benutzerregeln werden von Benutzern in einer Benutzeroberfläche eingerichtet, und Standardregeln können durch eine der folgenden Regeln festgelegt werden:

-   Von einem Systemadministrator implementierte Gruppenrichtlinien (diese verwenden nicht die [**ISearchCrawlScopeManager-Schnittstelle.)**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
-   Installation oder Update einer Anwendung wie Windows Search oder eines Protokollhandlers
-   Eine Setupanwendung zum Addition eines neuen Datenspeichers oder Containers

[**ISearchCrawlScopeManager bietet**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) zwei Methoden zum Hinzufügen neuer Bereichsregeln, wie in der folgenden Tabelle beschrieben. Pfade für Einschlussregeln für das Dateisystem müssen mit einem zurücken Schrägstrich ' ' enden (z. B. file:///C: Dateien), und Pfade für Ausschlussregeln müssen mit einem Sternchen enden (z. B. \\ \\ \\ file:///c: \\ Dateien \\ \* ). Nur Ausschlussregeln können Muster-URLs enthalten. Darüber hinaus wird empfohlen, Sicherheits-IDs (SIDs) von Benutzern in Pfade ein-/aus Sicherheitsgründen zu verwenden. Benutzerspezifische Pfade sind sicherer, da Abfragen dann in einem benutzerspezifischen Prozess ausgeführt werden. So wird beispielsweise sichergestellt, dass ein Benutzer keine Elemente sehen kann, die aus dem Posteingang eines anderen Benutzers indiziert wurden.

In der folgenden Tabelle werden die Methoden der ISearchCrawlScopeManager-Schnittstelle beschrieben, die zum Hinzufügen neuer Bereichsregeln verwendet werden.



| Methode                                                                              | Beschreibung                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddUserScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-adduserscoperule)       | Fügt eine Regel für eine URL hinzu, wie vom Benutzer angegeben. Diese Regeln überschreiben Standardregeln. Verwenden Sie diese Methode, wenn Sie eine Benutzeroberfläche implementiert haben, mit der Benutzer ihre eigenen Bereichsregeln und URLs verwalten können.                         |
| [**AddDefaultScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-adddefaultscoperule) | Fügt eine Regel für eine URL hinzu, wie von einer anderen Anwendung wie einem Protokollhandler angegeben. Verwenden Sie diese Methode, wenn Sie einen neuen Protokollhandler implementiert oder einen neuen Datenspeicher hinzugefügt haben. Diese Regeln können durch Benutzerregeln überschrieben werden. |



 

Jede Methode verwendet eine URL zu einem indexierbaren Speicherort und Flags, die bestimmen, ob die URL eingeschlossen oder ausgeschlossen werden soll. Der *Parameter fFollowFlags* ist für die zukünftige Verwendung reserviert. Wenn Sie eine neue Bereichsregel hinzufügen und die Durchforstungsbereich-Manager ermittelt, dass die Regel bereits vorhanden ist (basierend auf der angegebenen URL oder dem bereitgestellten Muster), wird der Arbeitsregelsatz aktualisiert, sodass (1) die alte Regel durch die neue Regel ersetzt wird und (2) alle Benutzerregeln, die ihn verwechseln, entfernt werden.

**Tipp:** Während der file:// standardmäßig im Durchforstungsbereich enthalten ist, werden Programmdateien nicht standardmäßig indiziert. Daher müssen Anwendungen, deren Daten im Verzeichnis Programme gespeichert sind, ihren Speicherort als Standardregel hinzufügen.

### <a name="notes-on-user-rules"></a>Hinweise zu Benutzerregeln

Wenn eine neue Benutzerregel mit einer vorhandenen Standardregel identisch ist, überschreibt die neue Benutzerregel die Standardregel im Arbeitsregelsatz. Wenn die neue Benutzerregel mit einer vorhandenen Benutzerregel identisch ist, wird die alte Benutzerregel ersetzt.

Das Festlegen des *Flags fOverrideChildren* führt zu den folgenden Ergebnissen im Arbeitsregelsatz:

-   **TRUE** führt zum Entfernen aller untergeordneten Regeln aus dem Arbeitsregelsatz (sowohl Benutzerregeln als auch Standardregeln).
-   FALSE führt dazu, dass dem Arbeitsregelsatz erneut alle Standardregeln hinzugefügt werden, die der neuen Benutzerregel untergestellt sind. Wenn eine untergeordnete Standardregel ein Einschluss und die neue Benutzerregel ein Ausschluss ist, wird die Standardregel in eine Einschlussbenutzerregel geändert.

 

## <a name="removing-scope-rules"></a>Entfernen von Bereichsregeln

Sie können die [**ISearchCrawlScopeManager-Schnittstelle**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) verwenden, um eine Bereichsregel aus dem Arbeitsregelsatz zu entfernen. Diese Schnittstelle stellt die folgenden beiden Methoden zum Entfernen von Bereichsregeln bereit.



| Methode                                                                                    | Beschreibung                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RemoveScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removescoperule)               | Entfernt eine Benutzerregel für eine angegebene URL aus dem Arbeitsregelsatz. Wenn die Benutzerregel ein Duplikat einer Standardregel ist oder diese überschreibt, verbleibt die Standardregel im Arbeitsregelsatz.                  |
| [**RemoveDefaultScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removedefaultscoperule) | Entfernt eine Standardregel für eine angegebene URL sowohl aus dem Arbeitsregelsatz als auch aus dem Standardregelsatz. Nach dem Aufruf dieser Methode können Sie diese Standardregel nicht mit revertToDefaultScopes zurücksetzen. |



 

Jede Methode verwendet eine URL und ein Flag, das angibt, ob die zu entfernende Regel eine Einschluss- oder Ausschlussregel ist. Diese Methoden geben einen Fehler zurück, wenn eine Regel mit dieser URL und dem Einschluss-/Ausschlussflag nicht gefunden wird.

**Tipp:** Wenn Sie einen Bereich vollständig aus dem Durchforstungsbereich entfernen möchten, verwenden Sie die [**RemoveRoot-Methode,**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) die den Suchstamm und alle zugehörigen Bereichsregeln entfernt. Dies gilt beispielsweise beim Deinstallieren als bewährte Methode.

Es ist auch möglich, alle benutzerspezifischen Außerkraftsetzungen eines Suchstamms zu entfernen und auf die ursprünglichen Regeln für den Suchstamm und den Standardbereich zurück zu setzen. Weitere Informationen finden Sie im nächsten Abschnitt.

> [!Note]  
> Wenn benutzer Windows Vista über Benutzerprofile in Systemsteuerung entfernt werden, entfernt CSM alle Regeln und Stämme, die ihre SID enthalten, und entfernt ihre indizierten Elemente aus dem Katalog. Auf Windows XP müssen Sie die Stämme und Regeln der Benutzer manuell entfernen.

 

 

## <a name="reverting-to-default-rules"></a>Zurücksetzen auf Standardregeln

Beim Wiederherstellen von Standardregeln werden alle Benutzerregeln für eine URL oder einen Stamm entfernt und alle Standardregeln im Arbeitsregelsatz wiederhergestellt. Regeln, die von gruppenrichtlinien festgelegt werden, werden jedoch nicht entfernt. Die [**RevertToDefaultScopes-Methode**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-reverttodefaultscopes) verwendet keine Parameter und gibt einen Fehlercode zurück, wenn sie nicht auf Standardregeln zurückverwenden kann.

 

## <a name="enumerating-scope-rules"></a>Aufzählen von Bereichsregeln

Der CSM aufzählt Bereichsregeln mithilfe einer Enumeratorschnittstelle im COM-Standardformat, [**IEnumSearchScopeRules.**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules) Sie können diese Schnittstelle verwenden, um Bereichsregeln für verschiedene Zwecke aufzählen. Beispielsweise können Sie den gesamten Arbeitsregelsatz in einer Benutzeroberfläche anzeigen oder feststellen, ob sich eine Regel oder das untergeordnete Einer Regel bereits im Durchforstungsbereich befindet.

 

## <a name="tracing-scope-rules"></a>Ablaufverfolgungsbereichsregeln

Mit dem CSM können Sie auch bestimmen, ob eine angegebene URL im Durchforstungsbereich enthalten ist und ob sie über eine übergeordnete oder untergeordnete Bereichsregel verfügt. Sie können auch herausfinden, warum eine URL in den Durchforstungsbereich eingeschlossen oder daraus ausgeschlossen wird. Diese Methoden sind nicht für die Verwendung mit Muster-URLs vorgesehen.

In der folgenden Tabelle werden die Methoden von [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) beschrieben, die zum Hinzufügen neuer Bereichsregeln verwendet werden.



| Methode                                                                                      | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetParentScopeVersionId**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-getparentscopeversionid) | Ruft die Versions-ID der übergeordneten Einschluss-URL ab. Mit dieser Methode können Sie überprüfen, ob sich der übergeordnete Bereich seit der letzten Überprüfung geändert hat.<br/> Beispiel: Wenn eine E-Mail-Anwendung vom Anbieter verwaltete Benachrichtigungen verwendet, kann sie die übergeordnete Bereichsversion erhalten, bevor sie geschlossen wird, und die Version erneut überprüfen, wenn sie geöffnet wird. Anschließend kann die Anwendung bestimmen, ob sie einen neuen Satz von Benachrichtigungen an den Indexer pushen muss.<br/> |
| [**HasChildScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-haschildscoperule)             | Gibt **TRUE zurück,** wenn die angegebene URL über eine untergeordnete Regel verfügt (eine Regel, die auf eine untergeordnete Ebene auf einer beliebigen Ebene innerhalb der URL-Hierarchie anwendung). <br/> Beispiel: Wenn die URL file:///C Ordner ist, gibt diese Methode TRUE zurück, wenn die CSM über eine Bereichsregel speziell für \\ \\ file:///C:  \\ \\ Ordnerunterordner \\ verfügt.<br/>                                                                                                                                              |
| [**HasParentScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-hasparentscoperule)           | Gibt **TRUE zurück,** wenn die angegebene URL über eine übergeordnete Regel verfügt (eine Regel, die auf einem übergeordneten Element auf einer beliebigen Ebene in der URL-Hierarchie gilt).<br/> Beispiel: Wenn die URL file:///C Ordnerunterordner ist, gibt diese Methode TRUE zurück, wenn der CSM über eine Bereichsregel speziell für file:///C \\ \\ Ordner  \\ \\ verfügt.<br/>                                                                                                                                                   |
| [**IncludedInCrawlScope**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope)       | Gibt **TRUE zurück,** wenn die angegebene URL im Durchforstungsbereich enthalten ist.                                                                                                                                                                                                                                                                                                                                                                                  |
| [**IncludedInCrawlScopeEx**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex)   | Gibt einen Wert aus der [**CLUSION \_ REASON-Enumeration**](/windows/win32/api/searchapi/ne-searchapi-clusion_reason) zurück, der erklärt, warum die URL in den Durchforstungsbereich eingeschlossen oder daraus ausgeschlossen wird, und ruft den Wert **TRUE** ab, wenn die URL im Durchforstungsbereich enthalten ist. Mit dieser Methode können Sie Konflikte in Ihrem Arbeitsregelsatz identifizieren.                                                                                                                                       |



 

 

> [!Note]  
> Die [**Methoden IncludedInCrawlScope**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope) und [**IncludedInCrawlScopeEx**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex) bestimmen, ob die URL ausschließlich anhand der Regeln in der CSM durchforscht wird. Es kann andere Gründe dafür geben, dass eine URL nicht durchforstet wird, z. B. das festgelegte FANCI-Bit (d. h., ein Benutzer hat die schnelle Indizierung im Dialogfeld Eigenschaft des Ordners nicht zulässig.

 

Wenn Sie der Meinung sind, dass ein Dateipfad ausgeschlossen werden sollte, aber als eingeschlossen aufgeführt wird, stellen Sie sicher, dass Ausschlussregeln mit " Pfad " &lt; &gt; \\ \* enden. Wenn Sie der Meinung sind, dass ein Datei- oder Dateipfad enthalten sein sollte, aber nicht, überprüfen Sie die FANCI-Biteinstellung für die Datei oder den Pfad. Klicken Sie hierzu mit der rechten Maustaste auf den Datei- oder Dateipfad, und wählen Sie Eigenschaften aus. Stellen Sie dann sicher, dass das Kontrollkästchen **Indexing Service** to index this folder (Indizierungsdienst zum Indizieren dieses Ordners zulassen) aktiviert ist. Wenn der Datei- oder Dateipfad hier nicht für die Indizierung markiert ist, wird er auch dann nicht indiziert, wenn er sich in einer Einschlussregel befindet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
</dt> <dt>

[**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2)
</dt> <dt>

[**ISearchScopeRule**](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)
</dt> <dt>

[**IEnumSearchScopeRules**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Verwalten von Suchsynten](-search-3x-wds-extidx-csm-searchroots.md)
</dt> </dl>

 

 




