---
description: Zertifikatsperrlisten
ms.assetid: 146e7e4a-4281-4f5c-8346-d6c0d5f5442f
title: Zertifikatsperrlisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b51ddee9f77b147d69b8895b3335d41e041da7f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343132"
---
# <a name="certificate-revocation-lists"></a>Zertifikatsperrlisten

In diesem Thema wird beschrieben, wie Sie die Zertifikat Sperr Liste (CRL) für widerrufene Treiber bei Verwendung des Certified Output Protection-Protokolls (COPP) untersuchen.

Die Zertifikat Sperr Liste enthält Digests von gesperrten Zertifikaten und kann nur von Microsoft bereitgestellt und signiert werden. Die CRL wird über Digital Rights Management (DRM)-Lizenzen verteilt. Die CRL kann alle Zertifikate in der Zertifikat Kette des Treibers widerrufen. Wenn ein Zertifikat in der Kette widerrufen wird, werden dieses Zertifikat und alle in der Kette untergeordneten Zertifikate ebenfalls gesperrt.

Zum erhalten der CRL muss die Anwendung das Windows Media-Format SDK, Version 9 oder höher, verwenden und die folgenden Schritte ausführen:

1.  Rufen Sie **wmkreatereader** auf, um das Windows Media Format SDK Reader-Objekt zu erstellen.
2.  Fragen Sie das Reader-Objekt für die **iwmdrmreader** -Schnittstelle ab.
3.  Rufen Sie **iwmdrmreader:: getdrmproperty** mit dem Wert g \_ wszwmdrmnet- \_ Widerruf auf, um die CRL abzurufen. Sie müssen diese Methode zweimal ausführen: einmal, um die Größe des zuzuordnenden Puffers abzurufen, und einmal, um den Puffer zu füllen. Der zweite-Rückruf gibt eine Zeichenfolge zurück, die die CRL enthält. Die gesamte Zeichenfolge ist Base-64-codiert.
4.  Decodieren Sie die Base-64-codierte Zeichenfolge. Hierfür können Sie die **cryptstringto Binary** -Funktion verwenden. Diese Funktion ist Teil von CryptoAPI.

> [!Note]  
> Um die **iwmdrmreader** -Schnittstelle verwenden zu können, müssen Sie eine statische DRM-Bibliothek von Microsoft abrufen und Ihre Anwendung mit dieser Bibliotheksdatei verknüpfen. Weitere Informationen finden Sie im Thema zum Abrufen der erforderlichen DRM-Bibliothek in der Dokumentation zum Windows Media-Format-SDK.

 

Wenn die Zertifikat Sperr Liste nicht auf dem Computer des Benutzers vorhanden ist, gibt die **getdrmproperty** -Methode die \_ \_ \_ nicht unterstützte Eigenschaft "NS E DRM" zurück \_ . Derzeit besteht die einzige Möglichkeit zum Abrufen der CRL darin, eine DRM-Lizenz zu erwerben.

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



Anschließend muss die Anwendung überprüfen, ob die CRL gültig ist. Vergewissern Sie sich hierzu, dass das Zertifikat der CRL, das Teil der Zertifikat Sperr Liste ist, direkt vom Microsoft-Stamm Zertifikat signiert ist und dass der Wert des signcrl-Elements auf 1 festgelegt ist. Überprüfen Sie außerdem die Signatur der CRL.

Nachdem die CRL überprüft wurde, kann Sie von der Anwendung gespeichert werden. Die CRL-Versionsnummer sollte vor dem Speichern auch geprüft werden, damit die Anwendung immer die neueste Version speichert.

Die CRL weist das folgende Format auf.



| `Section`            | Contents                                                             |
|--------------------|----------------------------------------------------------------------|
| Header             | 32-Bit-CRL version32-Bit-Anzahl von Einträgen                           |
| Sperr Einträge | Mehrere 160-Bit-Sperr Einträge                                  |
| Zertifikat        | 32-Bit-Zertifikat mit Längen variabler Länge                 |
| Signatur          | 8-Bit-Signatur type16-Bit-Signatur Längen variabler Länge |



 

> [!Note]  
> Alle ganzzahligen Werte sind unsigniert und werden in der Big-Endian-Notation (netzwerkbyte Reihenfolge) dargestellt.

 

CRL-Abschnitts Beschreibungen

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header
</dt> <dd>

Der-Header enthält die Versionsnummer der CRL und die Anzahl der Sperr Einträge in der CRL. Eine CRL kann NULL oder mehr Einträge enthalten.

</dd> <dt>

<span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>Sperr Einträge
</dt> <dd>

Jeder Sperr Eintrag ist der 160-Bit-Digest eines gesperrten Zertifikats. Vergleichen Sie diesen Digest mit dem DigestValue-Element innerhalb des Zertifikats.

</dd> <dt>

<span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>Stellt
</dt> <dd>

Der Abschnitt Zertifikat enthält einen 32-Bit-Wert, der die Länge (in Bytes) des XML-Zertifikats und seiner Zertifikat Kette sowie ein Bytearray angibt, das sowohl das XML-Zertifikat der Zertifizierungsstelle als auch die Zertifikat Kette enthält, die Microsoft als Stamm hat. Das Zertifikat muss von einer Zertifizierungsstelle signiert werden, die über die Berechtigung zum Ausstellen von CRLs verfügt.

> [!Note]  
> Das Zertifikat darf nicht auf Null enden.

 

</dd> <dt>

<span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Unter
</dt> <dd>

Der Signatur Abschnitt enthält den Typ und die Länge der Signatur sowie die digitale Signatur selbst. Der 8-Bit-Typ wird auf 2 festgelegt, um anzugeben, dass SHA-1 mit 1024-Bit-RSA-Verschlüsselung verwendet wird. Die Länge ist ein 16-Bit-Wert, der die Länge der digitalen Signatur in Bytes enthält. Die digitale Signatur wird über alle vorherigen Abschnitte der CRL berechnet.

Die Signatur wird mit dem digitalen rsassa-PSS-Signatur Schema berechnet, das in PKCS \# 1 (Version 2,1) definiert ist. Bei der Hash Funktion handelt es sich um SHA-1, der in Federal Information Processing Standard (FI) 180-2 definiert ist, und die Masken Generierungs Funktion ist MGF1, die in Abschnitt B. 2.1 in PKCS \# 1 (Version 2,1) definiert ist. Der RSASP1-und der RSAVP1-Vorgang verwenden RSA mit einem 1024-Bit-Modulo mit einem Verifizierungs Exponent von 65537.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Certified Output Protection-Protokolls (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



