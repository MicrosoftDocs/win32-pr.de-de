---
title: Angeben von Vergleichswerten
description: Jeder Attributtyp verfügt über eine Syntax, die den Typ der Vergleichswerte bestimmt, die Sie in einem Suchfilter für dieses Attribut angeben können.
ms.assetid: 72bd58e4-e1c3-40a5-9917-4910f40c52c5
ms.tgt_platform: multiple
keywords:
- Angeben von Vergleichswerten in AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edba238961cdc18b088b6b5bd5b06ff4be383add
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386750"
---
# <a name="how-to-specify-comparison-values"></a><span data-ttu-id="0b008-104">Angeben von Vergleichswerten</span><span class="sxs-lookup"><span data-stu-id="0b008-104">How to Specify Comparison Values</span></span>

<span data-ttu-id="0b008-105">Jeder Attributtyp verfügt über eine Syntax, die den Typ der Vergleichswerte bestimmt, die Sie in einem Suchfilter für dieses Attribut angeben können.</span><span class="sxs-lookup"><span data-stu-id="0b008-105">Each attribute type has a syntax that determines the type of comparison values that you can specify in a search filter for that attribute.</span></span>

<span data-ttu-id="0b008-106">In den folgenden Abschnitten werden die Anforderungen für jede Attributsyntax beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0b008-106">The following sections describe requirements for each attribute syntax.</span></span> <span data-ttu-id="0b008-107">Weitere Informationen zu Attributsyntaxen finden Sie unter [Syntaxes for Attributes in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="0b008-107">For more information about attribute syntaxes, see [Syntaxes for Attributes in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span></span>

<dl> <dt>

<span data-ttu-id="0b008-108"><span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>Boolean</span><span class="sxs-lookup"><span data-stu-id="0b008-108"><span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>Boolean</span></span>
</dt> <dd>

<span data-ttu-id="0b008-109">Der in einem Filter angegebene Wert muss ein Zeichenfolgenwert sein, der entweder "TRUE" oder "FALSE" ist.</span><span class="sxs-lookup"><span data-stu-id="0b008-109">The value specified in a filter must be a string value that is either "TRUE" or "FALSE".</span></span> <span data-ttu-id="0b008-110">In den folgenden Beispielen wird gezeigt, wie eine boolesche Vergleichszeichenfolge angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0b008-110">The following examples show how to specify a Boolean comparison string.</span></span>

<span data-ttu-id="0b008-111">Im folgenden Beispiel wird nach Objekten gesucht, für die **showInAdvancedViewOnly** auf TRUE festgelegt **ist:**</span><span class="sxs-lookup"><span data-stu-id="0b008-111">The following example will search for objects that have a **showInAdvancedViewOnly** set to **TRUE**:</span></span>


```C++
(showInAdvancedViewOnly=TRUE)
```



<span data-ttu-id="0b008-112">Im folgenden Beispiel wird nach Objekten gesucht, für die **showInAdvancedViewOnly** auf FALSE festgelegt **ist:**</span><span class="sxs-lookup"><span data-stu-id="0b008-112">The following example will search for objects that have a **showInAdvancedViewOnly** set to **FALSE**:</span></span>


```C++
(showInAdvancedViewOnly=FALSE)
```



</dd> <dt>

<span data-ttu-id="0b008-113"><span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>Ganze Zahl und Enumeration</span><span class="sxs-lookup"><span data-stu-id="0b008-113"><span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>Integer and Enumeration</span></span>
</dt> <dd>

<span data-ttu-id="0b008-114">Der in einem Filter angegebene Wert muss eine dezimale ganze Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="0b008-114">The value specified in a filter must be a decimal Integer.</span></span> <span data-ttu-id="0b008-115">Hexadezimalwerte müssen in decimal konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="0b008-115">Hexadecimal values must be converted to decimal.</span></span> <span data-ttu-id="0b008-116">Eine Wertvergleichszeichenfolge hat die folgende Form:</span><span class="sxs-lookup"><span data-stu-id="0b008-116">A value comparison string takes the following form:</span></span>


