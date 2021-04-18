---
title: Ausführen einer Attribut Bereichs Abfrage
description: Bei der Attribut Bereichs Abfrage handelt es sich um eine Such Einstellung, die die Durchführung einer Suche nach den Distinguished Name-Attributen eines Objekts ermöglicht.
ms.assetid: 026fbe17-5df7-4007-9d74-5c0abbe793b1
ms.tgt_platform: multiple
keywords:
- Ausführen einer Attribut Bereichs Abfrage ADSI
- ADSI, Search, idirector ysearch, andere Suchoptionen, Attribut Bereichs Abfrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10f5b666028c5fd46e7394b52a1328370e317bc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106341331"
---
# <a name="performing-an-attribute-scope-query"></a>Ausführen einer Attribut Bereichs Abfrage

Bei der Attribut Bereichs Abfrage handelt es sich um eine Such Einstellung, die die Durchführung einer Suche nach den Distinguished Name-Attributen eines Objekts ermöglicht. Das zu durchsuchende Attribut kann entweder ein-oder mehr wertig sein, muss jedoch den Typ der **ADS- \_ DN- \_ Zeichenfolge** aufweisen. Wenn die Suche durchgeführt wird, listet ADSI die Distinguished Name-Werte des Attributs auf und führt die Suche für die durch die Distinguished Names dargestellten Objekte durch. Wenn beispielsweise eine Attribut Bereichs bezogene Suche das [**Member**](/windows/desktop/ADSchema/a-member) -Attribut eines Group-Objekts durchführt, listet ADSI die Distinguished Names im **Member** -Attribut auf und durchsucht die einzelnen Mitglieder der Gruppe nach den angegebenen Suchkriterien.

Wenn eine Abfrage im Bereich eines Attributs für ein Attribut ausgeführt wird, das nicht den Typ **ADS \_ DN \_ String** hat, schlägt die Suche fehl. Die Abfrage mit dem Attribut Bereich erfordert auch, dass die **\_ \_ Such \_ Bereichseinstellung ADS searchpref** auf **ADS \_ Scope \_ Base** festgelegt ist. Die **\_ \_ Such \_ Bereichseinstellung ADS searchpref** wird automatisch auf **ADS \_ Scope \_ Base** festgelegt, aber wenn die Einstellung **ADS \_ searchpref \_ Search \_ Scope** auf einen anderen Wert festgelegt ist, schlägt [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) mit einem ungültigen **\_ \_ \_ Parameter E ADS** fehl.

Die Ergebnisse einer Attribut Bereichs Abfrage können mehrere Server umfassen, und ein Server gibt möglicherweise nicht alle für alle zurückgegebenen Zeilen angeforderten Daten zurück. Wenn dies der Fall ist, wenn die letzte Zeile durch den Aufruf von [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) oder [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow)abgerufen wird, gibt ADSI " **s \_ ADS \_ errorsoccrered** " anstelle von " **s \_ ADS \_ nomore \_ Rows**" zurück.

