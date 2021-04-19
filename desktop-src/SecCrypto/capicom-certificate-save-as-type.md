---
description: Definiert das Format einer Datei mit Zertifikat Informationen.
ms.assetid: 417a6d1b-6329-418c-823c-d82b94207fd6
title: CAPICOM_CERTIFICATE_SAVE_AS_TYPE-Enumeration (CAPICOM. h)
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
ms.openlocfilehash: 1e5365594a5a1cf1f06691c63b37c04f38530575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372050"
---
# <a name="capicom_certificate_save_as_type-enumeration"></a>\_ \_ \_ \_ Datentyp-Enumeration des CAPICOM-Zertifikats

Der Enumerationstyp " **CAPICOM- \_ Zertifikat \_ speichern \_ \_** unter" definiert das Format einer Datei mit Zertifikat Informationen. Dieser Enumerationstyp wurde von CAPICOM 2,0 eingeführt.

## <a name="members"></a>Member



| Member                                  | BESCHREIBUNG                                                                                                                                   | Wert |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ - \_ Zertifikat \_ als \_ PFX speichern** | Die Ausgabedatei wird als PFX-Datei (PKCS 12) formatiert, und alle zugehörigen privaten Schlüssel, die exportierbar sind, werden ebenfalls gespeichert.<br/> | 0     |
| **CAPICOM- \_ Zertifikat \_ speichern \_ als \_ CER** | Die Ausgabedatei wird als CER-Datei formatiert, ohne dass private Schlüssel gespeichert werden.<br/>                                                        | 1     |



## <a name="remarks"></a>Bemerkungen

Der Enumerationstyp " **CAPICOM- \_ Zertifikat \_ speichern \_ als \_** " wird von der [**Certificate. Save**](certificate-save.md) -Methode verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




