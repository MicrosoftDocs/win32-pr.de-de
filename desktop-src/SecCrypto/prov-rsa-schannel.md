---
description: Unterstützt sowohl RSA-als auch SChannel-Protokolle.
ms.assetid: f0c11a04-7931-424a-b085-0cc584ea7bb7
title: PROV_RSA_SCHANNEL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a76d7f5339f2e7f60ac34705437b1ef0a773fd6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758047"
---
# <a name="prov_rsa_schannel"></a>Prov \_ RSA \_ SChannel

Der Prov \_ RSA \_ SChannel-Anbietertyp unterstützt sowohl RSA-als auch [*SChannel*](../secgloss/s-gly.md) -Protokolle.

## <a name="algorithms-supported"></a>Unterstützte Algorithmen

Beschreibungen der einzelnen Algorithmen finden Sie im Glossar.



| Zweck      | Unterstützte Algorithmen                                                                                                                                                                                                                                                                                                          |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schlüsselaustausch | [*RSA*](../secgloss/r-gly.md)                                                                                                                                                                                                                                                                   |
| Signatur    | RSA                                                                                                                                                                                                                                                                                                                           |
| Verschlüsselung   | Jeder Prov \_ RSA \_ SChannel CSP muss mindestens einen der folgenden Algorithmen implementieren: [ *RC4*](../secgloss/r-gly.md)<br/> [*DES*](../secgloss/d-gly.md)<br/> [*Triple DES*](../secgloss/t-gly.md)<br/> |
| Hashing      | [*MD5*](../secgloss/m-gly.md)-[*SHA*](../secgloss/s-gly.md)<br/>                                                                                                                                                                                             |



 

 

 
