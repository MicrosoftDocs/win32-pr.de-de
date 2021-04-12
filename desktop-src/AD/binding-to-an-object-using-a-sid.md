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
# <a name="binding-to-an-object-using-a-sid"></a>Binden an ein Objekt mithilfe einer sid

In Windows Server 2003 ist es möglich, mithilfe der Objekt Sicherheits-ID (SID) und einer GUID eine Bindung an ein Objekt herzustellen. Die Objekt-SID wird im **objectSID** -Attribut gespeichert. Die Bindung an eine SID funktioniert nicht unter Windows 2000.

Der LDAP-Anbieter für Active Directory Domain Services stellt eine Methode bereit, mit der die Objekt-SID an ein Objekt gebunden werden soll. Das Format der Bindungs Zeichenfolge lautet:


```C++
LDAP://servername/<SID=XXXXX>
```



In diesem Beispiel ist "Servername" der Name des Verzeichnis Servers und "xxxxx" die Zeichen folgen Darstellung des hexadezimal Werts der SID. Der Servername ist optional. Die SID-Zeichenfolge wird in einem Formular angegeben, in dem jedes Zeichen in der Zeichenfolge die hexadezimale Darstellung der einzelnen Bytes der SID ist. Wenn das Array z. b. ist:


```C++
0xAB 0x14 0xE2
```



die SID-Bindungs Zeichenfolge wäre " &lt; sid = AB14E2 &gt; ". Die [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) -Funktion sollte nicht verwendet werden, um das sid-Array in eine Zeichenfolge zu konvertieren, da es jedem Byte Zeichen mit einem umgekehrten Schrägstrich vorangestellt ist, bei dem es sich nicht um ein gültiges Bindungs Zeichen folgen Format handelt.

Die SID-Zeichenfolge kann auch die Form " &lt; SID = S-x-x-xx-xxxxxxxxxx-xxxxxxxxxx-xxxxxxxxx-xxx &gt; " aufweisen, dabei ist der Teil "S-x-x-xx-xxxxxxxxxx-xxxxxxxxxxxx-xxxxxxxxx-xxx" identisch mit der Zeichenfolge, die von der [**convertsidtstringsid**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) -Funktion zurückgegeben wird.

Bei der Bindung mithilfe der Objekt-SID werden einige [**IADs**](/windows/desktop/api/iads/nn-iads-iads) und [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Methoden und-Eigenschaften nicht unterstützt. Die folgenden **IADs** -Eigenschaften werden nicht von Objekten unterstützt, die mithilfe der Objekt-SID durch eine Bindung abgerufen werden:

-   [**ADsPath**](/windows/desktop/ADSI/iads-property-methods)
-   [**Name**](/windows/desktop/ADSI/iads-property-methods)
-   [**Parent**](/windows/desktop/ADSI/iads-property-methods)

Die folgenden **IADsContainer** -Methoden werden nicht von Objekten unterstützt, die mithilfe der Objekt-SID durch eine Bindung abgerufen werden:

-   [**GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [**Stelle**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [**Lösch**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [**Copyhere**](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [**Muvehere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

Wenn Sie diese Methoden und Eigenschaften nach der Bindung an ein Objekt mithilfe der Objekt-SID verwenden möchten, verwenden Sie die [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) -Methode, um den Distinguished Name des Objekts abzurufen, und verwenden Sie dann den Distinguished Name, um die Bindung an das Objekt wiederherzustellen

Im folgenden Codebeispiel wird gezeigt, wie eine **objectSID** in eine bindbare Zeichenfolge konvertiert wird.


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



 

 