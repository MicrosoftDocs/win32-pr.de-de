---
description: Entfernt ein einzelnes Certificate-Objekt aus der Auflistung.
ms.assetid: dff82825-1a7d-4c1a-94e2-7f9d1281ecf2
title: ICertificates2::Remove-Methode
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
ms.openlocfilehash: 72ab0624784078b2c496032639c371280ff0019ac957d3c579e2c3c9080629bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770431"
---
# <a name="icertificates2remove-method"></a>ICertificates2::Remove-Methode

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Remove-Methode** entfernt ein einzelnes [**Certificate-Objekt**](certificate.md) aus der Auflistung. Diese Methode wurde in CAPICOM 2.0 eingeführt.

## <a name="syntax"></a>Syntax


```VB
Certificates.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

Indexwert für das [**Zertifikatobjekt,**](certificate.md) das entfernt werden soll. Dieser Parameter kann einer der folgenden möglichen Typen sein.



| type                                                                                                                                                                                                                                                              | Bedeutung                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Long"></span><span id="long"></span><span id="LONG"></span><dl> <dt>"Long"</dt><dt></dt> </dl>                                                | Das [**Certificate-Objekt**](certificate.md) am angegebenen Index in der Auflistung wird entfernt.<br/>                                                                                                          |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <dt>"String"</dt><dt></dt> </dl>                                        | Das erste [**Certificate-Objekt**](certificate.md) in der Auflistung, das dem [*SHA-1-Fingerabdruck*](../secgloss/s-gly.md) in der angegebenen Zeichenfolge entspricht, wird entfernt.<br/> |
| <span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span><dl> <dt>**[**Zertifikat**](certificate.md)**</dt><dt></dt> </dl> | Das erste [**Zertifikatobjekt**](certificate.md) in der Auflistung, das dem angegebenen **Zertifikatobjekt** entspricht, wird entfernt.<br/>                                                                           |



 

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



 

 
