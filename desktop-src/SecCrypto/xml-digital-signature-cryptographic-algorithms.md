---
description: CryptXML unterstützt die unten aufgeführten URIs nativ.
ms.assetid: 012bad01-228a-4bb0-b883-0c2c7abd9271
title: Kryptografische Algorithmen für digitale XML-Signaturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290be3708565cf144b5bf23bfcb1ddfe5252b227c12bbcebbd81b68d0fc2df07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895786"
---
# <a name="xml-digital-signature-cryptographic-algorithms"></a>Kryptografische Algorithmen für digitale XML-Signaturen

CryptXML unterstützt die unten aufgeführten URIs nativ. Wenn Unterstützung für kryptografische Algorithmen und Transformationen erforderlich ist, die nicht Teil der nativen Unterstützung sind, können Sie [Cryptography API: Next Generation](../seccng/cng-portal.md) und [XML Digital Signature Cryptographic Extensions](xml-digital-signature-cryptographic-extensions.md) verwenden, um neue Algorithmen zu unterstützen.

## <a name="supported-uris"></a>Unterstützte URIs

Digestmethoden



| Konstante                                 | URI-Wert                                                   |
|------------------------------------------|-------------------------------------------------------------|
| wszURI \_ XMLNS \_ DIGSIG \_ SHA1<br/>   | "https://www.w3.org/2000/09/xmldsig\#sha1"<br/>        |
| wszURI \_ XMLNS \_ DIGSIG \_ SHA256<br/> | "https://www.w3.org/2001/04/xmlenc\#sha256"<br/>       |
| wszURI \_ XMLNS \_ DIGSIG \_ SHA384<br/> | "https://www.w3.org/2001/04/xmldsig-more\#sha384"<br/> |
| wszURI \_ XMLNS \_ DIGSIG \_ SHA512<br/> | "https://www.w3.org/2001/04/xmlenc\#sha512"<br/>       |



 

Signaturmethoden



| Konstante                                        | URI-Wert                                                         |
|-------------------------------------------------|-------------------------------------------------------------------|
| wszURI \_ XMLNS \_ DIGSIG \_ RSA \_ SHA1<br/>     | "https://www.w3.org/2000/09/xmldsig\#rsa-sha1"<br/>          |
| wszURI \_ XMLNS \_ DIGSIG \_ DSA \_ SHA1<br/>     | "https://www.w3.org/2000/09/xmldsig\#dsa-sha1"<br/>          |
| wszURI \_ XMLNS \_ DIGSIG \_ RSA \_ SHA256<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#rsa-sha256"<br/>   |
| wszURI \_ XMLNS \_ DIGSIG \_ RSA \_ SHA384<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#rsa-sha384"<br/>   |
| wszURI \_ XMLNS \_ DIGSIG \_ RSA \_ SHA512<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#rsa-sha512"<br/>   |
| wszURI \_ XMLNS \_ DIGSIG \_ ECDSA \_ SHA1<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha1"<br/>   |
| wszURI \_ XMLNS \_ DIGSIG \_ ECDSA \_ SHA256<br/> | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha256"<br/> |
| wszURI \_ XMLNS \_ DIGSIG \_ ECDSA \_ SHA384<br/> | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha384"<br/> |
| wszURI \_ XMLNS \_ DIGSIG \_ ECDSA \_ SHA512<br/> | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha512"<br/> |
| wszURI \_ XMLNS \_ DIGSIG \_ HMAC \_ SHA1<br/>    | "https://www.w3.org/2000/09/xmldsig\#hmac-sha1"<br/>         |
| wszURI \_ XMLNS \_ DIGSIG \_ HMAC \_ SHA256<br/>  | "https://www.w3.org/2001/04/xmldsig-more\#hmac-sha256"<br/>  |
| wszURI \_ XMLNS \_ DIGSIG \_ HMAC \_ SHA384<br/>  | "https://www.w3.org/2001/04/xmldsig-more\#hmac-sha384"<br/>  |
| wszURI \_ XMLNS \_ DIGSIG \_ HMAC \_ SHA512<br/>  | "https://www.w3.org/2001/04/xmldsig-more\#hmac-sha512"<br/>  |



 

 

 
