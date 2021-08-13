---
description: Entfernt alle Certificate-Objekte aus einer Empfängerauflistung.
ms.assetid: 456fcfbc-4388-40f4-ab58-04508ee2141b
title: Recipients.Clear-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c956aacd7b61243fbaeb26ed1a29ed0fee4522d83d8b4ef3ac25b3b1921b42a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900807"
---
# <a name="recipientsclear-method"></a>Recipients.Clear-Methode

\[Die **Clear-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**CmsRecipientCollection-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System.Security.Cryptography.Pkcs-Namespace.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Die **Clear-Methode** entfernt alle [**Certificate-Objekte**](certificate.md) aus einer [**Recipients-Auflistung.**](recipients.md)

## <a name="syntax"></a>Syntax


```VB
Recipients.Clear()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück. Eine Anwendung, die diese Methode verwendet, muss Code enthalten, um eine von dieser Methode ausgelöste Ausnahme zu behandeln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> <dt>

[**Empfänger**](recipients.md)
</dt> </dl>

 

 
