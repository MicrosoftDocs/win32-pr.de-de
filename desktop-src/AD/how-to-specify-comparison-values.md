---
title: Angeben von Vergleichswerten
description: Jeder Attributtyp verfügt über eine Syntax, die den Typ der Vergleichswerte bestimmt, die Sie in einem Suchfilter für dieses Attribut angeben können.
ms.assetid: 72bd58e4-e1c3-40a5-9917-4910f40c52c5
ms.tgt_platform: multiple
keywords:
- Angeben von Vergleichswerten in AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5babc7d9781895c9671594214e4e036a85ef951cdb4b97ba34d708d160dd8fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188121"
---
# <a name="how-to-specify-comparison-values"></a>Angeben von Vergleichswerten

Jeder Attributtyp verfügt über eine Syntax, die den Typ der Vergleichswerte bestimmt, die Sie in einem Suchfilter für dieses Attribut angeben können.

In den folgenden Abschnitten werden die Anforderungen für jede Attributsyntax beschrieben. Weitere Informationen zu Attributsyntaxen finden Sie unter [Syntaxes for Attributes in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).

<dl> <dt>

<span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>Boolean
</dt> <dd>

Der in einem Filter angegebene Wert muss ein Zeichenfolgenwert sein, der entweder "TRUE" oder "FALSE" ist. In den folgenden Beispielen wird gezeigt, wie eine boolesche Vergleichszeichenfolge angegeben wird.

Im folgenden Beispiel wird nach Objekten gesucht, für die **showInAdvancedViewOnly** auf TRUE festgelegt **ist:**


```C++
(showInAdvancedViewOnly=TRUE)
```



Im folgenden Beispiel wird nach Objekten gesucht, für die **showInAdvancedViewOnly** auf **FALSE festgelegt ist:**


```C++
(showInAdvancedViewOnly=FALSE)
```



</dd> <dt>

<span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>Ganze Zahl und Enumeration
</dt> <dd>

Der in einem Filter angegebene Wert muss eine dezimale ganze Zahl sein. Hexadezimalwerte müssen in decimal konvertiert werden. Eine Wertvergleichszeichenfolge hat die folgende Form:


```C++
<attribute name>:<value>
```



" <attribute name> " ist der **lDAPDisplayName des** Attributs und "<value>" ist der Wert, der für den Vergleich verwendet werden soll.

Das folgende Codebeispiel zeigt einen Filter, der nach Objekten sucht, die über einen **groupType-Wert** verfügen, der dem **ADS GROUP TYPE UNIVERSAL \_ \_ \_ \_ GROUP** (8)-Flag und dem **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED** (0x80000000)-Flag entspricht. Die beiden kombinierten Flags 0x80000008, die in decimal konvertiert werden, 2147483656.


```C++
(groupType=2147483656)
```



Die LDAP-Abgleichsregeloperatoren können auch verwendet werden, um bitweise Vergleiche durchzuführen. Weitere Informationen zu Abgleichsregeln finden Sie unter [Suchfiltersyntax](/windows/desktop/ADSI/search-filter-syntax). Das folgende Codebeispiel zeigt einen Filter, der nach Objekten sucht, für die **ein groupType-Objekt** mit dem **Bit ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED** (0x80000000 = 2147483648) festgelegt ist.


```C++
(groupType:1.2.840.113556.1.4.803:=2147483648))
```



</dd> <dt>

<span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>OctetString
</dt> <dd>

Der in einem Filter angegebene Wert ist die zu findenden Daten. Die Daten müssen als zwei zeichencodierte Bytezeichenfolge dargestellt werden, wobei jedem Byte ein zurücker schräger Schrägstrich () voran \\ steht. Beispielsweise wird der 0x05 in der Zeichenfolge als \\ "05" angezeigt.

Die [**ADsEncodeBinaryData-Funktion**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) kann verwendet werden, um eine codierte Zeichenfolgendarstellung von Binärdaten zu erstellen. Die **ADsEncodeBinaryData-Funktion** codiert keine Bytewerte, die alphanumerische Zeichen darstellen. Stattdessen wird das Zeichen in der Zeichenfolge ohne Codierung platzieren. Dies führt dazu, dass die Zeichenfolge eine Mischung aus codierten und nicht codierten Zeichen enthält. Wenn die Binärdaten beispielsweise 0x05 0x1A 0x1B 0x43 0x32 sind, enthält die codierte Zeichenfolge \| \| \| \| \\ "05 \\ 1A \\ 1BC2". Dies hat keine Auswirkungen auf den Filter, und die Suchfilter funktionieren mit diesen Zeichenfolgentypen ordnungsgemäß.

