---
description: Fügt der Auflistung das angegebene OID-Objekt hinzu.
ms.assetid: 0ae087d6-768a-4538-b834-0f936680de05
title: OIDs.Add-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ff686ae816fa61d68e0a0c40326581025ced8f4c94fb5cffc633ff452ac4f0ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979651"
---
# <a name="oidsadd-method"></a>OIDs.Add-Methode

\[Die **Add-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**OidCollection-Klasse**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) im [**System.Security.Cryptography-Namespace.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Die **Add-Methode** fügt der Auflistung das angegebene [**OID-Objekt**](oid.md) hinzu.

## <a name="syntax"></a>Syntax


```VB
OIDs.Add( _
  ByVal OID _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OID* \[ In\]
</dt> <dd>

Das [**OID-Objekt,**](oid.md) das der Auflistung hinzugefügt werden soll. Das **OID-Objekt** wird in sortierter Reihenfolge basierend auf seinem gepunkteten Wert hinzugefügt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
