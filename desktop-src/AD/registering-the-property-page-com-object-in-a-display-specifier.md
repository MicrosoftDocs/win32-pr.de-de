---
title: Registrieren des COM-Objekts der Eigenschaften Seite in einem Anzeigespezifizierer
description: In diesem Thema wird gezeigt, wie Sie eine Erweiterungs-DLL registrieren, die eine Active Directory Eigenschaften Blatt mit der Windows-Registrierung und Active Directory enthält.
ms.assetid: e2d6142b-c2fe-4435-b4af-83f7cd45218b
ms.tgt_platform: multiple
keywords:
- Das COM-Objekt der Eigenschaften Seite wird in einem Anzeige Spezifizierer registriert Active Directory
- COM-Objekt Active Directory der Eigenschaften Seite, registrieren in einem Anzeigespezifizierer
- Anzeige spezifiker Active Directory, Registrieren des COM-Objekts der Eigenschaften Seite in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5b08ac0ea6329026a6d367e71064bde917b1a6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101427"
---
# <a name="registering-the-property-page-com-object-in-a-display-specifier"></a>Registrieren des COM-Objekts der Eigenschaften Seite in einem Anzeigespezifizierer

Wenn Sie com verwenden, um eine Eigenschaften Blatt-Erweiterungs-DLL für Active Directory Domain Services zu erstellen, müssen Sie die Erweiterung auch bei der Windows-Registrierung und Active Directory Domain Services registrieren. Durch die Registrierung der Erweiterung können die Active Directory Verwaltungs-MMC-Snap-Ins und die Windows-Shell die Erweiterung erkennen.

## <a name="registering-in-the-windows-registry"></a>Registrieren in der Windows-Registrierung

Wie alle com-Server muss eine Eigenschaften Blatt Erweiterung in der Windows-Registrierung registriert werden. Die Erweiterung wird unter dem folgenden Schlüssel registriert.

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

*<clsid>* die Zeichen folgen Darstellung der CLSID, die von der [**stringfromclsid**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) -Funktion erstellt wird. Unter dem *<clsid>* Schlüssel gibt es einen **InProcServer32** -Schlüssel, der das-Objekt als 32-Bit-in-proc-Server identifiziert. Unter der **InProcServer32** -Taste wird der Speicherort der dll im Standardwert angegeben, und das Threading Modell wird im **ThreadingModel** -Wert angegeben. Alle Eigenschaften Blatt Erweiterungen müssen das Threading Modell "Apartment" verwenden.

## <a name="registering-with-active-directory-domain-services"></a>Registrieren bei Active Directory Domain Services

Die Registrierung der Eigenschaften Blatt Erweiterung ist spezifisch für ein Gebiets Schema. Wenn die Eigenschafts Blatt Erweiterung auf alle Gebiets Schemas angewendet wird, muss Sie in allen Gebiets Schema-subcontainern im Container "Display Specifiers" im Objektklasse " [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) " registriert werden. Wenn die Eigenschaften Blatt Erweiterung für ein bestimmtes Gebiets Schema lokalisiert wird, registrieren Sie Sie im **Display specifier** -Objekt in diesem Gebiets Schema-unter Container. Weitere Informationen über die Anzeige spezifischere Container und Gebiets Schemas finden Sie unter [Anzeigen von Bezeichner](display-specifiers.md) und [displaySpecifier-Containern](displayspecifiers-container.md).

Es gibt drei anzeigespezifiziererattribute, unter denen eine Eigenschaften Blatt Erweiterung registriert werden kann. Dabei handelt es sich um [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellpropertypages**](/windows/desktop/ADSchema/a-shellpropertypages)und [**adminmultiselectpropertypages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages).

Das [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) -Attribut identifiziert Verwaltungs Eigenschaften Seiten, die in Active Directory administrativen Snap-Ins angezeigt werden sollen. Die Eigenschaften Seite wird angezeigt, wenn der Benutzereigenschaften für Objekte der entsprechenden Klasse in einem der Active Directory Verwaltungs-MMC-Snap-Ins anzeigt.

Das [**shellpropertypages**](/windows/desktop/ADSchema/a-shellpropertypages) -Attribut identifiziert die Eigenschaften Seiten der Endbenutzer, die in der Windows-Shell angezeigt werden. Die Eigenschaften Seite wird angezeigt, wenn der Benutzer die Eigenschaften für Objekte der entsprechenden Klasse im Windows-Explorer anzeigt. Ab den Windows Server 2003-Betriebssystemen werden von der Windows-Shell keine Objekte mehr aus Active Directory Domain Services angezeigt.