Platzhalter werden akzeptiert.

Das folgende Codebeispiel zeigt einen Filter, der eine codierte Zeichenfolge für **schemaIDGUID** mit dem GUID-Wert "{BF967ABA-0DE6-11D0-A285-00AA003049E2}" enthält:


```C++
(schemaidguid=\BA\7A\96\BF\E6\0D\D0\11\A2\85\00\AA\00\30\49\E2)
```



</dd> <dt>

<span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid
</dt> <dd>

Der in einem Filter angegebene Wert ist die codierte Bytezeichenfolgendarstellung der SID. Weitere Informationen zu codierten Bytezeichenfolgen finden Sie im vorherigen Abschnitt dieses Themas, in dem die OctetString-Syntax erläutert wird.

Das folgende Codebeispiel zeigt einen Filter, der eine codierte Zeichenfolge für **objectSid** mit dem SID-Zeichenfolgenwert "S-1-5-21-1935655697-308236825-1417001333" enthält:


```C++
(ObjectSid=\01\04\00\00\00\00\00\05\15\00\00\00\11\C3\5Fs\19R\5F\12u\B9uT)
```



</dd> <dt>

<span id="DN"></span><span id="dn"></span>Dn
</dt> <dd>

Der gesamte Distinguished Name muss angegeben werden, um eine Übereinstimmung zu finden.

Platzhalter werden nicht akzeptiert.

Beachten Sie, dass Sie mit dem **ObjectCategory-Attribut** auch **den lDAPDisplayName** der Klasse angeben können, die für das Attribut festgelegt ist.

Das folgende Beispiel zeigt einen  Filter, der einen Member angibt, der "CN=TestUser,DC=Fabrikam,DC=COM" enthält:


```C++
(member=CN=TestUser,DC=Fabrikam,DC=COM)
```



</dd> <dt>

<span id="INTEGER8"></span><span id="integer8"></span>INTEGER8
</dt> <dd>

Der in einem Filter angegebene Wert muss eine ganze Dezimalzahl sein. Konvertieren Sie Hexadezimalwerte in decimal.

Das folgende Codebeispiel zeigt einen Filter, der angibt, dass **creationTime** auf [**einen FILETIME-Wert**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) von "1999-12-31 23:59:59 (UTC/GMT)" festgelegt ist:


```C++
(creationTime=125911583990000000)
```



Die folgenden Funktionen erstellen einen filter für eine genaue Übereinstimmung (=) für ein großes Ganzzahlattribut und überprüfen das Attribut im Schema und dessen Syntax:


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

Attribute mit diesen Syntaxen sollten bestimmten Zeichensätzen entsprechen. Weitere Informationen finden Sie unter [Syntaxes for Attributes in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).

Derzeit werden Active Directory Domain Services Zeichensätze nicht erzwungen.

Der in einem Filter angegebene Wert ist eine Zeichenfolge. Beim Vergleich wird die Kleinschreibung beachtet.

</dd> <dt>

<span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>GeneralizedTime
</dt> <dd>

Der in einem Filter angegebene Wert ist eine Zeichenfolge, die das Datum in der folgenden Form darstellt:


```C++
YYYYMMDDHHMMSS.0Z
```



"0Z" gibt an, dass es keine differenzielle Zeit gibt. Beachten Sie, dass der Active Directory-Server Datum/Uhrzeit als Greenwich Mean Time (GMT) speichert. Wenn kein zeitdifferenzieller Wert angegeben wird, ist der Standardwert GMT.

Wenn die lokale Zeitzone nicht GMT ist, verwenden Sie einen differenziellen Wert, um Ihre lokale Zeitzone anzugeben, und wenden Sie das differenzielle auf GMT an. Die differenzielle Basiert auf: GMT=Local+differential.

Verwenden Sie zum Angeben eines differenziellen Werts Folgendes:


```C++
YYYYMMDDHHMMSS.0[+/-]HHMM
```



