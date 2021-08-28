---
title: Registrieren des COM-Objekts der Eigenschaftenseite in einem Anzeigespezifizierer
description: In diesem Thema wird gezeigt, wie Sie eine Erweiterungs-DLL registrieren, die ein Active Directory-Eigenschaftenblatt bei der Windows Active Directory enthält.
ms.assetid: e2d6142b-c2fe-4435-b4af-83f7cd45218b
ms.tgt_platform: multiple
keywords:
- Registrieren des COM-Objekts der Eigenschaftenseite in einem Active Directory-Anzeigespezifizierer
- Eigenschaftenseite COM-Objekt Active Directory , Registrierung in einem Anzeigespezifizierer
- Anzeigespezifizierer Active Directory , Registrieren des COM-Objekts der Eigenschaftenseite in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f6685e406cb1bfdc16f73dd2fddd94a195fe74a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881238"
---
# <a name="registering-the-property-page-com-object-in-a-display-specifier"></a>Registrieren des COM-Objekts der Eigenschaftenseite in einem Anzeigespezifizierer

Wenn Sie COM verwenden, um eine Dll für eigenschaftenblatterweiterungen für Active Directory Domain Services zu erstellen, müssen Sie die Erweiterung auch bei der Windows registrieren und Active Directory Domain Services. Durch das Registrieren der Erweiterung können die MMC-Snap-Ins der Active Directory-Verwaltung und die Windows Shell die Erweiterung erkennen.

## <a name="registering-in-the-windows-registry"></a>Registrieren in der Windows Registrierung

Wie alle COM-Server muss auch eine Eigenschaftenblatterweiterung in der Windows werden. Die Erweiterung wird unter dem folgenden Schlüssel registriert.

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

*&lt; clsid &gt; ist* die Zeichenfolgendarstellung der CLSID, die von der [**StringFromCLSID-Funktion erzeugt**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) wird. Unter dem *&lt; &gt; clsid-Schlüssel* befindet sich ein **InProcServer32-Schlüssel,** der das Objekt als 32-Bit-In-Proc-Server identifiziert. Unter dem **InProcServer32-Schlüssel** wird der Speicherort der DLL im Standardwert und das Threadingmodell im **ThreadingModel-Wert** angegeben. Alle Eigenschaftenblatterweiterungen müssen das Threadingmodell "Apartment" verwenden.

## <a name="registering-with-active-directory-domain-services"></a>Registrieren bei Active Directory Domain Services

Die Registrierung der Eigenschaftenblatterweiterung ist für ein einzelnes Locale spezifisch. Wenn die Eigenschaftenblatterweiterung für alle Locales gilt, muss sie in der Objektklasse [**displaySpecifier-Objekt**](/windows/desktop/ADSchema/c-displayspecifier) in allen Locale-Untercontainern im Container Anzeigespezifizierer registriert werden. Wenn die Eigenschaftenblatterweiterung für ein bestimmtes Locale lokalisiert ist, registrieren Sie sie im **displaySpecifier-Objekt** in diesem Untercontainer des Locale. Weitere Informationen zum Container "Display Specifiers" und zu den Lokalen finden Sie unter [Display Specifiers](display-specifiers.md) and DisplaySpecifiers Container (Anzeigespezifizierer und [DisplaySpecifiers-Container).](displayspecifiers-container.md)

Es gibt drei Anzeigespezifiziererattribute, unter denen eine Eigenschaftenblatterweiterung registriert werden kann. Dies [**sind adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages)und [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages).

Das [**attribut adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) identifiziert Verwaltungseigenschaftenseiten, die in Active Directory-Administrator-Snap-Ins angezeigt werden. Die Eigenschaftenseite wird angezeigt, wenn der Benutzer Eigenschaften für Objekte der entsprechenden Klasse in einem der MMC-Snap-Ins der Active Directory-Verwaltung einsichtet.

