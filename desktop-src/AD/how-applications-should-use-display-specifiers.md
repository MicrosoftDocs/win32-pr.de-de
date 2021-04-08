---
title: Verwendung von Anzeige Spezifikations Anwendungen durch Anwendungen
description: Verwenden Sie zum Anzeigen von Active Directory-Domäne Dienst Objekten die Anzeige Spezifizierer, um lokalisierte Anzeigedaten für Klassen-und Attribut Objekte abzurufen.
ms.assetid: 2ba62906-47ae-4aab-8cb1-a5734eae5984
ms.tgt_platform: multiple
keywords:
- Verwendung von Anzeige spezifiken in Anwendungen
- Anzeige spezifiker anzeigen, wie Anwendungen Anzeige spezifiken verwenden sollten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f7045b03da282a9c64b216031e3da03a427268
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734817"
---
# <a name="how-applications-should-use-display-specifiers"></a><span data-ttu-id="f8f06-105">Verwendung von Anzeige Spezifikations Anwendungen durch Anwendungen</span><span class="sxs-lookup"><span data-stu-id="f8f06-105">How Applications Should Use Display Specifiers</span></span>

<span data-ttu-id="f8f06-106">Verwenden Sie zum Anzeigen von Active Directory-Domäne Dienst Objekten die Anzeige Spezifizierer, um lokalisierte Anzeigedaten für Klassen-und Attribut Objekte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f8f06-106">To display Active Directory Domain Service objects, use display specifiers to obtain localized display data for class and attribute objects.</span></span> <span data-ttu-id="f8f06-107">Dies ermöglicht die Verwendung lokalisierter Anzeige Namen und Symbole und vermeidet unnötige Lokalisierung der Anzeigedaten.</span><span class="sxs-lookup"><span data-stu-id="f8f06-107">This enables localized display names and icons to be used and avoids unnecessary localization of the display data.</span></span>

## <a name="display-names"></a><span data-ttu-id="f8f06-108">Anzeigen Amen</span><span class="sxs-lookup"><span data-stu-id="f8f06-108">Display Names</span></span>

<span data-ttu-id="f8f06-109">Die Eigenschaften **classdisplayname** und **attributeDisplayNames** der Anzeige spezifiziererobjekte für das entsprechende Gebiets Schema sollten verwendet werden, um Anzeige Text für Klassen-und Attributnamen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f8f06-109">The **classDisplayName** and **attributeDisplayNames** properties of the display specifier objects for the appropriate locale should be used to obtain display text for class and attribute names.</span></span> <span data-ttu-id="f8f06-110">Verwenden Sie die Eigenschaften " **CN**", " **classdisplayname** " oder " **ldapDisplayName** " der **classSchema** -oder **attributeSchema** -Objekte nicht zum Abrufen von Anzeige Text Bezeichnungen, da diese Werte nicht lokalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="f8f06-110">Do not use the **cn**, **classDisplayName** or **ldapDisplayName** properties of the **classSchema** or **attributeSchema** objects to obtain display text labels because these values are not localized.</span></span> <span data-ttu-id="f8f06-111">Weitere Informationen zum Abrufen von lokalisiertem Text für ein Klassenobjekt finden Sie im folgenden Beispielcode.</span><span class="sxs-lookup"><span data-stu-id="f8f06-111">For more information about how to retrieve localized text for a class object, see the following sample code.</span></span>

## <a name="icons"></a><span data-ttu-id="f8f06-112">Symbole</span><span class="sxs-lookup"><span data-stu-id="f8f06-112">Icons</span></span>

<span data-ttu-id="f8f06-113">Die **IconPath** -Eigenschaft der anzeigespezifiziererobjekte für das entsprechende Gebiets Schema sollte verwendet werden, um das Symbol abzurufen, das für ein Klassenobjekt angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f8f06-113">The **iconPath** property of the display specifier objects for the appropriate locale should be used to obtain the icon to display for a class object.</span></span> <span data-ttu-id="f8f06-114">Weitere Informationen finden Sie unter [Klassen Symbole](class-icons.md).</span><span class="sxs-lookup"><span data-stu-id="f8f06-114">For more information, see [Class Icons](class-icons.md).</span></span> <span data-ttu-id="f8f06-115">Wenn kein lokalisiertes Symbol für ein Klassenobjekt angegeben wird, sollte für das Element ein Standard Symbol angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f8f06-115">If no localized icon is specified for a class object, a default icon should be displayed for the item.</span></span>

