---
description: Stellt die grundlegende Einschränkungserweiterung eines Zertifikats dar.
ms.assetid: c21794f6-7654-4140-8114-0edb398d6de8
title: BasicConstraints-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8cda73c4a698d40a602b39fd7822dabfbded9a7a35c27db16ca74f7993f7f684
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879520"
---
# <a name="basicconstraints-object"></a>BasicConstraints-Objekt

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**X509BasicConstraintsExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/previous-versions/windows/)\]

Das **BasicConstraints-Objekt** stellt die grundlegende Einschränkungserweiterung eines Zertifikats dar.

## <a name="when-to-use"></a>Verwendung

Das **BasicConstraints-Objekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Bestimmen Sie, ob die Erweiterung für grundlegende Einschränkungen vorhanden ist.
-   Bestimmen Sie, ob die Basiseinschränkungserweiterung als kritisch markiert ist.
-   Bestimmen Sie, ob das Zertifikat auf Zertifizierungsstellen beschränkt ist.
-   Bestimmen Sie, ob die Einschränkung für die Pfadlänge vorhanden ist, und rufen Sie den Einschränkungswert für die Pfadlänge ab.

## <a name="members"></a>Member

Das **BasicConstraints-Objekt** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **BasicConstraints-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                     | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsCertificateAuthority**](basicconstraints-iscertificateauthority.md)<br/>         | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob das Zertifikat für eine [*Zertifizierungsstelle (CA)*](../secgloss/c-gly.md) gilt.<br/> |
| [**IsCritical**](basicconstraints-iscritical.md)<br/>                                 | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob die Basiseinschränkungserweiterung als kritisch markiert ist.<br/>                                                                                                     |
| [**IsPathLenConstraintPresent**](basicconstraints-ispathlenconstraintpresent.md)<br/> | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob die Pfadlängeneinschränkung des Zertifikats vorhanden ist.<br/>                                                                                                   |
| [**IsPresent**](basicconstraints-ispresent.md)<br/>                                   | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob die Erweiterung für grundlegende Einschränkungen vorhanden ist. Dies ist die Standardeigenschaft.<br/>                                                                              |
| [**PathLenConstraint**](basicconstraints-pathlenconstraint.md)<br/>                   | Schreibgeschützt<br/> | Ruft den Wert der Pfadlängeneinschränkung ab.<br/>                                                                                                                                                      |



 

## <a name="remarks"></a>Hinweise

Das **BasicConstraints-Objekt** kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kryptografieobjekte](cryptography-objects.md)
</dt> </dl>

 

 
