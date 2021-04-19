---
description: Ruft einen booleschen Wert ab, der angibt, ob die grundlegende Einschränkungs Erweiterung vorhanden ist. Dies ist die Standard Eigenschaft.
ms.assetid: 775b37fc-5015-4096-9e94-608f13a5ed14
title: Basiceinschränkungs. ispree sent (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9632f0d1297f2effd7d1bcc6056b2327d7f38e26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370670"
---
# <a name="basicconstraintsispresent-property"></a>Basiceinschränkungs. ispree sent (Eigenschaft)

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**X509BasicConstraintsExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) -Namespace.\]

Die **ispree sent** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob die Erweiterung für grundlegende Einschränkungen vorhanden ist. Dies ist die Standard Eigenschaft.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
BasicConstraints.IsPresent As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

**True** gibt an, dass die grundlegende Einschränkungs Erweiterung vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Basiceinschränkungen**](basicconstraints.md)
</dt> </dl>

 

 
