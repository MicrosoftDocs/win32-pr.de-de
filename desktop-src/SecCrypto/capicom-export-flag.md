---
description: Der \_ \_ Enumerationstyp CAPICOM-exportflag definiert, ob Export Fehler des privaten Schlüssels ignoriert werden.
ms.assetid: 12e6862b-5c73-4e45-8829-8086048e94f3
title: CAPICOM_EXPORT_FLAG-Enumeration (CAPICOM. h)
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
ms.openlocfilehash: fe99b1123ae35083e5c59df37234821efd2db208
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369683"
---
# <a name="capicom_export_flag-enumeration"></a>CAPICOM \_ - \_ exportflag-Enumeration

Der Enumerationstyp **CAPICOM- \_ \_ exportflag** definiert, ob Export Fehler des privaten Schlüssels ignoriert werden.

## <a name="members"></a>Member



| Member                                                            | BESCHREIBUNG                                               | Wert |
|-------------------------------------------------------------------|-----------------------------------------------------------|-------|
| **Standardwert für CAPICOM- \_ Export \_**                                      | Alle Export Fehler des privaten Schlüssels werden nicht ignoriert.<br/> | 0     |
| **CAPICOM \_ - \_ Export \_ \_ Fehler beim \_ nicht \_ exportierbaren privaten Schlüssel \_ ignorieren** | Alle Export Fehler des privaten Schlüssels werden ignoriert.<br/>     | 1     |



## <a name="remarks"></a>Bemerkungen

Der \_ \_ Enumerationstyp CAPICOM-exportflag wird von der folgenden Methode verwendet:

-   [**Zertifikate. speichern**](certificates-save.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




