---
description: Die CAPICOM \_ KEY \_ STORAGE \_ FLAG-Enumeration definiert Schlüsselspeicherflags.
ms.assetid: 326cef75-24a5-4dc9-a7e9-a63dd3d8de54
title: CAPICOM_KEY_STORAGE_FLAG -Enumeration (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_STORAGE_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: cb1c2c4761403223c8ed0eb225709fbd189127bc9d56d60b82a534e2bc15b8e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879090"
---
# <a name="capicom_key_storage_flag-enumeration"></a>CAPICOM \_ KEY \_ STORAGE \_ FLAG-Enumeration

Die **CAPICOM \_ KEY STORAGE \_ \_ FLAG-Enumeration** definiert Schlüsselspeicherflags.

## <a name="members"></a>Member



| Member                                     | BESCHREIBUNG                           | Wert |
|--------------------------------------------|---------------------------------------|-------|
| **CAPICOM \_ KEY \_ STORAGE \_ DEFAULT**         | Standardspeicher für Schlüssel.<br/>       | 0     |
| **CAPICOM \_ KEY \_ STORAGE \_ EXPORTABLE**      | Der Schlüssel kann exportiert werden.<br/>     | 1     |
| **CAPICOM \_ KEY \_ STORAGE \_ USER \_ PROTECTED** | Der Schlüssel ist benutzergeschützt.<br/> | 2     |



## <a name="remarks"></a>Hinweise

Diese Enumeration wird von der folgenden Methode verwendet:

-   [**Certificate.Load**](certificate-load.md)
-   [**Store. Laden**](store-load.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