```C++
<attribute name>:<value>
```



<span data-ttu-id="0b008-117">" <attribute name> " ist der **lDAPDisplayName des** Attributs und "</span><span class="sxs-lookup"><span data-stu-id="0b008-117">"<attribute name>" is the **lDAPDisplayName** of the attribute and "</span></span><value><span data-ttu-id="0b008-118">" ist der Wert, der für den Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b008-118">" is the value to use for comparison.</span></span>

<span data-ttu-id="0b008-119">Das folgende Codebeispiel zeigt einen Filter, der nach Objekten sucht, die über einen **groupType-Wert** verfügen, der dem **ADS GROUP TYPE UNIVERSAL \_ \_ \_ \_ GROUP** (8)-Flag und dem **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED** (0x80000000)-Flag entspricht.</span><span class="sxs-lookup"><span data-stu-id="0b008-119">The following code example shows a filter that will search for objects that have a **groupType** value that is equal to the **ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** (8) flag and the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** (0x80000000) flag.</span></span> <span data-ttu-id="0b008-120">Die beiden flags kombinierten 0x80000008, die in decimal konvertiert werden, ist 2147483656.</span><span class="sxs-lookup"><span data-stu-id="0b008-120">The two flags combined equal 0x80000008, which converted to decimal is 2147483656.</span></span>


```C++
(groupType=2147483656)
```



