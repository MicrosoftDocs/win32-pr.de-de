---
description: Ruft den Signatur Geber der signierten ausführbaren Datei ab.
ms.assetid: aafa7006-b47c-4f4e-a5c4-bd96d297f939
title: Signedcode. Signer (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Signer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 053bb6c98c5b8776da2ca890de24359f41be1389
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371647"
---
# <a name="signedcodesigner-property"></a>Signedcode. Signer (Eigenschaft)

\[Die **Signatur** Geber Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen den Platform invoations Dienst (PInvoke) zum Aufrufen der Win32-API [**signersignetx**](signersignex.md)-, [**signertimestampex**](signertimestampex.md)-und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) -Funktionen, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx). Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]

Die **Signatur** Geber-Eigenschaft ruft den Signatur Geber der signierten ausführbaren Datei ab.

## <a name="syntax"></a>Syntax


```VB
SignedCode.Signer As Signer
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**Signatur**](signer.md) Geber Objekt, das Zugriff auf den Signatur Geber der signierten ausführbaren Datei bereitstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Signedcode**](signedcode.md)
</dt> </dl>

 

 
