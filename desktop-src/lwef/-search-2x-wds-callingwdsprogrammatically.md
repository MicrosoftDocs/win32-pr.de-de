---
title: Programmgesteuertes Aufrufen von WDS
description: Microsoft Windows Desktop Search (WDS) 2.x kann programmgesteuert mithilfe der ExecuteQuery- und ExecuteSQLQuery-Methoden in der ISearchDesktop-Schnittstelle abgefragt werden.
ms.assetid: 38426f63-2039-410e-8c70-ebd9fc269d74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8879001bcf284affd03ff472ac9327445b799acd44465b5bae9a8cb2d819b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976900"
---
# <a name="calling-wds-programmatically"></a>Programmgesteuertes Aufrufen von WDS

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren [Versionen Windows Search.](../search/-search-3x-wds-overview.md)

Microsoft Windows Desktop Search (WDS) 2.x kann programmgesteuert mithilfe der **Methoden ExecuteQuery** und **ExecuteSQLQuery** in der [**ISearchDesktop-Schnittstelle abgefragt**](/previous-versions//aa965729(v=vs.85)) werden. Die **ExecuteQuery-Methode** gibt basierend auf dem Abfragetext, den Spalten und den Einschränkungen, die als Parameter übergeben werden, einen Datensatzsatz aus dem Index zurück. Die **ExecuteSQLQuery-Methode** gibt auch einen Datensatzsatz von Ergebnissen zurück, erfordert jedoch, dass der exakte strukturierte Abfragesprache (SQL)-Befehl übergeben wird. **ExecuteQuery** sollte in den meisten Szenarien verwendet werden.

## <a name="regular-queries"></a>Reguläre Abfragen

Reguläre Abfragen sind abfragen, die vom Benutzer in das WDS-Eingabefeld eingegeben werden, einschließlich der [erweiterten Abfragesyntax](-search-2x-wds-aqsreference.md). Die Abfrage wird zusammen mit den zurück zu [](-search-2x-wds-schematable.md) gebenden WDS 2.x-Schemaspalten, der Spalte und der Reihenfolge zum Sortieren der Ergebnisse sowie allen Klauseln zum Einschränken der Ergebnisse an **ExecuteQuery** übergeben.

Die -Methode hat die Form:

`HRESULT ExecuteQuery(LPCWSTR lpcwstrQuery, LPCWSTR lpcwstrColumn, LPCWSTR lpcwstrSort, LPCWSTR lpcwstrRestriction, Recordset **ppiRs);`



| Direction | Variable           | BESCHREIBUNG                                                                                                                                                                                   |
|-----------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| In        | lpcwstrQuery       | Der Abfragetext. Diese Abfrage ist identisch mit einer Abfrage, die in das Suchtextfeld auf der Benutzeroberfläche der Windows Desktopsuche eingefügt wurde. <br/> Beispiel: `"from:Zara dinner plans"`<br/> |
| In        | lpcwstrColumn      | Die ein- und durch Kommas getrennten Spalten. <br/> Beispiel: `"DocTitle, Url"`<br/>                                                                                            |
| In        | lpcwstrSort        | Die zu sortierende Überschreibungsspalte, gefolgt von ASC für aufsteigend oder DESC für absteigend. <br/> Beispiel: `"LastAuthor DESC"`<br/>                                                  |
| In        | lpcwstrRestriction | Einschränkungen zum Anfügen über WHERE-Klauseln in Windows Desktopsuche auswählen. <br/> Beispiel: `"Contains(LastAuthor, 'Bill')"`<br/>                                       |
| aus       | ?n-n-n              | Der resultierende Datensatzsatz<br/>                                                                                                                                                           |



 

## <a name="sql-queries"></a>SQL-Abfragen

Die **ISearchDesktop.ExecuteSQLQuery-Methode** wird verwendet, um direkte WDS-Datenbankabfragen zu senden. Die Syntax für die Abfragen ähnelt der syntax für SharePoint Server, zusammen mit der Möglichkeit zur Verwendung von GROUP BY-Klauseln SQL Stil. Die Abfrage wird für den Index genau so ausgeführt, wie sie übergeben wird, ohne dass die erweiterte Abfragesyntax wie bei der ExecuteQuery-API verarbeitet wird.

https://msdn.microsoft.com/library/default.asp?url=/library/spssdk/html/\_tahoe\_search\_sql\_syntax.asp

Die -Methode hat die Form:

`HRESULT ExecuteSQLQuery(LPCWSTR lpcwstrSQL, Recordset **ppiRs);`



| Direction | Variable   | BESCHREIBUNG                                    |
|-----------|------------|------------------------------------------------|
| In        | lpcwstrSQL | Die SQL Abfrage, die für den WDS-Index ausgeführt werden soll. |
| aus       | ?n-n-n      | Der resultierende Datensatzsatz                       |



 

Ressourcen:

-   Unterstützungsdateien für die ISearchDesktop-Schnittstelle: https://addins.msn.com/support/WDSSDK.zip
-   ISearchDesktop-C#-Beispiel: https://addins.msn.com/support/WDSSample.zip

## <a name="sample-c-code"></a>C++-Beispielcode

> [!Note]
>
> DIESER CODE UND DIE INFORMATIONEN WERDEN "WIE BEFÄHRT" BEREITGESTELLT, OHNE JEGLICHE GEWÄHRLEISTUNG, ENTWEDER AUSGEDRÜCKT ODER KONKLUDENT, EINSCHLIEßLICH, ABER NICHT BESCHRÄNKT AUF DIE KONKLUDENTEN GEWÄHRLEISTUNGEN DER HANDELSIERBARKEIT UND/ODER EIGNUNG FÜR EINEN BESTIMMTEN ZWECK.
>
> Copyright (C) Microsoft. All rights reserved.

 


```
#include <stdio.h>
#include <wchar.h>
#include <windows.h>
#include <msnldl.h>
#include <adoint.h>
#include <adoguids.h>
 
HRESULT TestExecuteQuery(ISearchDesktop *psd)
{
ADORecordset *prs = NULL;
 
    HRESULT hr;
 
    hr = psd->ExecuteQuery( L"ToName:Moishe", 
                            L"DocTitle,DocFormat", 
                            L"PrimaryDate DESC", 
                            L"Contains('text')", 
                            &prs);
    if (SUCCEEDED(hr))
        prs->Release();
    return hr;
}
 
HRESULT TestExecuteSQLQuery(ISearchDesktop *psd)
{
    ADORecordset *prs = NULL;
    HRESULT hr;

    hr = psd->ExecuteSQLQuery(L"select DocTitle from MyIndex..Scope() where contains('text')", &prs);

    if (SUCCEEDED(hr))
      prs->Release();
    return hr;
}
 
extern "C" int __cdecl wmain( int argc, WCHAR * argv[] )
{
    SCODE sc = CoInitialize(0);
    ISearchDesktop *psd = NULL;
    HRESULT         hr;
     
    if (SUCCEEDED(hr = CoCreateInstance(__uuidof(SearchDesktop), NULL, CLSCTX_INPROC_SERVER, 
                                        __uuidof(ISearchDesktop), (void**)&psd)))
          {
             TestExecuteSQLQuery(psd);
             TestExecuteQuery(psd);
             psd->Release();
          }
          CoUninitialize();
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Erweiterte Abfragesyntax](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Wahrgenommene Typen](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Aufrufen von WDS über Webseiten](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