<span data-ttu-id="0b008-121">Die LDAP-Abgleichsregeloperatoren können auch verwendet werden, um bitweise Vergleiche durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="0b008-121">The LDAP matching rule operators can also be used to perform bitwise comparisons.</span></span> <span data-ttu-id="0b008-122">Weitere Informationen zu Abgleichsregeln finden Sie unter [Suchfiltersyntax](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="0b008-122">For more information about matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span> <span data-ttu-id="0b008-123">Das folgende Codebeispiel zeigt einen Filter, der nach Objekten sucht, deren **groupType** mit dem Bitsatz **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED** (0x80000000 = 2147483648) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0b008-123">The following code example shows a filter that will search for objects that have a **groupType** with the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** (0x80000000 = 2147483648) bit set.</span></span>


```C++
(groupType:1.2.840.113556.1.4.803:=2147483648))
```



</dd> <dt>

<span data-ttu-id="0b008-124"><span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>OctetString</span><span class="sxs-lookup"><span data-stu-id="0b008-124"><span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>OctetString</span></span>
</dt> <dd>

<span data-ttu-id="0b008-125">Der in einem Filter angegebene Wert ist die zu findenden Daten.</span><span class="sxs-lookup"><span data-stu-id="0b008-125">The value specified in a filter is the data to be found.</span></span> <span data-ttu-id="0b008-126">Die Daten müssen als zwei zeichencodierte Bytezeichenfolge dargestellt werden, wobei jedem Byte ein zurücker schräger Schrägstrich () voran \\ steht.</span><span class="sxs-lookup"><span data-stu-id="0b008-126">The data must be represented as a two character encoded byte string where each byte is preceded by a backslash (\\).</span></span> <span data-ttu-id="0b008-127">Beispielsweise wird der 0x05 in der Zeichenfolge als \\ "05" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0b008-127">For example, the value 0x05 will appear in the string as "\\05".</span></span>

<span data-ttu-id="0b008-128">Die [**ADsEncodeBinaryData-Funktion**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) kann verwendet werden, um eine codierte Zeichenfolgendarstellung von Binärdaten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0b008-128">The [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) function can be used to create an encoded string representation of binary data.</span></span> <span data-ttu-id="0b008-129">Die **ADsEncodeBinaryData-Funktion** codiert keine Bytewerte, die alphanumerische Zeichen darstellen.</span><span class="sxs-lookup"><span data-stu-id="0b008-129">The **ADsEncodeBinaryData** function does not encode byte values that represent alpha-numeric characters.</span></span> <span data-ttu-id="0b008-130">Stattdessen wird das Zeichen in der Zeichenfolge ohne Codierung platzieren.</span><span class="sxs-lookup"><span data-stu-id="0b008-130">It will, instead, place the character into the string without encoding it.</span></span> <span data-ttu-id="0b008-131">Dies führt dazu, dass die Zeichenfolge eine Mischung aus codierten und nicht codierten Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="0b008-131">This results in the string containing a mixture of encoded and unencoded characters.</span></span> <span data-ttu-id="0b008-132">Wenn die Binärdaten beispielsweise 0x05 0x1A 0x1B 0x43 0x32 sind, enthält die codierte Zeichenfolge \| \| \| \| \\ "05 \\ 1A \\ 1BC2".</span><span class="sxs-lookup"><span data-stu-id="0b008-132">For example, if the binary data is 0x05\|0x1A\|0x1B\|0x43\|0x32, the encoded string will contain "\\05\\1A\\1BC2".</span></span> <span data-ttu-id="0b008-133">Dies hat keine Auswirkungen auf den Filter, und die Suchfilter funktionieren mit diesen Zeichenfolgentypen ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="0b008-133">This has no effect on the filter and the search filters will work correctly with these types of strings.</span></span>

<span data-ttu-id="0b008-134">Platzhalter werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="0b008-134">Wildcards are accepted.</span></span>

<span data-ttu-id="0b008-135">Das folgende Codebeispiel zeigt einen Filter, der eine codierte Zeichenfolge für **schemaIDGUID** mit dem GUID-Wert "{BF967ABA-0DE6-11D0-A285-00AA003049E2}" enthält:</span><span class="sxs-lookup"><span data-stu-id="0b008-135">The following code example shows a filter that contains encoded string for **schemaIDGUID** with GUID value of "{BF967ABA-0DE6-11D0-A285-00AA003049E2}":</span></span>


```C++
(schemaidguid=\BA\7A\96\BF\E6\0D\D0\11\A2\85\00\AA\00\30\49\E2)
```



</dd> <dt>

<span data-ttu-id="0b008-136"><span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid</span><span class="sxs-lookup"><span data-stu-id="0b008-136"><span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid</span></span>
</dt> <dd>

<span data-ttu-id="0b008-137">Der in einem Filter angegebene Wert ist die codierte Bytezeichenfolgendarstellung der SID.</span><span class="sxs-lookup"><span data-stu-id="0b008-137">The value specified in a filter is the encoded byte string representation of the SID.</span></span> <span data-ttu-id="0b008-138">Weitere Informationen zu codierten Bytezeichenfolgen finden Sie im vorherigen Abschnitt dieses Themas, in dem die OctetString-Syntax erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="0b008-138">For more information about encoded byte strings, see the previous section in this topic which discusses OctetString syntax.</span></span>

<span data-ttu-id="0b008-139">Das folgende Codebeispiel zeigt einen Filter, der eine codierte Zeichenfolge für **objectSid** mit dem SID-Zeichenfolgenwert "S-1-5-21-1935655697-308236825-1417001333" enthält:</span><span class="sxs-lookup"><span data-stu-id="0b008-139">The following code example shows a filter that contains an encoded string for **objectSid** with SID string value of "S-1-5-21-1935655697-308236825-1417001333":</span></span>


```C++
(ObjectSid=\01\04\00\00\00\00\00\05\15\00\00\00\11\C3\5Fs\19R\5F\12u\B9uT)
```



</dd> <dt>

<span data-ttu-id="0b008-140"><span id="DN"></span><span id="dn"></span>Dn</span><span class="sxs-lookup"><span data-stu-id="0b008-140"><span id="DN"></span><span id="dn"></span>DN</span></span>
</dt> <dd>

<span data-ttu-id="0b008-141">Der gesamte Distinguished Name muss angegeben werden, um eine Übereinstimmung zu finden.</span><span class="sxs-lookup"><span data-stu-id="0b008-141">The entire distinguished name, to be matched, must be supplied.</span></span>

<span data-ttu-id="0b008-142">Platzhalter werden nicht akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="0b008-142">Wildcards are not accepted.</span></span>

<span data-ttu-id="0b008-143">Beachten Sie, dass Sie mit dem **ObjectCategory-Attribut** auch **den lDAPDisplayName** der Klasse angeben können, die für das Attribut festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0b008-143">Be aware that the **objectCategory** attribute also enables you to specify the **lDAPDisplayName** of the class set on the attribute.</span></span>

<span data-ttu-id="0b008-144">Das folgende Beispiel zeigt einen  Filter, der einen Member angibt, der "CN=TestUser,DC=Fabrikam,DC=COM" enthält:</span><span class="sxs-lookup"><span data-stu-id="0b008-144">The following example shows a filter that specifies a **member** that contains "CN=TestUser,DC=Fabrikam,DC=COM":</span></span>


```C++
(member=CN=TestUser,DC=Fabrikam,DC=COM)
```



</dd> <dt>

<span data-ttu-id="0b008-145"><span id="INTEGER8"></span><span id="integer8"></span>INTEGER8</span><span class="sxs-lookup"><span data-stu-id="0b008-145"><span id="INTEGER8"></span><span id="integer8"></span>INTEGER8</span></span>
</dt> <dd>

<span data-ttu-id="0b008-146">Der in einem Filter angegebene Wert muss eine ganze Dezimalzahl sein.</span><span class="sxs-lookup"><span data-stu-id="0b008-146">The value specified in a filter must be a decimal integer.</span></span> <span data-ttu-id="0b008-147">Konvertieren Sie Hexadezimalwerte in decimal.</span><span class="sxs-lookup"><span data-stu-id="0b008-147">Convert hexadecimal values to decimal.</span></span>

<span data-ttu-id="0b008-148">Das folgende Codebeispiel zeigt einen Filter, der angibt, dass **creationTime** auf [**einen FILETIME-Wert**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) von "1999-12-31 23:59:59 (UTC/GMT)" festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="0b008-148">The following code example shows a filter that specifies a **creationTime** set to a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) of "1999-12-31 23:59:59 (UTC/GMT)":</span></span>


