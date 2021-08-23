---
description: Zertifikatsperrlisten
ms.assetid: 146e7e4a-4281-4f5c-8346-d6c0d5f5442f
title: Zertifikatsperrlisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 703bb8813e95ebfe07783fa07284b2ae7dad0df2ff8a9205234ee9a4514192d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537304"
---
# <a name="certificate-revocation-lists"></a>Zertifikatsperrlisten

In diesem Thema wird beschrieben, wie die Zertifikatsperrliste (Certificate Revocation List, CRL) bei Verwendung des Certified Output Protection Protocol (COPP) auf gesperrte Treiber untersucht wird.

Die Zertifikatsperrliste enthält Digests gesperrter Zertifikate und kann nur von Microsoft bereitgestellt und signiert werden. Die CRL wird über DRM-Lizenzen (Digital Rights Management) verteilt. Die Zertifikatsperrliste kann jedes Zertifikat in der Zertifikatkette des Treibers widerrufen. Wenn ein Zertifikat in der Kette widerrufen wird, werden dieses Zertifikat und alle darunter liegenden Zertifikate in der Kette ebenfalls widerrufen.

Um die CRL zu erhalten, muss die Anwendung das Windows Media Format SDK, Version 9 oder höher, verwenden und die folgenden Schritte ausführen:

1.  Rufen Sie **WMCreateReader** auf, um das Readerobjekt Windows Media Format SDK zu erstellen.
2.  Fragen Sie das Readerobjekt nach der **IWMDRMReader-Schnittstelle** ab.
3.  Rufen Sie **IWMDRMReader::GetDRMProperty** mit dem Wert g \_ wszWMDRMNet \_ Revocation auf, um die Zertifikatsperrliste abzurufen. Sie müssen diese Methode zweimal aufrufen: Einmal, um die Größe des zuzuordnenden Puffers abzurufen, und einmal, um den Puffer zu füllen. Der zweite Aufruf gibt eine Zeichenfolge zurück, die die CRL enthält. Die gesamte Zeichenfolge ist base64-codiert.
4.  Decodieren Sie die Base64-codierte Zeichenfolge. Hierzu können Sie die **CryptStringToBinary-Funktion** verwenden. Diese Funktion ist Teil von CryptoAPI.

> [!Note]  
> Um die **IWMDRMReader-Schnittstelle** zu verwenden, müssen Sie eine statische DRM-Bibliothek von Microsoft abrufen und Ihre Anwendung mit dieser Bibliotheksdatei verknüpfen. Weitere Informationen finden Sie im Thema "Abrufen der erforderlichen DRM-Bibliothek" in der Windows Media Format SDK-Dokumentation.

 

Wenn die CRL auf dem Computer des Benutzers nicht vorhanden ist, gibt die **GetDRMProperty-Methode** NS \_ E \_ DRM \_ UNSUPPORTED \_ PROPERTY zurück. Derzeit besteht die einzige Möglichkeit zum Abrufen der CRL darin, eine DRM-Lizenz zu erwerben.

Der folgende Code zeigt eine Funktion, die die CRL zurückgibt:


```C++
////////////////////////////////////////////////////////////////////////
//  Name: GetCRL
//  Description: Gets the certificate revocation list (CRL).
//
//  ppBuffer: Receives a pointer to the buffer that contains the CRL.
//  pcbBuffer: Receives the size of the buffer returned in ppBuffer.
//
//  The caller must free the returned buffer by calling CoTaskMemFree.
////////////////////////////////////////////////////////////////////////
HRESULT GetCRL(BYTE **ppBuffer, DWORD *pcbBuffer)
{
    IWMReader *pReader = NULL;
    IWMDRMReader *pDrmReader = NULL;
    HRESULT hr = S_OK;

    // DRM attribute data.
    WORD cbAttributeLength = 0;
    BYTE *pDataBase64 = NULL;
    WMT_ATTR_DATATYPE type;

    // Buffer for base-64 decoded CRL.
    BYTE *pCRL = NULL;
    DWORD cbCRL = 0;

    // Create the WMReader object.
    hr = WMCreateReader(NULL, 0, &pReader);

    // Query for the IWMDRMReader interface.
    if (SUCCEEDED(hr))
    {
        hr = pReader->QueryInterface(
            IID_IWMDRMReader, (void**)&pDrmReader);
    }

    // Call GetDRMProperty once to find the size of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pDrmReader->GetDRMProperty(
            g_wszWMDRMNET_Revocation,
            &type,
            NULL,
            &cbAttributeLength
            );
    }

    // Allocate a buffer.
    if (SUCCEEDED(hr))
    {
        pDataBase64 = (BYTE*)CoTaskMemAlloc(cbAttributeLength);
        if (pDataBase64 == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Call GetDRMProperty again to get the property.
    if (SUCCEEDED(hr))
    {
        hr = pDrmReader->GetDRMProperty(
            g_wszWMDRMNET_Revocation,
            &type,
            pDataBase64,
            &cbAttributeLength
            );
    }

    // Find the size of the buffer for the base-64 decoding.
    if (SUCCEEDED(hr))
    {
        BOOL bResult = CryptStringToBinary(
            (WCHAR*)pDataBase64,    // Base-64 encoded string.
            0,                      // Null-terminated.
            CRYPT_STRING_BASE64,    
            NULL,                   // Buffer (NULL).
            &cbCRL,                 // Receives the size of the buffer. 
            NULL, NULL              // Optional.
            );
        if (!bResult)
        {
            hr = __HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // Allocate a buffer for the CRL.
    if (SUCCEEDED(hr))
    {
        pCRL = (BYTE*)CoTaskMemAlloc(cbCRL);
        if (pCRL == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Base-64 decode to get the CRL.
    if (SUCCEEDED(hr))
    {
        BOOL bResult = CryptStringToBinary(
            (WCHAR*)pDataBase64,    // Base-64 encoded string.
            0,                      // Null-terminated.
            CRYPT_STRING_BASE64,    
            pCRL,                   // Buffer.
            &cbCRL,                 // Receives the size of the buffer. 
            NULL, NULL              // Optional.
            );
        if (!bResult)
        {
            hr = __HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // Return the buffer to the caller. Caller must free the buffer.
    if (SUCCEEDED(hr))
    {
        *ppBuffer = pCRL;
        *pcbBuffer = cbCRL;
    }
    else
    {
        CoTaskMemFree(pCRL);
    }

    CoTaskMemFree(pDataBase64);
    SAFE_RELEASE(pReader);
    SAFE_RELEASE(pDrmReader);
    return hr;
}
```



