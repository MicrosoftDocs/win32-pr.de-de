---
description: Erläutert das generieren, abrufen, überprüfen und Exportieren von DSS-Schlüsseln und-Signaturen.
ms.assetid: d28fe531-af4b-4b5e-ab67-47ef70f8fa5b
title: DSS-Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f6ab8adcc4d551c4196e99ce48f5afdd380dc3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340179"
---
# <a name="dss-keys"></a>DSS-Schlüssel

-   [Erzeugen und Abrufen von DSS-Schlüsseln](#generating-and-retrieving-dss-keys)
-   [Erstellen von DSS-Signaturen](#generating-dss-signatures)
-   [Überprüfen einer DSS-Signatur](#verifying-a-dss-signature)
-   [Exportieren von DSS-Schlüsseln](#exporting-dss-keys)

## <a name="generating-and-retrieving-dss-keys"></a>Erzeugen und Abrufen von DSS-Schlüsseln

DSS-Schlüssel können durch einen Aufruf der [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) -Funktion generiert werden. Der Aufruf von " **CryptGenKey** " erfordert, dass entweder die \_ Signatur oder das calg- \_ DSS- \_ Zeichen im *algid* -Argument übergeben wird. Mit diesem Befehl werden die Werte P (primmodulus), Q (priv), G (Generator), X (Secret Exponent) und Y (Public Key) von Grund auf neu generiert und in einem [*Schlüssel-BLOB*](../secgloss/k-gly.md) im lokalen Speicher gespeichert.

**So generieren Sie ein DSS-Signatur Schlüsselpaar**

1.  Aufrufen der [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) -Funktion, um ein Handle für den Microsoft DSS-Kryptografieanbieter zu erhalten.
2.  Rufen Sie [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) auf, um die Schlüssel zu generieren. \_ \_ \_ Für das *algid* -Argument muss entweder die Signatur oder das calg-DSS-Zeichen übergeben werden, und die oberen 16 Bits des *dwFlags* -Arguments müssen auf die gewünschte Schlüsselgröße festgelegt werden. Wenn die oberen 16 Bits NULL sind, wird die Standard Schlüsselgröße von 1.024 Bits verwendet. Im *HKEY* -Argument wird ein [**hcryptkey**](hcryptkey.md) -Handle zurückgegeben.

**So rufen Sie einen Zeiger auf zuvor generierte Signatur Schlüssel ab**

1.  Aufrufen von [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) zum Abrufen eines Handles für den Microsoft DSS-Kryptografieanbieter.
2.  Rufen Sie die Funktion " [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) " mit dem " *dwkeyspec* "-Argument auf, das entweder auf " \_ Signature" oder "calg \_ DSS \_ Sign

**So rufen Sie die Werte P, Q und G ab**

1.  Aufrufen von [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) zum Abrufen eines Handles für den Microsoft DSS-Kryptografieanbieter.
2.  Rufen Sie [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) mit dem *dwkeyspec* -Argument auf, das entweder bei der \_ Signatur oder dem calg- \_ DSS- \_ Vorzeichen festgelegt ist
3.  Nennen Sie [**cryptgetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) mit dem *HKEY* -Argument, das auf den im vorherigen Schritt abgerufenen Zeiger festgelegt ist. Das *dwparam* -Argument muss auf das gewünschte Flag festgelegt werden. KP \_ P, KP \_ Q oder KP \_ G. Der Wert wird im *pbData* -Argument zurückgegeben, und die Länge der Daten wird im Argument " *pdwdatalen* " zurückgegeben. Der Wert wird ohne Header Informationen und im [*Little-Endian-*](../secgloss/l-gly.md) Format zurückgegeben.

## <a name="generating-dss-signatures"></a>Erstellen von DSS-Signaturen

Die zu Signier enden Daten müssen zunächst mit dem [*SHA*](../secgloss/s-gly.md) -Algorithmus [*gehackt*](../secgloss/h-gly.md) werden. Nach dem Hashwert der Daten wird eine [*DSS*](../secgloss/d-gly.md) -Signatur generiert, indem die [**cryptsignhash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) -Funktion aufgerufen wird.

**So generieren Sie eine DSS-Signatur**

1.  Aufrufen von [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) zum Abrufen eines Handles für den Microsoft DSS-Kryptografieanbieter.
2.  Nennen Sie [**cryptkreatehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) mit dem *algid* -Argument, das auf calg SHA festgelegt ist \_ , um ein Handle für ein SHA-Hash Objekt zu erhalten.
3.  Nennen Sie [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) mit dem *hhash* -Argument, das auf das im vorherigen Schritt abgerufene handle festgelegt ist. Dadurch wird ein Hash der Daten erstellt und ein Handle für den Hash im *phhash* -Argument des [**cryptkreatehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) -Funktions Aufrufes zurückgegeben.
4.  Nennen Sie [**cryptsignhash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) mit dem *hhash* -Argument, das auf das im vorherigen Schritt abgerufene handle festgelegt ist. \_ \_ \_ Im *dwkeyspec* -Parameter kann entweder die Signatur oder das calg-DSS-Zeichen übergeben werden. Die Signatur wird an die im *pbSignature* -Argument angegebene Adresse zurückgegeben, und die Länge der Signatur wird an die im *pdwsiglen* -Argument angegebene Adresse zurückgegeben. Ein **null** -Zeiger kann im *pbSignature* -Argument übergeben werden, und in diesem Fall wird die Signatur nicht generiert, aber die Länge der Signatur wird an die im *pdwsiglen* -Parameter angegebene Adresse zurückgegeben.

## <a name="verifying-a-dss-signature"></a>Überprüfen einer DSS-Signatur

Zum Überprüfen einer DSS-Signatur muss der öffentliche DSS-Schlüssel des Signatur Gebers importiert werden, für die [*signierten Daten*](../secgloss/s-gly.md) muss ein Hashwert verwendet werden, und die Signatur kann dann überprüft werden.

**So überprüfen Sie eine DSS-Signatur**

1.  Aufrufen von [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) zum Abrufen eines Handles für den Microsoft DSS-Kryptografieanbieter.
2.  Nennen Sie [**cryptimportkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) , um den öffentlichen DSS-Schlüssel des Signatur Gebers zu importieren.
3.  Nennen Sie [**cryptkreatehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) mit dem *algid* -Argument, das auf calg SHA festgelegt ist \_ , um ein Handle für ein SHA-Hash Objekt zu erhalten.
4.  Nennen Sie [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) mit dem *hhash* -Argument, das auf das im vorherigen Schritt abgerufene handle festgelegt wurde, und *pbData* , das auf die signierten Daten zeigt. Dadurch wird ein Hash der Daten erstellt und ein Handle für den Hash im *phhash* -Argument des [**cryptkreatehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) -Funktions Aufrufes zurückgegeben.
5.  Nennen Sie [**cryptverifysignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) mit den folgenden Einstellungen:

    *hhash* wird auf das Handle für den Hash festgelegt, der im vorherigen Schritt ausgeführt wurde.

    *pbSignature* verweist auf die Signatur, die überprüft werden soll.

    *dwsiglen* ist auf die Länge der Signatur festgelegt.

    *hpubkey* wird auf das Handle des in Schritt 2 importierten öffentlichen Schlüssels festgelegt.

    *dwFlags* ist auf 0 (null) festgelegt.

## <a name="exporting-dss-keys"></a>Exportieren von DSS-Schlüsseln

Wenn Sie [*signierte Daten*](../secgloss/s-gly.md) an jemanden senden, von dem die Signatur vom Empfänger überprüft werden muss, muss der öffentliche Schlüssel des Signatur Gebers dem Empfänger bereitgestellt werden und wird in der Regel zusammen mit den signierten Daten gesendet. Daher ist es erforderlich, die [*DSS*](../secgloss/d-gly.md) -Schlüssel in einem [*Schlüssel-BLOB*](../secgloss/k-gly.md) -Format zu exportieren.

**So exportieren Sie den öffentlichen DSS-Schlüssel**

1.  Aufrufen von [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) zum Abrufen eines Handles für den Microsoft DSS-Kryptografieanbieter.
2.  Rufen Sie [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) mit dem *dwkeyspec* -Argument auf, das entweder bei der \_ Signatur oder dem calg- \_ DSS- \_ Vorzeichen festgelegt ist
3.  Nennen Sie [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , wobei *HKEY* auf das im vorherigen Schritt abgerufene handle festgelegt ist, *dwblobtype* auf PublicKeyBlob und *dwFlags* auf NULL festgelegt ist. Das [*BLOB des öffentlichen*](../secgloss/p-gly.md) DSS-Schlüssels wird in *pbData* zurückgegeben, und die Länge des [*Schlüsselblobs*](../secgloss/k-gly.md) wird in " *pdwdatalen*" zurückgegeben. Ein **null** -Zeiger kann in *pbData* übergeben werden, und in diesem Fall wird nur die Länge des DSS-Schlüsselblobs zurückgegeben. Das BLOB, das beim Aufrufen von " **CryptExportKey** " zurückgegeben wird, weist das in den [DSS-Anbieter-Schlüsselblobs](dss-provider-key-blobs.md)beschriebene Format auf.

**So exportieren Sie den privaten DSS-Schlüssel**

-   Befolgen Sie das gleiche Verfahren wie beim Exportieren eines öffentlichen DSS-Schlüssels, mit dem Unterschied, dass *dwblobtype* beim Aufrufen von [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)auf privatekeyblob festgelegt ist. Das BLOB, das beim Aufrufen von " **CryptExportKey** " zurückgegeben wird, weist das in den [DSS-Anbieter-Schlüsselblobs](dss-provider-key-blobs.md)beschriebene Format auf.

 

 
