---
description: Legt den Klartextinhalt einer Umschlagnachricht fest oder ruft sie ab. Dies ist die Standardeigenschaft.
ms.assetid: 7927321f-fbda-45e0-9b9f-c10ecd3a98b1
title: EnvelopedData.Content (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4115b55b7f9542c5a31c9abd3bcbbaec5256be4283675becac2f011ec76c8cbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766071"
---
# <a name="envelopeddatacontent-property"></a>EnvelopedData.Content (Eigenschaft)

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**EnvelopedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**Namespace System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Die **Content-Eigenschaft** legt den Klartextinhalt einer Umschlagnachricht fest oder ruft sie ab. Dies ist die Standardeigenschaft.

## <a name="syntax"></a>Syntax


```VB
EnvelopedData.Content As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Klartextinhalt einer Umschlagnachricht.

## <a name="remarks"></a>Hinweise

Das Festlegen dieser Eigenschaft muss vor dem Aufrufen der [**Encrypt-Methode**](envelopeddata-encrypt.md) erfolgen. Wenn der Wert dieser Eigenschaft direkt oder indirekt [](../secgloss/s-gly.md) zurückgesetzt wird, wird der gesamte Zustand des Objekts zurückgesetzt, und alle verschlüsselten Inhalte im Objekt gehen verloren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
