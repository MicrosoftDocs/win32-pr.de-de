---
title: Iadspathname-Eigenschaften Methoden (IADs. h)
description: Die escapedmode-Eigenschaften werden abgerufen oder festgelegt.
ms.assetid: 007ec617-cff2-492a-a62c-50d65fefcd3b
ms.tgt_platform: multiple
keywords:
- Iadspathname-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsPathname Property Methods
- IADsPathname.EscapedMode
- IADsPathname.get_EscapedMode
- IADsPathname.get_EscapedMode
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 949bd41ddb04618d238c0ddf09782e12fb228b26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213728"
---
# <a name="iadspathname-property-methods"></a><span data-ttu-id="3ee6b-104">Iadspathname-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="3ee6b-104">IADsPathname Property Methods</span></span>

<span data-ttu-id="3ee6b-105">Die Eigenschaften Methoden der [**iadspathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) -Schnittstelle ruft die **escapedmode** -Eigenschaften ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="3ee6b-105">The property methods of the [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) interface get or set the **EscapedMode** properties.</span></span> <span data-ttu-id="3ee6b-106">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="3ee6b-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="3ee6b-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3ee6b-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="3ee6b-108">**Escapedmode**</span><span class="sxs-lookup"><span data-stu-id="3ee6b-108">**EscapedMode**</span></span>
<span data-ttu-id="3ee6b-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3ee6b-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="3ee6b-110">Überprüfen oder angeben, wie Escapezeichen in einem Pfadnamen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="3ee6b-110">Examine or specify how escaped characters are handled in a pathname.</span></span> <span data-ttu-id="3ee6b-111">Weitere Informationen und definierte Optionen finden Sie unter [**ADS-escapemodusenum \_ \_ \_**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span><span class="sxs-lookup"><span data-stu-id="3ee6b-111">For more information and defined options, see [**ADS\_ESCAPE\_MODE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span></span>

<dt>