```C++
(creationTime=125911583990000000)
```



<span data-ttu-id="0b008-149">Die folgenden Funktionen erstellen einen Filter für eine genaue Übereinstimmung (=) für ein großes Ganzzahlattribut und überprüfen das Attribut im Schema und dessen Syntax:</span><span class="sxs-lookup"><span data-stu-id="0b008-149">The following functions create an exact match (=) filter for a large integer attribute and verify the attribute in the schema and its syntax:</span></span>


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

<span data-ttu-id="0b008-150"><span id="PrintableString"></span><span id="printablestring"></span><span id="PRINTABLESTRING"></span>PrintableString</span><span class="sxs-lookup"><span data-stu-id="0b008-150"><span id="PrintableString"></span><span id="printablestring"></span><span id="PRINTABLESTRING"></span>PrintableString</span></span>
</dt> <dd>

<span data-ttu-id="0b008-151">Attribute mit diesen Syntaxen sollten bestimmten Zeichensätzen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0b008-151">Attributes with these syntaxes should adhere to specific character sets.</span></span> <span data-ttu-id="0b008-152">Weitere Informationen finden Sie unter [Syntaxes for Attributes in Active Directory Domain Services.](syntaxes-for-attributes-in-active-directory-domain-services.md)</span><span class="sxs-lookup"><span data-stu-id="0b008-152">For more information, see [Syntaxes for Attributes in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="0b008-153">Derzeit werden Active Directory Domain Services Zeichensätze nicht erzwungen.</span><span class="sxs-lookup"><span data-stu-id="0b008-153">Currently, Active Directory Domain Services do not enforce those character sets.</span></span>

<span data-ttu-id="0b008-154">Der in einem Filter angegebene Wert ist eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0b008-154">The value specified in a filter is a string.</span></span> <span data-ttu-id="0b008-155">Beim Vergleich wird die Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="0b008-155">The comparison is case-sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="0b008-156"><span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>GeneralizedTime</span><span class="sxs-lookup"><span data-stu-id="0b008-156"><span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>GeneralizedTime</span></span>
</dt> <dd>

