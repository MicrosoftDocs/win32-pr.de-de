---
description: Erläutert das Generieren, Abrufen, Überprüfen und Exportieren von DSS-Schlüsseln und -Signaturen.
ms.assetid: d28fe531-af4b-4b5e-ab67-47ef70f8fa5b
title: DSS-Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5497a2a02ac5614c056f819a3999ee3cca6c5da78229f92e57002ae6a9e401ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875310"
---
# <a name="dss-keys"></a>DSS-Schlüssel

-   [Generieren und Abrufen von DSS-Schlüsseln](#generating-and-retrieving-dss-keys)
-   [Generieren von DSS-Signaturen](#generating-dss-signatures)
-   [Überprüfen einer DSS-Signatur](#verifying-a-dss-signature)
-   [Exportieren von DSS-Schlüsseln](#exporting-dss-keys)

## <a name="generating-and-retrieving-dss-keys"></a>Generieren und Abrufen von DSS-Schlüsseln

DSS-Schlüssel können durch einen Aufruf der [**CryptGenKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) generiert werden. Der Aufruf von **CryptGenKey** erfordert, dass AT \_ SIGNATURE oder CALG \_ DSS \_ SIGN im *Algid-Argument* übergeben werden. Mit diesem Aufruf werden die Werte P (Primmodulus), Q (Primzahl), G (Generator), X (Geheimer Exponent) und Y (öffentlicher Schlüssel) von Grund auf neu generiert und in einem [*Schlüsselblob*](../secgloss/k-gly.md) im lokalen Speicher gespeichert.

**So generieren Sie ein DSS-Signaturschlüsselpaar**

1.  Rufen Sie die [**CryptAcquireContext-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) auf, um ein Handle für den Microsoft DSS-Kryptografieanbieter abzurufen.
2.  Rufen Sie [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) auf, um die Schlüssel zu generieren. At \_ Signature oder CALG \_ DSS \_ SIGN muss für das *Algid-Argument* übergeben werden, und die oberen 16 Bits des *dwFlags-Arguments* müssen auf die gewünschte Schlüsselgröße festgelegt werden. Wenn die oberen 16 Bits null sind, wird die Standardschlüsselgröße von 1.024 Bits verwendet. Ein [**HCRYPTKEY-Handle**](hcryptkey.md) wird im *hKey-Argument* zurückgegeben.

**So rufen Sie einen Zeiger auf zuvor generierte Signaturschlüssel ab**

1.  Rufen Sie [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) auf, um ein Handle für den Microsoft DSS-Kryptografieanbieter abzurufen.
2.  Rufen Sie die [**CryptGetUserKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) auf, wobei das *dwKeySpec-Argument* entweder auf AT \_ SIGNATURE oder CALG \_ DSS SIGN festgelegt \_ ist.

**So rufen Sie die P-, Q- und G-Werte ab**

1.  Rufen Sie [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) auf, um ein Handle für den Microsoft DSS-Kryptografieanbieter abzurufen.
2.  Rufen Sie [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) auf, wobei das *dwKeySpec-Argument* entweder auf AT \_ SIGNATURE oder CALG \_ DSS SIGN festgelegt \_ ist.
3.  Rufen Sie [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) auf, wobei das *hKey-Argument* auf den Zeiger festgelegt ist, der im vorherigen Schritt abgerufen wurde. Das *dwParam-Argument* muss auf das gewünschte Flag festgelegt werden. KP \_ P, KP \_ Q oder KP \_ G. Der Wert wird im *pbData-Argument* zurückgegeben, und die Länge der Daten wird im *pdwDataLen-Argument* zurückgegeben. Der Wert wird ohne Headerinformationen und im [*Little-Endian-Format*](../secgloss/l-gly.md) zurückgegeben.

## <a name="generating-dss-signatures"></a>Generieren von DSS-Signaturen

Daten, die signiert werden sollen, müssen zuerst mithilfe des [*SHA-Algorithmus*](../secgloss/s-gly.md) [*per Hashwert versehen*](../secgloss/h-gly.md) werden. Nach dem Hashing dieser Daten wird eine [*DSS-Signatur*](../secgloss/d-gly.md) generiert, indem die [**CryptSignHash-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) aufgerufen wird.

**So generieren Sie eine DSS-Signatur**

1.  Rufen Sie [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) auf, um ein Handle für den Microsoft DSS-Kryptografieanbieter abzurufen.
2.  Rufen Sie [**CryptCreateHash auf,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) wobei das *Algid-Argument* auf CALG SHA festgelegt \_ ist, um ein Handle für ein SHA-Hashobjekt abzurufen.
3.  Rufen Sie [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) auf, wobei das *hHash-Argument* auf das handle festgelegt ist, das im vorherigen Schritt abgerufen wurde. Dadurch wird ein Hash der Daten erstellt und ein Handle für den Hash im *phHash-Argument* des Aufrufs der [**CryptCreateHash-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) zurückgegeben.
4.  Rufen Sie [**CryptSignHash auf,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) wobei das *hHash-Argument* auf das handle festgelegt ist, das im vorherigen Schritt abgerufen wurde. Entweder AT \_ SIGNATURE oder CALG \_ DSS \_ SIGN kann im *dwKeySpec-Parameter* übergeben werden. Die Signatur wird an die adresse zurückgegeben, die im *pbSignature-Argument* bereitgestellt wird, und die Länge der Signatur wird an die Adresse zurückgegeben, die im *pdwSigLen-Argument* bereitgestellt wird. Ein **NULL-Zeiger** kann im *pbSignature-Argument* übergeben werden, und in diesem Fall wird die Signatur nicht generiert, aber die Länge der Signatur wird an die Adresse zurückgegeben, die im *pdwSigLen-Parameter* bereitgestellt wird.

## <a name="verifying-a-dss-signature"></a>Überprüfen einer DSS-Signatur

Um eine DSS-Signatur zu überprüfen, muss der öffentliche DSS-Schlüssel des Signaturgebers importiert werden, die [*signierten Daten*](../secgloss/s-gly.md) müssen gehasht werden, und dann kann die Signatur überprüft werden.

**So überprüfen Sie eine DSS-Signatur**

1.  Rufen Sie [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) auf, um ein Handle für den Microsoft DSS-Kryptografieanbieter abzurufen.
2.  Rufen Sie [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) auf, um den öffentlichen DSS-Schlüssel des Signierers zu importieren.
3.  Rufen Sie [**CryptCreateHash auf,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) wobei das *Algid-Argument* auf CALG SHA festgelegt \_ ist, um ein Handle für ein SHA-Hashobjekt abzurufen.
4.  Rufen Sie [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) auf, wobei das *hHash-Argument* auf das im vorherigen Schritt abgerufene Handle festgelegt ist und *pbData* auf die signierten Daten verweist. Dadurch wird ein Hash der Daten erstellt und ein Handle für den Hash im *phHash-Argument* des Aufrufs der [**CryptCreateHash-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) zurückgegeben.
5.  Rufen Sie [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) mit den folgenden Einstellungen auf:

    *hHash* wird auf das Handle für den Hash festgelegt, der im vorherigen Schritt ausgeführt wurde.

    *pbSignature* zeigt auf die zu überprüfende Signatur.

    *dwSigLen* wird auf die Länge der Signatur festgelegt.

    *hPubKey* ist auf das Handle des öffentlichen Schlüssels festgelegt, der in Schritt 2 importiert wurde.

    *dwFlags* ist auf 0 (null) festgelegt.

## <a name="exporting-dss-keys"></a>Exportieren von DSS-Schlüsseln

Wenn Sie [*signierte Daten*](../secgloss/s-gly.md) an eine Person senden, bei der die Signatur vom Empfänger überprüft werden muss, muss der öffentliche Schlüssel des Signaturgebers dem Empfänger bereitgestellt werden und wird in der Regel zusammen mit den signierten Daten gesendet. Daher ist es erforderlich, die [*DSS-Schlüssel*](../secgloss/d-gly.md) in einem [*Schlüsselblobformat*](../secgloss/k-gly.md) exportieren zu können.

**So exportieren Sie den öffentlichen DSS-Schlüssel**

1.  Rufen Sie [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) auf, um ein Handle für den Microsoft DSS-Kryptografieanbieter abzurufen.
2.  Rufen Sie [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) auf, wobei das *dwKeySpec-Argument* entweder auf AT \_ SIGNATURE oder CALG \_ DSS SIGN festgelegt \_ ist.
3.  Rufen Sie [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) auf, wobei *hKey* auf das im vorherigen Schritt abgerufene Handle festgelegt ist, *dwBlobType* auf PUBLICKEYBLOB und *dwFlags* auf 0 (null) festgelegt ist. Das BLOB des [*öffentlichen DSS-Schlüssels*](../secgloss/p-gly.md) wird in *pbData* zurückgegeben, und die Länge des [*Schlüsselblobs*](../secgloss/k-gly.md) wird in *pdwDataLen* zurückgegeben. Ein **NULL-Zeiger** kann in *pbData* übergeben werden, und in diesem Fall wird nur die Länge des DSS-Schlüsselblobs zurückgegeben. Das BLOB, das beim Aufruf von **CryptExportKey** zurückgegeben wird, weist das in [DSS-Anbieterschlüssel-BLOBs](dss-provider-key-blobs.md)beschriebene Format auf.

**So exportieren Sie den privaten DSS-Schlüssel**

-   Führen Sie das gleiche Verfahren wie beim Exportieren eines öffentlichen DSS-Schlüssels aus, außer dass *dwBlobType* beim Aufruf von [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)auf PRIVATEKEYBLOB festgelegt ist. Das BLOB, das beim Aufruf von **CryptExportKey** zurückgegeben wird, weist das in [DSS-Anbieterschlüssel-BLOBs](dss-provider-key-blobs.md)beschriebene Format auf.

 

 
