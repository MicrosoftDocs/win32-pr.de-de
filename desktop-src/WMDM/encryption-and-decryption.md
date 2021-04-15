---
title: Verschlüsselung und Entschlüsselung
description: Verschlüsselung und Entschlüsselung
ms.assetid: 6aef4138-0391-4edd-b4fc-d6d0ec3c735b
keywords:
- Windows Media Device Manager, Verschlüsselung
- Device Manager, Verschlüsselung
- Desktop Anwendungen, Verschlüsselung
- Dienstanbieter, Verschlüsselung
- Programmier Handbuch, Verschlüsselung
- Verschlüsselung
- Windows Media-Device Manager, Entschlüsselung
- Device Manager, Entschlüsselung
- Desktop Anwendungen, entschlüsseln
- Dienstanbieter, Entschlüsselung
- Programmier Handbuch, Entschlüsselung
- Entschlüsselung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78688c1b4ca9991d8b322c6991de96a51e7e8d22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390915"
---
# <a name="encryption-and-decryption"></a><span data-ttu-id="126ae-115">Verschlüsselung und Entschlüsselung</span><span class="sxs-lookup"><span data-stu-id="126ae-115">Encryption and Decryption</span></span>

<span data-ttu-id="126ae-116">Windows Media Device Manager erfordert die Verschlüsselung von Dateien, die zwischen dem Dienstanbieter und der Anwendung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="126ae-116">Windows Media Device Manager requires encryption of files sent between the service provider and the application.</span></span> <span data-ttu-id="126ae-117">Dafür können Sie zwei Methoden verwenden:</span><span class="sxs-lookup"><span data-stu-id="126ae-117">This can be done in one of two ways:</span></span>

-   <span data-ttu-id="126ae-118">Wenn der Dienstanbieter nur [**imdspobject:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) und [**imdspobject:: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)unterstützt, müssen die Daten von der Anwendung und dem Dienstanbieter mithilfe der Methoden [csecurechannelclient](csecurechannelclient-class.md) bzw. [csecurechannelserver](csecurechannelserver-class.md) verschlüsselt und entschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="126ae-118">If the service provider supports only [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) and [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write), the data must be encrypted and decrypted by the application and service provider by using [CSecureChannelClient](csecurechannelclient-class.md) and [CSecureChannelServer](csecurechannelserver-class.md) methods respectively.</span></span>
-   <span data-ttu-id="126ae-119">Wenn der Dienstanbieter [**IMDSPObject2:: Read onclearchannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) und [**IMDSPObject2:: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel)Service Provider unterstützt, kann die Anwendung eine teure sichere Kanalnachrichten Authentifizierung vermeiden.</span><span class="sxs-lookup"><span data-stu-id="126ae-119">If the service provider supports [**IMDSPObject2::ReadOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) and [**IMDSPObject2::WriteOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel), your application can avoid costly secure channel message authentication.</span></span> <span data-ttu-id="126ae-120">(Der sichere Kanal wird beibehalten, sodass Legacy-Dienstanbieter, die [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) nicht implementieren, weiterhin funktionieren können.)</span><span class="sxs-lookup"><span data-stu-id="126ae-120">(The secure channel is retained so that legacy service providers that do not implement [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) can still continue to function.)</span></span>

<span data-ttu-id="126ae-121">Die Verschlüsselungs Anforderung verhindert, dass böswillige Anwendungen Daten abrufen, die zwischen Softwarekomponenten übermittelt werden, und schützt außerdem die Integrität der Daten, die an das Gerät gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="126ae-121">The encryption requirement prevents malicious applications from obtaining data that is being passed between software components, and also protects the integrity of data being sent to or from the device.</span></span>

<span data-ttu-id="126ae-122">Die folgenden drei Methoden müssen verschlüsselt oder entschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="126ae-122">The following three methods require encryption or decryption.</span></span>



| <span data-ttu-id="126ae-123">Methode</span><span class="sxs-lookup"><span data-stu-id="126ae-123">Method</span></span>                                                                          | <span data-ttu-id="126ae-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="126ae-124">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="126ae-125">**Iwmdmoperation:: transferobjectdata**</span><span class="sxs-lookup"><span data-stu-id="126ae-125">**IWMDMOperation::TransferObjectData**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) | <span data-ttu-id="126ae-126">Asyl Verschlüsselung oder Entschlüsselung, abhängig davon, ob die Anwendung Daten sendet oder empfängt.</span><span class="sxs-lookup"><span data-stu-id="126ae-126">(Application) Encryption or decryption, depending on whether the application is sending or receiving data.</span></span> |
| [<span data-ttu-id="126ae-127">**Imdspobject:: Read**</span><span class="sxs-lookup"><span data-stu-id="126ae-127">**IMDSPObject::Read**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)                                   | <span data-ttu-id="126ae-128">(Dienstanbieter) Verschlüsselungs.</span><span class="sxs-lookup"><span data-stu-id="126ae-128">(Service provider) Encryption.</span></span>                                                                             |
| [<span data-ttu-id="126ae-129">**Imdspobject:: Write**</span><span class="sxs-lookup"><span data-stu-id="126ae-129">**IMDSPObject::Write**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)                                 | <span data-ttu-id="126ae-130">(Dienstanbieter) Entschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="126ae-130">(Service Provider) Decryption.</span></span>                                                                             |



 

