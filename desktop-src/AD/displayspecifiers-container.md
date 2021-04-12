---
title: DisplaySpecifier-Container
description: Anzeige spezifiatoren werden nach Gebiets Schema im displaySpecifier-Container des Konfigurations Containers gespeichert. Da der Konfigurations Container über die gesamte Gesamtstruktur repliziert wird, werden die Anzeige spezifizierte über alle Domänen in einer Gesamtstruktur hinweg weitergegeben.
ms.assetid: d7647c50-f95c-41ef-8d67-dc72542cae5a
ms.tgt_platform: multiple
keywords:
- DisplaySpecifier-Container
- Container, Anzeige spezifiker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 406258a6c9983581491420a49621e3d10df4601e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472588"
---
# <a name="displayspecifiers-container"></a>DisplaySpecifier-Container

Anzeige spezifiatoren werden nach Gebiets Schema im displaySpecifier-Container des Konfigurations Containers gespeichert. Da der Konfigurations Container über die gesamte Gesamtstruktur repliziert wird, werden die Anzeige spezifizierte über alle Domänen in einer Gesamtstruktur hinweg weitergegeben.

Der Konfigurations Container speichert den displayspecifies-Container, der dann Container speichert, die den einzelnen Gebiets Schemas entsprechen. Diese Gebiets Schema Container werden mithilfe der hexadezimalen Darstellung des Gebiets Schema Bezeichners benannt. Beispielsweise hat der Gebiets Schema Container US/English den Namen 409, der Container des deutschen Gebiets Schemas den Namen 407, und der Container des japanischen Gebiets Schemas heißt 411. Weitere Informationen und eine Liste der möglichen sprach Bezeichner finden Sie unter [sprach Bezeichner-Konstanten und-](/windows/desktop/Intl/language-identifier-constants-and-strings)Zeichen folgen.

Jeder locale-Container speichert Objekte der [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) -Klasse.

Um alle Anzeige Spezifizierer für ein Gebiets Schema aufzulisten, zählen Sie alle [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) -Objekte im angegebenen Gebiets Schema Container im DisplaySpecifiers-Container auf.

Das folgende Codebeispiel enthält eine Funktion, die an den Anzeige spezifizierercontainer für das angegebene Gebiets Schema gebunden wird:


```C++
/**********
This function returns a pointer to the display specifier container 
for the specified locale.

If locale is NULL, use default system locale and then return the 
locale in the locale parameter.
***********/
HRESULT BindToDisplaySpecifiersContainerByLocale(
    LCID *locale,
    IADs **ppDispSpecCont)
{
HRESULT hr = E_FAIL;
 
if ((!ppDispSpecCont)||(!locale))
    return E_POINTER;
 
// If no locale is specified, use the default system locale.
if (!(*locale))
{
    *locale = GetSystemDefaultLCID();
    if (!(*locale))
        return E_FAIL;
}
 
// Be sure that the locale is valid.
if (!IsValidLocale(*locale, LCID_SUPPORTED))
    return E_INVALIDARG;
 
LPOLESTR szPath = new OLECHAR[MAX_PATH*2];
IADs *pObj = NULL;
VARIANT var;
 
hr = ADsOpenObject(L"LDAP://rootDSE",
                     NULL,
                     NULL,
                     ADS_SECURE_AUTHENTICATION,
                     IID_IADs,
                     (void**)&pObj);
 
if (SUCCEEDED(hr))
{
    // Get the DN to the configuration container.
    hr = pObj->Get(CComBSTR("configurationNamingContext"), &var);
    if (SUCCEEDED(hr))
    {
        // Build the string to bind to the container for the
        // specified locale in the DisplaySpecifiers container.
        swprintf_s(
            szPath, 
            L"LDAP://cn=%x,cn=DisplaySpecifiers,%s", 
            *locale, 
            var.bstrVal);

        // Bind to the container.
        *ppDispSpecCont = NULL;
        hr = ADsOpenObject(szPath,
                     NULL,
                     NULL,
                     ADS_SECURE_AUTHENTICATION,
                     IID_IADs,
                     (void**)ppDispSpecCont);
 
        if(FAILED(hr))
        {
            if ((*ppDispSpecCont))
            {
                (*ppDispSpecCont)->Release();
                (*ppDispSpecCont) = NULL;
            }
        }
    }
}
 
// Cleanup.
VariantClear(&var);
if (pObj)
    pObj->Release();
 
return hr;
}
```



 

 