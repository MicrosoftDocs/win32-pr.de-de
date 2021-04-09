---
description: Die folgenden Eigenschaften werden von der icertrvsetupkeyinformation-Schnittstelle definiert.
ms.assetid: d805a011-8728-4687-8e4a-ad331617abe7
title: Eigenschaften von icertrvsetupkeyinformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2a41647c06015c011d4d7a36cddfd81466b3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865455"
---
# <a name="properties-of-icertsrvsetupkeyinformation"></a>Eigenschaften von icertrvsetupkeyinformation

Die folgenden Eigenschaften werden von der [**icertrvsetupkeyinformation**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetupkeyinformation) -Schnittstelle definiert.



| Eigenschaft                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Container Name**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_containername)                 | Ruft den Namen des [*Kryptografiedienstanbieters (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) zum generieren, speichern oder zugreifen auf den Schlüssel ab oder legt ihn fest.                                                                       |
| [**Vorhanden**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existing)                           | Dient zum Abrufen oder Festlegen eines Werts, der angibt, ob der private Schlüssel bereits vorhanden ist.                                                                                                                                                                                                                       |
| [**Existingcacertificate**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existingcacertificate) | Ruft den binären Wert ab, der mit [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) codiert wurde, oder legt diesen fest, der der binäre Wert des Zertifizierungsstellen Zertifikats ist, das einem vorhandenen Schlüssel entspricht. |
| [**HashAlgorithm**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_hashalgorithm)                 | Ruft den Namen des Hash Algorithmus ab, mit dem das Zertifizierungsstellen Zertifikat für den Schlüssel signiert oder überprüft wird, oder legt ihn fest.                                                                                                                                                                                                |
| [**Länge**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_length)                               | Ruft die Stärke des Schlüssels zu einem der vom CSP unterstützten Werte ab oder legt diese fest.                                                                                                                                                                                                                   |
| [**ProviderName**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_providername)                   | Ruft den Namen des CSP ab, der zum Generieren oder Speichern des privaten Schlüssels verwendet wird, oder legt ihn fest.                                                                                                                                                                                                               |



 

 

 
