---
description: Unterstützt sowohl digitale Signaturen als auch Datenverschlüsselung. Es gilt als allgemeiner Kryptografiedienstanbieter (CSP).
ms.assetid: da0b50ec-25a6-40dd-af83-73500b4a4c08
title: PROV_RSA_AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fa8d01e9fd212f2c39ab5615b12931738bc926
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042690"
---
# <a name="prov_rsa_aes"></a>Prov \_ RSA \_ AES

Der Prov \_ RSA \_ AES-Anbietertyp unterstützt sowohl [digitale Signaturen](digital-signatures.md) als auch Datenverschlüsselung. Es gilt als allgemeiner [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP). Der RSA- [*Algorithmus für öffentliche*](../secgloss/p-gly.md) Schlüssel wird für alle Vorgänge mit [*öffentlichem Schlüssel*](../secgloss/p-gly.md) verwendet.

## <a name="algorithms-supported"></a>Unterstützte Algorithmen

Beschreibungen der einzelnen Algorithmen finden Sie im Glossar.



| Zweck      | Unterstützte Algorithmen                                                                                                                                                                                                                                                                                       |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schlüsselaustausch | [*RSA*](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| Signatur    | [*RSA*](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| Verschlüsselung   | [*RC2*](../secgloss/r-gly.md)<br/> [*RC4*](../secgloss/r-gly.md)<br/> [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES) <br/>                                                       |
| Hashing      | [*MD2*](../secgloss/m-gly.md)<br/> [*MD4*](../secgloss/m-gly.md)<br/> [*MD5*](../secgloss/m-gly.md)<br/> [*SHA-1*](../secgloss/s-gly.md)<br/> SHA-2 (SHA-256, SHA-384 und SHA-512)<br/> |



 

## <a name="related-documentation"></a>Verwandte Dokumentationen

Dieser Anbietertyp wird von Microsoft und RSA-Datensicherheit definiert. Dies wird in den folgenden Dokumenten beschrieben:

-   *Microsoft Kryptografiedienstanbieter-Programmierer*, Microsoft, 1996.
-   RSA-Laboratorien, Kryptografiestandards für öffentliche Schlüssel, RSA-Datensicherheit, November 1993.

> [!Note]  
> Diese Ressourcen sind möglicherweise in einigen Sprachen und Ländern oder Regionen nicht verfügbar.

 

 

 
