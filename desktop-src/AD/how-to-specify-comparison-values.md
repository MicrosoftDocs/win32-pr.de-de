---
title: Angeben von Vergleichswerten
description: Jeder Attributtyp verfügt über eine Syntax, die den Typ der Vergleichswerte bestimmt, die Sie in einem Suchfilter für dieses Attribut angeben können.
ms.assetid: 72bd58e4-e1c3-40a5-9917-4910f40c52c5
ms.tgt_platform: multiple
keywords:
- Angeben der Vergleichswerte (AD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f9355bc4853fa6dc62645e1c241d8e26f731f9
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724489"
---
# <a name="how-to-specify-comparison-values"></a>Angeben von Vergleichswerten

Jeder Attributtyp verfügt über eine Syntax, die den Typ der Vergleichswerte bestimmt, die Sie in einem Suchfilter für dieses Attribut angeben können.

In den folgenden Abschnitten werden die Anforderungen für die einzelnen Attribut Syntax beschrieben. Weitere Informationen zur Attribut Syntax finden Sie unter [Syntax für Attribute in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).

<dl> <dt>

<span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>Booleschen
</dt> <dd>

Der in einem Filter angegebene Wert muss ein Zeichen folgen Wert sein, der entweder "true" oder "false" ist. In den folgenden Beispielen wird gezeigt, wie eine boolesche Vergleichs Zeichenfolge angegeben wird.

Im folgenden Beispiel wird nach Objekten gesucht, für die " **showInAdvancedViewOnly** " auf " **true**" festgelegt ist:


```C++
(showInAdvancedViewOnly=TRUE)
```



Im folgenden Beispiel wird nach Objekten gesucht, für die " **showInAdvancedViewOnly** " auf " **false**" festgelegt ist:


```C++
(showInAdvancedViewOnly=FALSE)
```



</dd> <dt>

<span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>Ganzzahl und Enumeration
</dt> <dd>

Der in einem Filter angegebene Wert muss eine ganze Dezimalzahl sein. Hexadezimale Werte müssen in decimal konvertiert werden. Eine Wert Vergleichs Zeichenfolge hat die folgende Form:


```C++
<attribute name>:<value>
```



" <attribute name> " ist der **ldapDisplayName** des Attributs und "<value>"ist der Wert, der für den Vergleich verwendet werden soll.

Das folgende Codebeispiel zeigt einen Filter, der nach Objekten mit einem **GroupType** -Wert sucht, der gleich dem **ADS- \_ \_ Gruppentyp \_ Universal \_ Group** (8)-Flag und dem **ADS- \_ \_ Gruppentyp \_ Security \_ aktiviertes** Flag (0x80000000) ist. Die beiden Flags kombinierten denselben 0x80000008-Wert, der in "Decimal" konvertiert wurde, ist 2147483656.


```C++
(groupType=2147483656)
```



Die Regeln für die LDAP-abgleichsregel können auch verwendet werden, um bitweise Vergleiche auszuführen. Weitere Informationen zu abgleichsregeln finden Sie unter [Such Filter Syntax](/windows/desktop/ADSI/search-filter-syntax). Das folgende Codebeispiel zeigt einen Filter, der nach Objekten sucht, die einen **GroupType** mit **\_ aktiviertem ADS- \_ Gruppentyp \_ Security- \_ aktiviertem** (0x80000000 = 2147483648) Bitset aufweisen.


```C++
(groupType:1.2.840.113556.1.4.803:=2147483648))
```



</dd> <dt>

<span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>Octetstring
</dt> <dd>

Der in einem Filter angegebene Wert ist die zu verwendenden Daten. Die Daten müssen als eine Zeichenfolge mit zwei Zeichen codiertem Byte dargestellt werden, wobei jedem Byte ein umgekehrter Schrägstrich () vorangestellt wird \) . Beispielsweise wird der Wert 0x05 in der Zeichenfolge als " \\ 05" angezeigt.

Die [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) -Funktion kann verwendet werden, um eine codierte Zeichen folgen Darstellung binärer Daten zu erstellen. Die **ADsEncodeBinaryData** -Funktion codiert keine Byte-Werte, die alphanumerische Zeichen darstellen. Stattdessen wird das Zeichen in die Zeichenfolge platziert, ohne es zu codieren. Dies führt dazu, dass die Zeichenfolge eine Mischung aus codierten und nicht codierten Zeichen enthält. Wenn die Binärdaten z. b. 0x05 \| 0x1A \| 0x1B \| 0x43 \| 0x32 sind, enthält die codierte Zeichenfolge " \\ 05 \\ 1a \\ 1bc2". Dies hat keine Auswirkung auf den Filter, und die Suchfilter funktionieren ordnungsgemäß mit diesen Zeichen folgen Typen.