<span data-ttu-id="0b008-157">Der in einem Filter angegebene Wert ist eine Zeichenfolge, die das Datum in der folgenden Form darstellt:</span><span class="sxs-lookup"><span data-stu-id="0b008-157">The value specified in a filter is a string that represents the date in the following form:</span></span>


```C++
YYYYMMDDHHMMSS.0Z
```



<span data-ttu-id="0b008-158">"0Z" gibt an, dass es keine differenzielle Zeit gibt.</span><span class="sxs-lookup"><span data-stu-id="0b008-158">"0Z" indicates no time differential.</span></span> <span data-ttu-id="0b008-159">Beachten Sie, dass der Active Directory-Server Datum/Uhrzeit als Greenwich Mean Time (GMT) speichert.</span><span class="sxs-lookup"><span data-stu-id="0b008-159">Be aware that the Active Directory server stores date/time as Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="0b008-160">Wenn kein zeitdifferenzieller Wert angegeben wird, ist der Standardwert GMT.</span><span class="sxs-lookup"><span data-stu-id="0b008-160">If a time differential is not specified, the default is GMT.</span></span>

<span data-ttu-id="0b008-161">Wenn die lokale Zeitzone nicht GMT ist, verwenden Sie einen differenziellen Wert, um Ihre lokale Zeitzone anzugeben, und wenden Sie das differenzielle auf GMT an.</span><span class="sxs-lookup"><span data-stu-id="0b008-161">If the local time zone is not GMT, use a differential value to specify your local time zone and apply the differential to GMT.</span></span> <span data-ttu-id="0b008-162">Die differenzielle Basiert auf: GMT=Local+differential.</span><span class="sxs-lookup"><span data-stu-id="0b008-162">The differential is based on: GMT=Local+differential.</span></span>

<span data-ttu-id="0b008-163">Verwenden Sie Folgendes, um ein differenzielles -Paar anzugeben:</span><span class="sxs-lookup"><span data-stu-id="0b008-163">To specify a differential, use:</span></span>


```C++
YYYYMMDDHHMMSS.0[+/-]HHMM
```



<span data-ttu-id="0b008-164">Das folgende Beispiel zeigt einen Filter, der eine **whenCreated-Zeit** angibt, die auf 23.03.2019 20:52:58 Uhr GMT festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="0b008-164">The following example shows a filter that specifies a **whenCreated** time set to 3/23/99 8:52:58 PM GMT:</span></span>


```C++
(whenCreated=19990323205258.0Z)
```



<span data-ttu-id="0b008-165">Das folgende Beispiel zeigt einen Filter, der eine **whenCreated-Zeit** angibt, die auf 23.03.2019 20:52:58 Uhr Normalzeit (differenziell + 12 Stunden) festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="0b008-165">The following example shows a filter that specifies a **whenCreated** time set to 3/23/99 8:52:58 PM New Zealand Standard Time (differential is +12 hours):</span></span>


```C++
(whenCreated=19990323205258.0+1200)
```



<span data-ttu-id="0b008-166">Das folgende Codebeispiel zeigt, wie die differenzielle Zeitzone berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="0b008-166">The following code example shows how to calculate time zone differential.</span></span> <span data-ttu-id="0b008-167">Die Funktion gibt die Differenz zwischen der aktuellen lokalen Zeitzone und GMT zurück.</span><span class="sxs-lookup"><span data-stu-id="0b008-167">The function returns the differential between the current local time zone and GMT.</span></span> <span data-ttu-id="0b008-168">Der zurückgegebene Wert ist eine Zeichenfolge im folgenden Format:</span><span class="sxs-lookup"><span data-stu-id="0b008-168">The value returned is a string in the following format:</span></span>


```C++
[+/-]HHMM
```



<span data-ttu-id="0b008-169">Pacific Normalzeit ist beispielsweise -0800.</span><span class="sxs-lookup"><span data-stu-id="0b008-169">For example, Pacific Standard Time is -0800.</span></span>


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

