---
description: Löscht den Zertifikat Speicher, der durch das aktuelle Speicher Objekt dargestellt wird.
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
ms.openlocfilehash: 41c6417dae5006eb2ecaf64660fd0007cdf37fd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360456"
---
# <a name="storedelete-method"></a>Store. Delete-Methode

\[Die **Delete** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Store-Klasse**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Mit der **Delete** -Methode wird der [*Zertifikat Speicher*](../secgloss/c-gly.md) gelöscht, der durch das aktuelle [**Speicher**](certificate.md) Objekt dargestellt wird. Mit dieser Methode werden nur nicht-Systemspeicher gelöscht.

## <a name="syntax"></a>Syntax


```VB
Store.Delete()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die folgenden Speicher sind Systemspeicher und können nicht gelöscht werden:

-   My
-   Root
-   Vertrauensstellung
-   CA
-   Userds
-   TrustedPublisher
-   Unzulässig
-   AuthRoot
-   TrustedPeople

Die **Delete** -Methode gibt einen Fehler zurück, wenn Sie von einem Webskript aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,1 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Speicher**](store.md)
</dt> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 
