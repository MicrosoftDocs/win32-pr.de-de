---
title: Binden an ein Objekt mithilfe einer sid
description: In Windows Server 2003 ist es möglich, mithilfe der Objekt Sicherheits-ID (SID) und einer GUID eine Bindung an ein Objekt herzustellen. Die Objekt-SID wird im objectSID-Attribut gespeichert. Die Bindung an eine SID funktioniert nicht unter Windows 2000.
ms.assetid: 18b4613c-eb93-4204-96f2-0f91d7900587
ms.tgt_platform: multiple
keywords:
- Binden an ein Objekt mithilfe einer SID-Werbe einblads
- Active Directory, verwenden, binden, binden an ein Objekt mithilfe einer sid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ad4ecf2d6faa385ab8085730e4f1cb0689e403
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472692"
---
# <a name="binding-to-an-object-using-a-sid"></a><span data-ttu-id="4d53a-107">Binden an ein Objekt mithilfe einer sid</span><span class="sxs-lookup"><span data-stu-id="4d53a-107">Binding to an Object Using a SID</span></span>

<span data-ttu-id="4d53a-108">In Windows Server 2003 ist es möglich, mithilfe der Objekt Sicherheits-ID (SID) und einer GUID eine Bindung an ein Objekt herzustellen.</span><span class="sxs-lookup"><span data-stu-id="4d53a-108">In Windows Server 2003, it is possible to bind to an object using the object Security Identifier (SID) as well as a GUID.</span></span> <span data-ttu-id="4d53a-109">Die Objekt-SID wird im **objectSID** -Attribut gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4d53a-109">The object SID is stored in the **objectSID** attribute.</span></span> <span data-ttu-id="4d53a-110">Die Bindung an eine SID funktioniert nicht unter Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4d53a-110">Binding to an SID does not work on Windows 2000.</span></span>

<span data-ttu-id="4d53a-111">Der LDAP-Anbieter für Active Directory Domain Services stellt eine Methode bereit, mit der die Objekt-SID an ein Objekt gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d53a-111">The LDAP provider for Active Directory Domain Services provides a method to bind to an object using the object SID.</span></span> <span data-ttu-id="4d53a-112">Das Format der Bindungs Zeichenfolge lautet:</span><span class="sxs-lookup"><span data-stu-id="4d53a-112">The binding string format is:</span></span>


```C++
LDAP://servername/<SID=XXXXX>
```



<span data-ttu-id="4d53a-113">In diesem Beispiel ist "Servername" der Name des Verzeichnis Servers und "xxxxx" die Zeichen folgen Darstellung des hexadezimal Werts der SID.</span><span class="sxs-lookup"><span data-stu-id="4d53a-113">In this example, "servername" is the name of the directory server and "XXXXX" is the string representation of the hexadecimal value of the SID.</span></span> <span data-ttu-id="4d53a-114">Der Servername ist optional.</span><span class="sxs-lookup"><span data-stu-id="4d53a-114">The "servername" is optional.</span></span> <span data-ttu-id="4d53a-115">Die SID-Zeichenfolge wird in einem Formular angegeben, in dem jedes Zeichen in der Zeichenfolge die hexadezimale Darstellung der einzelnen Bytes der SID ist.</span><span class="sxs-lookup"><span data-stu-id="4d53a-115">The SID string is specified in a form where each character in the string is the hexadecimal representation of each byte of the SID.</span></span> <span data-ttu-id="4d53a-116">Wenn das Array z. b. ist:</span><span class="sxs-lookup"><span data-stu-id="4d53a-116">For example, if the array is:</span></span>


```C++
0xAB 0x14 0xE2
```



<span data-ttu-id="4d53a-117">die SID-Bindungs Zeichenfolge wäre " &lt; sid = AB14E2 &gt; ".</span><span class="sxs-lookup"><span data-stu-id="4d53a-117">the SID binding string would be "&lt;SID=AB14E2&gt;".</span></span> <span data-ttu-id="4d53a-118">Die [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) -Funktion sollte nicht verwendet werden, um das sid-Array in eine Zeichenfolge zu konvertieren, da es jedem Byte Zeichen mit einem umgekehrten Schrägstrich vorangestellt ist, bei dem es sich nicht um ein gültiges Bindungs Zeichen folgen Format handelt.</span><span class="sxs-lookup"><span data-stu-id="4d53a-118">The [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) function should not be used to convert the SID array into a string because it precedes each byte character with a backslash, which is not a valid bind string format.</span></span>

