---
description: Unterstützt sowohl digitale Signaturen als auch Datenverschlüsselung. Es wird als allgemeiner Kryptografiedienstanbieter (CSP) betrachtet.
ms.assetid: da0b50ec-25a6-40dd-af83-73500b4a4c08
title: PROV_RSA_AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796ac0b77b91b9cffebc6f04ae3812b1bc25aabd885295e7dd3e1715bb4efc04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901590"
---
# <a name="prov_rsa_aes"></a>PROV \_ RSA \_ AES

Der PROV \_ RSA \_ AES-Anbietertyp unterstützt sowohl [digitale Signaturen](digital-signatures.md) als auch datenverschlüsselung. Es wird als [](../secgloss/c-gly.md) allgemeiner Kryptografiedienstanbieter (CSP) betrachtet. Der [*RSA-Algorithmus für öffentliche*](../secgloss/p-gly.md) Schlüssel wird für alle [*Vorgänge mit öffentlichem Schlüssel*](../secgloss/p-gly.md) verwendet.

## <a name="algorithms-supported"></a>Unterstützte Algorithmen

Beschreibungen der einzelnen Algorithmen finden Sie im Glossar.



| Zweck      | Unterstützte Algorithmen                                                                                                                                                                                                                                                                                       |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schlüssel Exchange | [*RSA*](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| Signatur    | [*RSA*](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| Verschlüsselung   | [*RC2*](../secgloss/r-gly.md)<br/> [*RC4*](../secgloss/r-gly.md)<br/> [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES) <br/>                                                       |
| Hashing      | [*MD2*](../secgloss/m-gly.md)<br/> [*MD4*](../secgloss/m-gly.md)<br/> [*MD5*](../secgloss/m-gly.md)<br/> [*SHA-1*](../secgloss/s-gly.md)<br/> SHA-2 (SHA-256, SHA-384 und SHA-512)<br/> |



 

## <a name="related-documentation"></a>Verwandte Dokumentationen

Dieser Anbietertyp wird von Microsoft und RSA Data Security definiert. Dies wird in den folgenden Dokumenten beschrieben:

-   *Microsoft Cryptographic Service Provider Programmer es Guide*, Microsoft, 1996.
-   RSA Rsa Rsas, Public Key Cryptography Standards, RSA Data Security, November 1993.

> [!Note]  
> Diese Ressourcen sind in einigen Sprachen und Ländern oder Regionen möglicherweise nicht verfügbar.

 

 

 
