---
description: Mit Hash-und digitalen Signatur Funktionen kann ein Benutzerdaten digital signieren, sodass jeder andere Benutzer überprüfen kann, ob die Daten seit der Signierung geändert wurden. Die Identität des Benutzers, der die Daten signiert hat, kann auch überprüft werden.
ms.assetid: dbe70506-f0d9-4239-a3af-8494fd6d4149
title: Hashes und digitale Signaturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc2894cbf53834551afef375fb5056df89675a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363648"
---
# <a name="hashes-and-digital-signatures"></a>Hashes und digitale Signaturen

Mit [Hash-und digitalen Signatur Funktionen](cryptography-functions.md)kann ein Benutzerdaten digital signieren, sodass jeder andere Benutzer überprüfen kann, ob die Daten seit der Signierung geändert wurden. Die Identität des Benutzers, der die Daten signiert hat, kann auch überprüft werden.

Eine [*digitale Signatur*](../secgloss/d-gly.md) besteht aus einer kleinen Menge an Binärdaten, in der Regel weniger als 256 Bytes. Diese Signatur kann mit der signierten Nachricht gebündelt oder separat gespeichert werden, je nachdem, wie eine bestimmte Anwendung implementiert wurde.

Der starke Kryptografieanbieter von Microsoft erstellt digitale Signaturen, die den RSA-PKCS ( [*Public Key Cryptography Standards*](../secgloss/p-gly.md) ) \# 1 entsprechen.

 

 
