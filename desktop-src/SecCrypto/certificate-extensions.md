---
description: Gibt eine Auflistung der Erweiterungen zurück, die dem Zertifikat zugeordnet sind.
ms.assetid: 07793061-6f94-4467-bb01-aa65db657658
title: ICertificate2::Extensions-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Extensions
- ICertificate2.Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e700fda2fb99e0ea0a3dfd8690fdfedbdeecb21bc84bfdb08cbf1f179536cbef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771612"
---
# <a name="icertificate2extensions-method"></a>ICertificate2::Extensions-Methode

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Extensions-Methode** gibt eine Auflistung der Erweiterungen zurück, die dem Zertifikat zugeordnet sind. Diese Methode wird in CAPICOM 2.0 eingeführt.

## <a name="syntax"></a>Syntax


```VB
Certificate.Extensions()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Ein [](extensions.md) Extensions-Objekt, das alle erweiterungen darstellt, die dem Zertifikat zugeordnet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
