---
description: Löscht den Zertifikatspeicher, der durch das aktuelle Store dargestellt wird.
ms.assetid: 274914ee-27a0-4bd6-8510-af897aab3a2d
title: Store. Delete-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36c4a02795468ca719790707356b12a1aa24c1882a0cf57faa9e0454af33467a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117972651"
---
# <a name="storedelete-method"></a>Store. Delete-Methode

\[Die **Delete-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**X509Store-Klasse**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Delete-Methode** löscht den [*Zertifikatspeicher,*](../secgloss/c-gly.md) der durch das aktuelle Store [**wird.**](certificate.md) Diese Methode löscht nur Nichtsystemspeicher.

## <a name="syntax"></a>Syntax


```VB
Store.Delete()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die folgenden Speicher sind Systemspeicher und können nicht gelöscht werden:

-   My
-   Root
-   Vertrauensstellung
-   CA
-   UserDS
-   TrustedPublisher
-   Unzulässig
-   AuthRoot
-   TrustedPeople

Die **Delete-Methode** gibt einen Fehler zurück, wenn sie von einem Webskript aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.1 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Speicher**](store.md)
</dt> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 
