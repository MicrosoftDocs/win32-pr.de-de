---
description: Gibt ein basiceinschränkungs-Objekt zurück, das die grundlegende Einschränkungs Erweiterung des Zertifikats darstellt.
ms.assetid: cc4e566a-5f68-4e28-9397-39f22a71e45b
title: 'ICertificate2:: basiceinschränkungs-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.BasicConstraints
- ICertificate2.BasicConstraints
- ICertificate.BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b511781c29d313715e7714f185dbff7e4b38f86c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360445"
---
# <a name="icertificate2basicconstraints-method"></a>ICertificate2:: basiceinschränkungs-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **basiceinschränkungs** -Methode gibt ein [**basiceinschränkungs**](basicconstraints.md) -Objekt zurück, das die grundlegende Einschränkungs Erweiterung des Zertifikats darstellt.

## <a name="syntax"></a>Syntax


```VB
Certificate.BasicConstraints()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Das [**basiceinschränkunsobjekt**](basicconstraints.md) , das die grundlegende Einschränkungs Erweiterung des Zertifikats darstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