## <a name="creating-new-objects"></a><span data-ttu-id="f8f06-116">Erstellen neuer Objekte</span><span class="sxs-lookup"><span data-stu-id="f8f06-116">Creating New Objects</span></span>

<span data-ttu-id="f8f06-117">Verwenden Sie nach Möglichkeit die entsprechenden Objekterstellungs-Assistenten, um neue Objekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f8f06-117">When possible, use the appropriate object creation wizards to create new objects.</span></span> <span data-ttu-id="f8f06-118">Weitere Informationen finden Sie unter [Aufrufen von Erstellungs-Assistenten aus Ihrer Anwendung](invoking-creation-wizards-from-your-application.md).</span><span class="sxs-lookup"><span data-stu-id="f8f06-118">For more information, see [Invoking Creation Wizards from Your Application](invoking-creation-wizards-from-your-application.md).</span></span>


<span data-ttu-id="f8f06-119">Im folgenden Codebeispiel wird gezeigt, wie Sie den Anzeige Text für eine Klasse und ein Attribut einer Klasse abrufen.</span><span class="sxs-lookup"><span data-stu-id="f8f06-119">The following code example shows how to obtain the display text for a class and an attribute of a class.</span></span>


```C++
#include <atlbase.h>

/**************************************************************************

    GetClassDisplaySpecifierContainer()

**************************************************************************/

HRESULT GetClassDisplaySpecifierContainer(LPWSTR pwszClass, 
                                          LCID locale, 
                                          IADs **ppads)
{
    if((NULL == pwszClass) || (NULL == ppads))
    {
        return E_INVALIDARG;
    }

    *ppads = NULL;
    
    // If no locale is specified, use the default system locale.
    if(0 == locale)
    {
        locale = GetSystemDefaultLCID();
        if(0 == locale)
        {
            return E_FAIL;
        }
    }
 
    // Verify that it is a valid locale.
    if(!IsValidLocale(locale, LCID_SUPPORTED))
    {
        return E_INVALIDARG;
    }
 
    HRESULT hr;
    IADs *padsRoot = NULL;
 
    hr = ADsOpenObject( L"LDAP://rootDSE",
                        NULL,
                        NULL,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs,
                        (void**)&padsRoot);
 
    if(SUCCEEDED(hr))
    {
        VARIANT var;

        VariantInit(&var);

        // Get the DN to the configuration container.
        hr = padsRoot->Get(CComBSTR(L"configurationNamingContext"), &var);
        
        if(SUCCEEDED(hr))
        {
            WCHAR wszPath[MAX_PATH * 2];

            // Build the string to bind to the container for the
            // specified locale in the DisplaySpecifiers container.
            swprintf_s(wszPath, 
                L"LDAP://cn=%s-Display,cn=%x,cn=DisplaySpecifiers,%s", 
                pwszClass, 
                locale, 
                var.bstrVal);

            VariantClear(&var);
            
            // Bind to the container.
            hr = ADsOpenObject( wszPath,
                                NULL,
                                NULL,
                                ADS_SECURE_AUTHENTICATION,
                                IID_IADs,
                                (void**)ppads);
 
        }

        padsRoot->Release();
    }

    return hr;
}

/**************************************************************************

    GetClassDisplayLabel()

**************************************************************************/

HRESULT GetClassDisplayLabel(LPWSTR pwszClass, 
                             LCID locale, 
                             BSTR *pbstrClassLabel)
{
    if((NULL == pwszClass) || (NULL == pbstrClassLabel))
    {
        return E_INVALIDARG;
    }

    *pbstrClassLabel = NULL;
    
    HRESULT hr;
    IADs *padsDispSpec;
    hr = GetClassDisplaySpecifierContainer(pwszClass, locale, &padsDispSpec);
    if(SUCCEEDED(hr))
    {
        VARIANT var;

        VariantInit(&var);

        // Get the classDisplayName property value.
        hr = padsDispSpec->Get(CComBSTR(L"classDisplayName"), &var);
        
        if(SUCCEEDED(hr))
        {
            if(VT_BSTR == var.vt)
            {
                // Do not free the BSTR. The caller will handle it.
                *pbstrClassLabel = var.bstrVal;
            }
            else
            {
                VariantClear(&var);
                hr = E_FAIL;
            }
        }
        
        padsDispSpec->Release();
    }

    return hr;
}

/**************************************************************************

    GetAttributeDisplayLabel()

**************************************************************************/

HRESULT GetAttributeDisplayLabel(LPWSTR pwszClass, 
                                 LPWSTR pwszAttribute, 
                                 LCID locale, 
                                 BSTR *pbstrAttributeLabel)
{
    if( (NULL == pwszClass) || 
        (NULL == pwszAttribute) || 
        (NULL == pbstrAttributeLabel))
    {
        return E_INVALIDARG;
    }

    *pbstrAttributeLabel = NULL;
    
    HRESULT hr;
    IADs *padsDispSpec;
    hr = GetClassDisplaySpecifierContainer(pwszClass, locale, &padsDispSpec);
    if(SUCCEEDED(hr))
    {
        VARIANT var;

        VariantInit(&var);

        // Get the attributeDisplayNames property values
        hr = padsDispSpec->GetEx(CComBSTR(L"attributeDisplayNames"), &var);
        
        if(SUCCEEDED(hr))
        {
            LONG        lStart, 
                        lEnd,
                        i;
            SAFEARRAY   *psa;
            VARIANT     varItem;

            VariantInit(&varItem);

            psa = V_ARRAY(&var);

            // Get the lower and upper bound.
            hr = SafeArrayGetLBound(psa, 1, &lStart);
            hr = SafeArrayGetUBound(psa, 1, &lEnd);

            /*
            The attributeDisplayNames values take the form 
            "<attribute name>,<display name>". Enumerate the values, looking 
            for the one that begins with the specified attribute name.
            */
            for(i = lStart; i <= lEnd; i++)
            {
                hr = SafeArrayGetElement(psa, &i, &varItem);
                if(SUCCEEDED(hr))
                {
                    WCHAR   wszTemp[MAX_PATH];

                    wcsncpy_s(wszTemp, 
                        V_BSTR(&varItem), 
                        lstrlenW(pwszAttribute) + 1);
                
                    if(0 == lstrcmpiW(pwszAttribute, wszTemp))
                    {
                        LPWSTR  pwszDisplayLabel;

                        /*
                        The proper value was found. Now, parse the value, looking 
                        for the first comma, which delimits the attribute name 
                        from the display name.
                        */
                        for(    pwszDisplayLabel = V_BSTR(&varItem); 
                                *pwszDisplayLabel; 
                                pwszDisplayLabel = CharNextW(pwszDisplayLabel))
                        {
                            if(',' == *pwszDisplayLabel)
                            {
                                /*
                                The delimiter was found. Set the string 
                                pointer to the next character, which is the 
                                first character of the display name.
                                */
                                pwszDisplayLabel = CharNextW(pwszDisplayLabel);
                                break;
                            }
                        }
                        
                        if(*pwszDisplayLabel)
                        {
                            // Copy the display name to the output.
                            *pbstrAttributeLabel = CComBSTR(pwszDisplayLabel).Detach();

                            hr = S_OK;
                        }

                        /*
                        Release the item variant because the break prevents 
                        it from getting released by the VariantClear call below.
                        */
                        VariantClear(&varItem);

                        break;
                    }

                    VariantClear(&varItem);
                }
            }
        }
        
        padsDispSpec->Release();
    }

    return hr;
}

```



 

 




