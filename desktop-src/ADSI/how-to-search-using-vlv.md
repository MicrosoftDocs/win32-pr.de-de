---
title: Suchen mit VLV
description: Active Directory unterstützt VLV-Suchen (Virtual List View). Diese Art von Suche ist speziell für große Resultsets konzipiert und ermöglicht es einer Anwendung, eine Teilmenge von Tausenden von Einträgen anzuzeigen, ohne jeden Eintrag tatsächlich abrufen zu müssen.
ms.assetid: fea04190-0846-4b62-99f4-7d8fb35fd510
ms.tgt_platform: multiple
keywords:
- Suchen mit VLV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a24250c8e54ccb7917f86b193152c62810b93
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949119"
---
# <a name="how-to-search-using-vlv"></a>Suchen mit VLV

Active Directory unterstützt VLV-Suchen (Virtual List View). Diese Art von Suche ist speziell für große Resultsets konzipiert und ermöglicht es einer Anwendung, eine Teilmenge von Tausenden von Einträgen anzuzeigen, ohne jeden Eintrag tatsächlich abrufen zu müssen.

Es gibt zwei unterschiedliche Möglichkeiten, wie eine VLV-Suche verwendet werden kann. Der erste besteht darin, die Attribute für bestimmte Einträge auf Grundlage eines numerischen Offsets abzurufen. Diese Methode ist nützlich, wenn Suchergebnisse als Reaktion auf einen scrollvorgang abgerufen werden.

Die zweite Möglichkeit, VLV-Suchen zu verwenden, besteht darin, nach einem Teil oder allen Textattributen zu suchen und nur die Ergebnisse der Suche anzuzeigen. Ein Beispiel für die Verwendung dieses Adressbuchs ist. Wenn der Benutzer ein "s" eingibt, kann die Anwendung eine VLV-Suche verwenden, um nach Einträgen zu suchen, die einen gemeinsamen Namen aufweisen, der mit "s" beginnt. Wenn der Benutzer dann dem "s" ein "m" hinzufügt, kann die Anwendung eine andere VLV-Suche verwenden, um nach Einträgen zu suchen, die einen gemeinsamen Namen aufweisen, der mit "SM" beginnt.

