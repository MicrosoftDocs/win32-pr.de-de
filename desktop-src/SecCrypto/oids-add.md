---
description: Fügt der Auflistung das angegebene Oid-Objekt hinzu.
ms.assetid: 0ae087d6-768a-4538-b834-0f936680de05
title: OIDs. Add-Methode
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
ms.openlocfilehash: d2fa007798a0657991ec8e37a7dddc9fb4c95b2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372126"
---
# <a name="oidsadd-method"></a>OIDs. Add-Methode

\[Die **Add** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**OidCollection-Klasse**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Die **Add** -Methode fügt der Auflistung das angegebene [**OID**](oid.md) -Objekt hinzu.

## <a name="syntax"></a>Syntax


```VB
OIDs.Add( _
  ByVal OID _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OID* \[ in\]
</dt> <dd>

Das [**OID**](oid.md) -Objekt, das der Auflistung hinzugefügt werden soll. Das **OID** -Objekt wird basierend auf dem gepunkteten Wert in sortierter Reihenfolge hinzugefügt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
