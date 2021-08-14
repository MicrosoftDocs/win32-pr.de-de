---
description: Die FileName-Eigenschaft legt den Pfad zur ausführbaren Datei fest oder ruft diesen ab. Dies ist die Standardeigenschaft.
ms.assetid: 2d2ea87b-86db-40b4-b052-8503beafa08c
title: SignedCode.FileName(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.FileName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 981ff6e1343f836ef145d1dac8c66b93d7a89c885a04cb2fe024740d7e35a53d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900380"
---
# <a name="signedcodefilename-property"></a>SignedCode.FileName(Eigenschaft)

\[Die **FileName-Eigenschaft** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen Platform Invocation Services (PInvoke), um die Win32-API-Funktionen [**SignerSignEx,**](signersignex.md) [**SignerTimeStampEx**](signertimestampex.md)und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) auf aufruft, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zu Plattformaufrufen.](https://msdn.microsoft.com/library/aa288468.aspx) .NET und CryptoAPI über [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Teil 1 und .NET und [CryptoAPI über P/Invoke: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) der Unterabschnitte [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) (Erweitern der .NET-Kryptografie mit CAPICOM und P/Invoke) können ebenfalls hilfreich sein.\]

Die **FileName-Eigenschaft** legt den Pfad zur ausführbaren Datei fest oder ruft diesen ab. Dies ist die Standardeigenschaft.

## <a name="syntax"></a>Syntax


```VB
SignedCode.FileName As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Pfad zur ausführbaren Datei.

## <a name="remarks"></a>Hinweise

Wenn der Wert der **FileName-Eigenschaft** geändert wird, wird der Status des gesamten [**SignedCode-Objekts**](signedcode.md) zurückgesetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
