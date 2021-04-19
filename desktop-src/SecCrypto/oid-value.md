---
description: Legt den Wert der OID-gepunkteten Nummer des Bezeichners fest oder ruft ihn ab.
ms.assetid: bb960e65-776e-4ae8-a557-62254dc10558
title: OID. Value-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d8c3c59cfd3eadfb8aec56c6814a2af6ce9ff900
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372758"
---
# <a name="oidvalue-property"></a>OID. Value-Eigenschaft

\[Die **value** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**OID-Klasse**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Die **value** -Eigenschaft legt den Wert der OID-gepunkteten Nummer des Bezeichners fest oder ruft ihn ab.

## <a name="syntax"></a>Syntax


```VB
OID.Value As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Wert der OID-gepunkteten Zahl des Bezeichners. Mögliche Werte finden Sie unter Wincrypt. h.

## <a name="remarks"></a>Bemerkungen

Wenn die **value** -Eigenschaft festgelegt ist, wird die [**FriendlyName**](oid-friendlyname.md) -Eigenschaft auf den entsprechenden anzeigen Amen festgelegt. Wenn die **FriendlyName** -Eigenschaft festgelegt ist, wird die **value** -Eigenschaft auf den entsprechenden punktierten Wert festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**OID**](oid.md)
</dt> </dl>

 

 