[**Adminmultiselectpropertypages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) ist nur unter den Betriebssystemen Windows Server 2003 verfügbar. Die Eigenschaften Seite wird angezeigt, wenn der Benutzer in einem der Active Directory-Verwaltungs-MMC-Snap-Ins Eigenschaften für mehr als ein Objekt der entsprechenden Klasse anzeigt.

Alle diese Attribute sind mehr wertig.

Die Werte für die Attribute " [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) " und " [**shellpropertypages**](/windows/desktop/ADSchema/a-shellpropertypages) " erfordern das folgende Format.


```C++
<order number>,<clsid>,<optional data>
```



Die Werte für das [**adminmultiselectpropertypages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) -Attribut erfordern das folgende Format.


```C++
<order number>,<clsid>
```



" &lt; Order Number &gt; " ist eine nicht signierte Zahl, die die Seitenposition im Blatt darstellt. Wenn ein Eigenschaften Blatt angezeigt wird, werden die Werte mithilfe eines Vergleichs der "Order Number"-Werte der einzelnen Werte sortiert &lt; &gt; . Wenn mehr als ein Wert dieselbe " &lt; Bestellnummer" aufweist &gt; , werden diese COM-Objekte der Eigenschaften Seite in der Reihenfolge geladen, in der Sie vom Active Directory Server gelesen werden. Wenn möglich, sollten Sie eine nicht vorhandene " &lt; Bestellnummer" verwenden, &gt; d. h. eine, die nicht von anderen Werten in der-Eigenschaft verwendet wird. Es gibt keine vorgeschriebene Anfangsposition, und Lücken sind in der Sequenz " &lt; Order Number &gt; " zulässig.

Die " &lt; CLSID &gt; " ist die Zeichen folgen Darstellung der CLSID, die von der [**stringfromclsid**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) -Funktion erstellt wird.

