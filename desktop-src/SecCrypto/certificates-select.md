---
description: Zeigt ein Dialogfeld für die Auswahl von Zertifikaten an und gibt eine Sammlung der ausgewählten Zertifikate zurück.
ms.assetid: dbf49a4b-6da1-4819-afcd-46db89a00fce
title: 'ICertificates2:: Select-Methode'
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
ms.openlocfilehash: cfd5b1cb5e269c14e05de25262fda711549bf02d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362141"
---
# <a name="icertificates2select-method"></a>ICertificates2:: Select-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **Select** -Methode zeigt ein Dialogfeld für die Auswahl von Zertifikaten an und gibt eine Sammlung der ausgewählten Zertifikate zurück. Diese Methode wurde in CAPICOM 2,0 eingeführt.

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

*Display String* \[ in, optional\]
</dt> <dd>

Eine Zeichenfolge, die den im Dialogfeld angezeigten Eingabe Aufforderungs Text enthält. Der Standardwert ist eine leere Zeichenfolge ("").

</dd> <dt>

*bmultiselect* \[ in, optional\]
</dt> <dd>

Boolescher Wert, der angibt, ob der Benutzer mehr als ein Zertifikat auswählen kann. True gibt an, dass mehrere Zertifikate mithilfe der STRG-oder der Umschalttaste ausgewählt werden können. Der Standardwert ist „FALSE“.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein [**Zertifikat**](certificates.md) Objekt, das die im Dialogfeld ausgewählten Zertifikate enthält.

**CAPICOM 2,1:** Das [**Zertifikat**](certificates.md) Objekt, das zurückgegeben wird, enthält Verweise auf die Zertifikate in der Sammlung, von der aus die Auswahl getroffen wurde. Alle Änderungen, die an den Zertifikaten im zurückgegebenen **Zertifikat** Objekt vorgenommen werden, werden in dieser Sammlung widergespiegelt.

**CAPICOM 2,0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 und CAPICOM 2.0.0.3:** Das [**Zertifikat**](certificates.md) Objekt, das zurückgegeben wird, enthält Kopien der Zertifikate in der Sammlung, aus der die Auswahl stammt. Alle Änderungen, die an den Zertifikaten im zurückgegebenen **Zertifikat** Objekt vorgenommen werden, werden in dieser Sammlung nicht widergespiegelt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