<span data-ttu-id="126ae-131">Verschlüsselung und Entschlüsselung werden von einzelnen Methoden aufrufen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="126ae-131">Encryption and decryption are both done by single method calls.</span></span> <span data-ttu-id="126ae-132">Die Verschlüsselung erfolgt durch [**csecurechannelclient:: verschlüsseltparam**](/previous-versions/bb231587(v=vs.85)) für Anwendungen oder durch [**csecurechannelserver:: verschlüsseltparam**](/previous-versions/ms868509(v=msdn.10)) für Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="126ae-132">Encryption is done by [**CSecureChannelClient::EncryptParam**](/previous-versions/bb231587(v=vs.85)) for applications or by [**CSecureChannelServer::EncryptParam**](/previous-versions/ms868509(v=msdn.10)) for service providers.</span></span> <span data-ttu-id="126ae-133">Die Entschlüsselung erfolgt durch [**csecurechannelclient::D ecryptparam**](/previous-versions/bb231586(v=vs.85)) für Anwendungen oder [**csecurechannelserver::D ecryptparam**](/previous-versions/bb231598(v=vs.85)) für Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="126ae-133">Decryption is done by [**CSecureChannelClient::DecryptParam**](/previous-versions/bb231586(v=vs.85)) for applications or [**CSecureChannelServer::DecryptParam**](/previous-versions/bb231598(v=vs.85)) for service providers.</span></span> <span data-ttu-id="126ae-134">Die Parameter sind zwischen den Client-und Server Methoden identisch.</span><span class="sxs-lookup"><span data-stu-id="126ae-134">The parameters are identical between the client and server methods.</span></span>

<span data-ttu-id="126ae-135">In den folgenden Schritten wird gezeigt, wie Daten verschlüsselt und entschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="126ae-135">The following steps show how to encrypt and decrypt data.</span></span> <span data-ttu-id="126ae-136">(Diese Schritte sind nur dann wichtig, wenn Ihre Anwendung mit einem Legacy Dienstanbieter kommuniziert, der [IWMDMOperation3:: transferobjectdataonclearchannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel)nicht implementiert.)</span><span class="sxs-lookup"><span data-stu-id="126ae-136">(These steps are important only if your application communicates with a legacy service provider that does not implement [IWMDMOperation3::TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel).)</span></span>

<span data-ttu-id="126ae-137">**Verschlüsselung**</span><span class="sxs-lookup"><span data-stu-id="126ae-137">**Encryption**</span></span>

