---
description: Mit Hash- und Digital Signature Functions kann ein Benutzer Daten digital signieren, sodass jeder andere Benutzer überprüfen kann, ob die Daten seit der Signatur nicht geändert wurden. Die Identität des Benutzers, der die Daten signiert hat, kann ebenfalls überprüft werden.
ms.assetid: dbe70506-f0d9-4239-a3af-8494fd6d4149
title: Hashes und digitale Signaturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd6367217343a067bbdd0d5a4ad5e9f4f47e9b744ee9f159046259ec2e26185
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006488"
---
# <a name="hashes-and-digital-signatures"></a>Hashes und digitale Signaturen

Mit [Hash- und Digital Signature Functions](cryptography-functions.md)kann ein Benutzer Daten digital signieren, sodass jeder andere Benutzer überprüfen kann, ob die Daten seit der Signatur nicht geändert wurden. Die Identität des Benutzers, der die Daten signiert hat, kann ebenfalls überprüft werden.

Eine [*digitale Signatur*](../secgloss/d-gly.md) besteht aus einer kleinen Menge binärer Daten, in der Regel weniger als 256 Bytes. Diese Signatur kann mit der signierten Nachricht gebündelt oder separat gespeichert werden, je nachdem, wie eine bestimmte Anwendung implementiert wurde.

Der starke Kryptografieanbieter von Microsoft erstellt digitale Signaturen, die den RSA [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \# 1 entsprechen.

 

 
