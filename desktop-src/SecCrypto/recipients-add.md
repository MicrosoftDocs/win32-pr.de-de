---
description: Fügt einer Empfänger Auflistung ein Zertifikat Objekt hinzu.
ms.assetid: 2a1b9e0f-ccbf-4042-871b-397de6b6fc35
title: Empfängers. Add-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 255d17485e3423d50cd86b092c2120605f0f1106
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357606"
---
# <a name="recipientsadd-method"></a>Empfängers. Add-Methode

\[Die **Add** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**cmsrecepentcollection-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Mit der **Add** -Methode wird einer [**Empfänger**](recipients.md) Auflistung ein [**Zertifikat**](certificate.md) Objekt hinzugefügt.

## <a name="syntax"></a>Syntax


```VB
Recipients.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zertifikat* \[ in\]
</dt> <dd>

Ausdruck, der in das [**Zertifikat**](certificate.md) Objekt aufgelöst wird, das der Auflistung hinzugefügt werden soll.

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

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> <dt>

[**Empfänger**](recipients.md)
</dt> </dl>

 

 
