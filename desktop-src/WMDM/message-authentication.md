---
title: Nachrichtenauthentifizierung
description: Nachrichtenauthentifizierung
ms.assetid: 6cb49f6b-e303-4840-9343-9891e75e07a4
keywords:
- Windows Medien Geräte-Manager,Nachrichtenauthentifizierung
- Geräte-Manager,Nachrichtenauthentifizierung
- Desktopanwendungen,Nachrichtenauthentifizierung
- Dienstanbieter,Nachrichtenauthentifizierung
- Programmierhandbuch, Nachrichtenauthentifizierung
- Nachrichtenauthentifizierung
- Nachrichtenauthentifizierungscode (MAC)
- MAC (Nachrichtenauthentifizierungscode)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2921b80d42207bab608c6a8260e6756d3e9f323eab70742acc787ff731ad4b80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584484"
---
# <a name="message-authentication"></a>Nachrichtenauthentifizierung

Nachrichtenauthentifizierung ist ein Prozess, mit dem Anwendungen und Dienstanbieter überprüfen können, ob zwischen ihnen übergebene Daten nicht manipuliert wurden. Windows Media Geräte-Manager ermöglicht Es Anwendungen und Dienstanbietern, die Nachrichtenauthentifizierung mithilfe von Nachrichtenauthentifizierungscodes (Message Authentication Codes, MACs) durchzuführen. So funktioniert die MAC-Authentifizierung:

Der Datensender, in der Regel der Dienstanbieter, übergibt ein oder mehrere Datenteile über eine einfache kryptografische Funktion, die eine einzelne Signatur, den MAC, für alle Daten erzeugt. Der Absender sendet dann alle signierten Daten zusammen mit dem MAC an den Empfänger (in der Regel die Anwendung). Der Empfänger übergibt die Daten über dieselbe kryptografische Funktion, um einen MAC zu generieren, und vergleicht sie mit dem gesendeten MAC. Wenn der MAC entspricht, wurden die Daten nicht geändert.

Für die MAC-Authentifizierung benötigt die Anwendung oder der Dienstanbieter einen Verschlüsselungsschlüssel und ein entsprechendes Zertifikat. Informationen dazu, wo sie zu erhalten sind, finden Sie unter [Tools für die Entwicklung](tools-for-development.md).

In den folgenden Schritten wird beschrieben, wie Daten vom Absender signiert und später vom Empfänger überprüft werden. In Windows Media Geräte-Manager verwendet der Dienstanbieter die [CSecureChannelServer-Klasse,](csecurechannelserver-class.md) um MACs zu generieren, und die Anwendung verwendet die [CSecureChannelClient-Klasse.](csecurechannelclient-class.md) Beide Klassen stellen identische Funktionen mit identischen Parametern zur Verfügung, sodass die folgenden Schritte für beide Klassen gelten.

Der Absender (in der Regel der Dienstanbieter):

1.  Hier erhalten Sie die zu signierten Daten.
2.  Erstellen Sie ein neues MAC-Handle, indem Sie **MACInit aufrufen.**
3.  Fügen Sie ein Datenstück hinzu, das durch Aufrufen von MACUpdate am Handle **signiert werden soll.** Diese Funktion akzeptiert das zuvor erstellte Handle sowie ein Datenstück, das signiert werden muss.
4.  Wiederholen Sie Schritt 3 mit jedem zusätzlichen Datenteil, der signiert werden muss. Es spielt keine Rolle, in welcher Reihenfolge dem MAC Daten hinzugefügt werden.
5.  Kopieren Sie den MAC aus dem Handle in einen neuen Bytepuffer, indem Sie **MACFinal aufrufen.** Diese Funktion akzeptiert das MAC-Handle und einen Puffer, den Sie zuordnen, und kopiert den MAC aus dem Handle in den bereitgestellten Puffer.

Beim Ausführen der MAC-Authentifizierung ist es wichtig, dass sowohl der Absender als auch der Empfänger dieselben Daten auf dem MAC abhören. Für die Anwendungsmethoden, die einen MAC bereitstellen, sind in der Regel alle Parameter im MAC-Wert enthalten (mit Ausnahme des MAC selbst, natürlich). Betrachten Sie beispielsweise die **IWMDMOperation::TransferObjectData-Methode:**

`HRESULT TransferObjectData(BYTE* pData, DWORD* pdwSize, BYTE[WMDM_MAC_LENGTH] abMac);`

In dieser Methode würde der MAC *pData und* *pdwSize enthalten.* Wenn Sie nicht beide Parameter angeben, stimmen die von Ihnen erstellten MAC-Computer nicht mit dem MAC überein, der an *abMac übergeben wurde.* Ein Dienstanbieter muss sicherstellen, dass alle erforderlichen Parameter in der Anwendungsmethode im MAC-Wert gespeichert werden.

Der folgende C++-Code veranschaulicht das Erstellen eines MAC in der Implementierung [**von IMDSPStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)durch einen Dienstanbieter.


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

Wenn der Empfänger die [**IWMDMOperation3-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) nicht implementiert hat, sollte er die gleichen Schritte wie der Absender ausführen und dann die beiden MAC-Werte vergleichen. Das folgende C++-Codebeispiel zeigt, wie eine Anwendung den mac überprüft, der in einem Aufruf von [**IWMDMStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) empfangen wurde, um sicherzustellen, dass die Seriennummer während der Übertragung nicht manipuliert wurde.


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

[**Verwenden von sicheren authentifizierten Kanälen**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 




