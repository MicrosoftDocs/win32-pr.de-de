---
title: Verschlüsselung und Entschlüsselung
description: Verschlüsselung und Entschlüsselung
ms.assetid: 6aef4138-0391-4edd-b4fc-d6d0ec3c735b
keywords:
- Windows Medien Geräte-Manager,Verschlüsselung
- Geräte-Manager,Verschlüsselung
- Desktopanwendungen, Verschlüsselung
- Dienstanbieter,Verschlüsselung
- Programmierhandbuch,Verschlüsselung
- Verschlüsselung
- Windows Medien Geräte-Manager,Entschlüsselung
- Geräte-Manager,Entschlüsselung
- Desktopanwendungen,Entschlüsselung
- Dienstanbieter,Entschlüsselung
- Programmierhandbuch,Entschlüsselung
- Entschlüsselung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c154910709007e502c1505fc6fc3274665942c9eabe8e24de5b30fe932d813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584668"
---
# <a name="encryption-and-decryption"></a>Verschlüsselung und Entschlüsselung

Windows Medien Geräte-Manager erfordert die Verschlüsselung von Dateien, die zwischen dem Dienstanbieter und der Anwendung gesendet werden. Dafür können Sie zwei Methoden verwenden:

-   Wenn der Dienstanbieter nur [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) und [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)unterstützt, müssen die Daten von der Anwendung und dem Dienstanbieter mithilfe der [Methoden CSecureChannelClient](csecurechannelclient-class.md) bzw. [CSecureChannelServer](csecurechannelserver-class.md) verschlüsselt und entschlüsselt werden.
-   Wenn der Dienstanbieter [**IMDSPObject2::ReadOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) und [**IMDSPObject2::WriteOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel)unterstützt, kann Ihre Anwendung kostspielige sichere Kanalnachrichtenauthentifizierung vermeiden. (Der sichere Kanal wird beibehalten, sodass Legacydienstanbieter, die [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) nicht implementieren, weiterhin funktionieren können.)

Die Verschlüsselungsanforderung verhindert, dass schädliche Anwendungen Daten abrufen, die zwischen Softwarekomponenten übergeben werden, und schützt auch die Integrität der Daten, die an das Gerät oder vom Gerät gesendet werden.

Die folgenden drei Methoden erfordern eine Verschlüsselung oder Entschlüsselung.



| Methode                                                                          | BESCHREIBUNG                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMDMOperation::TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) | (Anwendung) Verschlüsselung oder Entschlüsselung, je nachdem, ob die Anwendung Daten sendet oder empfängt. |
| [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)                                   | (Dienstanbieter) Verschlüsselung.                                                                             |
| [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)                                 | (Dienstanbieter) Entschlüsselung.                                                                             |



 

Die Verschlüsselung und Entschlüsselung erfolgt jeweils durch einzelne Methodenaufrufe. Die Verschlüsselung erfolgt durch [**CSecureChannelClient::EncryptParam**](/previous-versions/bb231587(v=vs.85)) für Anwendungen oder durch [**CSecureChannelServer::EncryptParam**](/previous-versions/ms868509(v=msdn.10)) für Dienstanbieter. Die Entschlüsselung erfolgt durch [**CSecureChannelClient::D ecryptParam**](/previous-versions/bb231586(v=vs.85)) für Anwendungen oder [**CSecureChannelServer::D ecryptParam**](/previous-versions/bb231598(v=vs.85)) für Dienstanbieter. Die Parameter sind zwischen der Client- und der Servermethode identisch.

Die folgenden Schritte zeigen, wie Daten verschlüsselt und entschlüsselt werden. (Diese Schritte sind nur wichtig, wenn Ihre Anwendung mit einem Legacy-Dienstanbieter kommuniziert, der [IWMDMOperation3::TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel)nicht implementiert.)

**Verschlüsselung**

1.  Erstellen Sie den MAC-Schlüssel für die verschlüsselten Daten, wie unter [Nachrichtenauthentifizierung](message-authentication.md)beschrieben.
2.  Rufen Sie **EncryptParam** mit den zu verschlüsselnden Daten auf, um eine verschlüsselungsbasierte Verschlüsselung durchzuführen.

Im folgenden Codebeispiel wird die Implementierung von [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)eines Dienstanbieters veranschaulicht. Diese Methode erstellt den MAC-Schlüssel mithilfe der Daten zum Verschlüsseln und der Größe der Daten und sendet beide an die Anwendung.


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

1.  Rufen Sie **DecryptParam** mit den zu verschlüsselnden Daten auf, um eine direkte Entschlüsselung durchzuführen.
2.  Überprüfen Sie den MAC-Schlüssel für die entschlüsselten Daten, wie unter [Nachrichtenauthentifizierung](message-authentication.md)beschrieben.

Im folgenden Codebeispiel wird die Implementierung von [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)durch einen Dienstanbieter veranschaulicht. Diese Methode erstellt den MAC-Schlüssel mithilfe der Daten zum Verschlüsseln und der Größe der Daten und sendet beide an die Anwendung.


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

[**Verwenden von sicheren authentifizierten Kanälen**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 