Um eine VLV-Suche auszuführen, weisen Sie ADSI an, das VLV-Steuerelement zu verwenden. Rufen Sie dazu die [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode mit einer Suchoption " **ADS \_ searchpref \_ VLV** " mit einem **adstype \_ Prov- \_ spezifischen** Wert auf. Der **spezifische adstype \_ Prov \_** -Wert ist ein Zeiger auf eine [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) -Struktur, die Daten über die Suche enthält. Die [**getvlvitemcount**](example-code-for-using-a-vlv-search.md) -Beispiel Funktion zeigt, wie beide Sucheinstellungen festgelegt werden.

Bei allen VLV-Such Vorgängen muss die serverseitige Ergebnis Sortierung verwendet werden. Dies erfolgt durch Festlegen der Sortierung " **ADS \_ searchpref" \_ \_ für** die Suche. Weitere Informationen zur Sortierung **\_ \_ \_ von ADS searchpref** nach Such Vorgängen finden Sie unter [Sortieren der Suchergebnisse mit idirector ysearch](sorting-the-search-results-with-idirectorysearch.md).

Wenn eine VLV-Suche durchgeführt wird, wird eine bestimmte Menge von Metadaten über die Suche in einer Spalte zurückgegeben, die durch Aufrufen von [**idirector ysearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) mit dem Antwort Bezeichner **ADS \_ VLV \_** abgerufen wird. Diese Daten sind in einer [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) -Struktur enthalten. Besonders wichtig sind die Member **dwcontentcount** und **lpcontextid** . Das **dwcontentcount** -Element enthält die Anzahl der Ergebnisse, die den VLV-Suchkriterien entsprechen. Dieser Wert kann als Schätzung der Gesamtzahl der Elemente verwendet werden, die für eine Suche dieses Typs zurückgegeben werden. Der **lpcontextid** -Member enthält einen Server definierten Wert, der an die nächste Suche übergeben werden kann, um die Suche zu identifizieren. Die Verwendung von **lpcontextid** kann die Suchleistung verbessern. Beachten Sie, dass **lpcontextid** ein Server definierter Wert ist und seine Länge im **dwcontextidlength** -Element enthalten ist. Dieser Puffer wird freigegeben, wenn die [**IDirectorySearch:: freecolumschlag**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) -Methode aufgerufen wird. Daher muss der Aufrufer einen Puffer der entsprechenden Größe zuordnen und den Inhalt des Puffers zwischen den Such Vorgängen kopieren und speichern.

Weitere Informationen zum LDAP-VLV-Steuerelement finden Sie unter [Suchen mit dem LDAP-VLV-Steuer](/previous-versions/windows/desktop/ldap/searching-with-the-ldap-vlv-control)Element.

Weitere Informationen finden Sie unter

-   Abrufen der Anzahl von Elementen
-   Suchen nach Offset
-   Suchen nach Zeichenfolge
-   [Beispiel Code für die Verwendung einer VLV-Suche](example-code-for-using-a-vlv-search.md)

## <a name="obtaining-the-number-of-items"></a>Abrufen der Anzahl von Elementen

**Führen Sie die folgenden Schritte aus, um eine Schätzung der Anzahl der Elemente zu erhalten, die für eine bestimmte Suche zurückgegeben werden.**

1.  Füllen Sie eine [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) -Struktur mit allen NULL-oder **null** -Werten aus.
2.  Füllen Sie eine Werbung mit der [**\_ searchpref- \_ Info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) mit den folgenden Werten aus.

    -   Legen Sie den **dwsearchpref** -Member auf **ADS \_ searchpref \_ VLV** fest.
    -   Legen Sie den **vValue. dwType** -Member auf **adstype \_ Prov \_ Specific** fest.
    -   Legen Sie den **vValue. ProviderSpecific. dwLength** -Member auf die Größe der [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) -Struktur fest.
    -   Legen Sie den **vValue. ProviderSpecific. lpValue** -Member auf die Adresse der [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) -Struktur aus Schritt 1 fest.

3.  Füllen Sie eine [**ADS \_ SortKey**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) -Struktur aus, wie in [Sortieren der Suchergebnisse mit IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md) zum Sortieren nach dem gewünschten Attribut gezeigt.
4.  Füllen Sie eine weitere Werbung mithilfe von [**\_ searchpref- \_ Informationen**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) aus, um die [**ADS \_ SortKey**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) -Struktur den Sucheinstellungen hinzuzufügen, wie unter [Sortieren der Suchergebnisse mit IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md)gezeigt.
5.  Fügen Sie alle anderen gewünschten Sucheinstellungen hinzu, und nennen Sie [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) , um die Sucheinstellungen festzulegen.
6.  Führen Sie die Suche mit [**idirector ysearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch)durch.
7.  Rufen Sie die erste Zeile der Ergebnisse ab, indem Sie [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow)aufrufen.
8.  Rufen Sie [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) mit **ADS \_ VLV \_ Response** auf, um die VLV-Such Metadaten abzurufen.
9.  Wandeln Sie die **padsvalues->ProviderSpecific. lpValue** der [**ADS- \_ Such \_ Spalten**](/windows/desktop/api/Iads/ns-iads-ads_search_column) Struktur in einen [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) -Struktur Zeiger um. Der **dwcontentcount** -Member dieser **ADS \_ VLV** -Struktur enthält die ungefähre Anzahl von Elementen, die durch eine Suche dieses Typs zurückgegeben werden.
10. Wenn andere VLV-Suchen desselben Typs durchgeführt werden, erstellen Sie eine Kopie der **lpcontextid** -Daten, und bewahren Sie Sie für die nächste VLV-Suche auf.

Die [**getvlvitemcount**](example-code-for-using-a-vlv-search.md) -Beispiel Funktion zeigt, wie dies funktioniert.

## <a name="searching-by-offset"></a>Suchen nach Offset

VLV sucht so schnell, dass es möglich ist, anhand eines numerischen Offsets nach einem bestimmten Ergebnis zu suchen. Wenn beispielsweise eine Suche dazu führt, dass 10.000 Elemente zurückgegeben werden, ermöglicht eine VLV-Suche das Abrufen der Informationen für ungefähr das 4072nd-Element, ohne alle Elemente vor dem fraglichen Element abrufen zu müssen.

Offsets werden als Verhältnis zwischen Offset und Inhalts Anzahl angegeben. Die Verhältnisse sind nützlich, da der Server möglicherweise keine genaue Schätzung der Anzahl der Einträge in der Liste hat oder die Listengröße geändert wird, wenn der Benutzer Sie durchsucht. Da Sie den Anfang und das Ende der Liste angeben müssen, können Sie einen geschätzten Wert für die Anzahl von Inhalten in der ersten Such Anforderung zusammen mit einem Offset-Wert verwenden. Der Server verwendet diese Daten, um die entsprechenden Offsets in der Liste basierend auf der Idee der Inhalts Anzahl zu berechnen, die in der Antwort an den Client über den **dwcontentcount** -Member der [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) -Struktur gesendet wird. Wenn Sie z. b. die Listengröße auf 3000 und den Offset auf den Listeneintrag 1500 festlegen möchten, legen Sie **dwcontentcount** auf 3000 und **dwOffset** auf 1500 fest. Wenn der Server die tatsächliche Listengröße auf 4500 schätzt, berechnet er den Offset auf 2250 und gibt die neuen Schätzwerte in **dwcontentcount** und **dwOffset** zurück.

> [!Note]
>
> Alle numerischen Werte in einer VLV-Suche sind Näherungen und sollten nicht für absolute Werte verwendet werden. Wenn Sie z. b. eine VLV-Suche für das 50. Element in einer Ration von 100 ausgeben, ist es nicht garantiert, dass Sie das exakte mittlere Element erhalten.
>
> **Führen Sie die folgenden Schritte aus, um ein bestimmtes Element nach Offset zu suchen.**
>
> 1.  Füllen Sie eine [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) -Struktur mit den folgenden Werten aus. Zusätzliche Member der Struktur sollten auf NULL oder **null** festgelegt werden.
>
>     -   Legen Sie den **dwcontentcount** -Member auf den maximalen Wert für das Verhältnis der abzurufenden Elemente fest.
>     -   Legen Sie den **dwOffset** -Member auf das Verhältnis (relativ zu **dwcontentcount**) der Elemente fest, die abgerufen werden sollen.
>     -   Legen Sie den **lpcontextid** -Member auf die Adresse der Kopie des Kontext-ID-Puffers und **dwcontextidlength** auf die Länge des Kontext-ID-Puffers in Bytes fest. Wenn keine Kontext-ID gespeichert wurde, müssen beide Member 0 (null) oder **null** sein.
>
> 2.  Legen Sie die Sucheinstellungen fest, wie in den Schritten 2 bis 5 der Prozedur Abrufen der Anzahl von Elementen dargestellt.
> 3.  Führen Sie die Suche mit [**idirector ysearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch)durch.
> 4.  Rufen Sie die erste Zeile der Ergebnisse ab, indem Sie [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow)aufrufen.
> 5.  Rufen Sie [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) mit dem Namen des abzurufenden Attributs auf, um die eigentlichen Daten für das angeforderte Element abzurufen.
> 6.  Rufen Sie [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) mit **ADS \_ VLV \_ Response** auf, um die VLV-Such Metadaten abzurufen.
> 7.  Wandeln Sie die **padsvalues->ProviderSpecific. lpValue** der [**ADS- \_ Such \_ Spalten**](/windows/desktop/api/Iads/ns-iads-ads_search_column) Struktur in einen [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) -Struktur Zeiger um.
> 8.  Erstellen Sie eine Kopie der **lpcontextid** -Daten, und bewahren Sie Sie für die nächste VLV-Suche auf.

 

Die Funktion [**getvlvitemtext**](example-code-for-using-a-vlv-search.md) Example zeigt, wie dies funktioniert.

Es ist auch möglich, mehrere Daten Zeilen mit einem einzelnen Suchvorgang abzurufen. Dies erfolgt in Schritt 1, indem die **dwbeforecount** -und **dwaftercount** -Elemente der [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) -Struktur entsprechend festgelegt werden. Das **dwbeforecount** -Element enthält die Anzahl der Elemente, die in der Liste vor dem fraglichen Element angezeigt werden, und das **dwaftercount** -Element enthält die Anzahl der Elemente, die nach dem fraglichen Element in der Liste angezeigt werden. Beide Zahlen schließen das Element selbst aus. Wenn Sie also **dwbeforecount** auf 10 und **dwaftercount** auf 10 festlegen, werden insgesamt 21 Elemente zurückgegeben. Diese Option ermöglicht das Zwischenspeichern der Suchergebnisse auf Clientseite.

## <a name="searching-by-string"></a>Suchen nach Zeichenfolge

Es ist auch möglich, eine VLV-Suche zu verwenden, um Elemente zu suchen, die ein Zeichen folgen Attribut aufweisen, dessen Wert ganz oder teilweise mit einer Zeichenfolge übereinstimmt, ohne alle Elemente abrufen zu müssen. Die Zeichen folgen Entsprechungen werden für das in der [**ADS \_ SortKey**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) -Struktur der **ADS \_ searchpref- \_ Sortierung \_** nach der Such Einstellung angegebene Attribut ausgeführt.

**Führen Sie die folgenden Schritte aus, um nach einem bestimmten Element durch eine Zeichenfolge zu suchen.**

1.  Füllen Sie eine [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) -Struktur mit den folgenden Werten aus. Zusätzliche Member der Struktur sollten auf NULL oder **null** festgelegt werden.

    -   Legen Sie das **psztarget** -Element auf einen Zeiger auf eine NULL-terminierte Zeichenfolge fest, die die zu suchende Zeichenfolge enthält.
    -   Legen Sie den **lpcontextid** -Member auf die Adresse der Kopie des Kontext-ID-Puffers und **dwcontextidlength** auf die Länge des Kontext-ID-Puffers in Bytes fest. Wenn keine Kontext-ID gespeichert wurde, müssen beide Member 0 (null) oder **null** sein.

2.  Legen Sie die Sucheinstellungen fest, wie in den Schritten 2 bis 5 der Prozedur Abrufen der Anzahl von Elementen dargestellt.
3.  Führen Sie die Suche mit [**idirector ysearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch)durch.
4.  Rufen Sie die erste Zeile der Ergebnisse ab, indem Sie [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow)aufrufen.
5.  Rufen Sie [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) mit dem Namen des abzurufenden Attributs auf, um die eigentlichen Daten für das angeforderte Element abzurufen.
6.  Rufen Sie [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) mit **ADS \_ VLV \_ Response** auf, um die VLV-Such Metadaten abzurufen.
7.  Wandeln Sie die **padsvalues->ProviderSpecific. lpValue** der [**ADS- \_ Such \_ Spalten**](/windows/desktop/api/Iads/ns-iads-ads_search_column) Struktur in einen [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) -Struktur Zeiger um.
8.  Erstellen Sie eine Kopie der **lpcontextid** -Daten, und bewahren Sie Sie für die nächste VLV-Suche auf. Wenn dies erforderlich ist, enthält der **dwOffset** -Member den 1-basierten Index des ersten Elements, dessen Zeichen folgen Attribut mit dem in **psztarget** angegebenen Wert beginnt.

Die [**getvlvitemsbystring**](example-code-for-using-a-vlv-search.md) -Beispiel Funktion zeigt, wie dies funktioniert.

Ähnlich wie bei der Suche nach Index ist es auch möglich, mehrere Daten Zeilen mit einem einzelnen Suchvorgang abzurufen. Dies erfolgt auf die gleiche Weise, indem die **dwbeforecount** -und **dwaftercount** -Elemente der [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) -Struktur entsprechend festgelegt werden.

 

 