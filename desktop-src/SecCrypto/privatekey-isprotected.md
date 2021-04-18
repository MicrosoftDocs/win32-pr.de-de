---
description: Gibt einen booleschen Wert zurück, der angibt, ob der private Schlüssel geschützt ist.
ms.assetid: 6a329581-0ff8-45fa-9997-5fcf043287cb
title: PrivateKey. IsProtected-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsProtected
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 33ba72935b2c3f9f9cf537469e043160f9ce2d7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371234"
---
# <a name="privatekeyisprotected-method"></a>PrivateKey. IsProtected-Methode

\[Die **IsProtected** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Certificate2. PrivateKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **IsProtected** -Methode gibt einen booleschen Wert zurück, der angibt, ob der private Schlüssel geschützt ist.

## <a name="syntax"></a>Syntax


```VB
PrivateKey.IsProtected()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

True gibt an, dass der private Schlüssel geschützt ist.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert dieser Methode ist abhängig vom verwendeten [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP). Mit dieser Methode wird ein vertrauenswürdiger Wert zurückgegeben, wenn ein Microsoft CSP verwendet wird. Wenn es sich bei dem CSP nicht um einen Microsoft CSP handelt, kann der Rückgabewert als nicht vertrauenswürdig eingestuft werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
