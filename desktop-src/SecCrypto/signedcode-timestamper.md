---
description: Die TimeStamper-Eigenschaft ruft den Zeitstempel der signierten ausführbaren Datei ab.
ms.assetid: f630b94f-015a-4387-938f-1b8c6b7895e9
title: SignedCode.TimeStamper-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.TimeStamper
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b5bd6f9376f74d46373f6731c66b2452503c6105fff31ce28b4fc76ac126c44d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118899349"
---
# <a name="signedcodetimestamper-property"></a>SignedCode.TimeStamper-Eigenschaft

\[Die **TimeStamper-Eigenschaft** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Verwenden Sie stattdessen Platform Invocation Services (PInvoke), um die Win32-API-Funktionen [**SignerSignEx,**](signersignex.md) [**SignerTimeStampEx**](signertimestampex.md)und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) aufzurufen, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren. Informationen zu PInvoke finden Sie unter [Tutorial zu Plattformaufrufen.](https://msdn.microsoft.com/library/aa288468.aspx) Die [Unterabschnitte .NET und CryptoAPI über P/Invoke: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.NET und CryptoAPI über P/Invoke: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) der Erweiterung der [.NET-Kryptografie mit CAPICOM und P/Invoke](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]

Die **TimeStamper-Eigenschaft** ruft den Zeitstempel der signierten ausführbaren Datei ab.

## <a name="syntax"></a>Syntax


```VB
SignedCode.TimeStamper As Signer
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**Signer-Objekt,**](signer.md) das Zugriff auf den Zeitstempel der signierten ausführbaren Datei bereitstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