Das folgende Beispiel zeigt einen Filter, der eine **whenCreated-Zeit** angibt, die auf 23.03.2019 20:52:58 Uhr GMT festgelegt ist:


```C++
(whenCreated=19990323205258.0Z)
```



Das folgende Beispiel zeigt einen Filter, der eine **whenCreated-Zeit** angibt, die auf 23.03.2019 20:52:58 Uhr Normalzeit (differenziell : +12 Stunden) festgelegt ist:


```C++
(whenCreated=19990323205258.0+1200)
```



Das folgende Codebeispiel zeigt, wie die differenzielle Zeitzone berechnet wird. Die Funktion gibt die Differenz zwischen der aktuellen lokalen Zeitzone und GMT zurück. Der zurückgegebene Wert ist eine Zeichenfolge im folgenden Format:


```C++
[+/-]HHMM
```



Pacific Normalzeit ist beispielsweise -0800.


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

<span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>UTCTime
</dt> <dd>

Der in einem Filter angegebene Wert ist eine Zeichenfolge, die das Datum in der folgenden Form darstellt:


```C++
YYMMDDHHMMSSZ
```



Z gibt an, dass es keine differenzielle Zeit gibt. Beachten Sie, dass der Active Directory-Server Datum und Uhrzeit als GMT-Zeit speichert. Wenn kein zeitdifferenzieller Wert angegeben wird, ist GMT der Standardwert.

Der Sekundenwert ("SS") ist optional.

Wenn GMT nicht die lokale Zeitzone ist, wenden Sie einen lokalen differenziellen Wert an, um Ihre lokale Zeitzone anzugeben. Der differenzielle Wert ist: GMT=Local+differential.

Verwenden Sie zum Angeben eines differenziellen -Werts das folgende Formular:


```C++
YYMMDDHHMMSS[+/-]HHMM
```



Das folgende Beispiel zeigt einen Filter, der eine **myTimeAttrib-Zeit** angibt, die auf 23.03.2019 20:52:58 Uhr GMT festgelegt ist:


```C++
(myTimeAttrib=990323205258Z)
```



Das folgende Beispiel zeigt einen Filter, der eine **myTimeAttrib-Zeit** angibt, die ohne Angabe von Sekunden auf 23.03.99 20:52:58 Uhr festgelegt ist:


```C++
(myTimeAttrib=9903232052Z)
```



Das folgende Beispiel zeigt einen Filter, der eine **myTimeAttrib-Zeit** angibt, die auf 23.03.2019 20:52:58 Uhr Normalzeit (differenziell: 12 Stunden) festgelegt ist. Dies entspricht 3/23/99 8:52:58 AM GMT.


```C++
(myTimeAttrib=990323205258+1200)
```



</dd> <dt>

<span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>DirectoryString
</dt> <dd>

Der in einem Filter angegebene Wert ist eine Zeichenfolge. DirectoryString kann Unicode-Zeichen enthalten. Bei dem Vergleich wird Groß- und Kleinschreibung nicht unterschieden.

</dd> <dt>

<span id="OID"></span><span id="oid"></span>Oid
</dt> <dd>

Die gesamte übereinstimmende OID muss angegeben werden.

Platzhalter werden nicht akzeptiert.

Mit **dem objectCategory-Attribut** können Sie **den lDAPDisplayName** der Für das Attribut festgelegten Klasse angeben.

Das folgende Beispiel zeigt einen Filter, der **governsID für** die Volumeklasse angibt:


```C++
(governsID=1.2.840.113556.1.5.36)
```



Zwei gleichwertige Filter, die das **systemMustContain-Attribut** mit **uNCName** angeben, das über eine OID von 1.2.840.113556.1.4.137 verfügt:


```C++
(SystemMustContain=uNCName)
 
(SystemMustContain=1.2.840.113556.1.4.137)
```



</dd> <dt>

<span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>Andere Syntaxen
</dt> <dd>

Die folgenden Syntaxen werden in einem Filter ausgewertet, der einer Oktettzeichenfolge ähnelt:

-   ObjectSecurityDescriptor
-   AccessPointDN
-   PresentationAddresses
-   ReplicaLink
-   DNWithString
-   DNWithOctetString
-   ORName

</dd> </dl>

 

 