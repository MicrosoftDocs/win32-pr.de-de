---
description: Zeigt ein Dialogfeld zum Auswählen von Zertifikaten an und gibt eine Sammlung dieser ausgewählten Zertifikate zurück.
ms.assetid: dbf49a4b-6da1-4819-afcd-46db89a00fce
title: ICertificates2::Select-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Select
- ICertificates2.Select
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 50e10a9487318c7b89e89afb3d10d5974524c821b76618ca8ffd1f282e844f65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770485"
---
# <a name="icertificates2select-method"></a>ICertificates2::Select-Methode

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Select-Methode** zeigt ein Dialogfeld zum Auswählen von Zertifikaten an und gibt eine Sammlung dieser ausgewählten Zertifikate zurück. Diese Methode wurde in CAPICOM 2.0 eingeführt.

## <a name="syntax"></a>Syntax


```VB
Certificates.Select( _
  [ ByVal Title ], _
  [ ByVal DisplayString ], _
  [ ByVal bMultiSelect ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Titel* \[ in, optional\]
</dt> <dd>

Eine Zeichenfolge, die den Titel für das Dialogfeld enthält. Der Standardwert ist eine leere Zeichenfolge ("").

</dd> <dt>

*DisplayString* \[ in, optional\]
</dt> <dd>

Eine Zeichenfolge, die den im Dialogfeld angezeigten Eingabeaufforderungstext enthält. Der Standardwert ist eine leere Zeichenfolge ("").

</dd> <dt>

*bMultiSelect* \[ in, optional\]
</dt> <dd>

Boolescher Wert, der angibt, ob der Benutzer mehrere Zertifikate auswählen kann. True gibt an, dass mehrere Zertifikate mit der STRG- oder UMSCHALTTASTE ausgewählt werden können. Der Standardwert ist „FALSE“.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein [**Certificates-Objekt,**](certificates.md) das die im Dialogfeld ausgewählten Zertifikate enthält.

**CAPICOM 2.1:** Das [**zurückgegebene Certificates-Objekt**](certificates.md) enthält Verweise auf die Zertifikate in der Auflistung, aus der die Auswahl getroffen wurde. Alle Änderungen an den Zertifikaten im zurückgegebenen **Certificates-Objekt** werden in dieser Sammlung widergespiegelt.

**CAPICOM 2.0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 und CAPICOM 2.0.0.3:** Das [**zurückgegebene Certificates-Objekt**](certificates.md) enthält Kopien der Zertifikate in der Sammlung, aus der die Auswahl getroffen wurde. Alle Änderungen, die an den Zertifikaten im zurückgegebenen **Certificates-Objekt** vorgenommen wurden, werden in dieser Sammlung nicht widergespiegelt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