" &lt; Optionale Daten &gt; " ist ein Zeichen folgen Wert, der nicht erforderlich ist. Dieser Wert kann durch das COM-Objekt der Eigenschaften Seite abgerufen werden, indem der [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Zeiger an die zugehörige [**ishellextinit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) -Methode weitergegeben wird. Das COM-Objekt der Eigenschaften Seite erhält diese Daten durch Aufrufen von [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) mit dem Zwischenablage Format [**cfstr \_ dspropertypageinfo**](cfstr-dspropertypageinfo.md) . Dadurch wird ein **HGLOBAL** bereitstellt, das eine [**dspropertypageinfo**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) -Struktur enthält. die **dspropertypageinfo** -Struktur enthält eine Unicode-Zeichenfolge, die die " &lt; optionalen Daten &gt; " enthält. Die " &lt; optionalen Daten &gt; " sind mit dem Attribut " [**adminmultiselectpropertypages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) " nicht zulässig. Im folgenden C/C++-Codebeispiel wird gezeigt, wie die " &lt; optionalen Daten" abgerufen werden &gt; .


```C++
fe.cfFormat = RegisterClipboardFormat(CFSTR_DSPROPERTYPAGEINFO);
fe.ptd = NULL;
fe.dwAspect = DVASPECT_CONTENT;
fe.lindex = -1;
fe.tymed = TYMED_HGLOBAL;
hr = pDataObj->GetData(&fe, &stm);
if(SUCCEEDED(hr))
{
    DSPROPERTYPAGEINFO *pPageInfo;
    
    pPageInfo = (DSPROPERTYPAGEINFO*)GlobalLock(stm.hGlobal);
    if(pPageInfo)
    {
        LPWSTR  pwszData;

        pwszData = (LPWSTR)((LPBYTE)pPageInfo + pPageInfo->offsetString);
        pwszData = NULL;
        
        GlobalUnlock(stm.hGlobal);
    }

    ReleaseStgMedium(&stm);
}
```



Eine Eigenschaften Blatt Erweiterung kann mehr als eine Eigenschaften Seite implementieren. eine mögliche Verwendung der " &lt; optionalen Daten &gt; " besteht darin, die Seiten für die Anzeige zu benennen. Dies bietet die Flexibilität, mehrere COM-Objekte, eine für jede Seite oder ein einzelnes COM-Objekt zu implementieren, um mehrere Seiten zu verarbeiten.

Das folgende Codebeispiel ist ein Beispiel Wert, der für die Attribute [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellpropertypages**](/windows/desktop/ADSchema/a-shellpropertypages)oder [**adminmultiselectpropertypages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) verwendet werden kann.


```C++
1,{6dfe6485-a212-11d0-bcd5-00c04fd8d5b6}
```



> [!IMPORTANT]
> Bei der Windows-Shell werden Anzeige spezifiziererdaten bei der Benutzeranmeldung abgerufen und für die Benutzersitzung zwischengespeichert. Bei administrativen Snap-Ins werden die Anzeige spezifiziererdaten abgerufen, wenn das Snap-In geladen wird. Sie werden für die Lebensdauer des Prozesses zwischengespeichert. Bei der Windows-Shell bedeutet dies, dass Änderungen an Anzeige spezifiken wirksam werden, nachdem ein Benutzer sich abmeldet und sich dann erneut anmeldet. Bei den administrativen Snap-Ins werden die Änderungen wirksam, wenn das Snap-in oder die Konsolen Datei geladen wird.

 

## <a name="adding-a-value-to-the-property-sheet-extension-attributes"></a>Hinzufügen eines Werts zu den Eigenschaften Blatt-Erweiterungs Attributen

Im folgenden Verfahren wird beschrieben, wie Sie eine Eigenschaften Blatt Erweiterung unter einem der Eigenschaften Blatt-Erweiterungs Attribute registrieren.

**Registrieren einer Eigenschaften Blatt Erweiterung unter einem der Eigenschaften Blatt-Erweiterungs Attribute**

1.  Stellen Sie sicher, dass die Erweiterung nicht bereits in den Attributwerten vorhanden ist.
2.  Fügen Sie den neuen Wert am Ende der Bestellliste der Eigenschaften Seite hinzu. Dies ist der " &lt; Order Number &gt; "-Teil des Attribut Werts auf den nächsten Wert nach der höchsten vorhandenen Bestellnummer festgelegt.
3.  Die [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) -Methode wird verwendet, um dem Attribut den neuen Wert hinzuzufügen. Der Parameter " *lncontrolcode* " muss auf die Anzeige **Eigenschaft " \_ \_ Append** " festgelegt werden, damit der neue Wert an die vorhandenen Werte angehängt wird und die vorhandenen Werte daher nicht überschreibt. Die [**IADs::**](/windows/desktop/api/iads/nf-iads-iads-setinfo) *-Methode muss nachträglich aufgerufen werden, um die Änderung in das Verzeichnis zu übertragen.

Beachten Sie, dass die gleiche Eigenschaften Blatt Erweiterung für mehr als eine Objektklasse registriert werden kann.

Die [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) -Methode wird verwendet, um dem Attribut den neuen Wert hinzuzufügen. Der Parameter " *lncontrolcode* " muss auf die **ADS-Eigenschaft " \_ \_ Append**" festgelegt werden, sodass der neue Wert an die vorhandenen Werte angehängt wird und die vorhandenen Werte daher nicht überschreibt. Die [**IADs::**](/windows/desktop/api/iads/nf-iads-iads-setinfo) *-Methode muss nach aufgerufen werden, um die Änderung in das Verzeichnis zu übertragen.

Im folgenden Codebeispiel wird der Group-Klasse im Standard Gebiets Schema des Computers eine Eigenschaften Blatt Erweiterung hinzugefügt. Beachten Sie, dass die **addpropertypagededisplayspecifier** -Funktion die CLSID der Eigenschafts Blatt Erweiterung in den vorhandenen Werten überprüft, die höchste Bestellnummer abruft und den Wert für die Eigenschaften Seite mithilfe von [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) mit der **ADS- \_ Eigenschaft \_ Append** -Steuerungs Code hinzufügt.


```C++
//  Add msvcrt.dll to the project.
//  Add activeds.lib to the project.
//  Add adsiid.lib to the project.

#include "stdafx.h"
#include <wchar.h>
#include <objbase.h>
#include <activeds.h>
#include "atlbase.h"

HRESULT AddPropertyPageToDisplaySpecifier(LPOLESTR szClassName, //  ldapDisplayName of the class.
                                          CLSID *pPropPageCLSID //  CLSID of property page COM object.
                                         );

HRESULT BindToDisplaySpecifiersContainerByLocale(LCID *locale,
                                                 IADsContainer **ppDispSpecCont
                                                 );

HRESULT GetDisplaySpecifier(IADsContainer *pContainer, LPOLESTR szDispSpec, IADs **ppObject);

//  Entry point for the application.
void wmain(int argc, wchar_t *argv[ ])
{

    wprintf(L"This program adds a sample property page to the display specifier for group class in the local computer's default locale.\n");

    // Initialize COM.
    CoInitialize(NULL);
    HRESULT hr = S_OK;

    //  Class ID for the sample property page.
    LPOLESTR szCLSID = L"{D9FCE809-8A10-11d2-A7E7-00C04F79DC0F}";
    LPOLESTR szClass = L"group";
    CLSID clsid;
    //  Convert to GUID.
    hr = CLSIDFromString(
        szCLSID,  //  Pointer to the string representation of the CLSID.
        &clsid    //  Pointer to the CLSID.
        );

    hr = AddPropertyPageToDisplaySpecifier(szClass, //  ldapDisplayName of the class.
                                           &clsid //  CLSID of property page COM object.
                                          );
    if (S_OK == hr)
        wprintf(L"Property page registered successfully\n");
    else if (S_FALSE == hr)
        wprintf(L"Property page was not added because it was already registered.\n");
    else
        wprintf(L"Property page was not added. HR: %x.\n");

    //  Uninitialize COM.
    CoUninitialize();
    return;
}

//  Adds a property page to Active Directory admin snap-ins.
HRESULT AddPropertyPageToDisplaySpecifier(LPOLESTR szClassName, //  ldapDisplayName of class.
                                          CLSID *pPropPageCLSID //  CLSID of property page COM object.
                                         )
{
    HRESULT hr = E_FAIL;
    IADsContainer *pContainer = NULL;
    LPOLESTR szDispSpec = new OLECHAR[MAX_PATH];
    IADs *pObject = NULL;
    VARIANT var;
    CComBSTR sbstrProperty = L"adminPropertyPages";
    LCID locale = NULL;
    //  Get the display specifier container using default system locale.
    //  When adding a property page COM object, specify the locale
    //  because the registration is locale-specific.
    //  This means if you created a property page
    //  for German, explicitly add it to the 407 container,
    //  so that it will be used when a computer is running with locale
    //  set to German and not the locale set on the
    //  computer where this application is running.
    hr = BindToDisplaySpecifiersContainerByLocale(&locale,
                                                  &pContainer
                                                 );
    //  Handle fail case where dispspec object
    //  is not found and give option to create one.

    if (SUCCEEDED(hr))
    {
        //  Bind to display specifier object for the specified class.
        //  Build the display specifier name.
#ifdef _MBCS
        wcscpy_s(szDispSpec, szClassName);
        wcscat_s(szDispSpec, L"-Display");
        hr = GetDisplaySpecifier(pContainer, szDispSpec, &pObject);
#endif _MBCS#endif _MBCS
        if (SUCCEEDED(hr))
        {
            //  Convert GUID to string.
            LPOLESTR szDSGUID = new WCHAR [39];
            ::StringFromGUID2(*pPropPageCLSID, szDSGUID, 39); 

            //  Get the adminPropertyPages property.
            hr = pObject->GetEx(sbstrProperty, &var);
            if (SUCCEEDED(hr))
            {
                LONG lstart, lend;
                SAFEARRAY *sa = V_ARRAY(&var);
                VARIANT varItem;
                //  Get the lower and upper bound.
                hr = SafeArrayGetLBound(sa, 1, &lstart);
                if (SUCCEEDED(hr))
                {
                    hr = SafeArrayGetUBound(sa, 1, &lend);
                }
                if (SUCCEEDED(hr))
                {
                    //  Iterate the values to verify if the prop page CLSID
                    //  is already registered.
                    VariantInit(&varItem);
                    BOOL bExists = FALSE;
                    UINT uiLastItem = 0;
                    UINT uiTemp = 0;
                    INT iOffset = 0;
                    LPOLESTR szMainStr = new OLECHAR[MAX_PATH];
                    LPOLESTR szItem = new OLECHAR[MAX_PATH];
                    LPOLESTR szStr = NULL;
                    for (long idx=lstart; idx <= lend; idx++)
                    {
                        hr = SafeArrayGetElement(sa, &idx, &varItem);
                        if (SUCCEEDED(hr))
                        {
#ifdef _MBCS
                            //  Verify that the specified CLSID is already registered.
                            wcscpy_s(szMainStr,varItem.bstrVal);
                            if (wcsstr(szMainStr,szDSGUID))
                                bExists = TRUE;
                            //  Get the index which is the number before the first comma.
                            szStr = wcschr(szMainStr, ',');
                            iOffset = (int)(szStr - szMainStr);
                            wcsncpy_s(szItem, szMainStr, iOffset);
                            szItem[iOffset]=0L;
                            uiTemp = _wtoi(szItem);
                            if (uiTemp > uiLastItem)
                                uiLastItem = uiTemp;
                            VariantClear(&varItem);
#endif _MBCS
                        }
                    }
                    //  If the CLSID is not registered, add it.
                    if (!bExists)
                    {
                        //  Build the value to add.
                        LPOLESTR szValue = new OLECHAR[MAX_PATH];
                        //  Next index to add at end of list.
#ifdef _MBCS
                        uiLastItem++;
                        _itow_s(uiLastItem, szValue, 10);   
                        wcscat_s(szValue,L",");
                        //  Add the class ID for the property page.
                        wcscat_s(szValue,szDSGUID);
                        wprintf(L"Value to add: %s\n", szValue);
#endif _MBCS

                        VARIANT varAdd;
                        //  Only one value to add
                        LPOLESTR pszAddStr[1];
                        pszAddStr[0]=szValue;
                        ADsBuildVarArrayStr(pszAddStr, 1, &varAdd);

                        hr = pObject->PutEx(ADS_PROPERTY_APPEND, sbstrProperty, varAdd);
                        if (SUCCEEDED(hr))
                        {
                            //  Commit the change.
                            hr = pObject->SetInfo();
                        }
                    }
                    else
                        hr = S_FALSE;
                }
            }
            VariantClear(&var);
        }
        if (pObject)
            pObject->Release();
    }

    return hr;
}

//  This function returns a pointer to the display specifier container 
//  for the specified locale.
//  If locale is NULL, use the default system locale and then return the locale in the locale param.
HRESULT BindToDisplaySpecifiersContainerByLocale(LCID *locale,
                                                 IADsContainer **ppDispSpecCont
                                                )
{
    HRESULT hr = E_FAIL;

    if ((!ppDispSpecCont)||(!locale))
        return E_POINTER;

    //  If no locale is specified, use the default system locale.
    if (!(*locale))
    {
        *locale = GetSystemDefaultLCID();
        if (!(*locale))
            return E_FAIL;
    }

    //  Verify that it is a valid locale.
    if (!IsValidLocale(*locale, LCID_SUPPORTED))
        return E_INVALIDARG;

    LPOLESTR szPath = new OLECHAR[MAX_PATH*2];
    IADs *pObj = NULL;
    VARIANT var;

    hr = ADsOpenObject(L"LDAP://rootDSE",
                       NULL,
                       NULL,
                       ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                       IID_IADs,
                       (void**)&pObj);

    if (SUCCEEDED(hr))
    {
        //  Get the DN to the config container.
        hr = pObj->Get(CComBSTR("configurationNamingContext"), &var);
        if (SUCCEEDED(hr))
        {
#ifdef _MBCS
            //  Build the string to bind to the DisplaySpecifiers container.
            swprintf_s(szPath,L"LDAP://cn=%x,cn=DisplaySpecifiers,%s", *locale, var.bstrVal);
            //  Bind to the DisplaySpecifiers container.
            *ppDispSpecCont = NULL;
            hr = ADsOpenObject(szPath,
                               NULL,
                               NULL,
                               ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                               IID_IADsContainer,
                               (void**)ppDispSpecCont);
#endif _MBCS

            if(FAILED(hr))
            {
                if (*ppDispSpecCont)
                {
                    (*ppDispSpecCont)->Release();
                    (*ppDispSpecCont) = NULL;
                }
            }
        }
    }
    //   Cleanup.
    VariantClear(&var);
    if (pObj)
        pObj->Release();

    return hr;
}

HRESULT GetDisplaySpecifier(IADsContainer *pContainer, LPOLESTR szDispSpec, IADs **ppObject)
{
    HRESULT hr = E_FAIL;
    CComBSTR sbstrDSPath;
    IDispatch *pDisp = NULL;

    if (!pContainer)
    {
        hr = E_POINTER;
        return hr;
    }

    //  Verify other pointers.
    //  Initialize the output pointer.
    (*ppObject) = NULL;

    //  Build relative path to the display specifier object.
    sbstrDSPath = "CN=";
    sbstrDSPath += szDispSpec;

    //  Use child object binding with IADsContainer::GetObject.
    hr = pContainer->GetObject(CComBSTR("displaySpecifier"),
        sbstrDSPath,
        &pDisp);
    if (SUCCEEDED(hr))
    {
        hr = pDisp->QueryInterface(IID_IADs, (void**)ppObject);
        if (FAILED(hr))
        {
            //  Clean up.
            if (*ppObject)
                (*ppObject)->Release();
        }
    }

    if (pDisp)
        pDisp->Release();

    return hr;

}
```



 

 