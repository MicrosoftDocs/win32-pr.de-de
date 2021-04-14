---
description: Erläutert, wie Diffie-Hellman Schlüssel generiert, ausgetauscht, importiert und exportiert werden.
ms.assetid: 623a8c9e-3f6a-470b-be30-dec13342bb90
title: Diffie-Hellman Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00eaddd580ac74e18e26498175f87b5d81b8e20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350148"
---
# <a name="diffie-hellman-keys"></a>Diffie-Hellman Schlüssel

-   [Erstellen von Diffie-Hellman Schlüsseln](#generating-diffie-hellman-keys)
-   [Austauschen von Diffie-Hellman Schlüsseln](#exchanging-diffie-hellman-keys)
-   [Exportieren eines Diffie-Hellman privaten Schlüssels](#exporting-a-diffie-hellman-private-key)
-   [Beispiel Code](#example-code)

## <a name="generating-diffie-hellman-keys"></a>Erstellen von Diffie-Hellman Schlüsseln

Führen Sie die folgenden Schritte aus, um einen Diffie-Hellman Schlüssel zu generieren:

1.  Aufrufen der [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) -Funktion, um ein Handle für den Kryptografieanbieter von Microsoft Diffie-Hellman zu erhalten.
2.  Generieren Sie den neuen Schlüssel. Es gibt zwei Möglichkeiten, diesen – zu erreichen, indem CryptoAPI alle neuen Werte für g, P und X generiert, oder wenn vorhandene Werte für g und P verwendet werden und ein neuer Wert für X generiert wird.

    **So generieren Sie den Schlüssel, indem Sie alle neuen Werte generieren**

    1.  Aufrufen der [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) -Funktion, wobei entweder **calg \_ dh \_ SF** (speichern und Weiterleiten) oder **calg \_ dh \_ ephem** (kurzlebige) im *algid* -Parameter übergeben wird. Der Schlüssel wird mithilfe neuer, zufälliger Werte für G und P generiert, ein neu berechneter Wert für X, und sein Handle wird im *phkey* -Parameter zurückgegeben.
    2.  Der neue Schlüssel ist jetzt einsatzbereit. Die Werte von G und P müssen bei einem [*Schlüsselaustausch*](../secgloss/e-gly.md)zusammen mit dem Schlüssel an den Empfänger gesendet werden (oder von einer anderen Methode gesendet werden).

    **So generieren Sie den Schlüssel mithilfe vordefinierter Werte für G und P**

    1.  Rufen Sie [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) auf, indem Sie entweder **calg \_ dh \_ SF** (speichern und Weiterleiten) oder **calg \_ dh \_ ephem** (kurzlebige) im *algid* -Parameter und **crypt \_ pregen** für den *dwFlags* -Parameter übergeben. Ein Schlüssel Handle wird generiert und im *phkey* -Parameter zurückgegeben.
    2.  Initialisieren Sie eine [**crypt \_ Data \_ BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) -Struktur mit dem **pbData** -Member, der auf den P-Wert festgelegt ist. Das [*BLOB*](../secgloss/b-gly.md) enthält keine Header Informationen, und der **pbData** -Member weist das [*Little-Endian-*](../secgloss/l-gly.md) Format auf.
    3.  Der Wert von P wird durch Aufrufen der [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) -Funktion festgelegt, wobei das in Schritt a abgerufene Schlüssel Handle im *HKEY* -Parameter, das **KP- \_ P** -Flag im *dwparam* -Parameter und ein Zeiger auf die-Struktur mit dem Wert P im *pbData* -Parameter übergeben werden.
    4.  Initialisieren Sie eine [**crypt \_ Data \_ BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) -Struktur mit dem **pbData** -Member, der auf den Wert G festgelegt ist. Das BLOB enthält keine Header Informationen, und der **pbData** -Member weist das Little-Endian-Format auf.
    5.  Der Wert von "G" wird durch Aufrufen der Funktion " [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) " festgelegt, wobei das in Schritt a abgerufene Schlüssel Handle im *HKEY* -Parameter, das **KP \_ G** -Flag im *dwparam* -Parameter und ein Zeiger auf die Struktur mit dem Wert "G" im *pbData* -Parameter übergeben werden.
    6.  Der Wert von "X" wird durch Aufrufen der Funktion " [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) " generiert, wobei das in Schritt a abgerufene Schlüssel Handle im *HKEY* -Parameter, das **KP \_ X** -Flag im *dwparam* -Parameter und **null** im *pbData* -Parameter übergeben wird.
    7.  Wenn alle Funktionsaufrufe erfolgreich waren, ist der Diffie-Hellman öffentliche Schlüssel einsatzbereit.

3.  Wenn der Schlüssel nicht mehr benötigt wird, zerstören Sie ihn, indem Sie das Schlüssel Handle an die [**cryptdestroykey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) -Funktion übergeben.

Wenn **calg \_ dh \_ SF** in den vorherigen Prozeduren angegeben wurde, werden die Schlüsselwerte im Speicher gespeichert, wobei jeder Rückruf von [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)verwendet wird. Die Werte G und P können dann mithilfe der [**cryptgetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) -Funktion abgerufen werden. Einige CSPs verfügen möglicherweise über hart codierte G-und P-Werte. In diesem Fall wird ein ". **\_ fixedparameter** "-Fehler zurückgegeben, wenn **cryptsetkeyparam** mit **KP \_ G** oder **KP \_ P** aufgerufen wird, das im *dwparam* -Parameter angegeben ist. Wenn **cryptdestroykey** aufgerufen wird, wird das Handle für den Schlüssel zerstört, aber die Schlüsselwerte werden im CSP beibehalten. Wenn jedoch **calg \_ dh \_ ephem** angegeben wurde, wird das Handle für den Schlüssel zerstört, und alle Werte werden vom CSP gelöscht.

## <a name="exchanging-diffie-hellman-keys"></a>Austauschen von Diffie-Hellman Schlüsseln

Der Zweck des Diffie-Hellman Algorithmus besteht darin, dass zwei oder mehr Parteien einen identischen geheimen Sitzungsschlüssel erstellen und freigeben können, indem Informationen über ein nicht sicheres Netzwerk freigegeben werden. Die Informationen, die über das Netzwerk freigegeben werden, sind in Form von einigen Konstanten Werten und einem Diffie-Hellman öffentlichen Schlüssel. Der Prozess, der von zwei Schlüsselaustausch Parteien verwendet wird, lautet wie folgt:

-   Beide Parteien stimmen den Diffie-Hellman Parametern zu, bei denen es sich um eine Primzahl (P) und eine Generator Nummer (G) handelt.
-   Partei 1 sendet den Diffie-Hellman öffentlichen Schlüssel an Partei 2.
-   Partei 2 berechnet den geheimen Sitzungsschlüssel anhand der Informationen, die in seinem privaten Schlüssel und dem öffentlichen Schlüssel von Partei 1 enthalten sind.
-   Partei 2 sendet ihren Diffie-Hellman öffentlichen Schlüssel an Partei 1.
-   Partei 1 berechnet den geheimen Sitzungsschlüssel anhand der Informationen, die in seinem privaten Schlüssel und dem öffentlichen Schlüssel von Partei 2 enthalten sind.
-   Beide Parteien verfügen jetzt über denselben Sitzungsschlüssel, der zum Verschlüsseln und Entschlüsseln von Daten verwendet werden kann. Die hierfür erforderlichen Schritte werden im folgenden Verfahren beschrieben.

**So bereiten Sie einen Diffie-Hellman öffentlichen Schlüssel für die Übertragung vor**

1.  Aufrufen der [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) -Funktion, um ein Handle für den Kryptografieanbieter von Microsoft Diffie-Hellman zu erhalten.
2.  Erstellen Sie einen Diffie-Hellman Schlüssel, indem Sie die Funktion [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) aufrufen, um einen neuen Schlüssel zu erstellen, oder indem Sie die Funktion [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) aufrufen, um einen vorhandenen Schlüssel abzurufen.
3.  Rufen Sie die erforderliche Größe für das Diffie-Hellman Schlüsselblob ab, indem Sie den [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)aufrufen und **null** für den *pbData* -Parameter übergeben. Die erforderliche Größe wird in " *pdwdatalen*" zurückgegeben.
4.  Arbeitsspeicher für das Schlüssel-BLOB zuweisen.
5.  Erstellen Sie ein [*BLOB für den öffentlichen Schlüssel*](../secgloss/p-gly.md) Diffie-Hellman, indem Sie die Funktion [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) aufrufen, indem Sie **PublicKeyBlob** im Parameter *dwblobtype* und das Handle an den Diffie-Hellman Schlüssel im *HKEY* -Parameter übergeben. Dieser Funktions Aufrufvorgang bewirkt die Berechnung des Werts des öffentlichen Schlüssels (G ^ X) mod P.
6.  Wenn alle vorhergehenden Funktionsaufrufe erfolgreich waren, kann das BLOB des Diffie-Hellman öffentlichen Schlüssels jetzt codiert und übertragen werden.

**So importieren Sie einen Diffie-Hellman öffentlichen Schlüssel und berechnen den geheimen Sitzungsschlüssel**

1.  Aufrufen der [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) -Funktion, um ein Handle für den Kryptografieanbieter von Microsoft Diffie-Hellman zu erhalten.
2.  Erstellen Sie einen Diffie-Hellman Schlüssel, indem Sie die Funktion [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) aufrufen, um einen neuen Schlüssel zu erstellen, oder indem Sie die Funktion [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) aufrufen, um einen vorhandenen Schlüssel abzurufen.
3.  Um den Diffie-Hellman öffentlichen Schlüssel in den CSP zu importieren, müssen Sie die Funktion [**cryptimportkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) aufrufen und einen Zeiger auf das BLOB des öffentlichen Schlüssels im *pbData* -Parameter, die Länge des BLOBs im Parameter *dwdatalen* und das Handle für den Diffie-Hellman Schlüssel im *hpubkey* -Parameter übergeben. Dies bewirkt, dass die Berechnung (Y ^ X) mod P ausgeführt wird. auf diese Weise wird der gemeinsame geheime Schlüssel erstellt und der [*Schlüsselaustausch*](../secgloss/e-gly.md)abgeschlossen. Dieser Funktions aufruter gibt ein Handle für den neuen geheimen Schlüssel, den Sitzungsschlüssel im *HKEY* -Parameter zurück.
4.  An diesem Punkt ist der importierte Diffie-Hellman vom Typ **calg \_ agreedkey \_ any**. Bevor der Schlüssel verwendet werden kann, muss er in einen Sitzungs Schlüsseltyp konvertiert werden. Dies wird erreicht, indem die [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) -Funktion mit *dwparam* auf **KP \_ algid** festgelegt und *pbData* auf einen Zeiger auf einen [**ALG- \_ ID**](alg-id.md) -Wert festgelegt wird, der einen Sitzungsschlüssel darstellt, z. b. **calg \_ RC4**. Der Schlüssel muss konvertiert werden, bevor der gemeinsam verwendete Schlüssel in der [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) -Funktion oder der [**cryptentschlpt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) -Funktion verwendet wird. Aufrufe an eine dieser Funktionen, bevor der Schlüsseltyp umgewandelt wird, können nicht ausgeführt werden.
5.  Der geheime Sitzungsschlüssel kann jetzt für die Verschlüsselung oder Entschlüsselung verwendet werden.
6.  Wenn der Schlüssel nicht mehr benötigt wird, zerstören Sie den Schlüssel Handle durch Aufrufen der [**cryptdestroykey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) -Funktion.

## <a name="exporting-a-diffie-hellman-private-key"></a>Exportieren eines Diffie-Hellman privaten Schlüssels

Um einen Diffie-Hellman privaten Schlüssel zu exportieren, führen Sie die folgenden Schritte aus:

1.  Aufrufen der [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) -Funktion, um ein Handle für den Kryptografieanbieter von Microsoft Diffie-Hellman zu erhalten.
2.  Erstellen Sie einen Diffie-Hellman Schlüssel, indem Sie die Funktion [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) aufrufen, um einen neuen Schlüssel zu erstellen, oder indem Sie die Funktion [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) aufrufen, um einen vorhandenen Schlüssel abzurufen.
3.  Erstellen Sie einen Diffie-Hellman [*privaten Schlüsselblob*](../secgloss/p-gly.md) , indem Sie die [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) -Funktion aufrufen und dabei **privatekeyblob** im Parameter *dwblobtype* und das Handle an den Diffie-Hellman Schlüssel im *HKEY* -Parameter übergeben.
4.  Wenn das Schlüssel Handle nicht mehr benötigt wird, können Sie die Funktion " [**cryptdestroykey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) " aufrufen, um das Schlüssel Handle zu zerstören.

## <a name="example-code"></a>Beispielcode

Im folgenden Beispiel wird gezeigt, wie ein Diffie-Hellman Schlüssel erstellt, exportiert, importiert und verwendet wird, um einen Schlüsselaustausch auszuführen.


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



 

 
