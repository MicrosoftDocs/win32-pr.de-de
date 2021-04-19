---
description: Entfernt ein einzelnes Zertifikat Objekt aus der Auflistung.
ms.assetid: dff82825-1a7d-4c1a-94e2-7f9d1281ecf2
title: 'ICertificates2:: Remove-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Remove
- ICertificates2.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6a2f9336a420f1d014e178f67cae02cf85f0fd44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359748"
---
# <a name="icertificates2remove-method"></a>ICertificates2:: Remove-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **Remove** -Methode entfernt ein einzelnes [**Zertifikat**](certificate.md) Objekt aus der Auflistung. Diese Methode wurde in CAPICOM 2,0 eingeführt.

## <a name="syntax"></a>Syntax


```VB
Certificates.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

Der Indexwert für das zu entfernende [**Zertifikat**](certificate.md) Objekt. Dieser Parameter kann einen der folgenden möglichen Typen aufweisen.



| type                                                                                                                                                                                                                                                              | Bedeutung                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Long"></span><span id="long"></span><span id="LONG"></span><dl> <dt>* * * * Long * *</dt> * * <dt></dt> </dl>                                                | Das [**Zertifikat**](certificate.md) Objekt am angegebenen Index in die Auflistung wird entfernt.<br/>                                                                                                          |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <dt>* * * * Zeichenfolge * *</dt> * * <dt></dt> </dl>                                        | Das erste [**Zertifikat**](certificate.md) Objekt in der Auflistung, das mit dem in der angegebenen Zeichenfolge enthaltenen [*SHA-1-*](../secgloss/s-gly.md) Fingerabdruck übereinstimmt, wird entfernt.<br/> |
| <span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span><dl> <dt>**[**Zertifikat**](certificate.md)**</dt><dt></dt> </dl> | Das erste [**Zertifikat**](certificate.md) Objekt in der Auflistung, das mit dem angegebenen **Zertifikat** Objekt übereinstimmt, wird entfernt.<br/>                                                                           |



 

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



 

 
