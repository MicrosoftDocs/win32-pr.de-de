---
description: Ruft einen booleschen Wert ab, der angibt, ob die KeyUsage-Erweiterung vorhanden ist.
ms.assetid: d666049a-4b40-42b6-8c2d-c27a1bb4c48a
title: KeyUsage. ispree sent (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f70754c15a248cda69f93fcab2a0052bd8351261
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360253"
---
# <a name="keyusageispresent-property"></a>KeyUsage. ispree sent (Eigenschaft)

\[Die **ispree sent** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **ispree sent** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob die [**KeyUsage**](keyusage.md) -Erweiterung vorhanden ist.

Diese Eigenschaft ist die Standard Eigenschaft des [**KeyUsage**](keyusage.md) -Objekts.

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

**True** gibt an, dass die KeyUsage-Erweiterung vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Endeinheits Zertifikaten der**](keyusage.md)
</dt> </dl>

 

 
