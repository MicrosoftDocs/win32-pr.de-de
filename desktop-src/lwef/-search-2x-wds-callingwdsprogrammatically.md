---
title: Programm gesteuertes Aufrufen von WDS
description: Die Microsoft Windows-Desktop Suche (WDS) 2. x kann Programm gesteuert mithilfe der executeQuery-Methode und der ExecuteSQLQuery-Methode in der ISearchDesktop-Schnittstelle abgefragt werden.
ms.assetid: 38426f63-2039-410e-8c70-ebd9fc269d74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc76264b7939311273fbda334292dfb255cde8f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727049"
---
# <a name="calling-wds-programmatically"></a>Programm gesteuertes Aufrufen von WDS

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .

Die Microsoft Windows-Desktop Suche (WDS) 2. x kann Programm gesteuert mithilfe der **ExecuteQuery** -Methode und der **ExecuteSQLQuery** -Methode in der [**ISearchDesktop-**](/previous-versions//aa965729(v=vs.85)) Schnittstelle abgefragt werden. Die **ExecuteQuery** -Methode gibt basierend auf dem Abfragetext, den Spalten und den Einschränkungen, die als Parameter übergeben werden, einen Daten Satz Satz aus dem Index zurück. Die **ExecuteSQLQuery** -Methode gibt auch einen Datensatz-Satz von Ergebnissen zurück, erfordert jedoch den genauen Structured Query Language (SQL)-Befehl, der übermittelt werden soll. **ExecuteQuery** sollte in den meisten Szenarien verwendet werden.

## <a name="regular-queries"></a>Reguläre Abfragen

Reguläre Abfragen sind solche, die vom Benutzer in das WDS-Eingabefeld eingegeben werden, einschließlich der [erweiterten Abfrage Syntax](-search-2x-wds-aqsreference.md). Die Abfrage wird zusammen mit den zurück zugebende WDS 2. x- [Schema](-search-2x-wds-schematable.md) Spalten, der Spalte und der Reihenfolge zum Sortieren von Ergebnissen an **ExecuteQuery** und in allen Klauseln zur Einschränkung der Ergebnisse von übergeben.

Die-Methode weist das folgende Format auf:

`HRESULT ExecuteQuery(LPCWSTR lpcwstrQuery, LPCWSTR lpcwstrColumn, LPCWSTR lpcwstrSort, LPCWSTR lpcwstrRestriction, Recordset **ppiRs);`



| Richtung | Variable           | BESCHREIBUNG                                                                                                                                                                                   |
|-----------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| In        | lpcwstrinquery       | Der Abfragetext. Diese Abfrage ist identisch mit einer Abfrage, die in das Such Textfeld in der Benutzeroberfläche der Windows-Desktop Suche eingegeben wurde. <br/> Beispiel: `"from:Zara dinner plans"`<br/> |
| In        | lpcwstrincolumn      | Die einzuschließenden Spalten, getrennt durch Kommas. <br/> Beispiel: `"DocTitle, Url"`<br/>                                                                                            |
| In        | lpcwstrausort        | Die zu sortierende Überschreibungs Spalte, gefolgt von ASC für aufsteigend oder absteigend für absteigend. <br/> Beispiel: `"LastAuthor DESC"`<br/>                                                  |
| In        | lpcwstraueinschränkung | Einschränkungen zum Anfügen von WHERE-Klauseln in der Windows-Desktop Suche wählen Sie aus. <br/> Beispiel: `"Contains(LastAuthor, 'Bill')"`<br/>                                       |
| aus       | ppirs              | Der resultierende Daten Satz Satz<br/>                                                                                                                                                           |



 

## <a name="sql-queries"></a>SQL-Abfragen

Die **ISearchDesktop.Executesqlquery** -Methode wird verwendet, um direkte WDS-Datenbankabfragen zu senden. Die Syntax für die Abfragen ähnelt der für SharePoint Server verwendeten, zusammen mit der Möglichkeit, SQL GROUP BY-Klauseln im Monarch-Stil zu verwenden. Die Abfrage wird für den Index genau so ausgeführt, wie Sie übergeben wird, ohne dass eine zusätzliche Verarbeitung der erweiterten Abfrage Syntax erfolgt, wie die ExecuteQuery-API dies tut.

https://msdn.microsoft.com/library/default.asp?url=/library/spssdk/html/\_tahoe\_search\_sql\_syntax.asp

Die-Methode weist das folgende Format auf:

`HRESULT ExecuteSQLQuery(LPCWSTR lpcwstrSQL, Recordset **ppiRs);`



| Richtung | Variable   | BESCHREIBUNG                                    |
|-----------|------------|------------------------------------------------|
| In        | lpcwstrausql | Die SQL-Abfrage, die für den WDS-Index ausgeführt wird. |
| aus       | ppirs      | Der resultierende Daten Satz Satz                       |



 

Ressourcen:

-   Unterstützungs Dateien für die ISearchDesktop-Schnittstelle: https://addins.msn.com/support/WDSSDK.zip
-   ISearchDesktop c#-Beispiel: https://addins.msn.com/support/WDSSample.zip

## <a name="sample-c-code"></a>Beispiel C++ Code

> [!Note]
>
> Dieser Code und diese Informationen werden "wie immer" bereitgestellt, ohne jegliche Gewährleistungen jeglicher Art, entweder ausgedrückt oder impliziert, einschließlich, aber nicht beschränkt auf die impliziten Gewährleistungen der Handels Üblichkeit und/oder Eignung für einen bestimmten Zweck.
>
> Copyright (C) Microsoft. Alle Rechte vorbehalten.

 


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

[Aufrufen von WDS von Webseiten](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

