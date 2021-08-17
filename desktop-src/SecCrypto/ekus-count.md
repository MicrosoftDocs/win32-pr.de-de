---
description: Ruft die Anzahl der EKU-Objekte in der Auflistung ab.
ms.assetid: a38ac480-4f9b-4d69-a7e6-fae4993fe2cf
title: EKUs.Count-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4ef512c62058d2f4726c21aa8631fef5230ec35ecfe39a3b8dc5470fc93b74e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767164"
---
# <a name="ekuscount-property"></a>EKUs.Count-Eigenschaft

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ExtensionCollection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Count-Eigenschaft** ruft die Anzahl der [**EKU-Objekte**](eku.md) in der Auflistung ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
EKUs.Count As Long
```



## <a name="property-value"></a>Eigenschaftswert

Die Anzahl der [**EKU-Objekte**](eku.md) in der Auflistung. Jedes **EKU-Objekt** stellt eine einzelne EKU-Eigenschaft (Extended Key Usage) eines Zertifikats dar.

## <a name="remarks"></a>Hinweise

Die **Count-Eigenschaft** kann verwendet werden, um das letzte [**EKU-Objekt**](eku.md) in einer Auflistung anzugeben, wenn ein bestimmtes **EKU-Objekt** mithilfe der [**EKUs.Item-Eigenschaft abgerufen**](ekus-item.md) wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
