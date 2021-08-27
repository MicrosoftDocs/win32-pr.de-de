---
description: Der Microsoft RSA/Schannel Cryptographic Provider unterstützt Hashing, Datensignatur und Signaturüberprüfung.
ms.assetid: 34ede85a-579f-400f-a53e-e40711fcaaf3
title: Microsoft RSA/Schannel Cryptographic Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b38ef6573cada965c0b5e982d7808a7fe2b7670271f4f8ce1fd51c99d002db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100690"
---
# <a name="microsoft-rsaschannel-cryptographic-provider"></a>Microsoft RSA/Schannel Cryptographic Provider

Der Microsoft [*RSA*](../secgloss/r-gly.md) / [*Schannel*](../secgloss/s-gly.md) Cryptographic Provider unterstützt Hashing, Datensignatur und Signaturüberprüfung. Der Algorithmusbezeichner CALG \_ SSL3 \_ SHAMD5 wird für die SSL 3.0- und TLS 1.0-Clientauthentifizierung verwendet. Dieser CSP unterstützt die Schlüsselableitung für die Protokolle SSL2, PCT1, SSL3 und TLS1. Der [*Hash*](../secgloss/h-gly.md) besteht aus einer Verkettung eines MD5-Hashs mit einem SHA-Hash und mit einem privaten [*RSA-Schlüssel*](../secgloss/p-gly.md)signiert. Sie kann in andere Länder/Regionen exportiert werden.



|                   | Wert                         |
|-------------------|-------------------------------|
| **Anbietertyp** | PROV \_ RSA \_ SCHANNEL           |
| **Anbietername** | MS \_ DEF \_ RSA \_ SCHANNEL \_ PROV  |



 

Weitere Informationen zu RSA/Schannel-Anbietern finden Sie unter [CSP-Funktionen.](cryptography-functions.md)

 

 
