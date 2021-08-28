---
description: Gibt ein BasicConstraints-Objekt zurück, das die grundlegende Einschränkungserweiterung des Zertifikats darstellt.
ms.assetid: cc4e566a-5f68-4e28-9397-39f22a71e45b
title: ICertificate2::BasicConstraints-Methode
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
ms.openlocfilehash: 8958a942a8c56dfe39c8a96bcf3f80cefcb7978feac186a80432cbe8f03b5c4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127150"
---
# <a name="icertificate2basicconstraints-method"></a>ICertificate2::BasicConstraints-Methode

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **BasicConstraints-Methode** gibt ein [**BasicConstraints-Objekt**](basicconstraints.md) zurück, das die grundlegende Einschränkungserweiterung des Zertifikats darstellt.

## <a name="syntax"></a>Syntax


```VB
Certificate.BasicConstraints()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Das [**BasicConstraints-Objekt,**](basicconstraints.md) das die grundlegende Einschränkungserweiterung des Zertifikats darstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
