---
description: Cryptxml unterstützt nativ die unten aufgeführten URIs.
ms.assetid: 012bad01-228a-4bb0-b883-0c2c7abd9271
title: Kryptografiealgorithmen für die digitale XML-Signatur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896348375d1d1a51288980aad3793dfffc69eb18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349008"
---
# <a name="xml-digital-signature-cryptographic-algorithms"></a>Kryptografiealgorithmen für die digitale XML-Signatur

Cryptxml unterstützt nativ die unten aufgeführten URIs. Wenn für kryptografische Algorithmen und Transformationen, die nicht Teil der systemeigenen Unterstützung sind, Unterstützung benötigt wird, können Sie [kryptografieapi: Next Generation](../seccng/cng-portal.md) und [kryptografische Erweiterungen der XML-Signatur](xml-digital-signature-cryptographic-extensions.md) verwenden, um neue Algorithmen zu unterstützen.

## <a name="supported-uris"></a>Unterstützte URIs

Digest-Methoden



| Konstante                                 | URI-Wert                                                   |
|------------------------------------------|-------------------------------------------------------------|
| wszuri \_ xmlns \_ digsig \_ SHA1<br/>   | "https://www.w3.org/2000/09/xmldsig\#sha1"<br/>        |
| wszuri \_ xmlns \_ digsig \_ SHA256<br/> | "https://www.w3.org/2001/04/xmlenc\#sha256"<br/>       |
| wszuri \_ xmlns \_ digsig \_ SHA384<br/> | "https://www.w3.org/2001/04/xmldsig-more\#sha384"<br/> |
| wszuri \_ xmlns \_ digsig \_ SHA512<br/> | "https://www.w3.org/2001/04/xmlenc\#sha512"<br/>       |



 

Signatur Methoden



| Konstante                                        | URI-Wert                                                         |
|-------------------------------------------------|-------------------------------------------------------------------|
| wszuri \_ xmlns- \_ \_ RSA \_ SHA1<br/>     | "https://www.w3.org/2000/09/xmldsig\#rsa-sha1"<br/>          |
| wszuri \_ xmlns \_ digsig \_ DSA \_ SHA1<br/>     | "https://www.w3.org/2000/09/xmldsig\#dsa-sha1"<br/>          |
| wszuri \_ xmlns \_ digsig \_ RSA \_ SHA256<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#rsa-sha256"<br/>   |
| wszuri \_ xmlns \_ digsig \_ RSA \_ SHA384<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#rsa-sha384"<br/>   |
| wszuri \_ xmlns \_ digsig \_ RSA \_ SHA512<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#rsa-sha512"<br/>   |
| wszuri \_ xmlns- \_ \_ ECDSA \_ SHA1<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha1"<br/>   |
| wszuri \_ xmlns- \_ \_ ECDSA \_ SHA256<br/> | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha256"<br/> |
| wszuri \_ xmlns- \_ \_ ECDSA \_ SHA384<br/> | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha384"<br/> |
| wszuri \_ xmlns- \_ \_ ECDSA \_ SHA512<br/> | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha512"<br/> |
| wszuri \_ xmlns \_ \_ HMAC \_ SHA1<br/>    | "https://www.w3.org/2000/09/xmldsig\#hmac-sha1"<br/>         |
| wszuri \_ xmlns \_ \_ HMAC \_ SHA256<br/>  | "https://www.w3.org/2001/04/xmldsig-more\#hmac-sha256"<br/>  |
| wszuri \_ xmlns \_ \_ HMAC \_ SHA384<br/>  | "https://www.w3.org/2001/04/xmldsig-more\#hmac-sha384"<br/>  |
| wszuri \_ xmlns \_ \_ HMAC \_ SHA512<br/>  | "https://www.w3.org/2001/04/xmldsig-more\#hmac-sha512"<br/>  |



 

 

 
