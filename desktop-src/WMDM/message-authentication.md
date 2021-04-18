---
title: Nachrichten Authentifizierung
description: Nachrichten Authentifizierung
ms.assetid: 6cb49f6b-e303-4840-9343-9891e75e07a4
keywords:
- Windows Media Device Manager, Nachrichten Authentifizierung
- Device Manager, Nachrichten Authentifizierung
- Desktop Anwendungen, Nachrichten Authentifizierung
- Dienstanbieter, Nachrichten Authentifizierung
- Programmier Handbuch, Nachrichten Authentifizierung
- Nachrichten Authentifizierung
- Message Authentication Code (Mac)
- Mac (Message Authentication Code)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14805e2074509e918902aae9eb9e9680ca52a6d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337969"
---
# <a name="message-authentication"></a><span data-ttu-id="539dd-111">Nachrichten Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="539dd-111">Message Authentication</span></span>

<span data-ttu-id="539dd-112">Die Nachrichten Authentifizierung ist ein Prozess, mit dem Anwendungen und Dienstanbieter überprüfen können, ob die zwischen Ihnen übergebenen Daten nicht manipuliert wurden.</span><span class="sxs-lookup"><span data-stu-id="539dd-112">Message authentication is a process that enables applications and service providers to verify that data passed between them has not been tampered with.</span></span> <span data-ttu-id="539dd-113">Mithilfe von Windows Media Device Manager können Anwendungen und Dienstanbieter die Nachrichten Authentifizierung mithilfe von Nachrichten Authentifizierungscodes (Macs) durchführen.</span><span class="sxs-lookup"><span data-stu-id="539dd-113">Windows Media Device Manager allows applications and service providers to perform message authentication by using message authentication codes (MACs).</span></span> <span data-ttu-id="539dd-114">Die Mac-Authentifizierung funktioniert wie folgt:</span><span class="sxs-lookup"><span data-stu-id="539dd-114">Here is how MAC authentication works:</span></span>

<span data-ttu-id="539dd-115">Der Daten Absender, normalerweise der Dienstanbieter, übergibt ein oder mehrere Datenelemente über eine unidirektionale Kryptografiefunktion, die für alle Daten eine einzige Signatur, den Mac, erzeugt.</span><span class="sxs-lookup"><span data-stu-id="539dd-115">The data sender, usually the service provider, passes one or more pieces of data through a one-way cryptographic function that produces a single signature, the MAC, for all the data.</span></span> <span data-ttu-id="539dd-116">Anschließend sendet der Absender alle signierten Daten zusammen mit dem Mac an den Empfänger (in der Regel die Anwendung).</span><span class="sxs-lookup"><span data-stu-id="539dd-116">The sender then sends all the signed pieces of data together with the MAC to the receiver (usually the application).</span></span> <span data-ttu-id="539dd-117">Der Empfänger übergibt die Daten über dieselbe Kryptografiefunktion, um einen Mac zu generieren, und vergleicht ihn mit dem gesendeten Mac.</span><span class="sxs-lookup"><span data-stu-id="539dd-117">The receiver passes the data through the same cryptographic function to generate a MAC and compares it to the MAC that was sent.</span></span> <span data-ttu-id="539dd-118">Wenn der Mac übereinstimmt, wurden die Daten nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="539dd-118">If the MAC matches, the data has not been modified.</span></span>

