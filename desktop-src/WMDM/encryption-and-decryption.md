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
# <a name="encryption-and-decryption"></a>Verschlüsselung und Entschlüsselung

Windows Media Device Manager erfordert die Verschlüsselung von Dateien, die zwischen dem Dienstanbieter und der Anwendung gesendet werden. Dafür können Sie zwei Methoden verwenden:

-   Wenn der Dienstanbieter nur [**imdspobject:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) und [**imdspobject:: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)unterstützt, müssen die Daten von der Anwendung und dem Dienstanbieter mithilfe der Methoden [csecurechannelclient](csecurechannelclient-class.md) bzw. [csecurechannelserver](csecurechannelserver-class.md) verschlüsselt und entschlüsselt werden.
-   Wenn der Dienstanbieter [**IMDSPObject2:: Read onclearchannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) und [**IMDSPObject2:: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel)Service Provider unterstützt, kann die Anwendung eine teure sichere Kanalnachrichten Authentifizierung vermeiden. (Der sichere Kanal wird beibehalten, sodass Legacy-Dienstanbieter, die [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) nicht implementieren, weiterhin funktionieren können.)

Die Verschlüsselungs Anforderung verhindert, dass böswillige Anwendungen Daten abrufen, die zwischen Softwarekomponenten übermittelt werden, und schützt außerdem die Integrität der Daten, die an das Gerät gesendet werden.

Die folgenden drei Methoden müssen verschlüsselt oder entschlüsselt werden.



| Methode                                                                          | BESCHREIBUNG                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Iwmdmoperation:: transferobjectdata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) | Asyl Verschlüsselung oder Entschlüsselung, abhängig davon, ob die Anwendung Daten sendet oder empfängt. |
| [**Imdspobject:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)                                   | (Dienstanbieter) Verschlüsselungs.                                                                             |
| [**Imdspobject:: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)                                 | (Dienstanbieter) Entschlüsselung.                                                                             |



 

Verschlüsselung und Entschlüsselung werden von einzelnen Methoden aufrufen durchgeführt. Die Verschlüsselung erfolgt durch [**csecurechannelclient:: verschlüsseltparam**](/previous-versions/bb231587(v=vs.85)) für Anwendungen oder durch [**csecurechannelserver:: verschlüsseltparam**](/previous-versions/ms868509(v=msdn.10)) für Dienstanbieter. Die Entschlüsselung erfolgt durch [**csecurechannelclient::D ecryptparam**](/previous-versions/bb231586(v=vs.85)) für Anwendungen oder [**csecurechannelserver::D ecryptparam**](/previous-versions/bb231598(v=vs.85)) für Dienstanbieter. Die Parameter sind zwischen den Client-und Server Methoden identisch.

In den folgenden Schritten wird gezeigt, wie Daten verschlüsselt und entschlüsselt werden. (Diese Schritte sind nur dann wichtig, wenn Ihre Anwendung mit einem Legacy Dienstanbieter kommuniziert, der [IWMDMOperation3:: transferobjectdataonclearchannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel)nicht implementiert.)

**Verschlüsselung**

1.  Erstellen Sie den Mac-Schlüssel für die verschlüsselten Daten, wie in [Nachrichten Authentifizierung](message-authentication.md)beschrieben.
2.  Nennen Sie **verschlüsseltparam** mit den zu verschlüsselnden Daten, um eine direkte Verschlüsselung auszuführen.

Im folgenden Codebeispiel wird die Implementierung von [**imdspobject:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)eines Dienstanbieters veranschaulicht. Diese Methode erstellt den Mac-Schlüssel mithilfe der zu verschlüsselnden Daten und der Größe der Daten und sendet beide an die Anwendung.


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



**Entschlüsselung**

1.  Wenden Sie **decryptparam** mit den zu verschlüsselnden Daten an, um eine direkte Entschlüsselung auszuführen.
2.  Überprüfen Sie den Mac-Schlüssel für die entschlüsselten Daten, wie in [Nachrichten Authentifizierung](message-authentication.md)beschrieben.

Im folgenden Codebeispiel wird die Implementierung von [**imdspobject:: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)eines Dienstanbieters veranschaulicht. Diese Methode erstellt den Mac-Schlüssel mithilfe der zu verschlüsselnden Daten und der Größe der Daten und sendet beide an die Anwendung.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden sicherer authentifizierter Kanäle**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 