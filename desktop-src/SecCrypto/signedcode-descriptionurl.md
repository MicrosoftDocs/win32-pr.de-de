---
description: Legt die URL einer Beschreibung der signierten ausführbaren Datei fest oder ruft Sie ab.
ms.assetid: 854c76fb-5cb3-4200-bab0-fa3fa5bd3abe
title: Signedcode. DescriptionUrl (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.DescriptionURL
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 628d176595031f2b87b9fcb5f58ff81838d49be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359260"
---
# <a name="signedcodedescriptionurl-property"></a>Signedcode. DescriptionUrl (Eigenschaft)

\[Die **DescriptionUrl** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen den Platform invoations Dienst (PInvoke) zum Aufrufen der Win32-API [**signersignetx**](signersignex.md)-, [**signertimestampex**](signertimestampex.md)-und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) -Funktionen, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx). Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]

Die **DescriptionUrl** -Eigenschaft legt die URL einer Beschreibung der signierten ausführbaren Datei fest oder ruft Sie ab.

## <a name="syntax"></a>Syntax


```VB
SignedCode.DescriptionURL As String
```



## <a name="property-value"></a>Eigenschaftswert

Die URL einer Beschreibung der signierten ausführbaren Datei.

## <a name="remarks"></a>Bemerkungen

Die **deskriptionurl** ist die URL, zu der die [**Beschreibung**](signedcode-description.md) im Dialogfeld Authenticode-Überprüfung Links angezeigt wird. Wenn diese Eigenschaft **null** ist, kann die **Beschreibung** nicht als Link verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Signedcode**](signedcode.md)
</dt> </dl>

 

 
