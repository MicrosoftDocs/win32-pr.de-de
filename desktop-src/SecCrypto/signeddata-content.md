---
description: Legt die zu Signier enden Daten fest oder ruft Sie ab. Dies ist die Standard Eigenschaft.
ms.assetid: 554ca500-403d-4c2a-868e-9e635d0b358e
title: SignedData. Content (Eigenschaft)
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
ms.openlocfilehash: 3c2ac97eeee317b4ec170338f666e5b5d9277861
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371765"
---
# <a name="signeddatacontent-property"></a>SignedData. Content (Eigenschaft)

\[Die **Content** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**SignedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Die **Content** -Eigenschaft legt die zu Signier enden Daten fest oder ruft Sie ab. Dies ist die Standard Eigenschaft.

## <a name="syntax"></a>Syntax


```VB
SignedData.Content As String
```



## <a name="property-value"></a>Eigenschaftswert

Die zu signierenden Daten.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft muss initialisiert werden, bevor die [**Sign**](signeddata-sign.md) -Methode aufgerufen wird. Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte [*Status*](../secgloss/s-gly.md) des Objekts zurückgesetzt, und alle Signaturen, die dem-Objekt zugeordnet waren, bevor die-Eigenschaft geändert wurde, gehen verloren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
