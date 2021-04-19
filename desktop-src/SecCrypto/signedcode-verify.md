---
description: Überprüft die Authenticode-Signatur für den signierten Code.
ms.assetid: eecd692d-6b20-4644-a3d9-fba07ee667d7
title: Signedcode. Verify-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ad9ad2cdbf9c8b7970f50446bba0da7a3afdcd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370823"
---
# <a name="signedcodeverify-method"></a>Signedcode. Verify-Methode

\[Die **Verifizierungs** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen den Platform invoations Dienst (PInvoke) zum Aufrufen der Win32-API [**signersignetx**](signersignex.md)-, [**signertimestampex**](signertimestampex.md)-und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) -Funktionen, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx). Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]

Die **Verify** -Methode überprüft die Authenticode-Signatur für den signierten Code.

## <a name="syntax"></a>Syntax


```VB
SignedCode.Verify( _
  [ ByVal bUIAllowed ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

für den Kauf *zulässig* \[ in, optional\]
</dt> <dd>

Ein boolescher Wert, der angibt, ob ein Dialogfeld verwendet wird, um die Signatur zu überprüfen. True gibt an, dass ein Dialogfeld generiert wird, um zu bestimmen, ob der Code vertrauenswürdig ist. Der Standardwert ist „FALSE“.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Signedcode**](signedcode.md)
</dt> </dl>

 

 
