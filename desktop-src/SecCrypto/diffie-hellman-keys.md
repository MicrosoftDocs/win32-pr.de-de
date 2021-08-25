---
description: Erläutert das Generieren, Austauschen, Importieren und Exportieren Diffie-Hellman Schlüsseln.
ms.assetid: 623a8c9e-3f6a-470b-be30-dec13342bb90
title: Diffie-Hellman Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4082650b030ab1643b83cb154718176d445c98788b15a7bcadd1db97c30bab7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875500"
---
# <a name="diffie-hellman-keys"></a>Diffie-Hellman Schlüssel

-   [Generieren Diffie-Hellman Schlüsseln](#generating-diffie-hellman-keys)
-   [Austauschen Diffie-Hellman Schlüsseln](#exchanging-diffie-hellman-keys)
-   [Exportieren eines Diffie-Hellman privaten Schlüssels](#exporting-a-diffie-hellman-private-key)
-   [Beispielcode](#example-code)

## <a name="generating-diffie-hellman-keys"></a>Generieren Diffie-Hellman Schlüsseln

Um einen Schlüssel Diffie-Hellman generieren, führen Sie die folgenden Schritte aus:

1.  Rufen Sie die [**CryptAcquireContext-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) auf, um ein Handle für den Microsoft Diffie-Hellman Cryptographic Provider zu erhalten.
2.  Generieren Sie den neuen Schlüssel. Hierfür gibt es zwei Möglichkeiten: CryptoAPI generiert alle neuen Werte für G, P und X oder vorhandene Werte für G und P und generiert einen neuen Wert für X.

    **So generieren Sie den Schlüssel durch Generieren aller neuen Werte**

    1.  Rufen Sie [**die CryptGenKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) auf, und übergeben Sie **entweder CALG DH \_ \_ SF** (store and forward) oder **CALG DH \_ \_ EPHEM** (kurzlebig) im *Algid-Parameter.* Der Schlüssel wird mit neuen Zufallswerten für G und P, einem neu berechneten Wert für X, generiert, und sein Handle wird im *phKey-Parameter* zurückgegeben.
    2.  Der neue Schlüssel ist jetzt einsatzbereit. Die Werte von G und P müssen zusammen mit dem Schlüssel (oder von einer anderen Methode) an den Empfänger gesendet werden, wenn ein [*Schlüsselaustausch verwendet wird.*](../secgloss/e-gly.md)

    **So generieren Sie den Schlüssel mit vordefinierten Werten für G und P**

    1.  Rufen Sie [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) auf, indem Sie **entweder CALG \_ DH \_ SF** (store and forward) oder **CALG DH \_ \_ EPHEM (kurzlebig)** im *Algid-Parameter* und **CRYPT \_ PREGEN** für den *dwFlags-Parameter* übergeben. Ein Schlüsselhand handle wird generiert und im *phKey-Parameter* zurückgegeben.
    2.  Initialisieren Sie [**eine CRYPT \_ DATA \_ BLOB-Struktur**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) mit dem **pbData-Member,** der auf den P-Wert festgelegt ist. Das [*BLOB*](../secgloss/b-gly.md) enthält keine Headerinformationen, und **das pbData-Element** hat [*das Little-Endian-Format.*](../secgloss/l-gly.md)
    3.  Der Wert von P wird festgelegt, indem die [**CryptSetKeyParam-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) aufgerufen wird. Dabei wird das in Schritt a abgerufene Schlüsselhand handle im *hKey-Parameter,* das **KP \_ P-Flag** im *dwParam-Parameter* und ein Zeiger auf die -Struktur übergeben, die den Wert von P im *pbData-Parameter* enthält.
    4.  Initialisieren Sie [**eine CRYPT \_ DATA \_ BLOB-Struktur**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) mit dem **pbData-Member,** der auf den G-Wert festgelegt ist. Das BLOB enthält keine Headerinformationen, und **das pbData-Element** hat das Little-Endian-Format.
    5.  Der Wert von G wird festgelegt, indem die [**CryptSetKeyParam-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) aufgerufen wird. Dabei wird das in Schritt a abgerufene Schlüsselhand handle im *hKey-Parameter,* das **KP \_ G-Flag** im *dwParam-Parameter* und ein Zeiger auf die -Struktur übergeben, die den Wert von G im *pbData-Parameter* enthält.
    6.  Der Wert von X wird generiert, indem die [**CryptSetKeyParam-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) aufgerufen wird, und das in Schritt a abgerufene Schlüsselhand handle im *hKey-Parameter,* das **KP \_ X-Flag** im *dwParam-Parameter* und **NULL** im *pbData-Parameter* übergeben.
    7.  Wenn alle Funktionsaufrufe erfolgreich waren, Diffie-Hellman öffentlichen Schlüssel einsatzbereit.

3.  Wenn der Schlüssel nicht mehr benötigt wird, zerstören Sie ihn, indem Sie das Schlüsselhandler an die [**CryptDestroyKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) übergeben.

Wenn **CALG \_ DH \_ SF** in den vorherigen Prozeduren angegeben wurde, werden die Schlüsselwerte bei jedem Aufruf von [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)im Speicher beibehalten. Die G- und P-Werte können dann mithilfe der [**CryptGetKeyParam-Funktion abgerufen**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) werden. Einige CSPs verfügen möglicherweise über hart codierte G- und P-Werte. In diesem Fall wird **ein NTE \_ FIXEDPARAMETER-Fehler** zurückgegeben, wenn **CryptSetKeyParam** mit **KP \_ G** oder **KP \_ P** aufgerufen wird, die im *dwParam-Parameter angegeben* sind. Wenn **CryptDestroyKey** aufgerufen wird, wird das Handle für den Schlüssel zerstört, aber die Schlüsselwerte werden im CSP beibehalten. Wenn jedoch **CALG \_ DH \_ EPHEM** angegeben wurde, wird das Handle für den Schlüssel zerstört, und alle Werte werden aus dem CSP gelöscht.

## <a name="exchanging-diffie-hellman-keys"></a>Austauschen Diffie-Hellman Schlüsseln

Der Diffie-Hellman-Algorithmus soll es zwei oder mehr Parteien ermöglichen, einen identischen, geheimen Sitzungsschlüssel zu erstellen und gemeinsam zu nutzen, indem Informationen über ein nicht sicheres Netzwerk gemeinsam genutzt werden. Die Informationen, die über das Netzwerk freigegeben werden, sind in Form von konstanten Werten und einem Diffie-Hellman Schlüssel. Der prozess, der von zwei Schlüsselaustausch-Parteien verwendet wird, ist wie folgt:

-   Beide Parteien stimmen den parametern Diffie-Hellman, bei denen es sich um eine Primzahl (P) und eine Generatornummer (G) handelt.
-   Partei 1 sendet ihren Diffie-Hellman öffentlichen Schlüssel an Partei 2.
-   Partei 2 berechnet den geheimen Sitzungsschlüssel anhand der Informationen, die im privaten Schlüssel und im öffentlichen Schlüssel der Partei 1 enthalten sind.
-   Partei 2 sendet ihren Diffie-Hellman öffentlichen Schlüssel an Partei 1.
-   Partei 1 berechnet den geheimen Sitzungsschlüssel anhand der Informationen, die in ihrem privaten Schlüssel und im öffentlichen Schlüssel der Partei 2 enthalten sind.
-   Beide Parteien verfügen nun über denselben Sitzungsschlüssel, der zum Verschlüsseln und Entschlüsseln von Daten verwendet werden kann. Die dafür erforderlichen Schritte werden im folgenden Verfahren gezeigt.

**So bereiten Sie Diffie-Hellman öffentlichen Schlüssel für die Übertragung vor**

1.  Rufen Sie die [**CryptAcquireContext-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) auf, um ein Handle für den Microsoft Diffie-Hellman Cryptographic Provider zu erhalten.
2.  Erstellen Sie Diffie-Hellman Schlüssel, indem Sie die [**CryptGenKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) aufrufen, um einen neuen Schlüssel zu erstellen, oder indem Sie die [**CryptGetUserKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) aufrufen, um einen vorhandenen Schlüssel abzurufen.
3.  Rufen Sie die Größe ab, die zum Speichern des Diffie-Hellman-Schlüsselblobs erforderlich ist, indem Sie [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)aufrufen und **NULL** für den *pbData-Parameter* übergeben. Die erforderliche Größe wird in *pdwDataLen zurückgegeben.*
4.  Ordnen Sie Arbeitsspeicher für das SchlüsselBLOB zu.
5.  Erstellen Sie Diffie-Hellman [](../secgloss/p-gly.md) öffentlichen SchlüsselBLOB, indem Sie die [**CryptExportKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) aufrufen und **PUBLICKEYBLOB** im *dwBlobType-Parameter* und das Handle an den Diffie-Hellman-Schlüssel im *hKey-Parameter* übergeben. Dieser Funktionsaufruf bewirkt die Berechnung des öffentlichen Schlüsselwerts (G^X) mod P.
6.  Wenn alle vorherigen Funktionsaufrufe erfolgreich waren, kann Diffie-Hellman blob des öffentlichen Schlüssels jetzt codiert und übertragen werden.

**So importieren Sie Diffie-Hellman öffentlichen Schlüssel und berechnen den geheimen Sitzungsschlüssel**

1.  Rufen Sie die [**CryptAcquireContext-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) auf, um ein Handle für den Microsoft Diffie-Hellman Cryptographic Provider zu erhalten.
2.  Erstellen Sie Diffie-Hellman Schlüssel, indem Sie die [**CryptGenKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) aufrufen, um einen neuen Schlüssel zu erstellen, oder indem Sie die [**CryptGetUserKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) aufrufen, um einen vorhandenen Schlüssel abzurufen.
3.  Um den öffentlichen Diffie-Hellman-Schlüssel in den CSP zu importieren, rufen Sie die [**CryptImportKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) auf, und übergeben Sie einen Zeiger auf das BLOB des öffentlichen Schlüssels im *parameter pbData,* die Länge des BLOB im *dwDataLen-Parameter* und das Handle für den Diffie-Hellman-Schlüssel im *hPubKey-Parameter.* Dies bewirkt, dass die Berechnung (Y^X) mod P ausgeführt wird, wodurch der freigegebene geheime Schlüssel erstellt und der [*Schlüsselaustausch abgeschlossen wird.*](../secgloss/e-gly.md) Dieser Funktionsaufruf gibt ein Handle für den neuen geheimen Sitzungsschlüssel im *hKey-Parameter* zurück.
4.  An diesem Punkt ist die importierte Diffie-Hellman typ **CALG \_ AGREEDKEY \_ ANY.** Bevor der Schlüssel verwendet werden kann, muss er in einen Sitzungsschlüsseltyp konvertiert werden. Dies wird erreicht, indem die [**CryptSetKeyParam-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) mit *dwParam* auf **KP \_ ALGID** und *pbData* auf einen Zeiger auf einen [**ALG-ID-Wert \_**](alg-id.md) festgelegt wird, der einen Sitzungsschlüssel darstellt, z. B. **CALG \_ RC4**. Der Schlüssel muss konvertiert werden, bevor der gemeinsam genutzte Schlüssel in der [**CryptEncrypt-**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) oder [**CryptDecrypt-Funktion verwendet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) wird. Aufrufe, die vor der Konvertierung des Schlüsseltyps an eine dieser Funktionen vorgenommen werden, führen zu einem Fehler.
5.  Der geheime Sitzungsschlüssel kann jetzt für die Verschlüsselung oder Entschlüsselung verwendet werden.
6.  Wenn der Schlüssel nicht mehr benötigt wird, zerstören Sie das Schlüsselhandler, indem Sie die [**CryptDestroyKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) aufrufen.

## <a name="exporting-a-diffie-hellman-private-key"></a>Exportieren eines Diffie-Hellman privaten Schlüssels

Führen Sie zum Exportieren Diffie-Hellman privaten Schlüssels die folgenden Schritte aus:

1.  Rufen Sie die [**CryptAcquireContext-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) auf, um ein Handle für den Microsoft Diffie-Hellman Cryptographic Provider zu erhalten.
2.  Erstellen Sie Diffie-Hellman Schlüssel, indem Sie die [**CryptGenKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) aufrufen, um einen neuen Schlüssel zu erstellen, oder indem Sie die [**CryptGetUserKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) aufrufen, um einen vorhandenen Schlüssel abzurufen.
3.  Erstellen Sie [*Diffie-Hellman*](../secgloss/p-gly.md) privaten SchlüsselBLOB, indem Sie die [**CryptExportKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) aufrufen und **PRIVATEKEYBLOB** im *dwBlobType-Parameter* und das Handle an den Diffie-Hellman-Schlüssel im *hKey-Parameter* übergeben.
4.  Wenn das Schlüsselhandler nicht mehr benötigt wird, rufen Sie die [**CryptDestroyKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) auf, um das Schlüsselhandler zu zerstören.

## <a name="example-code"></a>Beispielcode

Im folgenden Beispiel wird gezeigt, wie Sie einen Schlüssel für einen Schlüsselaustausch erstellen, exportieren, importieren und Diffie-Hellman verwenden.


```C++
#include <tchar.h>
#include <windows.h>
#include <wincrypt.h>
#pragma comment(lib, "crypt32.lib")

// The key size, in bits.
#define DHKEYSIZE 512

// Prime in little-endian format.
static const BYTE g_rgbPrime[] = 
{
    0x91, 0x02, 0xc8, 0x31, 0xee, 0x36, 0x07, 0xec, 
    0xc2, 0x24, 0x37, 0xf8, 0xfb, 0x3d, 0x69, 0x49, 
    0xac, 0x7a, 0xab, 0x32, 0xac, 0xad, 0xe9, 0xc2, 
    0xaf, 0x0e, 0x21, 0xb7, 0xc5, 0x2f, 0x76, 0xd0, 
    0xe5, 0x82, 0x78, 0x0d, 0x4f, 0x32, 0xb8, 0xcb,
    0xf7, 0x0c, 0x8d, 0xfb, 0x3a, 0xd8, 0xc0, 0xea, 
    0xcb, 0x69, 0x68, 0xb0, 0x9b, 0x75, 0x25, 0x3d,
    0xaa, 0x76, 0x22, 0x49, 0x94, 0xa4, 0xf2, 0x8d 
};

// Generator in little-endian format.
static BYTE g_rgbGenerator[] = 
{
    0x02, 0x88, 0xd7, 0xe6, 0x53, 0xaf, 0x72, 0xc5,
    0x8c, 0x08, 0x4b, 0x46, 0x6f, 0x9f, 0x2e, 0xc4,
    0x9c, 0x5c, 0x92, 0x21, 0x95, 0xb7, 0xe5, 0x58, 
    0xbf, 0xba, 0x24, 0xfa, 0xe5, 0x9d, 0xcb, 0x71, 
    0x2e, 0x2c, 0xce, 0x99, 0xf3, 0x10, 0xff, 0x3b,
    0xcb, 0xef, 0x6c, 0x95, 0x22, 0x55, 0x9d, 0x29,
    0x00, 0xb5, 0x4c, 0x5b, 0xa5, 0x63, 0x31, 0x41,
    0x13, 0x0a, 0xea, 0x39, 0x78, 0x02, 0x6d, 0x62
};

BYTE g_rgbData[] = {0x01, 0x02, 0x03, 0x04,    0x05, 0x06, 0x07, 0x08};

int _tmain(int argc, _TCHAR* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    
    BOOL fReturn;
    HCRYPTPROV hProvParty1 = NULL; 
    HCRYPTPROV hProvParty2 = NULL; 
    DATA_BLOB P;
    DATA_BLOB G;
    HCRYPTKEY hPrivateKey1 = NULL;
    HCRYPTKEY hPrivateKey2 = NULL;
    PBYTE pbKeyBlob1 = NULL;
    PBYTE pbKeyBlob2 = NULL;
    HCRYPTKEY hSessionKey1 = NULL;
    HCRYPTKEY hSessionKey2 = NULL;
    PBYTE pbData = NULL;

    /************************
    Construct data BLOBs for the prime and generator. The P and G 
    values, represented by the g_rgbPrime and g_rgbGenerator arrays 
    respectively, are shared values that have been agreed to by both 
    parties.
    ************************/
    P.cbData = DHKEYSIZE/8;
    P.pbData = (BYTE*)(g_rgbPrime);

    G.cbData = DHKEYSIZE/8;
    G.pbData = (BYTE*)(g_rgbGenerator);

    /************************
    Create the private Diffie-Hellman key for party 1. 
    ************************/
    // Acquire a provider handle for party 1.
    fReturn = CryptAcquireContext(
        &hProvParty1, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 1.
    fReturn = CryptGenKey(
        hProvParty1, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Create the private Diffie-Hellman key for party 2. 
    ************************/
    // Acquire a provider handle for party 2.
    fReturn = CryptAcquireContext(
        &hProvParty2, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 2.
    fReturn = CryptGenKey(
        hProvParty2, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 1's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen1;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob1 = (PBYTE)malloc(dwDataLen1)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob1,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 2's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen2;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob2 = (PBYTE)malloc(dwDataLen2)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob2,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Party 1 imports party 2's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty1,
        pbKeyBlob2,
        dwDataLen2,
        hPrivateKey1,
        0,
        &hSessionKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }
    
    /************************
    Party 2 imports party 1's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty2,
        pbKeyBlob1,
        dwDataLen1,
        hPrivateKey2,
        0,
        &hSessionKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Convert the agreed keys to symmetric keys. They are currently of 
    the form CALG_AGREEDKEY_ANY. Convert them to CALG_RC4.
    ************************/
    ALG_ID Algid = CALG_RC4;

    // Enable the party 1 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey1,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Enable the party 2 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey2,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Encrypt some data with party 1's session key. 
    ************************/
    // Get the size.
    DWORD dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        NULL, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate a buffer to hold the encrypted data.
    pbData = (PBYTE)malloc(dwLength);
    if(!pbData)
    {
        goto ErrorExit;
    }

    // Copy the unencrypted data to the buffer. The data will be 
    // encrypted in place.
    memcpy(pbData, g_rgbData, sizeof(g_rgbData)); 

    // Encrypt the data.
    dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        pbData, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }
  
    /************************
    Decrypt the data with party 2's session key. 
    ************************/
    dwLength = sizeof(g_rgbData);
    fReturn = CryptDecrypt(
        hSessionKey2,
        0,
        TRUE,
        0,
        pbData,
        &dwLength);
    if(!fReturn)
    {
        goto ErrorExit;
    }


ErrorExit:
    if(pbData)
    {
        free(pbData);
        pbData = NULL;
    }

    if(hSessionKey2)
    {
        CryptDestroyKey(hSessionKey2);
        hSessionKey2 = NULL;
    }

    if(hSessionKey1)
    {
        CryptDestroyKey(hSessionKey1);
        hSessionKey1 = NULL;
    }

    if(pbKeyBlob2)
    {
        free(pbKeyBlob2);
        pbKeyBlob2 = NULL;
    }

    if(pbKeyBlob1)
    {
        free(pbKeyBlob1);
        pbKeyBlob1 = NULL;
    }

    if(hPrivateKey2)
    {
        CryptDestroyKey(hPrivateKey2);
        hPrivateKey2 = NULL;
    }

    if(hPrivateKey1)
    {
        CryptDestroyKey(hPrivateKey1);
        hPrivateKey1 = NULL;
    }

    if(hProvParty2)
    {
        CryptReleaseContext(hProvParty2, 0);
        hProvParty2 = NULL;
    }

    if(hProvParty1)
    {
        CryptReleaseContext(hProvParty1, 0);
        hProvParty1 = NULL;
    }

    return 0;
}
```



 

 
