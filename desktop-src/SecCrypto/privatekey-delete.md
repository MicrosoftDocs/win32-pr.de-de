---
description: Löscht den Container für den privaten Schlüssel, auf den vom PrivateKey-Objekt verwiesen wird.
ms.assetid: 80bbe46b-1ec5-4d47-82b0-5a3177f86389
title: PrivateKey. Delete-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dc5778e631abba9eb8cf122ddb99a4692c988f4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370585"
---
# <a name="privatekeydelete-method"></a>PrivateKey. Delete-Methode

\[Die **Delete** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Certificate2. PrivateKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **Delete** -Methode löscht den Container für den privaten Schlüssel, auf den vom [**PrivateKey**](privatekey.md) -Objekt verwiesen wird.

## <a name="syntax"></a>Syntax


```VB
PrivateKey.Delete()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

> [!IMPORTANT]
> Diese Methode löscht den Container für den privaten Schlüssel, auf den vom [**PrivateKey**](privatekey.md) -Objekt und allen privaten Schlüsseln im Container verwiesen wird. Alle Elemente, die mit den öffentlichen Schlüsseln verschlüsselt werden, die den gelöschten privaten Schlüsseln entsprechen, können nicht mehr entschlüsselt werden.

 

Diese Methode löst CAPICOM \_ E \_ nicht \_ zulässig aus, wenn eine Skripterstellung aus einer webbasierten Anwendung erfolgt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
