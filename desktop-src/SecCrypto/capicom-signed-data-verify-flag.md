---
description: Gibt an, was überprüft wird, wenn eine digitale Signatur überprüft wird.
ms.assetid: e6259c3f-caed-42f4-832c-250365caa0d7
title: CAPICOM_SIGNED_DATA_VERIFY_FLAG-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_SIGNED_DATA_VERIFY_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: bc8db48ee067e8d12bffa9dbff433384058013b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371461"
---
# <a name="capicom_signed_data_verify_flag-enumeration"></a>Von CAPICOM \_ signierte Datenüberprüfung- \_ \_ Flag- \_ Enumeration

Die in **CAPICOM \_ signierte \_ datenüberprüfungsflag \_ \_** -Enumeration gibt an, was überprüft wird, wenn eine [*digitale Signatur*](../secgloss/d-gly.md) überprüft wird.

## <a name="members"></a>Member



| Member                                           | BESCHREIBUNG                                                                                                 | Wert |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------|
| **nur CAPICOM- \_ Signatur überprüfen \_ \_**             | Nur die Signatur wird geprüft.<br/>                                                                   | 0     |
| **CAPICOM \_ \_ -Signatur \_ und \_ Zertifikat überprüfen** | Sowohl die Signatur als auch die Gültigkeit des Zertifikats, das zum Erstellen der Signatur verwendet wird, werden überprüft.<br/> | 1     |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