<span data-ttu-id="3ee6b-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3ee6b-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3ee6b-113">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="3ee6b-113">Scripting data type: **Long**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EscapedMode(
  [out] long* retval
);
HRESULT get_EscapedMode(
  [in] long* lnEscapedMode
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="3ee6b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ee6b-114">Remarks</span></span>

<span data-ttu-id="3ee6b-115">Der **escapedmode** stellt einen Status dar.</span><span class="sxs-lookup"><span data-stu-id="3ee6b-115">**EscapedMode** represents a state.</span></span> <span data-ttu-id="3ee6b-116">Sie können diese aktivieren bzw. deaktivieren, indem Sie Sie auf ADS \_ escapedmode \_ on oder ADS \_ escapedmode \_ Off/ADS \_ escapedmode \_ Off \_ per festlegen.</span><span class="sxs-lookup"><span data-stu-id="3ee6b-116">You can turn it on or off, by setting it to ADS\_ESCAPEDMODE\_ON or ADS\_ESCAPEDMODE\_OFF/ADS\_ESCAPEDMODE\_OFF\_EX.</span></span> <span data-ttu-id="3ee6b-117">Wenn Sie aktiviert oder deaktiviert ist, werden alle nachfolgenden Abruf Zeichen mit Escapezeichen oder ohne Escapezeichen versehen.</span><span class="sxs-lookup"><span data-stu-id="3ee6b-117">When it is turned on, or off, all subsequent retrievals produce escaped or unescaped path strings.</span></span>

<span data-ttu-id="3ee6b-118">In ADSI ist nur der [**iadspathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) in der Lage, Pfade zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="3ee6b-118">In ADSI only the [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) is capable of unescaping paths.</span></span> <span data-ttu-id="3ee6b-119">Alle anderen ADSI-Schnittstellen geben immer escapepfade zurück.</span><span class="sxs-lookup"><span data-stu-id="3ee6b-119">All other ADSI interfaces always return escaped paths.</span></span> <span data-ttu-id="3ee6b-120">Der Standardzustand von " **escapedmode** " lautet "ADS \_ escapedmode default" gemäß \_ Definition in der ADS-escapesequenzenum. [**\_ \_ \_**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)</span><span class="sxs-lookup"><span data-stu-id="3ee6b-120">The default state of **EscapedMode** is ADS\_ESCAPEDMODE\_DEFAULT as defined in [**ADS\_ESCAPE\_MODE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span></span>

## <a name="examples"></a><span data-ttu-id="3ee6b-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3ee6b-121">Examples</span></span>

<span data-ttu-id="3ee6b-122">Im folgenden Codebeispiel wird gezeigt, wie die **escapedmode** -Eigenschaft zum Aktivieren/Deaktivieren der folgenden drei Sonderzeichen verwendet wird: "=", "," und "/".</span><span class="sxs-lookup"><span data-stu-id="3ee6b-122">The following code example shows how to use the **EscapedMode** property turn on/off escaping of the following three special characters: "=",",", and "/".</span></span>


```VB
Dim path As New Pathname
path.Set "CN=joy\=ful\,\/*", ADS_SETTYPE_DN
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' All escaped, producing:
                                          ' "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' Only "/" is unescaped:
                                          ' "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEDMODE_OFF_EX
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' All are unescaped:
                                          ' "LDAP://CN=joy=ful,/*"
 
 
path.Set "LDAP://CN=joy\=ful\,\/*", ADS_SETTYPE_FULL
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF_EX
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy=ful,/*"
```



<span data-ttu-id="3ee6b-123">Im folgenden Codebeispiel wird gezeigt, wie die **escapedmode** -Eigenschaft zum Aktivieren/Deaktivieren der folgenden drei Sonderzeichen verwendet wird: "=", "," und "/".</span><span class="sxs-lookup"><span data-stu-id="3ee6b-123">The following code example shows how to use the **EscapedMode** property turn on/off escaping of the following three special characters: "=",",", and "/".</span></span>


```VB
<%
Dim path
const ADS_SETTYPE_FULL = 1
const ADS_SETTYPE_DN   = 4
const ADS_FORMAT_WINDOWS = 1
const ADS_ESCAPEDMODE_ON = 2
const ADS_ESCAPEDMODE_OFF = 3
const ADS_ESCAPEDMODE_OFF_EX = 4
 
Set path = CreateObject("Pathname")
path.Set "CN=joy\=ful\,\/*", ADS_SETTYPE_DN
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  
' All escaped, producing:  "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  
' Only "/" is unescaped: "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEDMODE_OFF_EX
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  ' All are unescaped:
                                          ' "LDAP://CN=joy=ful,/*"
 
 
path.Set "LDAP://CN=joy\=ful\,\/*", ADS_SETTYPE_FULL
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF_EX
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy=ful,/*"
%>
```



<span data-ttu-id="3ee6b-124">Im folgenden Codebeispiel wird gezeigt, wie Sie mit der **escapedmode** -Eigenschaft arbeiten.</span><span class="sxs-lookup"><span data-stu-id="3ee6b-124">The following code example shows how to work with the **EscapedMode** property.</span></span> <span data-ttu-id="3ee6b-125">Die Fehlerüberprüfung wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3ee6b-125">Error checking is ignored.</span></span>


```C++
IADsPathname *pPathname=NULL;
HRESULT hr;
 
hr = CoCreateInstance(CLSID_Pathname,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IADsPathname,
                      (void**)&pPathname);
 
if(FAILED(hr)) 
{
    if(pPathname) pPathname->Release();
    return NULL;
}
 
pPathname->AddRef();
hr = pPathname->Set(CComBSTR("LDAP://CN=joy/ful\/*"), 
                    ADS_SETTYPE_FULL); 
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_OFF);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Unescaped path: %S\n",bstr);   

// Producing "LDAP://CN=joy/ful/*"

SysFreeString(bstr);
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_ON);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Escaped path: %S\n",bstr);

// Producing "LDAP://CN=joy/ful\/*"

SysFreeString(bstr);
 
// Set the path using ADS_SETTYPE_DN
 
hr = pPathname->Set(CComBSTR("CN=joy/ful\/*"), ADS_SETTYPE_DN); 
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_OFF);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Unescaped path: %S\n",bstr);   

// Producing "LDAP://CN=joy/ful/*"

SysFreeString(bstr);
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_ON);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Escaped path: %S\n",bstr);

// Producing "LDAP://CN=joy\/ful\/*"

SysFreeString(bstr);
 
hr = pPathname->Release();
```



## <a name="requirements"></a><span data-ttu-id="3ee6b-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ee6b-126">Requirements</span></span>



| <span data-ttu-id="3ee6b-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ee6b-127">Requirement</span></span> | <span data-ttu-id="3ee6b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="3ee6b-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ee6b-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ee6b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3ee6b-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ee6b-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3ee6b-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ee6b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3ee6b-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ee6b-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3ee6b-133">Header</span><span class="sxs-lookup"><span data-stu-id="3ee6b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ee6b-134"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ee6b-134"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="3ee6b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3ee6b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ee6b-136"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ee6b-136"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="3ee6b-137">IID</span><span class="sxs-lookup"><span data-stu-id="3ee6b-137">IID</span></span><br/>                      | <span data-ttu-id="3ee6b-138">IID \_ iadspathname ist als D592AED4-F420-11D0-A36E-00C04FB950DC definiert.</span><span class="sxs-lookup"><span data-stu-id="3ee6b-138">IID\_IADsPathname is defined as D592AED4-F420-11D0-A36E-00C04FB950DC</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="3ee6b-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ee6b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ee6b-140">**IADsPathname**</span><span class="sxs-lookup"><span data-stu-id="3ee6b-140">**IADsPathname**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspathname)
</dt> <dt>

[<span data-ttu-id="3ee6b-141">**ADS \_ - \_ escapesmodusenum \_**</span><span class="sxs-lookup"><span data-stu-id="3ee6b-141">**ADS\_ESCAPE\_MODE\_ENUM**</span></span>](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)
</dt> </dl>

 

 





