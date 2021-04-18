---
description: Legt den nur-Text-Inhalt einer zu umzurufenden Nachricht fest oder ruft ihn ab. Dies ist die Standard Eigenschaft.
ms.assetid: 7927321f-fbda-45e0-9b9f-c10ecd3a98b1
title: EnvelopedData. Content-Eigenschaft
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
ms.openlocfilehash: ce87dba503d8e8eec2dc21a9024c1071b3255f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372036"
---
# <a name="envelopeddatacontent-property"></a>EnvelopedData. Content-Eigenschaft

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**EnvelopedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Die **Content** -Eigenschaft legt den nur-Text-Inhalt einer Nachricht fest, die eingeschlossene werden soll, oder ruft ihn ab. Dies ist die Standard Eigenschaft.

## <a name="syntax"></a>Syntax


```VB
EnvelopedData.Content As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Klartext-Inhalt einer zu umzurufenden Nachricht.

## <a name="remarks"></a>Bemerkungen

Das Festlegen dieser Eigenschaft muss erfolgen, bevor die [**Verschlüsselungs**](envelopeddata-encrypt.md) Methode aufgerufen wird. Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte [*Status*](../secgloss/s-gly.md) des Objekts zurückgesetzt, und alle verschlüsselten Inhalte im Objekt gehen verloren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
