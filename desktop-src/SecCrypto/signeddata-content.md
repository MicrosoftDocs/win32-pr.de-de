---
description: Legt die zu signierten Daten fest oder ruft sie ab. Dies ist die Standardeigenschaft.
ms.assetid: 554ca500-403d-4c2a-868e-9e635d0b358e
title: SignedData.Content(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b9f4439f7fc7c2a71887fcb78991cf54a814a8682f991545ec33301e2fb9bc95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118899234"
---
# <a name="signeddatacontent-property"></a>SignedData.Content(Eigenschaft)

\[Die **Content-Eigenschaft** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**SignedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**Namespace System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Die **Content-Eigenschaft** legt die zu signierten Daten fest oder ruft sie ab. Dies ist die Standardeigenschaft.

## <a name="syntax"></a>Syntax


```VB
SignedData.Content As String
```



## <a name="property-value"></a>Eigenschaftswert

Die zu signierenden Daten.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft muss initialisiert werden, bevor die [**Sign-Methode**](signeddata-sign.md) aufgerufen wird. Wenn der Wert dieser Eigenschaft direkt oder indirekt [](../secgloss/s-gly.md) zurückgesetzt wird, wird der gesamte Zustand des Objekts zurückgesetzt, und jede Signatur, die dem Objekt zugeordnet war, bevor die Eigenschaft geändert wurde, geht verloren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