<span data-ttu-id="4d53a-119">Die SID-Zeichenfolge kann auch die Form " &lt; SID = S-x-x-xx-xxxxxxxxxx-xxxxxxxxxx-xxxxxxxxx-xxx &gt; " aufweisen, dabei ist der Teil "S-x-x-xx-xxxxxxxxxx-xxxxxxxxxxxx-xxxxxxxxx-xxx" identisch mit der Zeichenfolge, die von der [**convertsidtstringsid**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4d53a-119">The SID string can also take the form "&lt;SID=S-X-X-XX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXX&gt;", where the "S-X-X-XX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXX" portion is the same as the string returned by the [**ConvertSidToStringSid**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) function.</span></span>

<span data-ttu-id="4d53a-120">Bei der Bindung mithilfe der Objekt-SID werden einige [**IADs**](/windows/desktop/api/iads/nn-iads-iads) und [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Methoden und-Eigenschaften nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4d53a-120">When binding using the object SID, some [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) methods and properties are not supported.</span></span> <span data-ttu-id="4d53a-121">Die folgenden **IADs** -Eigenschaften werden nicht von Objekten unterstützt, die mithilfe der Objekt-SID durch eine Bindung abgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="4d53a-121">The following **IADs** properties are not supported by objects obtained by binding using the object SID:</span></span>

-   [<span data-ttu-id="4d53a-122">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="4d53a-122">**ADsPath**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="4d53a-123">**Name**</span><span class="sxs-lookup"><span data-stu-id="4d53a-123">**Name**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="4d53a-124">**Parent**</span><span class="sxs-lookup"><span data-stu-id="4d53a-124">**Parent**</span></span>](/windows/desktop/ADSI/iads-property-methods)

<span data-ttu-id="4d53a-125">Die folgenden **IADsContainer** -Methoden werden nicht von Objekten unterstützt, die mithilfe der Objekt-SID durch eine Bindung abgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="4d53a-125">The following **IADsContainer** methods are not supported by objects obtained by binding using the object SID:</span></span>

-   [<span data-ttu-id="4d53a-126">**GetObject**</span><span class="sxs-lookup"><span data-stu-id="4d53a-126">**GetObject**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [<span data-ttu-id="4d53a-127">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="4d53a-127">**Create**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [<span data-ttu-id="4d53a-128">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="4d53a-128">**Delete**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [<span data-ttu-id="4d53a-129">**Copyhere**</span><span class="sxs-lookup"><span data-stu-id="4d53a-129">**CopyHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [<span data-ttu-id="4d53a-130">**Muvehere**</span><span class="sxs-lookup"><span data-stu-id="4d53a-130">**MoveHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

<span data-ttu-id="4d53a-131">Wenn Sie diese Methoden und Eigenschaften nach der Bindung an ein Objekt mithilfe der Objekt-SID verwenden möchten, verwenden Sie die [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) -Methode, um den Distinguished Name des Objekts abzurufen, und verwenden Sie dann den Distinguished Name, um die Bindung an das Objekt wiederherzustellen</span><span class="sxs-lookup"><span data-stu-id="4d53a-131">To use these methods and properties after binding to an object using the object SID, use the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to retrieve the object distinguished name and then use the distinguished name to bind to the object again.</span></span>

<span data-ttu-id="4d53a-132">Im folgenden Codebeispiel wird gezeigt, wie eine **objectSID** in eine bindbare Zeichenfolge konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="4d53a-132">The following code example shows how to convert an **objectSid** into a bindable string.</span></span>


```C++
HRESULT VariantArrayToBytes(VARIANT Variant, 
    LPBYTE *ppBytes, 
    DWORD *pdwBytes);

/********

    GetSIDBindStringFromVariant()

    Converts a SID in VARIANT form, such as an objectSid value, and 
    converts it into a bindable string in the form:

    LDAP://<SID=xxxxxxx...>

    The returned string is allocated with AllocADsMem and must be 
    freed by the caller with FreeADsMem.

*********/

LPWSTR GetSIDBindStringFromVariant(VARIANT vSID)
{
    LPWSTR pwszReturn = NULL;

    if(VT_ARRAY & vSID.vt) 
    {
        HRESULT hr;
        LPBYTE pByte;
        DWORD dwBytes = 0;

        hr = VariantArrayToBytes(vSID, &pByte, &dwBytes);
        if(S_OK == hr)
        {
            // Convert the BYTE array into a string of hex 
            // characters.
            CComBSTR sbstrTemp = "LDAP://<SID=";

            for(DWORD i = 0; i < dwBytes; i++)
            {
                WCHAR wszByte[3];

                swprintf_s(wszByte, L"%02x", pByte[i]);
                sbstrTemp += wszByte;
            }

            sbstrTemp += ">";
            pwszReturn = 
               (LPWSTR)AllocADsMem((sbstrTemp.Length() + 1) * 
                sizeof(WCHAR));
            if(pwszReturn)
            {
                wcscpy_s(pwszReturn, sbstrTemp.m_str);
            }

            FreeADsMem(pByte);
        }
    }

    return pwszReturn;
}

/*********

    VariantArrayToBytes()

    This function converts a VARIANT array into an array of BYTES. 
    This function allocates the buffer using AllocADsMem. The 
    caller must free this memory with FreeADsMem when it is no 
    longer required.

**********/

HRESULT VariantArrayToBytes(VARIANT Variant, 
    LPBYTE *ppBytes, 
    DWORD *pdwBytes)
{
    if(!(Variant.vt & VT_ARRAY) ||
        !Variant.parray ||
        !ppBytes ||
        !pdwBytes)
    {
        return E_INVALIDARG;
    }

    *ppBytes = NULL;
    *pdwBytes = 0;

    HRESULT hr = E_FAIL;
    SAFEARRAY *pArrayVal = NULL;
    CHAR HUGEP *pArray = NULL;
    
    // Retrieve the safe array.
    pArrayVal = Variant.parray;
    DWORD dwBytes = pArrayVal->rgsabound[0].cElements;
    *ppBytes = (LPBYTE)AllocADsMem(dwBytes);
    if(NULL == *ppBytes) 
    {
        return E_OUTOFMEMORY;
    }

    hr = SafeArrayAccessData(pArrayVal, (void HUGEP * FAR *) &pArray);
    if(SUCCEEDED(hr))
    {
        // Copy the bytes to the safe array.
        CopyMemory(*ppBytes, pArray, dwBytes);
        SafeArrayUnaccessData( pArrayVal );
        *pdwBytes = dwBytes;
    }
    
    return hr;
}
```



 

 