Platzhalter werden akzeptiert.

Das folgende Codebeispiel zeigt einen Filter, der die codierte Zeichenfolge für **schemaIdGUID** mit dem GUID-Wert "{BF967ABA-0DE6-11D0-A285-00AA003049E2}" enthält:


```C++
(schemaidguid=\BA\7A\96\BF\E6\0D\D0\11\A2\85\00\AA\00\30\49\E2)
```



</dd> <dt>

<span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid
</dt> <dd>

Der in einem Filter angegebene Wert ist die codierte Byte Zeichen folgen Darstellung der SID. Weitere Informationen zu codierten Byte Zeichenfolgen finden Sie im vorherigen Abschnitt in diesem Thema, in dem die octetstring-Syntax erläutert wird.

Das folgende Codebeispiel zeigt einen Filter, der eine codierte Zeichenfolge für **objectSID** mit dem SID-Zeichen folgen Wert "S-1-5-21-1935655697-308236825-1417001333" enthält:


```C++
(ObjectSid=\01\04\00\00\00\00\00\05\15\00\00\00\11\C3\5Fs\19R\5F\12u\B9uT)
```



</dd> <dt>

<span id="DN"></span><span id="dn"></span>Derte
</dt> <dd>

Der gesamte Distinguished Name, der abgeglichen werden soll, muss angegeben werden.

Platzhalter werden nicht akzeptiert.

Beachten Sie, dass Sie mit dem **objectCategory** -Attribut auch den **ldapDisplayName** der Klasse festlegen können, die für das Attribut festgelegt ist.

Das folgende Beispiel zeigt einen Filter, der einen **Member** angibt, der "CN = testuser, DC = fabrikam, DC = com" enthält:


```C++
(member=CN=TestUser,DC=Fabrikam,DC=COM)
```



</dd> <dt>

<span id="INTEGER8"></span><span id="integer8"></span>INTEGER8
</dt> <dd>

Der in einem Filter angegebene Wert muss eine ganze Dezimalzahl sein. Konvertieren von hexadezimalen Werten in Dezimalzahlen.

Im folgenden Codebeispiel wird ein Filter gezeigt, der einen " **deationtime** "-Wert angibt, der auf eine [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) von "1999-12-31 23:59:59 (UTC/GMT)" festgelegt ist:


```C++
(creationTime=125911583990000000)
```



Die folgenden Funktionen erstellen einen exakten Übereinstimmungs Filter (=) für ein großes integer-Attribut und überprüfen das-Attribut im Schema und seine Syntax:


```C++
//***************************************************************************
//
//  CheckAttribute()
//
//***************************************************************************

HRESULT CheckAttribute(LPOLESTR szAttribute, LPOLESTR szSyntax)
{
    HRESULT hr = E_FAIL;
    BSTR bstr;
    IADsProperty *pObject = NULL;
    LPWSTR szPrefix = L"LDAP://schema/";
    LPWSTR szPath;
     
    if((!szAttribute) || (!szSyntax))
    {
        return E_POINTER;
    }

    // Allocate a buffer large enough to hold the ADsPath of the attribute.
    szPath = new WCHAR[lstrlenW(szPrefix) + lstrlenW(szAttribute) + 1];
    if(NULL == szPath)
    {
        return E_OUTOFMEMORY;
    }
     
    // Create the ADsPath of the attribute.
    wcscpy_s(szPath, szPrefix);
    wcscat_s(szPath, szAttribute);

    hr = ADsOpenObject( szPath,
                        NULL,
                        NULL,
                        ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                        IID_IADsProperty,
                        (void**)&pObject);
    if(SUCCEEDED(hr)) 
    {
        hr = pObject->get_Syntax(&bstr);
        if (SUCCEEDED(hr)) 
        {
            if (0==lstrcmpiW(bstr, szSyntax)) 
            {
                hr = S_OK;
            }
            else
            {
                hr = S_FALSE;
            }
        }

        SysFreeString(bstr);
    }
    
    if(pObject)
    {
        pObject->Release();
    }

    delete szPath;
    
    return hr;
}

//***************************************************************************
//
//  CreateExactMatchFilterLargeInteger()
//
//***************************************************************************

HRESULT CreateExactMatchFilterLargeInteger( LPOLESTR szAttribute, 
                                            INT64 liValue, 
                                            LPOLESTR *pszFilter)
{
    HRESULT hr = E_FAIL;
     
    if ((!szAttribute) || (!pszFilter))
    {
        return E_POINTER;
    }
     
    // Verify that the attribute exists and has 
    // Integer8 (Large Integer) syntax.
     
    hr = CheckAttribute(szAttribute, L"Integer8");
    if (S_OK == hr) 
    {
        LPWSTR szFormat = L"%s=%I64d";
        LPWSTR szTempFilter = new WCHAR[lstrlenW(szFormat) + lstrlenW(szAttribute) + 20 + 1];

        if(NULL == szTempFilter)
        {
            return E_OUTOFMEMORY;
        }
        
        swprintf_s(szTempFilter, L"%s=%I64d", szAttribute, liValue);
     
        // Allocate buffer for the filter string.
        // Caller must free the buffer using CoTaskMemFree.
        *pszFilter = (OLECHAR *)CoTaskMemAlloc(sizeof(OLECHAR) * (lstrlenW(szTempFilter) + 1));
        if (*pszFilter) 
        {
            wcscpy_s(*pszFilter, szTempFilter);
            hr = S_OK;
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }

        delete szTempFilter;
    }

    return hr;
}
```



