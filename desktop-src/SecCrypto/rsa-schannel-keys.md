---
description: Generieren, abrufen und Exportieren von RSA/SChannel-Schlüsseln.
ms.assetid: 3069232f-d016-4973-ae39-89b0e2a03cd7
title: RSA/SChannel-Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c9d23de40f32a499013928086ccb52fc1d1e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526327"
---
# <a name="rsaschannel-keys"></a>RSA/SChannel-Schlüssel

## <a name="generating-and-retrieving-rsaschannel-keys"></a>Erstellen und Abrufen von RSA/SChannel-Schlüsseln

[*RSA*](../secgloss/r-gly.md) / [*SChannel*](../secgloss/s-gly.md) -Schlüssel können durch Aufrufen der [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) -Funktion generiert werden. Der Aufruf von **CryptGenKey** erfordert, dass ein an \_ keyexchange-Algorithmus bezeichnerbezeichner im *algid* -Parameter übergeben wird.

**So generieren Sie ein öffentliches/privates RSA/SChannel-Schlüsselpaar**

1.  Aufrufen der [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) -Funktion, um ein Handle für den [Kryptografieanbieter von Microsoft RSA/SChannel](microsoft-rsa-schannel-cryptographic-provider.md)zu erhalten.
2.  Rufen Sie die [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) -Funktion auf, um die Schlüssel zu generieren. An \_ keyexchange muss für den *algid* -Parameter übergeben werden, und die oberen 16 Bits des *dwFlags* -Parameters müssen auf die gewünschte Schlüsselgröße (512 Bits) festgelegt werden. Ein [**hcryptkey**](hcryptkey.md) -Struktur handle wird im *HKEY* -Parameter zurückgegeben.

**So rufen Sie einen Zeiger auf zuvor generierte RSA/SChannel-Benutzerschlüssel ab**

1.  Aufrufen der [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) -Funktion, um ein Handle für den [Kryptografieanbieter von Microsoft RSA/SChannel](microsoft-rsa-schannel-cryptographic-provider.md)zu erhalten.
2.  Rufen Sie die Funktion [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) auf, bei der der Parameter *dwkeyspec* bei keyexchange auf festgelegt ist \_ .

## <a name="exporting-rsaschannel-keys"></a>Exportieren von RSA/SChannel-Schlüsseln

[*Hauptschlüssel*](../secgloss/m-gly.md) können in einfache Schlüsselblob-Strukturen exportiert werden. Dies sollte auf die gleiche Weise wie der Export von normalen [*RC4*](../secgloss/r-gly.md) -oder [*Daten Verschlüsselungs Standard*](../secgloss/d-gly.md) - [*Massen Verschlüsselungsschlüsseln*](../secgloss/b-gly.md)implementiert werden, wie in [Simple Key BLOB](https://www.bing.com/search?q=Simple+Key+BLOB)beschrieben. Der **aikeyalg** -Member der [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur ist auf den Algorithmusbezeichner des Haupt Schlüssels (calg \_ das PCT1 verwendet \_ Master, calg \_ SSL2 verwendet \_ Master, calg \_ SSL3 \_ Master oder calg \_ das TLS1 verwendet \_ Master) festgelegt.

Wenn die [**cpexportkey**](https://www.bing.com/search?q=**CPExportKey**) -Funktion einen SSL2 verwendet-Hauptschlüssel exportiert und das \_ Flag "Crypt SSL2 verwendet \_ Fallback" festgelegt ist, legen Sie zur Vermeidung von Versions Rollback-Angriffen die ersten acht Bytes des [](../secgloss/p-gly.md) Verschlüsselungs Blocks auf 0x03 anstatt auf zufällige Daten fest.

Wenn die **crypt \_ destroykey** -Konstante im *dwFlags* -Parameter der [**cpexportkey**](https://www.bing.com/search?q=**CPExportKey**) -Funktion angegeben wird, zerstört der CSP den Schlüssel oder das Schlüssel Handle nach dem Exportieren des Schlüssels. Dieses Flag ist nur für die Verwendung mit nicht transparenten [*blobnetzen*](../secgloss/o-gly.md)vorgesehen.

 

 
