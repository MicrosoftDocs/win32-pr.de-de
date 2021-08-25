---
description: Definiert das Format einer Datei, die Zertifikatinformationen enthält.
ms.assetid: 2118746a-9fa4-4e6a-82ce-e57f154f4a94
title: CAPICOM_CERTIFICATES_SAVE_AS_TYPE-Enumeration (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATES_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 70185a7a48b7dc195727991fb0dcc35f4909451fa0e4da5f4100e8385adebc2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879370"
---
# <a name="capicom_certificates_save_as_type-enumeration"></a>CAPICOM \_ CERTIFICATES SAVE AS \_ \_ \_ TYPE-Enumeration

Der **CAPICOM \_ CERTIFICATES SAVE AS \_ \_ TYPE-Enumerationstyp \_** definiert das Format einer Datei mit Zertifikatinformationen. Dieser Enumerationstyp wurde mit CAPICOM 2.0 eingeführt.

## <a name="members"></a>Member



| Member                                          | BESCHREIBUNG                                          | Wert |
|-------------------------------------------------|------------------------------------------------------|-------|
| **\_CAPICOM-ZERTIFIKATE \_ SPEICHERN ALS \_ \_ SERIALISIERT** | Die gespeicherten Zertifikate werden serialisiert.<br/>    | 0     |
| **\_CAPICOM-ZERTIFIKATE \_ SPEICHERN ALS \_ \_ PKCS7**      | Die Zertifikate werden als PKCS \# 7 gespeichert.<br/> | 1     |
| **\_CAPICOM-ZERTIFIKATE \_ SPEICHERN ALS \_ \_ PFX**        | Die Zertifikate werden als PFX gespeichert.<br/>      | 2     |



## <a name="remarks"></a>Hinweise

Der ENUMERATIONstyp CAPICOM \_ CERTIFICATES SAVE AS TYPE wird von der \_ \_ \_ [**Certificates.Save-Methode**](certificates-save.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




