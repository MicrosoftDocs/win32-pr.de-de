---
description: Fügt der Auflistung ein Zertifikat Objekt hinzu.
ms.assetid: 0973018d-1e83-41b4-a250-7dd5be2fb664
title: 'ICertificates2:: Add-Methode'
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
ms.openlocfilehash: d56120c6f584e828c3aadca037d75263d5350f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354681"
---
# <a name="icertificates2add-method"></a>ICertificates2:: Add-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Mit der **Add** -Methode wird der Auflistung ein [**Zertifikat**](certificate.md) Objekt hinzugefügt. Diese Methode wird in CAPICOM 2,0 eingeführt.

## <a name="syntax"></a>Syntax


```VB
Certificates.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zertifikat* \[ in\]
</dt> <dd>

Das [**Zertifikat**](certificate.md) Objekt, das der Auflistung hinzugefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
