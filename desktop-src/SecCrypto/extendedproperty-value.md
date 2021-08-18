---
description: Legt die erweiterten Eigenschaftsdaten fest oder ruft sie ab.
ms.assetid: 115bb52a-e64d-4d84-a491-35f6dba25a58
title: ExtendedProperty.Value-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperty.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b2210457bc984aca561a87424edd8496d5913190910f898654cd10955314e6f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007068"
---
# <a name="extendedpropertyvalue-property"></a>ExtendedProperty.Value-Eigenschaft

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen Platform Invocation Services (PInvoke), um die Win32-API-Funktion [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) aufzurufen und die Eigenschaften abzurufen. Informationen zu PInvoke finden Sie unter [Tutorial zu Plattformaufrufen.](https://msdn.microsoft.com/library/aa288468.aspx) Die [Unterabschnitte .NET und CryptoAPI über P/Invoke: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.NET und CryptoAPI über P/Invoke: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) der Erweiterung der [.NET-Kryptografie mit CAPICOM und P/Invoke](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]

Die **Value-Eigenschaft** legt die erweiterten Eigenschaftsdaten fest oder ruft sie ab.

## <a name="syntax"></a>Syntax


```VB
ExtendedProperty.Value( _
  [ ByVal EncodingType ] _
) As String
```



## <a name="property-value"></a>Eigenschaftswert

Die erweiterten Eigenschaftsdaten in dem durch *EncodingType* angegebenen Format.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