<span data-ttu-id="0b008-170"><span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>UTCTime</span><span class="sxs-lookup"><span data-stu-id="0b008-170"><span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>UTCTime</span></span>
</dt> <dd>

<span data-ttu-id="0b008-171">Der in einem Filter angegebene Wert ist eine Zeichenfolge, die das Datum in der folgenden Form darstellt:</span><span class="sxs-lookup"><span data-stu-id="0b008-171">The value specified in a filter is a string that represents the date in the following form:</span></span>


```C++
YYMMDDHHMMSSZ
```



<span data-ttu-id="0b008-172">Z gibt an, dass es keine differenzielle Zeit gibt.</span><span class="sxs-lookup"><span data-stu-id="0b008-172">Z indicates no time differential.</span></span> <span data-ttu-id="0b008-173">Beachten Sie, dass der Active Directory-Server Datum und Uhrzeit als GMT-Zeit speichert.</span><span class="sxs-lookup"><span data-stu-id="0b008-173">Be aware that the Active Directory server stores date and time as GMT time.</span></span> <span data-ttu-id="0b008-174">Wenn kein zeitdifferenzieller Wert angegeben wird, ist GMT der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="0b008-174">If a time differential is not specified, GMT is the default.</span></span>

<span data-ttu-id="0b008-175">Der Sekundenwert ("SS") ist optional.</span><span class="sxs-lookup"><span data-stu-id="0b008-175">The seconds value ("SS") is optional.</span></span>

<span data-ttu-id="0b008-176">Wenn GMT nicht die lokale Zeitzone ist, wenden Sie einen lokalen differenziellen Wert an, um Ihre lokale Zeitzone anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0b008-176">If GMT is not the local time zone, apply a local differential value to specify your local time zone.</span></span> <span data-ttu-id="0b008-177">Der differenzielle Wert ist: GMT=Local+differential.</span><span class="sxs-lookup"><span data-stu-id="0b008-177">The differential is: GMT=Local+differential.</span></span>

<span data-ttu-id="0b008-178">Verwenden Sie zum Angeben eines differenziellen -Werts das folgende Formular:</span><span class="sxs-lookup"><span data-stu-id="0b008-178">To specify a differential, use the following form:</span></span>


```C++
YYMMDDHHMMSS[+/-]HHMM
```



<span data-ttu-id="0b008-179">Das folgende Beispiel zeigt einen Filter, der eine **myTimeAttrib-Zeit** angibt, die auf 23.03.2019 20:52:58 Uhr GMT festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="0b008-179">The following example shows a filter that specifies a **myTimeAttrib** time set to 3/23/99 8:52:58 PM GMT:</span></span>


```C++
(myTimeAttrib=990323205258Z)
```



<span data-ttu-id="0b008-180">Das folgende Beispiel zeigt einen Filter, der eine **myTimeAttrib-Zeit** ohne Angabe von Sekunden auf 23.03.99 20:52:58 Uhr angibt:</span><span class="sxs-lookup"><span data-stu-id="0b008-180">The following example shows a filter that specifies a **myTimeAttrib** time set to 3/23/99 8:52:58 PM without seconds specified:</span></span>


```C++
(myTimeAttrib=9903232052Z)
```



<span data-ttu-id="0b008-181">Das folgende Beispiel zeigt einen Filter, der eine **myTimeAttrib-Zeit** angibt, die auf 23.03.2019 20:52:58 Uhr Normalzeit (differenziell: 12 Stunden) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0b008-181">The following example shows a filter that specifies a **myTimeAttrib** time set to 3/23/99 8:52:58 PM New Zealand Standard Time (differential is 12 hours).</span></span> <span data-ttu-id="0b008-182">Dies entspricht 3/23/99 8:52:58 AM GMT.</span><span class="sxs-lookup"><span data-stu-id="0b008-182">This is equivalent to 3/23/99 8:52:58 AM GMT.</span></span>


```C++
(myTimeAttrib=990323205258+1200)
```



</dd> <dt>

<span data-ttu-id="0b008-183"><span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>DirectoryString</span><span class="sxs-lookup"><span data-stu-id="0b008-183"><span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>DirectoryString</span></span>
</dt> <dd>