</dd> <dt>

<span id="PrintableString"></span><span id="printablestring"></span><span id="PRINTABLESTRING"></span>PrintableString
</dt> <dd>

Attribute mit diesen Syntaxen sollten bestimmten Zeichensätzen entsprechen. Weitere Informationen finden Sie unter [Syntax für Attribute in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).

Derzeit erzwingen Active Directory Domain Services diese Zeichensätze nicht.

Der in einem Filter angegebene Wert ist eine Zeichenfolge. Beim Vergleich wird die Groß-/Kleinschreibung beachtet.

</dd> <dt>

<span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>Generalizedtime
</dt> <dd>

Der in einem Filter angegebene Wert ist eine Zeichenfolge, die das Datum in der folgenden Form darstellt:


```C++
YYYYMMDDHHMMSS.0Z
```



"0z" weist auf keine Zeit differenzielle Abweichung hin. Beachten Sie, dass der Active Directory Server Datum/Uhrzeit als Greenwich Mean Time (GMT) speichert. Wenn keine Zeit differenzielle Angabe angegeben ist, lautet der Standardwert GMT.

Wenn die lokale Zeitzone nicht GMT ist, verwenden Sie einen differenziellen Wert, um die lokale Zeitzone anzugeben, und wenden Sie die differenzielle Zeit auf GMT an. Das differenzielle differenzielle basiert auf: GMT = local + Differential.

Verwenden Sie Folgendes, um eine differenzielle Angabe anzugeben:


```C++
YYYYMMDDHHMMSS.0[+/-]HHMM
```



Das folgende Beispiel zeigt einen Filter, der eine festgelegte Uhrzeit angibt, die auf 3/23/99 8:52:58 Uhr GMT festgelegt **wurde** :


```C++
(whenCreated=19990323205258.0Z)
```



Das folgende Beispiel zeigt einen Filter, der eine fest **gelegte Uhrzeit angibt** , die auf 3/23/99 8:52:58 Uhr Neuseeland Normalzeit (differenziell = + 12 Stunden) festgelegt ist:


```C++
(whenCreated=19990323205258.0+1200)
```



Im folgenden Codebeispiel wird die Berechnung der Zeit Zonen differenziell veranschaulicht. Die-Funktion gibt das differenzielle zwischen der aktuellen lokalen Zeitzone und GMT zurück. Der zurückgegebene Wert ist eine Zeichenfolge im folgenden Format:


```C++
[+/-]HHMM
```



Pacific Normalzeit ist beispielsweise-0800.


