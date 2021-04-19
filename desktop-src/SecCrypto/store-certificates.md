---
description: Ruft die-Auflistung ab, die alle Zertifikate im Speicher enthält.
ms.assetid: 06cfc0e9-8a77-4e10-b559-4d42ac93c01b
title: Store. Zertifikats (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 979cf31c98286ca5bdd2df709176a27a5abb2321
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356459"
---
# <a name="storecertificates-property"></a>Store. Zertifikats (Eigenschaft)

\[Die Eigenschaft **Zertifikate** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**X509Store-Klasse**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Mit der Eigenschaft **Zertifikate** wird die Sammlung abgerufen, die alle Zertifikate im Speicher enthält. Dies ist die Standard Eigenschaft.

## <a name="syntax"></a>Syntax


```VB
Store.Certificates As Certificates
```



## <a name="property-value"></a>Eigenschaftswert

Die Sammlung der Zertifikate im Speicher.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Speicher**](store.md)
</dt> </dl>

 

 