<span data-ttu-id="0b008-184">Der in einem Filter angegebene Wert ist eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0b008-184">The value specified in a filter is a string.</span></span> <span data-ttu-id="0b008-185">DirectoryString kann Unicode-Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="0b008-185">DirectoryString can contain Unicode characters.</span></span> <span data-ttu-id="0b008-186">Bei dem Vergleich wird Groß- und Kleinschreibung nicht unterschieden.</span><span class="sxs-lookup"><span data-stu-id="0b008-186">The comparison is case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="0b008-187"><span id="OID"></span><span id="oid"></span>Oid</span><span class="sxs-lookup"><span data-stu-id="0b008-187"><span id="OID"></span><span id="oid"></span>OID</span></span>
</dt> <dd>

<span data-ttu-id="0b008-188">Die gesamte übereinstimmende OID muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0b008-188">The entire OID to be matched must be supplied.</span></span>

<span data-ttu-id="0b008-189">Platzhalter werden nicht akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="0b008-189">Wildcards are not accepted.</span></span>

<span data-ttu-id="0b008-190">Mit **dem objectCategory-Attribut** können Sie **den lDAPDisplayName** der Für das Attribut festgelegten Klasse angeben.</span><span class="sxs-lookup"><span data-stu-id="0b008-190">The **objectCategory** attribute enables you to specify the **lDAPDisplayName** of the class set for the attribute.</span></span>

<span data-ttu-id="0b008-191">Das folgende Beispiel zeigt einen Filter, der **governsID für** die Volumeklasse angibt:</span><span class="sxs-lookup"><span data-stu-id="0b008-191">The following example shows a filter that specifies **governsID** for volume class:</span></span>


```C++
(governsID=1.2.840.113556.1.5.36)
```



<span data-ttu-id="0b008-192">Zwei entsprechende Filter, die das **systemMustContain-Attribut** mit **uNCName** angeben, das über eine OID von 1.2.840.113556.1.4.137 verfügt:</span><span class="sxs-lookup"><span data-stu-id="0b008-192">Two equivalent filters that specifies **systemMustContain** attribute containing **uNCName**, which has an OID of 1.2.840.113556.1.4.137:</span></span>


```C++
(SystemMustContain=uNCName)
 
(SystemMustContain=1.2.840.113556.1.4.137)
```



</dd> <dt>

<span data-ttu-id="0b008-193"><span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>Andere Syntaxen</span><span class="sxs-lookup"><span data-stu-id="0b008-193"><span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>Other Syntaxes</span></span>
</dt> <dd>

<span data-ttu-id="0b008-194">Die folgenden Syntaxen werden in einem Filter ausgewertet, der einer Oktettzeichenfolge ähnelt:</span><span class="sxs-lookup"><span data-stu-id="0b008-194">The following syntaxes are evaluated in a filter similar to an octet string:</span></span>

-   <span data-ttu-id="0b008-195">ObjectSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="0b008-195">ObjectSecurityDescriptor</span></span>
-   <span data-ttu-id="0b008-196">AccessPointDN</span><span class="sxs-lookup"><span data-stu-id="0b008-196">AccessPointDN</span></span>
-   <span data-ttu-id="0b008-197">PresentationAddresses</span><span class="sxs-lookup"><span data-stu-id="0b008-197">PresentationAddresses</span></span>
-   <span data-ttu-id="0b008-198">ReplicaLink</span><span class="sxs-lookup"><span data-stu-id="0b008-198">ReplicaLink</span></span>
-   <span data-ttu-id="0b008-199">DNWithString</span><span class="sxs-lookup"><span data-stu-id="0b008-199">DNWithString</span></span>
-   <span data-ttu-id="0b008-200">DNWithOctetString</span><span class="sxs-lookup"><span data-stu-id="0b008-200">DNWithOctetString</span></span>
-   <span data-ttu-id="0b008-201">ORName</span><span class="sxs-lookup"><span data-stu-id="0b008-201">ORName</span></span>

</dd> </dl>

 

 