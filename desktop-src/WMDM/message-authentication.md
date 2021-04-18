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
# <a name="message-authentication"></a>Nachrichten Authentifizierung

Die Nachrichten Authentifizierung ist ein Prozess, mit dem Anwendungen und Dienstanbieter überprüfen können, ob die zwischen Ihnen übergebenen Daten nicht manipuliert wurden. Mithilfe von Windows Media Device Manager können Anwendungen und Dienstanbieter die Nachrichten Authentifizierung mithilfe von Nachrichten Authentifizierungscodes (Macs) durchführen. Die Mac-Authentifizierung funktioniert wie folgt:

Der Daten Absender, normalerweise der Dienstanbieter, übergibt ein oder mehrere Datenelemente über eine unidirektionale Kryptografiefunktion, die für alle Daten eine einzige Signatur, den Mac, erzeugt. Anschließend sendet der Absender alle signierten Daten zusammen mit dem Mac an den Empfänger (in der Regel die Anwendung). Der Empfänger übergibt die Daten über dieselbe Kryptografiefunktion, um einen Mac zu generieren, und vergleicht ihn mit dem gesendeten Mac. Wenn der Mac übereinstimmt, wurden die Daten nicht geändert.

Um die Mac-Authentifizierung auszuführen, erfordert die Anwendung oder der Dienstanbieter einen Verschlüsselungsschlüssel und ein entsprechendes Zertifikat. Informationen dazu, wo Sie diese erhalten, finden Sie unter [Tools für die Entwicklung](tools-for-development.md).

In den folgenden Schritten wird beschrieben, wie Daten vom Absender signiert und später vom Empfänger geprüft werden. In Windows Media Device Manager verwendet der Dienstanbieter die [csecurechannelserver](csecurechannelserver-class.md) -Klasse, um Macs zu generieren, und die Anwendung verwendet die [csecurechannelclient](csecurechannelclient-class.md) -Klasse. Beide Klassen stellen identische Funktionen mit identischen Parametern bereit, sodass die folgenden Schritte für beide Klassen gelten.

Der Absender (in der Regel der Dienstanbieter):

1.  Die zu Signier enden Daten.
2.  Erstellen Sie ein neues Mac-Handle durch Aufrufen von **Macinit**.
3.  Fügen Sie ein Datenelement hinzu, das im handle signiert werden soll, indem Sie **macupdate** aufrufen. Diese Funktion akzeptiert das zuvor erstellte Handle sowie ein Datenelement, das signiert werden muss.
4.  Wiederholen Sie Schritt 3 mit jedem weiteren Datenelement, das signiert werden muss. Es spielt keine Rolle, in welcher Reihenfolge Daten dem Mac hinzugefügt werden.
5.  Kopieren Sie den Mac aus dem Handle in einen neuen Byte Puffer, indem Sie **macfinal** aufrufen. Diese Funktion akzeptiert das Mac-Handle und einen Puffer, den Sie zuordnen, und kopiert den Mac aus dem Handle in den bereitgestellten Puffer.

Beim Durchführen der Mac-Authentifizierung ist es wichtig, dass sowohl der Absender als auch der Empfänger die gleichen Daten auf dem Mac ablegen. Für die Anwendungsmethoden, die einen Mac bereitstellen, sind normalerweise alle Parameter im Mac-Wert enthalten (mit Ausnahme des Mac selbst). Stellen Sie sich beispielsweise die **iwmdmoperation:: transferobjectdata** -Methode vor:

`HRESULT TransferObjectData(BYTE* pData, DWORD* pdwSize, BYTE[WMDM_MAC_LENGTH] abMac);`

Bei dieser Methode würde der Mac *pData* und *pdwSize* enthalten. Wenn Sie nicht beide Parameter einschließen, entspricht der von Ihnen erstellte Mac nicht dem Mac, der an *abmac* übermittelt wurde. Ein Dienstanbieter muss sicherstellen, dass alle erforderlichen Parameter in der Anwendungsmethode in den Mac-Wert eingefügt werden.

Der folgende C++-Code veranschaulicht das Erstellen eines Macs in der Implementierung eines Dienstanbieters von [**imdspstorageglobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber).


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



Der Empfänger (in der Regel die Anwendung):

Wenn der Empfänger die [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) -Schnittstelle nicht implementiert hat, sollte er die gleichen Schritte wie der Absender ausführen und dann die beiden Mac-Werte vergleichen. Im folgenden C++-Codebeispiel wird gezeigt, wie eine Anwendung den in einem [**callmdmstorageglobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) empfangenen Mac überprüft, um sicherzustellen, dass die Seriennummer bei der Übertragung nicht manipuliert wurde.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden sicherer authentifizierter Kanäle**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 




