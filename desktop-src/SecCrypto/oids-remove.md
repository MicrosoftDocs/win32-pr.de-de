---
description: Entfernt das angegebene Oid-Objekt aus der Auflistung.
ms.assetid: c5eb6831-b195-4dc1-a6bd-d4245f9b0213
title: OIDs. Remove-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 000310e0034d413dea16a45f79647c3e0f7cf52d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350790"
---
# <a name="oidsremove-method"></a>OIDs. Remove-Methode

\[Die **Remove** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**OidCollection-Klasse**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Die **Remove** -Methode entfernt das angegebene [**OID**](oid.md) -Objekt aus der Auflistung.

## <a name="syntax"></a>Syntax


```VB
OIDs.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

Der Index des zu entfernenden [**OID**](oid.md) -Objekts. Dabei kann es sich entweder um einen Index in der Auflistung oder um den gepunkteten Wert der OID handeln.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