Das [**shellPropertyPages-Attribut**](/windows/desktop/ADSchema/a-shellpropertypages) identifiziert Eigenschaftenseiten von Endbenutzern, die in der Windows angezeigt werden. Die Eigenschaftenseite wird angezeigt, wenn der Benutzer die Eigenschaften für Objekte der entsprechenden Klasse im Windows anzeigt. Ab den Betriebssystemen Windows Server 2003 zeigt die Windows-Shell keine Objekte mehr aus Active Directory Domain Services.

[**AdminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) ist nur auf den betriebssystemen Windows Server 2003 verfügbar. Die Eigenschaftenseite wird angezeigt, wenn der Benutzer Eigenschaften für mehr als ein Objekt der entsprechenden Klasse in einem der MMC-Snap-Ins der Active Directory-Verwaltung einsichtet.

Alle diese Attribute sind mehrwertige Attribute.

Die Werte für [**die Attribute adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) und [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) erfordern das folgende Format.


```C++
<order number>,<clsid>,<optional data>
```



Die Werte für das [**adminMultiselectPropertyPages-Attribut**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) erfordern das folgende Format.


```C++
<order number>,<clsid>
```



Die &lt; "Bestellnummer" &gt; ist eine Zahl ohne Vorzeichen, die die Seitenposition auf dem Blatt darstellt. Wenn ein Eigenschaftenblatt angezeigt wird, werden die Werte anhand eines Vergleichs der Bestellnummer jedes &lt; Werts &gt; sortiert. Wenn mehr als ein Wert über die gleiche "Bestellnummer" verfügt, werden diese COM-Objekte der Eigenschaftenseite in der Reihenfolge geladen, in der sie vom &lt; &gt; Active Directory-Server gelesen werden. Wenn möglich, sollten Sie eine nicht vorhandene "Bestellnummer" verwenden, d.> eine, die nicht von anderen Werten &lt; &gt; in der -Eigenschaft verwendet wird. Es gibt keine vorgeschriebene Anfangsposition, und Lücken sind in der Sequenz " &lt; Bestellnummer &gt; " zulässig.

&lt;"clsid" &gt; ist die Zeichenfolgendarstellung der CLSID, die von der [**StringFromCLSID-Funktion erzeugt**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) wird.

Der &lt; optionale &gt; Datenwert ist ein Zeichenfolgenwert, der nicht erforderlich ist. Dieser Wert kann vom COM-Objekt der Eigenschaftenseite mithilfe des [**IDataObject-Zeigers**](/windows/win32/api/objidl/nn-objidl-idataobject) abgerufen werden, der an die [**IShellExtInit::Initialize-Methode übergeben**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) wird. Das COM-Objekt der Eigenschaftenseite ruft diese Daten ab, indem [**es IDataObject::GetData mit**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) dem [**CFSTR \_ DSPROPERTYPAGEINFO-Zwischenablageformat**](cfstr-dspropertypageinfo.md) aufruft. Dies stellt ein **HGLOBAL-Objekt** mit einer [**DSPROPERTYPAGEINFO-Struktur**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) zur Verfügung. Die **DSPROPERTYPAGEINFO-Struktur** enthält eine Unicode-Zeichenfolge, die die &lt; optionalen Daten &gt; enthält. Das &lt; optionale &gt; Datenattribut [**"adminMultiselectPropertyPages" ist nicht**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) zulässig. Das folgende C/C++-Codebeispiel zeigt, wie die optionalen &lt; Daten abgerufen &gt; werden.


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



Eine Eigenschaftenblatterweiterung kann mehrere Eigenschaftenseiten implementieren. Eine mögliche Verwendung von &lt; "optional data" ist das &gt; Benennen der anzuzeigenden Seiten. Dies bietet die Flexibilität, mehrere COM-Objekte zu implementieren, eines für jede Seite oder ein einzelnes COM-Objekt, um mehrere Seiten zu verarbeiten.

