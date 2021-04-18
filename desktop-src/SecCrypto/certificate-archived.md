---
description: Legt einen booleschen Wert fest, der angibt, ob das Zertifikat archiviert ist, oder ruft diesen ab.
ms.assetid: a6526b0e-e76b-4f03-a6ba-9e380e362364
title: Certificate. archiviert (Eigenschaft)
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
ms.openlocfilehash: e1d8cdea3e43bbe10ee87f8f4aa605740a15e6ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372006"
---
# <a name="certificatearchived-property"></a>Certificate. archiviert (Eigenschaft)

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **Archivierte** Eigenschaft legt einen booleschen Wert fest oder ruft ihn ab, der angibt, ob das Zertifikat archiviert ist.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Certificate.Archived As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

Ein boolescher Wert, der angibt, ob das Zertifikat archiviert ist. **True** gibt an, dass das Zertifikat archiviert wird. Beachten Sie, dass das Zertifikat durch Ändern des Werts von **false** in **true** archiviert wird.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft löst CAPICOM \_ E \_ nicht \_ zulässig aus, wenn eine Skripterstellung aus einer webbasierten Anwendung erfolgt.

> [!Note]  
> Ein archiviertes Zertifikat ist auf der Benutzeroberfläche der Zertifikat Verwaltung nicht sichtbar. Außerdem werden Archivierte Zertifikate nicht in die [**Store. Open**](store-open.md) -Methode eingeschlossen, es sei denn, dass CAPICOM \_ Store \_ Open \_ include \_ archiviert angegeben wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