```C++
//***************************************************************************
//
//  GetLocalTimeZoneDifferential()
//
//***************************************************************************

HRESULT GetLocalTimeZoneDifferential(LPOLESTR *pszDifferential)
{
    if(NULL == pszDifferential)
    {
        return E_INVALIDARG;
    }
    
    HRESULT hr = E_FAIL;
    DWORD dwReturn;
    TIME_ZONE_INFORMATION timezoneinfo;
    LONG lTimeDifferential;
    LONG lHours;
    LONG lMinutes;
    
    dwReturn  = GetTimeZoneInformation(&timezoneinfo);

    switch (dwReturn)
    {
    case TIME_ZONE_ID_STANDARD:
        lTimeDifferential = timezoneinfo.Bias + timezoneinfo.StandardBias;
        
        // Bias is in minutes. Calculate the hours for HHMM format.
        lHours = -(lTimeDifferential/60);
        
        // Bias is in minutes. Calculate the minutes for HHMM format.
        lMinutes = lTimeDifferential%60L;

        hr = S_OK;
        break;

    case TIME_ZONE_ID_DAYLIGHT:
        lTimeDifferential = timezoneinfo.Bias + timezoneinfo.DaylightBias;
        
        // Bias is in minutes. Calculate the hours for HHMM format.
        // Apply the additive inverse.
        // Bias is based on GMT=Local+Bias.
        // A differential, based on GMT=Local-Bias, is required.
        lHours = -(lTimeDifferential/60);
        
        // Bias is in minutes. Calculate the minutes for HHMM format.
        lMinutes = lTimeDifferential%60L;
        
        hr = S_OK;
        break;

    case TIME_ZONE_ID_INVALID:
    default:
        hr = E_FAIL;
        break;
    }
     
    if (SUCCEEDED(hr))
    {
        // The caller must free the memory using CoTaskMemFree.
        *pszDifferential = (OLECHAR *)CoTaskMemAlloc(sizeof(OLECHAR) * (3 + 2 + 1));
        if (*pszDifferential)
        {
            swprintf_s(*pszDifferential, L"%+03d%02d", lHours, lMinutes);
            
            hr = S_OK;
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
     
    return hr;
}
```



</dd> <dt>

<span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>UtcTime
</dt> <dd>

Der in einem Filter angegebene Wert ist eine Zeichenfolge, die das Datum in der folgenden Form darstellt:


```C++
YYMMDDHHMMSSZ
```



Z gibt an, dass kein Zeitunterschied besteht. Beachten Sie, dass der Active Directory Server Datum und Uhrzeit als GMT-Zeit speichert. Wenn keine Zeit differenzielle Angabe festgelegt ist, ist GMT die Standardeinstellung.

Der Sekundenwert ("SS") ist optional.

Wenn GMT nicht die lokale Zeitzone ist, wenden Sie einen lokalen differenziellen Wert an, um die lokale Zeitzone anzugeben. Das differenzielle differenzielle ist: GMT = local + Differential.

Verwenden Sie das folgende Format, um eine differenzielle Angabe anzugeben:


```C++
YYMMDDHHMMSS[+/-]HHMM
```



Das folgende Beispiel zeigt einen Filter, der einen auf 3/23/99 8:52:58 Uhr GMT festgelegten Wert von " **mytimeatkurzer b** " angibt:


```C++
(myTimeAttrib=990323205258Z)
```



Das folgende Beispiel zeigt einen Filter, der einen Wert von " **mytimeatkurzer b** " angibt, der auf 3/23/99 8:52:58 Uhr festgelegt ist


```C++
(myTimeAttrib=9903232052Z)
```



Das folgende Beispiel zeigt einen Filter, der einen Zeitraum von **mytimeatyb** angibt, der auf 3/23/99 8:52:58 Uhr Neuseeland Normalzeit (differenziell ist 12 Stunden) festgelegt ist. Dies entspricht 3/23/99 8:52:58 Uhr GMT.


```C++
(myTimeAttrib=990323205258+1200)
```



</dd> <dt>

<span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>Directoriystring
</dt> <dd>

Der in einem Filter angegebene Wert ist eine Zeichenfolge. Directoriystring kann Unicode-Zeichen enthalten. Bei dem Vergleich wird Groß- und Kleinschreibung nicht unterschieden.

</dd> <dt>

<span id="OID"></span><span id="oid"></span>OID
</dt> <dd>

Die gesamte OID, die abgeglichen werden soll, muss angegeben werden.

Platzhalter werden nicht akzeptiert.

Mit dem **objectCategory** -Attribut können Sie den **ldapDisplayName** des Klassen Satzes für das-Attribut angeben.

Das folgende Beispiel zeigt einen Filter, der die **governsId** für die volumeklasse angibt:


```C++
(governsID=1.2.840.113556.1.5.36)
```



Zwei äquivalente Filter, der das **systemmustare** -Attribut angibt, das **uncname** enthält, das eine OID von 1.2.840.113556.1.4.137 hat:


```C++
(SystemMustContain=uNCName)
 
(SystemMustContain=1.2.840.113556.1.4.137)
```



</dd> <dt>

<span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>Weitere Syntaxen
</dt> <dd>

Die folgenden Syntaxen werden in einem Filter ausgewertet, der einer Oktett-Zeichenfolge ähnelt:

-   Objectsecuritydescriptor
-   Access spointdn
-   Presentationadressen
-   Replicalink
-   Dnwithstring
-   Dnwithoctetstring
-   Orname

</dd> </dl>

 

 