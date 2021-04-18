---
description: Ruft die Anzahl der EKU-Objekte in der Auflistung ab.
ms.assetid: a38ac480-4f9b-4d69-a7e6-fae4993fe2cf
title: EKUs. Count-Eigenschaft
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
ms.openlocfilehash: 41e77f3803fa65db1573c6619ebf1265b7418924
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354700"
---
# <a name="ekuscount-property"></a>EKUs. Count-Eigenschaft

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ExtensionCollection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **count** -Eigenschaft ruft die Anzahl der [**EKU**](eku.md) -Objekte in der Auflistung ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
EKUs.Count As Long
```



## <a name="property-value"></a>Eigenschaftswert

Die Anzahl der [**EKU**](eku.md) -Objekte in der Auflistung. Jedes **EKU** -Objekt stellt eine einzelne EKU (Extended Key Usage)-Eigenschaft eines Zertifikats dar.

## <a name="remarks"></a>Bemerkungen

Die **count** -Eigenschaft kann verwendet werden, um das letzte [**EKU**](eku.md) -Objekt in einer Auflistung anzugeben, wenn ein bestimmtes **EKU** -Objekt mithilfe der [**EKUs. Item**](ekus-item.md) -Eigenschaft abgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
