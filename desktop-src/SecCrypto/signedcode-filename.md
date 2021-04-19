---
description: Die FileName-Eigenschaft legt den Pfad zur ausführbaren Datei fest oder ruft ihn ab. Dies ist die Standard Eigenschaft.
ms.assetid: 2d2ea87b-86db-40b4-b052-8503beafa08c
title: Signedcode. filename (Eigenschaft)
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
ms.openlocfilehash: e6e31e57376f987b2b5cb47e5e6bd8a0d5e85fba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362170"
---
# <a name="signedcodefilename-property"></a>Signedcode. filename (Eigenschaft)

\[Die **filename** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen den Platform invoations Dienst (PInvoke) zum Aufrufen der Win32-API [**signersignetx**](signersignex.md)-, [**signertimestampex**](signertimestampex.md)-und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) -Funktionen, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx). Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]

Die **filename** -Eigenschaft legt den Pfad zur ausführbaren Datei fest oder ruft ihn ab. Dies ist die Standard Eigenschaft.

## <a name="syntax"></a>Syntax


```VB
SignedCode.FileName As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Pfad zur ausführbaren Datei.

## <a name="remarks"></a>Bemerkungen

Wenn der Wert der **filename** -Eigenschaft geändert wird, wird der Status des gesamten [**signedcode**](signedcode.md) -Objekts zurückgesetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Signedcode**](signedcode.md)
</dt> </dl>

 

 
