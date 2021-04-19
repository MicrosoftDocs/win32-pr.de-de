---
description: Legt den anzeigen Amen für den Bezeichner fest oder ruft ihn ab.
ms.assetid: 53f84d0d-c189-4fd2-a383-29fd0d22de08
title: OID. FriendlyName (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.FriendlyName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1976980d1a22f4246f0ace686941cc4bcec87c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370301"
---
# <a name="oidfriendlyname-property"></a>OID. FriendlyName (Eigenschaft)

\[Die **FriendlyName** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**OID-Klasse**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Die **FriendlyName** -Eigenschaft legt den anzeigen Amen für den Bezeichner fest oder ruft ihn ab.

## <a name="syntax"></a>Syntax


```VB
OID.FriendlyName As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Anzeige Name für die [**OID**](oid.md).

## <a name="remarks"></a>Bemerkungen

Wenn die **FriendlyName** -Eigenschaft festgelegt ist, wird die [**value**](oid-value.md) -Eigenschaft auf den entsprechenden punktierten Wert festgelegt. Wenn die **value** -Eigenschaft festgelegt ist, wird die **FriendlyName** -Eigenschaft auf den entsprechenden anzeigen Amen festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**OID**](oid.md)
</dt> </dl>

 

 
