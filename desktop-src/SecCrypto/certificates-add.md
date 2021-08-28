---
description: Fügt der Auflistung ein Certificate-Objekt hinzu.
ms.assetid: 0973018d-1e83-41b4-a250-7dd5be2fb664
title: ICertificates2::Add-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Add
- ICertificates2.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d4de1c00e3f006a69fa3c6babfa2aa44a1ad618050e5802ac4c9578dc3f93937
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101050"
---
# <a name="icertificates2add-method"></a>ICertificates2::Add-Methode

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Add-Methode** fügt der Auflistung ein [**Certificate-Objekt**](certificate.md) hinzu. Diese Methode wird in CAPICOM 2.0 eingeführt.

## <a name="syntax"></a>Syntax


```VB
Certificates.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zertifikat* \[ In\]
</dt> <dd>

Das [**Certificate-Objekt,**](certificate.md) das der Auflistung hinzugefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
