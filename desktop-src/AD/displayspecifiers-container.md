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
# <a name="displayspecifiers-container"></a><span data-ttu-id="6ea0a-106">DisplaySpecifier-Container</span><span class="sxs-lookup"><span data-stu-id="6ea0a-106">DisplaySpecifiers Container</span></span>

<span data-ttu-id="6ea0a-107">Anzeige spezifiatoren werden nach Gebiets Schema im displaySpecifier-Container des Konfigurations Containers gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6ea0a-107">Display specifiers are stored, by locale, in the DisplaySpecifiers container of the Configuration container.</span></span> <span data-ttu-id="6ea0a-108">Da der Konfigurations Container über die gesamte Gesamtstruktur repliziert wird, werden die Anzeige spezifizierte über alle Domänen in einer Gesamtstruktur hinweg weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="6ea0a-108">Because the Configuration container is replicated across the entire forest, display specifiers are propagated across all domains in a forest.</span></span>

<span data-ttu-id="6ea0a-109">Der Konfigurations Container speichert den displayspecifies-Container, der dann Container speichert, die den einzelnen Gebiets Schemas entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6ea0a-109">The Configuration container stores the DisplaySpecifiers container, which then stores containers that correspond to each locale.</span></span> <span data-ttu-id="6ea0a-110">Diese Gebiets Schema Container werden mithilfe der hexadezimalen Darstellung des Gebiets Schema Bezeichners benannt.</span><span class="sxs-lookup"><span data-stu-id="6ea0a-110">These locale containers are named using the hexadecimal representation of the locale identifier.</span></span> <span data-ttu-id="6ea0a-111">Beispielsweise hat der Gebiets Schema Container US/English den Namen 409, der Container des deutschen Gebiets Schemas den Namen 407, und der Container des japanischen Gebiets Schemas heißt 411.</span><span class="sxs-lookup"><span data-stu-id="6ea0a-111">For example, the US/English locale container is named 409, the German locale's container is named 407, and the Japanese locale's container is named 411.</span></span> <span data-ttu-id="6ea0a-112">Weitere Informationen und eine Liste der möglichen sprach Bezeichner finden Sie unter [sprach Bezeichner-Konstanten und-](/windows/desktop/Intl/language-identifier-constants-and-strings)Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="6ea0a-112">For more information, and a list of possible language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

<span data-ttu-id="6ea0a-113">Jeder locale-Container speichert Objekte der [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="6ea0a-113">Each locale container stores objects of the [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) class.</span></span>

<span data-ttu-id="6ea0a-114">Um alle Anzeige Spezifizierer für ein Gebiets Schema aufzulisten, zählen Sie alle [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) -Objekte im angegebenen Gebiets Schema Container im DisplaySpecifiers-Container auf.</span><span class="sxs-lookup"><span data-stu-id="6ea0a-114">To list all display specifiers for a locale, enumerate all the [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) objects in the specified locale container within the DisplaySpecifiers container.</span></span>

<span data-ttu-id="6ea0a-115">Das folgende Codebeispiel enthält eine Funktion, die an den Anzeige spezifizierercontainer für das angegebene Gebiets Schema gebunden wird:</span><span class="sxs-lookup"><span data-stu-id="6ea0a-115">The following code example contains a function that binds to the display specifier container for the specified locale:</span></span>


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



 

 