---
description: Legt die Beschreibung der signierten ausführbaren Datei fest oder ruft sie ab.
ms.assetid: 39ce37bd-fe3e-4195-a132-93f3743f7370
title: SignedCode.Description (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Description
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6046beae61aebaf33ea5eedb6ef2ec643f2edb39dbbedc61372085be2220068b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900350"
---
# <a name="signedcodedescription-property"></a>SignedCode.Description (Eigenschaft)

\[Die **Description-Eigenschaft** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen Platform Invocation Services (PInvoke), um die Win32-API-Funktionen [**SignerSignEx,**](signersignex.md) [**SignerTimeStampEx**](signertimestampex.md)und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) auf aufruft, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zu Plattformaufrufen.](https://msdn.microsoft.com/library/aa288468.aspx) .NET und CryptoAPI über [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Teil 1 und .NET und [CryptoAPI über P/Invoke: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) der Unterabschnitte [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) (Erweitern der .NET-Kryptografie mit CAPICOM und P/Invoke) können ebenfalls hilfreich sein.\]

Die **Description-Eigenschaft** legt die Beschreibung der signierten ausführbaren Datei fest oder ruft sie ab.

## <a name="syntax"></a>Syntax


```VB
SignedCode.Description As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Beschreibung der signierten ausführbaren Datei.

## <a name="remarks"></a>Hinweise

Die Beschreibung ist der Text, der im Dialogfeld Authenticode-Überprüfung angezeigt wird. Der Text sollte die signierte ausführbare Datei beschreiben. Wenn diese Eigenschaft **NULL ist,** zeigt das Dialogfeld den Namen der ausführbaren Datei an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
