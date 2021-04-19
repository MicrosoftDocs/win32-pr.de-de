---
description: Cryptxml bietet einen Low-Level-Satz an APIs, mit denen Anwendungen eingehüllte, umhüllende und getrennte Signaturen erstellen und überprüfen können. Sie können cryptxml zum Erstellen und Überprüfen von Inhalten verwenden, die in Signatur Objekt Elementen, einschließlich Manifesten, gespeichert sind.
ms.assetid: 962dffdb-caa6-4aa7-b5c6-3a9de8cfaf6c
title: XML-Funktionen der digitalen Signatur-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ae330fdd8ba75ece885e8ed0b7e2c91e60fc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362502"
---
# <a name="xml-digital-signature-api-functionality"></a>XML-Funktionen der digitalen Signatur-API

Cryptxml bietet einen Low-Level-Satz an APIs, mit denen Anwendungen eingehüllte, umhüllende und getrennte Signaturen erstellen und überprüfen können. Sie können cryptxml zum Erstellen und Überprüfen von Inhalten verwenden, die in Signatur Objekt Elementen, einschließlich Manifesten, gespeichert sind. Ein öffentlicher/privater, gemeinsam verwendeter Schlüssel oder ein [*X. 509*](../secgloss/x-gly.md) -Zertifikat oder eine Zertifikat Kette kann zum Signieren und Überprüfen der digitalen XML- [*Signatur*](../secgloss/d-gly.md)verwendet werden.

Anwendungen, die cryptxml zum Überprüfen externer Verweise verwenden (Verweise, die auf ein externes Dokument oder eine externe Datei außerhalb des Dokument Kontexts abzielen), müssen die externen URIs auflösen und die zu verdauenden Daten abrufen.

Informationen zu den kryptografischen Algorithmen, die von cryptxml unterstützt werden, finden Sie unter [Kryptografiealgorithmen für die digitale XML-Signatur](xml-digital-signature-cryptographic-algorithms.md)

Cryptxml bietet Unterstützung für Kanonisierungsalgorithmen mit den folgenden bezeichlern.



| Konstante                                              | URI-Wert                                                                  |
|-------------------------------------------------------|----------------------------------------------------------------------------|
| wszuri- \_ Kanonisierung \_ C14N<br/>             | "https://www.w3.org/TR/2001/REC-xml-c14n-20010315"<br/>               |
| wszuri- \_ Kanonisierung \_ C14NC<br/>            | "https://www.w3.org/TR/2001/REC-xml-c14n-20010315\#WithComments"<br/> |
| wszuri \_ Canonicalization \_ exslusive \_ C14N<br/>  | "https://www.w3.org/2001/10/xml-exc-c14n\#"<br/>                      |
| wszuri \_ Canonicalization \_ exslusive \_ C14NC<br/> | "https://www.w3.org/2001/10/xml-exc-c14n\#WithComments"<br/>          |



 

Cryptxml bietet Unterstützung für die Transformation für eingeschlossene Signaturen.



| Konstante                                       | URI-Wert                                                           |
|------------------------------------------------|---------------------------------------------------------------------|
| wszuri \_ xmlns- \_ Transformation \_<br/> | "https://www.w3.org/2000/09/xmldsig\#enveloped-signature"<br/> |



 

Standardmäßig unterstützt cryptxml keine XPath-oder XSLT-Transformationen. Wenn dies erforderlich ist, können Anwendungen diese Transformationen zusätzlich zu "cryptxml" implementieren.

 

 
