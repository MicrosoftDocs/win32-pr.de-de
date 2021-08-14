---
description: Der CAPICOM \_ EXPORT \_ FLAG-Enumerationstyp definiert, ob Exportfehler für private Schlüssel ignoriert werden.
ms.assetid: 12e6862b-5c73-4e45-8829-8086048e94f3
title: CAPICOM_EXPORT_FLAG -Enumeration (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EXPORT_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: d6be9953640eeb2eb1d6c7fad812f5efe2d2da2f6888a01b4450c638ab68bfca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772465"
---
# <a name="capicom_export_flag-enumeration"></a>CAPICOM \_ EXPORT \_ FLAG-Enumeration

Der **CAPICOM \_ EXPORT \_ FLAG-Enumerationstyp** definiert, ob Exportfehler für private Schlüssel ignoriert werden.

## <a name="members"></a>Member



| Member                                                            | BESCHREIBUNG                                               | Wert |
|-------------------------------------------------------------------|-----------------------------------------------------------|-------|
| **CAPICOM \_ EXPORT \_ DEFAULT**                                      | Exportfehler bei privaten Schlüsseln werden nicht ignoriert.<br/> | 0     |
| **CAPICOM \_ EXPORT \_ IGNORE \_ PRIVATE \_ KEY \_ NOT \_ EXPORTABLE \_ ERROR** | Alle Exportfehler beim privaten Schlüssel werden ignoriert.<br/>     | 1     |



## <a name="remarks"></a>Hinweise

Der CAPICOM \_ EXPORT \_ FLAG-Enumerationstyp wird von der folgenden Methode verwendet:

-   [**Certificates.Save**](certificates-save.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




