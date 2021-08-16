---
description: Legt einen booleschen Wert fest, der angibt, ob das Zertifikat archiviert wird, oder ruft diesen ab.
ms.assetid: a6526b0e-e76b-4f03-a6ba-9e380e362364
title: Certificate.Archived-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Archived
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d2e3ab848caa24cb77a8cb45e992eeac7365af0de743fa148b07b484239fa658
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771949"
---
# <a name="certificatearchived-property"></a>Certificate.Archived-Eigenschaft

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Eigenschaft Archiviert** legt einen booleschen Wert fest oder ruft diesen ab, der angibt, ob das Zertifikat archiviert wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Certificate.Archived As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

Ein boolescher Wert, der angibt, ob das Zertifikat archiviert wird. True gibt an, dass das Zertifikat archiviert wird. Beachten Sie, dass das Zertifikat durch Ändern des Werts von **FALSE** in **TRUE** archiviert wird.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft löst CAPICOM \_ E \_ NOT ALLOWED \_ aus, wenn ein Skript aus einer webbasierten Anwendung erstellt wird.

> [!Note]  
> Ein archiviertes Zertifikat ist auf der Benutzeroberfläche der Zertifikatverwaltung nicht sichtbar. Außerdem werden archivierte Zertifikate nicht in die [**Store eingeschlossen. Open-Methode,**](store-open.md) es sei denn, CAPICOM \_ STORE OPEN INCLUDE \_ \_ \_ ARCHIVED ist angegeben.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
