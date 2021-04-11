---
description: Der Kryptografieanbieter Microsoft RSA/SChannel unterstützt Hashwert, Daten Signierung und Signatur Überprüfung.
ms.assetid: 34ede85a-579f-400f-a53e-e40711fcaaf3
title: Kryptografieanbieter für Microsoft RSA/SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9420849d62c0b728d8f3dbccc4210de3a1394308
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958999"
---
# <a name="microsoft-rsaschannel-cryptographic-provider"></a>Kryptografieanbieter für Microsoft RSA/SChannel

Der Kryptografieanbieter von Microsoft [*RSA*](../secgloss/r-gly.md) / [*SChannel*](../secgloss/s-gly.md) unterstützt Hashwert, Daten Signierung und Signatur Überprüfung. Der Algorithmusbezeichner calg \_ SSL3 \_ SHAMD5 wird für SSL 3,0-und TLS 1,0-Client Authentifizierung verwendet. Dieser CSP unterstützt die Schlüssel Ableitung für die Protokolle SSL2 verwendet, das PCT1 verwendet, SSL3 und das TLS1 verwendet. Der [*Hash*](../secgloss/h-gly.md) besteht aus einer Verkettung eines MD5-Hashs mit einem SHA-Hash und der Signierung mit einem privaten RSA- [*Schlüssel*](../secgloss/p-gly.md). Sie kann in andere Länder/Regionen exportiert werden.



|                |                                  |
|----------------|----------------------------------|
| Anbietertyp: | **Prov \_ RSA \_ SChannel**          |
| Anbieter Name: | **MS \_ DEF \_ RSA \_ SChannel \_ Prov** |



 

Weitere Informationen zu RSA/SChannel-Anbietern finden Sie unter [CSP-Funktionen](cryptography-functions.md).

 

 
