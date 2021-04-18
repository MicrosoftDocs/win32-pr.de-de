---
description: Stellt die grundlegende Einschränkungs Erweiterung eines Zertifikats dar.
ms.assetid: c21794f6-7654-4140-8114-0edb398d6de8
title: Basiceinschränkungs-Objekt
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
ms.openlocfilehash: 85e912542b09b02297f5119392115857259f70f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358699"
---
# <a name="basicconstraints-object"></a>Basiceinschränkungs-Objekt

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**X509BasicConstraintsExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) -Namespace.\]

Das **basiceinschränkunsobjekt** stellt die grundlegende Einschränkungs Erweiterung eines Zertifikats dar.

## <a name="when-to-use"></a>Verwendung

Das **basiceinschränkungs** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:

-   Bestimmen Sie, ob die Erweiterung für grundlegende Einschränkungen vorhanden ist.
-   Bestimmen Sie, ob die Erweiterung für Basis Einschränkungen als kritisch markiert ist.
-   Bestimmen Sie, ob das Zertifikat auf Zertifizierungsstellen beschränkt ist.
-   Bestimmen Sie, ob die Einschränkung der Pfadlänge vorhanden ist, und rufen Sie den Einschränkungs Wert der Pfadlänge ab

## <a name="members"></a>Member

Das **basiceinschränkungs** -Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **basiceinschränkungs** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                                     | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iscertificateauthority**](basicconstraints-iscertificateauthority.md)<br/>         | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob das Zertifikat für eine Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca) gilt.<br/> |
| [**IsCritical**](basicconstraints-iscritical.md)<br/>                                 | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob die grundlegende Einschränkungs Erweiterung als kritisch markiert ist.<br/>                                                                                                     |
| [**Ispathlenbeschränintpresent**](basicconstraints-ispathlenconstraintpresent.md)<br/> | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob die Pfadlängen Einschränkung des Zertifikats vorhanden ist.<br/>                                                                                                   |
| [**IsPresent**](basicconstraints-ispresent.md)<br/>                                   | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob die grundlegende Einschränkungs Erweiterung vorhanden ist. Dies ist die Standard Eigenschaft.<br/>                                                                              |
| [**PathLenConstraint**](basicconstraints-pathlenconstraint.md)<br/>                   | Schreibgeschützt<br/> | Ruft den Wert der Path-Längen Einschränkung ab.<br/>                                                                                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Das **basiceinschränkunsobjekt** kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kryptografieobjekte](cryptography-objects.md)
</dt> </dl>

 

 