Wenn Sie eine Attribut Bereichs Abfrage angeben möchten, legen Sie die Suchoption **ADS \_ searchpref- \_ Attribut \_ Abfrage** mit einem **adstype \_ Case- \_ \_ Zeichen** folgen Wert auf den ldapDisplayName des zu durchsuchenden Attributs fest [**, das an \_ \_**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) die [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode übergeben wird. Dieser Vorgang wird im folgenden Codebeispiel gezeigt.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBUTE_QUERY;
SearchPref.vValue.dwType = ADSTYPE_CASE_IGNORE_STRING;
SearchPref.vValue.Boolean = L"member";
```



Im folgenden Codebeispiel wird gezeigt, wie Sie die Suchoption **ADS \_ searchpref- \_ Attribut \_ Abfrage** verwenden.


```C++
/***************************************************************************

    SearchGroupMembers()

    Searches the members of a group that are of type user and prints each 
    user's cn and distinguishedName values to the console.

    Parameters:

    pwszGroupDN - Contains the distinguished name of the group whose 
    members will be searched.

***************************************************************************/

HRESULT SearchGroupMembers(LPCWSTR pwszGroupDN)
{
    HRESULT hr;
    CComPtr<IDirectorySearch> spSearch;
    CComBSTR sbstrADsPath;
 
    // Bind to the group and get the IDirectorySearch interface.
    sbstrADsPath = "LDAP://";
    sbstrADsPath += pwszGroupDN;
    hr = ADsOpenObject(sbstrADsPath,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IDirectorySearch,
        (void**)&spSearch);
    if(FAILED(hr))
    {
        return hr;
    }
 
    ADS_SEARCHPREF_INFO SearchPrefs[1];

    // Set the ADS_SEARCHPREF_ATTRIBUTE_QUERY search preference.
    SearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_ATTRIBUTE_QUERY;
    SearchPrefs[0].vValue.dwType = ADSTYPE_CASE_IGNORE_STRING;
    SearchPrefs[0].vValue.CaseIgnoreString = L"member";

    // Set the search preferences.
    hr = spSearch->SetSearchPreference(SearchPrefs, sizeof(SearchPrefs)/sizeof(ADS_SEARCHPREF_INFO));
    if(FAILED(hr))
    {
        return hr;
    }

    ADS_SEARCH_HANDLE hSearch;
    
    // Create the search filter.
    LPWSTR pwszSearchFilter = L"(&(objectClass=user))";
 
    // Set attributes to return.
    LPWSTR rgpwszAttributes[] = {L"cn", L"distinguishedName"};
    DWORD dwNumAttributes = sizeof(rgpwszAttributes)/sizeof(LPWSTR);
 
    // Execute the search.
    hr = spSearch->ExecuteSearch(pwszSearchFilter,
        rgpwszAttributes,
        dwNumAttributes,
        &hSearch);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the first result row.
    hr = spSearch->GetFirstRow(hSearch);
    while(S_OK == hr)
    {
        ADS_SEARCH_COLUMN col;

        // Enumerate the retrieved attributes.
        for(DWORD i = 0; i < dwNumAttributes; i++)
        {
            hr = spSearch->GetColumn(hSearch, rgpwszAttributes[i], &col);
            if(SUCCEEDED(hr))
            {
                switch(col.dwADsType)
                {
                case ADSTYPE_DN_STRING:
                    wprintf(L"%s: %s\n\n", rgpwszAttributes[i], col.pADsValues[0].DNString);
                    break;

                case ADSTYPE_CASE_IGNORE_STRING:
                    wprintf(L"%s: %s\n\n", rgpwszAttributes[i], col.pADsValues[0].CaseExactString);
                    break;

                default:
                    break;
                }
                
                // Free the column.
                spSearch->FreeColumn(&col);
            }
        }
        
        // Get the next row.
        hr = spSearch->GetNextRow(hSearch);
    }

    // Close the search handle to cleanup.
    hr = spSearch->CloseSearchHandle(hSearch);

    return hr;
}
```



Wenn diese Suche ausgeführt wird und die Ergebnisse aufgezählt werden, gibt Sie den **Namen**, die **Telefonnummer** und die **Büronummer** aller Benutzer Objekte zurück, die **in der Element Attribut Liste** der Gruppe enthalten sind.

Fehlerbehandlung: die Ergebnisse einer Abfrage im Attribut Bereich können mehrere Server umfassen, und ein Server gibt möglicherweise nicht alle für alle zurückgegebenen Zeilen angeforderten Daten zurück. Wenn dies der Fall ist, wenn die letzte Zeile durch den Aufruf von [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) oder [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow)abgerufen wird, gibt ADSI die **e \_ ADS \_ errorsoccurrred** anstelle von **s \_ ADS \_ nomore- \_ Zeilen** zurück.

 

 