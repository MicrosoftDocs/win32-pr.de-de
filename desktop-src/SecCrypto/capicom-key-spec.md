---
description: Die CAPICOM \_ KEY \_ SPEC-Enumeration definiert Schlüsselspezifikationen.
ms.assetid: e4aaaf69-ab28-4e8c-8a8a-6dc662299865
title: CAPICOM_KEY_SPEC -Enumeration (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_SPEC
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 211830b57d37240edf0df97524ef3865ebe600b33e814353f3a0d021b1b0d88c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772445"
---
# <a name="capicom_key_spec-enumeration"></a>CAPICOM \_ KEY \_ SPEC-Enumeration

Die **CAPICOM \_ KEY \_ SPEC-Enumeration** definiert Schlüsselspezifikationen.

## <a name="members"></a>Member



| Member                              | BESCHREIBUNG                                                | Wert |
|-------------------------------------|------------------------------------------------------------|-------|
| **CAPICOM \_ KEY \_ SPEC \_ KEYEXCHANGE** | Der Schlüssel kann zum Verschlüsseln und Signieren verwendet werden.<br/> | 1     |
| **\_ \_ CAPICOM-SCHLÜSSELSPEZIFIKATIONSSIGNATUR \_**   | Der Schlüssel kann nur zum Signieren verwendet werden.<br/>           | 2     |



## <a name="remarks"></a>Hinweise

Die **CAPICOM \_ KEY \_ SPEC-Enumeration** wird von den folgenden Methoden und Eigenschaften verwendet:

-   [**PrivateKey.KeySpec-Eigenschaft.**](privatekey-keyspec.md)
-   [**PrivateKey.Open-Methode.**](privatekey-open.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




