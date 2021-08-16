---
description: Definiert das Format einer Datei, die Zertifikatinformationen enthält.
ms.assetid: 417a6d1b-6329-418c-823c-d82b94207fd6
title: CAPICOM_CERTIFICATE_SAVE_AS_TYPE -Enumeration (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 2000bd582475a227fdb638649ee1a634e488a21a7c09d84dd6e21dafc5e9aa42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772641"
---
# <a name="capicom_certificate_save_as_type-enumeration"></a>CAPICOM \_ CERTIFICATE SAVE AS \_ \_ \_ TYPE-Enumeration

Der **CAPICOM \_ CERTIFICATE SAVE AS \_ \_ TYPE-Enumerationstyp \_** definiert das Format einer Datei, die Zertifikatinformationen enthält. Dieser Enumerationstyp wurde mit CAPICOM 2.0 eingeführt.

## <a name="members"></a>Member



| Member                                  | Beschreibung                                                                                                                                   | Wert |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ CERTIFICATE \_ SAVE \_ AS \_ PFX** | Die Ausgabedatei wird als PFX-Datei (PKCS 12) formatiert, und alle zugehörigen privaten Schlüssel, die exportierbar sind, werden ebenfalls gespeichert.<br/> | 0     |
| **CAPICOM \_ CERTIFICATE \_ SAVE \_ AS \_ CER** | Die Ausgabedatei wird als CER-Datei formatiert, ohne dass private Schlüssel gespeichert werden.<br/>                                                        | 1     |



## <a name="remarks"></a>Hinweise

Der **CAPICOM \_ CERTIFICATE SAVE AS \_ \_ TYPE-Enumerationstyp \_** wird von der [**Certificate.Save-Methode**](certificate-save.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