Als Nächstes muss die Anwendung überprüfen, ob die CRL gültig ist. Stellen Sie hierzu sicher, dass das Zertifikat der Zertifikatsperrliste, das Teil der Zertifikatsperrliste ist, direkt vom Microsoft-Stammzertifikat signiert ist und der Wert des SignCRL-Elements auf 1 festgelegt ist. Überprüfen Sie außerdem die Signatur der Sperrliste.

Nachdem die Sperrliste überprüft wurde, kann sie von der Anwendung gespeichert werden. Die CRL-Versionsnummer sollte auch vor dem Speichern überprüft werden, damit die Anwendung immer die neueste Version speichert.

Die CRL weist das folgende Format auf.



| `Section`            | Contents                                                             |
|--------------------|----------------------------------------------------------------------|
| Header             | 32-Bit-CRL-Version32-Bit-Anzahl von Einträgen                           |
| Sperreinträge | Mehrere 160-Bit-Sperreinträge                                  |
| Zertifikat        | 32-Bit-ZertifikatlängeVariable-Längenzertifikat                 |
| Signatur          | 8-Bit-Signaturtyp16-Bit-SignaturlängeVariable-Längensignatur |



 

> [!Note]  
> Alle ganzzahligen Werte sind ohne Vorzeichen und werden in Big-Endian-Notation (Netzwerk-Bytereihenfolge) dargestellt.

 

CRL-Abschnittsbeschreibungen

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header
</dt> <dd>

Der Header enthält die Versionsnummer der Zertifikatsperrliste und die Anzahl der Sperreinträge in der Zertifikatsperrliste. Eine Sperrliste kann 0 (null) oder mehr Einträge enthalten.

</dd> <dt>

<span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>Sperreinträge
</dt> <dd>

Jeder Sperreintrag ist der 160-Bit-Digest eines gesperrten Zertifikats. Vergleichen Sie diesen Digest mit dem DigestValue-Element innerhalb des Zertifikats.

</dd> <dt>

<span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>Zertifikat
</dt> <dd>

Der Abschnitt certificate enthält einen 32-Bit-Wert, der die Länge (in Bytes) des XML-Zertifikats und seiner Zertifikatkette sowie ein Bytearray angibt, das sowohl das XML-Zertifikat der Zertifizierungsstelle (Certificate Authority, CA) als auch die Zertifikatkette mit Microsoft als Stamm enthält. Das Zertifikat muss von einer Zertifizierungsstelle signiert werden, die über die Berechtigung zum Ausstellen von CRLs verfügt.

> [!Note]  
> Das Zertifikat darf nicht NULL-terminiert sein.

 

</dd> <dt>

<span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signatur
</dt> <dd>

Der Signaturabschnitt enthält den Signaturtyp und die Länge sowie die digitale Signatur selbst. Der 8-Bit-Typ ist auf 2 festgelegt, um anzugeben, dass SHA-1 mit 1024-Bit-RSA-Verschlüsselung verwendet wird. Die Länge ist ein 16-Bit-Wert, der die Länge der digitalen Signatur in Bytes enthält. Die digitale Signatur wird für alle vorherigen Abschnitte der Sperrliste berechnet.

Die Signatur wird mithilfe des in PKCS \# 1 (Version 2.1) definierten Schemas für digitale Signaturen RSATUR-PSS berechnet. Die Hashfunktion ist SHA-1, die in Federal Information Processing Standard (FIPS) 180-2 definiert ist, und die Maskengenerierungsfunktion ist MGF1, die in Abschnitt B.2.1 in PKCS \# 1 (Version 2.1) definiert ist. Die RSASP1- und RSAVP1-Vorgänge verwenden RSA mit einem 1024-Bit-Modulus mit einem Überprüfungs exponenten 65537.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Certified Output Protection Protocol (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



