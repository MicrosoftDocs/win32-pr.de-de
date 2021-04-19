---
description: Ruft einen booleschen Wert ab, der angibt, ob die KeyUsage-Erweiterung als kritisch markiert ist.
ms.assetid: f7d53570-2b89-40a9-ab56-fcae4e4cb70c
title: KeyUsage. IsCritical (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b1829da9c9ddbcf5261f4cc595b72b8596193078
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355858"
---
# <a name="keyusageiscritical-property"></a>KeyUsage. IsCritical (Eigenschaft)

\[Die **IsCritical** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **IsCritical** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob die KeyUsage-Erweiterung als kritisch markiert ist.

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsCritical As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

**True** gibt an, dass die KeyUsage-Erweiterung als kritisch markiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Endeinheits Zertifikaten der**](keyusage.md)
</dt> </dl>

 

 
