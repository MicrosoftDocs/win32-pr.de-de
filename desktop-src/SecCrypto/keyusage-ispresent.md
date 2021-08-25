---
description: Ruft einen booleschen Wert ab, der angibt, ob die KeyUsage-Erweiterung vorhanden ist.
ms.assetid: d666049a-4b40-42b6-8c2d-c27a1bb4c48a
title: KeyUsage.IsPresent-Eigenschaft
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
ms.openlocfilehash: d2eb962445717743512de396065304f70c31f02cfa4f3448a08a2731ed1fd377
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992860"
---
# <a name="keyusageispresent-property"></a>KeyUsage.IsPresent-Eigenschaft

\[Die **IsPresent-Eigenschaft** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System.Security.Cryptography.X509Certificates-Namespace.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **IsPresent-Eigenschaft** ruft einen booleschen Wert ab, der angibt, ob die [**KeyUsage-Erweiterung**](keyusage.md) vorhanden ist.

Diese Eigenschaft ist die Standardeigenschaft des [**KeyUsage-Objekts.**](keyusage.md)

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True gibt an, dass die KeyUsage-Erweiterung vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