Das folgende Codebeispiel ist ein Beispielwert, der für die [**Attribute adminPropertyPages,**](/windows/desktop/ADSchema/a-adminpropertypages) [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages)oder [**adminMultiselectPropertyPages verwendet**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) werden kann.


```C++
1,{6dfe6485-a212-11d0-bcd5-00c04fd8d5b6}
```



> [!IMPORTANT]
> Für die Windows-Shell werden Anzeigespezifiziererdaten bei der Benutzeranmeldung abgerufen und für die Benutzersitzung zwischengespeichert. Bei administrativen Snap-Ins werden die Anzeigespezifiziererdaten beim Laden des Snap-Ins abgerufen und für die Lebensdauer des Prozesses zwischengespeichert. Für die Windows Shell gibt dies an, dass Änderungen an Anzeigespezifizierern wirksam werden, nachdem sich ein Benutzer abgemelgt hat und sich dann erneut anmeldet. Für die administrativen Snap-Ins werden Änderungen wirksam, wenn das Snap-In oder die Konsolendatei geladen wird.

 

## <a name="adding-a-value-to-the-property-sheet-extension-attributes"></a>Hinzufügen eines Werts zu den Eigenschaftenblatterweiterungsattributen

Im folgenden Verfahren wird beschrieben, wie Sie eine Eigenschaftenblatterweiterung unter einem der Eigenschaftenblatterweiterungsattribute registrieren.

**Registrieren einer Eigenschaftenblatterweiterung unter einem der Eigenschaftenblatterweiterungsattribute**

1.  Stellen Sie sicher, dass die Erweiterung nicht bereits in den Attributwerten vorhanden ist.
2.  Fügen Sie den neuen Wert am Ende der Sortierungsliste der Eigenschaftenseite hinzu. Dies wird für den Teil " Bestellnummer " des Attributwerts auf den nächsten Wert nach &lt; &gt; der höchsten vorhandenen Bestellnummer festgelegt.
3.  Die [**IADs::P utEx-Methode**](/windows/desktop/api/iads/nf-iads-iads-putex) wird verwendet, um dem Attribut den neuen Wert hinzuzufügen. Der *lnControlCode-Parameter* muss auf **ADS PROPERTY \_ \_ APPEND** festgelegt werden, damit der neue Wert an die vorhandenen Werte angefügt wird und daher die vorhandenen Werte nicht überschreibt. Die [**IADs::SetInfo-Methode**](/windows/desktop/api/iads/nf-iads-iads-setinfo) muss anschließend aufgerufen werden, um die Änderung im Verzeichnis zu commiten.

Beachten Sie, dass dieselbe Eigenschaftenblatterweiterung für mehrere Objektklassen registriert werden kann.

Die [**IADs::P utEx-Methode**](/windows/desktop/api/iads/nf-iads-iads-putex) wird verwendet, um dem Attribut den neuen Wert hinzuzufügen. Der *lnControlCode-Parameter* muss auf **ADS PROPERTY \_ \_ APPEND** festgelegt werden, damit der neue Wert an die vorhandenen Werte angefügt wird und daher die vorhandenen Werte nicht überschreibt. Die [**IADs::SetInfo-Methode**](/windows/desktop/api/iads/nf-iads-iads-setinfo) muss nach aufgerufen werden, um die Änderung an das Verzeichnis zu commiten.

Im folgenden Codebeispiel wird der Gruppenklasse im Standard-Locale des Computers eine Eigenschaftenblatterweiterung hinzufügt. Beachten Sie, dass die **AddPropertyPageToDisplaySpecifier-Funktion** die CLSID der Eigenschaftenblatterweiterung in den vorhandenen Werten überprüft, die höchste Reihenfolgennummer erhält und den Wert für die Eigenschaftenseite mithilfe von [**IADs::P utEx**](/windows/desktop/api/iads/nf-iads-iads-putex) mit dem **ADS PROPERTY \_ \_ APPEND-Steuerelementcode** hinzufügt.


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



 

 
