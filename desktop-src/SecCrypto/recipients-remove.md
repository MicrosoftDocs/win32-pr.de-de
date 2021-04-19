---
description: Entfernt ein Zertifikat Objekt aus einer Empfänger Auflistung.
ms.assetid: bb75f6d0-4bab-40dd-9d0c-f0431da9c5f3
title: Empfängers. Remove-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06d276e2d8e75e8822cee3503a7e8342a94a6b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351251"
---
# <a name="recipientsremove-method"></a>Empfängers. Remove-Methode

\[Die **Remove** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**cmsrecepentcollection-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Die **Remove** -Methode entfernt ein [**Zertifikat**](certificate.md) Objekt aus einer [**Empfänger**](recipients.md) Auflistung.

## <a name="syntax"></a>Syntax


```VB
Recipients.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

Der Index des [**Zertifikat**](certificate.md) Objekts, das aus der Auflistung entfernt werden soll.

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

 

 