1.  <span data-ttu-id="126ae-138">Erstellen Sie den Mac-Schlüssel für die verschlüsselten Daten, wie in [Nachrichten Authentifizierung](message-authentication.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="126ae-138">Create the MAC key for the encrypted data, as described in [Message Authentication](message-authentication.md).</span></span>
2.  <span data-ttu-id="126ae-139">Nennen Sie **verschlüsseltparam** mit den zu verschlüsselnden Daten, um eine direkte Verschlüsselung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="126ae-139">Call **EncryptParam** with the data to encrypt, to perform in-place encryption.</span></span>

<span data-ttu-id="126ae-140">Im folgenden Codebeispiel wird die Implementierung von [**imdspobject:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)eines Dienstanbieters veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="126ae-140">The following code example demonstrates a service provider's implementation of [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read).</span></span> <span data-ttu-id="126ae-141">Diese Methode erstellt den Mac-Schlüssel mithilfe der zu verschlüsselnden Daten und der Größe der Daten und sendet beide an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="126ae-141">This method creates the MAC key using the data to encrypt and the size of the data, and sends them both to the application.</span></span>


```C++
HRESULT CMyStorage::Read(
    BYTE  *pData,
    DWORD *pdwSize,
    BYTE   abMac[WMDM_MAC_LENGTH])
{
    HRESULT  hr;
    DWORD    dwToRead;         // Bytes to read.
    DWORD    dwRead   = NULL;  // Bytes read.
    BYTE    *pTmpData = NULL;  // Temporary buffer to hold data before 
                               // it is copied to pData.

    // Use a global CSecureChannelServer member to verify that 
    // the client is authenticated.
    if (!(g_pAppSCServer->fIsAuthenticated()))
    {
        return WMDM_E_NOTCERTIFIED;
    }
    

    // Verify that the handle to the file to read is valid.
    if(m_hFile == INVALID_HANDLE_VALUE)
    {
        return E_FAIL;
    }

    // Create a buffer to hold the data read.    
    dwToRead = *pdwSize;
    pTmpData = new BYTE [dwToRead] ;
    if(!pTmpData)
        return E_OUTOFMEMORY;

    // Read data into the temporary buffer.
    if(ReadFile(m_hFile,(LPVOID)pTmpData,dwToRead,&dwRead,NULL)) 
    { 
        *pdwSize = dwRead; 

        if( dwRead )
        {
            // Create a MAC from all the parameters.
            // CORg is a macro that goes to Error label on failure.
            // MAC consists of data and size of data.
            HMAC hMAC;
            
            CORg(g_pAppSCServer->MACInit(&hMAC));
            CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pTmpData), dwRead));
            CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(DWORD)));
            CORg(g_pAppSCServer->MACFinal(hMAC, abMac));
            
            // Encrypt the data.
            CORg(g_pAppSCServer->EncryptParam(pTmpData, dwRead));
            
            // Copy data from the temporary buffer into the out parameter.
            memcpy(pData, pTmpData, dwRead);
        }
    
        hr = S_OK; 
    }
    else
    { 
        *pdwSize = 0; 

        hr = E_FAIL; 
    }

Error:

    if(pTmpData) 
    {
        delete [] pTmpData;
    }

    return hr;
} 
```



<span data-ttu-id="126ae-142">**Entschlüsselung**</span><span class="sxs-lookup"><span data-stu-id="126ae-142">**Decryption**</span></span>

1.  <span data-ttu-id="126ae-143">Wenden Sie **decryptparam** mit den zu verschlüsselnden Daten an, um eine direkte Entschlüsselung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="126ae-143">Call **DecryptParam** with the data to encrypt, to perform in-place decryption.</span></span>
2.  <span data-ttu-id="126ae-144">Überprüfen Sie den Mac-Schlüssel für die entschlüsselten Daten, wie in [Nachrichten Authentifizierung](message-authentication.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="126ae-144">Verify the MAC key for the decrypted data, as described in [Message Authentication](message-authentication.md).</span></span>

<span data-ttu-id="126ae-145">Im folgenden Codebeispiel wird die Implementierung von [**imdspobject:: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)eines Dienstanbieters veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="126ae-145">The following code example demonstrates a service provider's implementation of [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write).</span></span> <span data-ttu-id="126ae-146">Diese Methode erstellt den Mac-Schlüssel mithilfe der zu verschlüsselnden Daten und der Größe der Daten und sendet beide an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="126ae-146">This method creates the MAC key using the data to encrypt and the size of the data, and sends them both to the application.</span></span>


```C++
HRESULT CMyStorage::Write(BYTE *pData, DWORD *pdwSize,
                                 BYTE abMac[WMDM_MAC_LENGTH])
{
    HRESULT  hr;
    DWORD    dwWritten = 0;
    BYTE    *pTmpData  = NULL;          // Temporary buffer to hold the 
                                        // data during decryption.
    BYTE     pTempMac[WMDM_MAC_LENGTH]; // Temporary MAC that will be 
                                        // copied into the abMac
                                        // out parameter.

    if( m_hFile == INVALID_HANDLE_VALUE )
    {
        return E_FAIL;
    }

    // Allocate the temporary buffer and copy the encrypted data into it.
    pTmpData = new BYTE [*pdwSize];
    if(!pTmpData)
        return E_OUTOFMEMORY;
    memcpy(pTmpData, pData, *pdwSize);

    // Decrypt the data.
    CHRg(g_pAppSCServer->DecryptParam(pTmpData, *pdwSize));

    // Check the MAC passed to the method. The MAC is built from
    // the data and data size parameters.
    // CORg is a macro that goes to the Error label on failure.
    HMAC hMAC;
    CORg(g_pAppSCServer->MACInit(&hMAC));
    CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pTmpData), *pdwSize));
    CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(*pdwSize)));
    CORg(g_pAppSCServer->MACFinal(hMAC, pTempMac));

    // If the MAC values don't match, return an error.
    if (memcmp(abMac, pTempMac, WMDM_MAC_LENGTH) != 0)
    {
        hr = WMDM_E_MAC_CHECK_FAILED;
        goto Error;
    }

    // The MAC values matched, so write the decrypted data to a local file.
    if( WriteFile(m_hFile,pTmpData,*pdwSize,&dwWritten,NULL) ) 
    {
        hr = S_OK;
    }
    else 
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }

    *pdwSize = dwWritten;

Error:

    if( pTmpData )
    {
        delete [] pTmpData;
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="126ae-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="126ae-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="126ae-148">**Verwenden sicherer authentifizierter Kanäle**</span><span class="sxs-lookup"><span data-stu-id="126ae-148">**Using Secure Authenticated Channels**</span></span>](using-secure-authenticated-channels.md)
</dt> </dl>

 

 