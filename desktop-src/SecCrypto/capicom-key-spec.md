---
description: Die CAPICOM \_ Key \_ spec-Enumeration definiert Schlüssel Spezifikationen.
ms.assetid: e4aaaf69-ab28-4e8c-8a8a-6dc662299865
title: CAPICOM_KEY_SPEC-Enumeration (CAPICOM. h)
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
ms.openlocfilehash: 153f0431d78ff595b4d568fd7a677abea0d28be7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364685"
---
# <a name="capicom_key_spec-enumeration"></a>CAPICOM- \_ schlüsselspezifikations \_ Enumeration

Die **CAPICOM \_ Key \_ spec** -Enumeration definiert Schlüssel Spezifikationen.

## <a name="members"></a>Member



| Member                              | BESCHREIBUNG                                                | Wert |
|-------------------------------------|------------------------------------------------------------|-------|
| **CAPICOM- \_ Schlüssel \_ Spezifikation \_ keyexchange** | Der Schlüssel kann für die Verschlüsselung und Signierung verwendet werden.<br/> | 1     |
| **CAPICOM \_ Key \_ spec- \_ Signatur**   | Der Schlüssel kann nur für die Signierung verwendet werden.<br/>           | 2     |



## <a name="remarks"></a>Bemerkungen

Die **CAPICOM \_ - \_ schlüsselspezifikations** Enumeration wird von den folgenden Methoden und Eigenschaften verwendet:

-   [**PrivateKey. KeySpec**](privatekey-keyspec.md) -Eigenschaft.
-   [**PrivateKey. Open**](privatekey-open.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




