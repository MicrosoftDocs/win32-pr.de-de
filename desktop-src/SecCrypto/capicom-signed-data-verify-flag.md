---
description: Gibt an, was überprüft wird, wenn eine digitale Signatur überprüft wird.
ms.assetid: e6259c3f-caed-42f4-832c-250365caa0d7
title: CAPICOM_SIGNED_DATA_VERIFY_FLAG-Enumeration (Capicom.h)
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
ms.openlocfilehash: 8f087a9a28d06e63bc19d75974bccba05da4c77658f81401fd994a7eadb9726a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772084"
---
# <a name="capicom_signed_data_verify_flag-enumeration"></a>CAPICOM \_ SIGNED DATA VERIFY \_ \_ \_ FLAG-Enumeration

Die **CAPICOM \_ SIGNED DATA VERIFY \_ \_ \_ FLAG-Enumeration** gibt an, was überprüft wird, wenn eine [*digitale Signatur*](../secgloss/d-gly.md) überprüft wird.

## <a name="members"></a>Member



| Member                                           | Beschreibung                                                                                                 | Wert |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM– NUR SIGNATUR \_ ÜBERPRÜFEN \_ \_**             | Nur die Signatur wird überprüft.<br/>                                                                   | 0     |
| **CAPICOM \_ VERIFY \_ SIGNATURE \_ AND \_ CERTIFICATE** | Sowohl die Signatur als auch die Gültigkeit des Zertifikats, das zum Erstellen der Signatur verwendet wird, werden überprüft.<br/> | 1     |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