<span data-ttu-id="539dd-119">Um die Mac-Authentifizierung auszuführen, erfordert die Anwendung oder der Dienstanbieter einen Verschlüsselungsschlüssel und ein entsprechendes Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="539dd-119">To perform MAC authentication, the application or service provider requires an encryption key and a matching certificate.</span></span> <span data-ttu-id="539dd-120">Informationen dazu, wo Sie diese erhalten, finden Sie unter [Tools für die Entwicklung](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="539dd-120">For information on where to get these, see [Tools for Development](tools-for-development.md).</span></span>

<span data-ttu-id="539dd-121">In den folgenden Schritten wird beschrieben, wie Daten vom Absender signiert und später vom Empfänger geprüft werden.</span><span class="sxs-lookup"><span data-stu-id="539dd-121">The following steps describe how data is signed by the sender, and later checked by the receiver.</span></span> <span data-ttu-id="539dd-122">In Windows Media Device Manager verwendet der Dienstanbieter die [csecurechannelserver](csecurechannelserver-class.md) -Klasse, um Macs zu generieren, und die Anwendung verwendet die [csecurechannelclient](csecurechannelclient-class.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="539dd-122">In Windows Media Device Manager, the service provider uses the [CSecureChannelServer](csecurechannelserver-class.md) class to generate MACs, and the application uses the [CSecureChannelClient](csecurechannelclient-class.md) class.</span></span> <span data-ttu-id="539dd-123">Beide Klassen stellen identische Funktionen mit identischen Parametern bereit, sodass die folgenden Schritte für beide Klassen gelten.</span><span class="sxs-lookup"><span data-stu-id="539dd-123">Both classes provide identical functions with identical parameters, so the following steps apply to both classes.</span></span>

<span data-ttu-id="539dd-124">Der Absender (in der Regel der Dienstanbieter):</span><span class="sxs-lookup"><span data-stu-id="539dd-124">The sender (typically the service provider):</span></span>

1.  <span data-ttu-id="539dd-125">Die zu Signier enden Daten.</span><span class="sxs-lookup"><span data-stu-id="539dd-125">Get the data to be signed.</span></span>
2.  <span data-ttu-id="539dd-126">Erstellen Sie ein neues Mac-Handle durch Aufrufen von **Macinit**.</span><span class="sxs-lookup"><span data-stu-id="539dd-126">Create a new MAC handle by calling **MACInit**.</span></span>
3.  <span data-ttu-id="539dd-127">Fügen Sie ein Datenelement hinzu, das im handle signiert werden soll, indem Sie **macupdate** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="539dd-127">Add a piece of data to be signed to the handle by calling **MACUpdate**.</span></span> <span data-ttu-id="539dd-128">Diese Funktion akzeptiert das zuvor erstellte Handle sowie ein Datenelement, das signiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="539dd-128">This function accepts the previously created handle, plus a piece of data that must be signed.</span></span>
4.  <span data-ttu-id="539dd-129">Wiederholen Sie Schritt 3 mit jedem weiteren Datenelement, das signiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="539dd-129">Repeat step 3 with each additional piece of data that must be signed.</span></span> <span data-ttu-id="539dd-130">Es spielt keine Rolle, in welcher Reihenfolge Daten dem Mac hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="539dd-130">It does not matter in what order data is added to the MAC.</span></span>
5.  <span data-ttu-id="539dd-131">Kopieren Sie den Mac aus dem Handle in einen neuen Byte Puffer, indem Sie **macfinal** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="539dd-131">Copy the MAC from the handle to a new byte buffer by calling **MACFinal**.</span></span> <span data-ttu-id="539dd-132">Diese Funktion akzeptiert das Mac-Handle und einen Puffer, den Sie zuordnen, und kopiert den Mac aus dem Handle in den bereitgestellten Puffer.</span><span class="sxs-lookup"><span data-stu-id="539dd-132">This function accepts the MAC handle and a buffer that you allocate, and copies the MAC from the handle into the provided buffer.</span></span>

<span data-ttu-id="539dd-133">Beim Durchführen der Mac-Authentifizierung ist es wichtig, dass sowohl der Absender als auch der Empfänger die gleichen Daten auf dem Mac ablegen.</span><span class="sxs-lookup"><span data-stu-id="539dd-133">When performing MAC authentication, it is important that both the sender and the receiver are putting the same data into the MAC.</span></span> <span data-ttu-id="539dd-134">Für die Anwendungsmethoden, die einen Mac bereitstellen, sind normalerweise alle Parameter im Mac-Wert enthalten (mit Ausnahme des Mac selbst).</span><span class="sxs-lookup"><span data-stu-id="539dd-134">For the application methods that provide a MAC, typically all parameters are included in the MAC value (except for the MAC itself, of course).</span></span> <span data-ttu-id="539dd-135">Stellen Sie sich beispielsweise die **iwmdmoperation:: transferobjectdata** -Methode vor:</span><span class="sxs-lookup"><span data-stu-id="539dd-135">For example, consider the **IWMDMOperation::TransferObjectData** method:</span></span>

`HRESULT TransferObjectData(BYTE* pData, DWORD* pdwSize, BYTE[WMDM_MAC_LENGTH] abMac);`

<span data-ttu-id="539dd-136">Bei dieser Methode würde der Mac *pData* und *pdwSize* enthalten.</span><span class="sxs-lookup"><span data-stu-id="539dd-136">In this method, the MAC would include *pData* and *pdwSize*.</span></span> <span data-ttu-id="539dd-137">Wenn Sie nicht beide Parameter einschließen, entspricht der von Ihnen erstellte Mac nicht dem Mac, der an *abmac* übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="539dd-137">If you do not include both the parameters, the MAC you create will not match the MAC passed to *abMac*.</span></span> <span data-ttu-id="539dd-138">Ein Dienstanbieter muss sicherstellen, dass alle erforderlichen Parameter in der Anwendungsmethode in den Mac-Wert eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="539dd-138">A service provider must be sure to put all the required parameters in the application method into the MAC value.</span></span>

<span data-ttu-id="539dd-139">Der folgende C++-Code veranschaulicht das Erstellen eines Macs in der Implementierung eines Dienstanbieters von [**imdspstorageglobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber).</span><span class="sxs-lookup"><span data-stu-id="539dd-139">The following C++ code demonstrates creating a MAC in a service provider's implementation of [**IMDSPStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber).</span></span>


```C++
HRESULT CMyDevice::GetSerialNumber(
    PWMDMID pSerialNumber, 
    BYTE abMac[WMDM_MAC_LENGTH])
{
    HRESULT hr;

    // g_pSecureChannelServer is a global CSecureChannelServer object
    // created earlier.

    // Standard check that the CSecureChannelServer was authenticated previously.
    if ( !(g_pSecureChannelServer->fIsAuthenticated()) )
    {
        return WMDM_E_NOTCERTIFIED;
    }

    // Call a helper function to get the device serial number.
    hr = UtilGetSerialNumber(m_wcsName, pSerialNumber, TRUE);
    if(hr == HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED))
    {
        hr = WMDM_E_NOTSUPPORTED;
    }

    if(hr == S_OK)
    {
        // Create the MAC handle.
        HMAC hMAC;
        hr = g_pSecureChannelServer->MACInit(&hMAC);
        if(FAILED(hr))
            return hr;

        // Add the serial number to the MAC.
        g_pSecureChannelServer->MACUpdate(hMAC, (BYTE*)(pSerialNumber), sizeof(WMDMID));
        if(FAILED(hr))
            return hr;

        // Get the created MAC value from the handle.
        g_pSecureChannelServer->MACFinal(hMAC, abMac);
        if(FAILED(hr))
            return hr;
    }

    return hr;
}
```



<span data-ttu-id="539dd-140">Der Empfänger (in der Regel die Anwendung):</span><span class="sxs-lookup"><span data-stu-id="539dd-140">The receiver (typically the application):</span></span>

<span data-ttu-id="539dd-141">Wenn der Empfänger die [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) -Schnittstelle nicht implementiert hat, sollte er die gleichen Schritte wie der Absender ausführen und dann die beiden Mac-Werte vergleichen.</span><span class="sxs-lookup"><span data-stu-id="539dd-141">If the receiver has not implemented the [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) interface, it should perform the same steps as the sender, and then compare the two MAC values.</span></span> <span data-ttu-id="539dd-142">Im folgenden C++-Codebeispiel wird gezeigt, wie eine Anwendung den in einem [**callmdmstorageglobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) empfangenen Mac überprüft, um sicherzustellen, dass die Seriennummer bei der Übertragung nicht manipuliert wurde.</span><span class="sxs-lookup"><span data-stu-id="539dd-142">The following C++ code example shows how an application would check the MAC received in a call to [**IWMDMStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) to ensure that the serial number was not tampered with in transit.</span></span>


```C++
//
// Get and verify the serial number.
//
WMDMID serialNumber;
BYTE receivedMAC[WMDM_MAC_LENGTH];
hr = pIWMDMDevice->GetSerialNumber(&serialNumber, receivedMAC);

// Check the MAC to guarantee the serial number has not been tampered with.
if (hr == S_OK)
{
    // Initialize a MAC handle, 
    // add all parameters to the MAC,
    // and retrieve the calculated MAC value.
    // m_pSAC is a global CSecureChannelClient object created earlier.
    HMAC hMAC;
    BYTE calculatedMAC[WMDM_MAC_LENGTH];
    hr = m_pSAC->MACInit(&hMAC);
    if(FAILED(hr))
        return hr;

    hr = m_pSAC->MACUpdate(hMAC, (BYTE*)(&serialNumber), sizeof(serialNumber));
    if(FAILED(hr))
        return hr;

    hr = m_pSAC->MACFinal(hMAC, (BYTE*)calculatedMAC);
    if(FAILED(hr))
        return hr;

    // If the two MAC values match, the MAC is authentic. 
    if (memcmp(calculatedMAC, receivedMAC, sizeof(calculatedMAC)) == 0)
    {
        // The MAC is authentic; print the serial number.
        CHAR* serialNumberBuffer = 
            new CHAR[serialNumber.SerialNumberLength + 1];
        ZeroMemory(serialNumberBuffer, 
            (serialNumber.SerialNumberLength + 1) * sizeof(CHAR));
        memcpy(serialNumberBuffer, serialNumber.pID, 
            serialNumber.SerialNumberLength * sizeof(CHAR));
        // TODO: Display the serial number.
        delete serialNumberBuffer;
    }
    else
    {
        // TODO: Display a message indicating that the serial number MAC 
        // does not match.
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="539dd-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="539dd-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="539dd-144">**Verwenden sicherer authentifizierter Kanäle**</span><span class="sxs-lookup"><span data-stu-id="539dd-144">**Using Secure Authenticated Channels**</span></span>](using-secure-authenticated-channels.md)
</dt> </dl>

 

 




