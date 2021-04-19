---
description: Lädt ein Signaturzertifikat aus einer angegebenen PFX-Datei.
ms.assetid: 98963354-c237-40d0-9235-8318728e2c8e
title: Signer. Load-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9a817a95ca825b67b54a41fc674db10bf81b5740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372612"
---
# <a name="signerload-method"></a>Signer. Load-Methode

\[Die **Load** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**CmsSigner-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Die **Load** -Methode lädt ein Signaturzertifikat aus einer angegebenen PFX-Datei.

## <a name="syntax"></a>Syntax


```VB
Signer.Load( _
  ByVal FileName, _
  [ ByVal Password ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FileName* 
</dt> <dd>

Der Name der PFX-Datei, die das Signaturzertifikat enthält.

</dd> <dt>

*Kennwort* \[ optionale\]
</dt> <dd>

Zeichenfolge, die das Klartext-Kennwort enthält, das zum Öffnen der Datei verwendet wird. Bis zu 32 Unicode-Zeichen, einschließlich eines abschließenden NULL-Zeichens, können für das Kennwort verwendet werden. Der Standardwert ist eine leere Zeichenfolge (""). Informationen zum Schützen des Kennworts finden Sie unter Behandeln von Kenn [Wörtern](../secbp/handling-passwords.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode lädt das erste Zertifikat in der PFX-Datei, der ein privater Schlüssel zugeordnet ist.

Diese Methode löst CAPICOM \_ E \_ nicht \_ zulässig aus, wenn eine Skripterstellung aus einer webbasierten Anwendung erfolgt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Signatur Geber**](signer.md)
</dt> </dl>

 

 
