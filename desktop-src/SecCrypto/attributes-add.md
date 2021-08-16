---
description: Fügt der Auflistung ein Attribute-Objekt hinzu.
ms.assetid: dc2fe542-7168-4ffa-a10d-b2c051c4d42c
title: Attributes.Add-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5639a4bed96dcf4cef315b4550cd2982778d6ecc68024364f06eb377cbd8b0d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773515"
---
# <a name="attributesadd-method"></a>Attributes.Add-Methode

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**CryptographicAttributeObjectCollection-Klasse**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System.Security.Cryptography-Namespace.**](/previous-versions/windows/)\]

Die **Add-Methode** fügt der [**Auflistung ein Attribute-Objekt**](attribute.md) hinzu.

## <a name="syntax"></a>Syntax


```VB
Attributes.Add( _
  ByVal Attribute _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Attribut* \[ In\]
</dt> <dd>

Das [**Attributobjekt,**](attribute.md) das am Ende der Auflistung hinzugefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück. Eine Anwendung, die diese Methode verwendet, muss Code enthalten, um eine von dieser Methode ausgelöste Ausnahme zu behandeln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Kryptografieobjekte](cryptography-objects.md)
</dt> <dt>

[**Attribute**](attributes.md)
</dt> </dl>

 

 
