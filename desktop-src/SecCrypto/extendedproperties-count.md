---
description: Ruft die Anzahl der ExtendedProperty-Objekte in der Auflistung ab.
ms.assetid: 50bc8485-7285-4704-80db-c2e0d68e8cb0
title: ExtendedProperties.Count-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c34aa63da5276c573d5c3f260d5d7a5956045813695991756ede6c9f69be29ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007268"
---
# <a name="extendedpropertiescount-property"></a>ExtendedProperties.Count-Eigenschaft

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen Platform Invocation Services (PInvoke), um die Win32-API-Funktion [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) auf aufruft und die Eigenschaften zu erhalten. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zu Plattformaufrufen.](https://msdn.microsoft.com/library/aa288468.aspx) .NET und CryptoAPI über [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Teil 1 und .NET und [CryptoAPI über P/Invoke: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) der Unterabschnitte [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) (Erweitern der .NET-Kryptografie mit CAPICOM und P/Invoke) können ebenfalls hilfreich sein.\]

Die **Count-Eigenschaft** ruft die Anzahl der [**ExtendedProperty-Objekte**](extendedproperty.md) in der Auflistung ab.

## <a name="syntax"></a>Syntax


```VB
ExtendedProperties.Count As Long
```



## <a name="property-value"></a>Eigenschaftswert

Die Anzahl der [**ExtendedProperty-Objekte**](extendedproperty.md) in der Auflistung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
