---
description: Definiert, welche Informationen von einem Zertifikat abgefragt werden sollen.
ms.assetid: b603c06b-e6d4-4d5d-92b2-3b4f5b93478a
title: CAPICOM_CERT_INFO_TYPE -Enumeration (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERT_INFO_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 480238556fce0470c51f00c394dd8566160686561342ec91da2e136c44a43cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879420"
---
# <a name="capicom_cert_info_type-enumeration"></a>CAPICOM \_ CERT \_ INFO \_ TYPE-Enumeration

Der **CAPICOM \_ CERT \_ INFO TYPE-Enumerationstyp \_** definiert, welche Informationen von einem Zertifikat abgefragt werden sollen.

## <a name="members"></a>Member



| Member                                         | BESCHREIBUNG                                                                                  | Wert |
|------------------------------------------------|----------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ CERT \_ INFO \_ SUBJECT \_ SIMPLE \_ NAME** | Gibt den Anzeigenamen des Zertifikatsubjekts zurück.<br/>                              | 0     |
| **CAPICOM \_ CERT \_ INFO \_ ISSUER \_ SIMPLE \_ NAME**  | Gibt den Anzeigenamen des Zertifikatausstellers zurück.<br/>                        | 1     |
| **CAPICOM \_ CERT \_ INFO \_ SUBJECT \_ EMAIL \_ NAME**  | Gibt die E-Mail-Adresse des Zertifikatsubjekts zurück.<br/>                             | 2     |
| **CAPICOM \_ CERT \_ INFO \_ ISSUER \_ EMAIL \_ NAME**   | Gibt die E-Mail-Adresse des Zertifikatausstellers zurück.<br/>                       | 3     |
| **CAPICOM \_ CERT \_ INFO \_ SUBJECT \_ UPN**          | Gibt den UPN des Zertifikatssubjekts zurück. Eingeführt in CAPICOM 2.0.<br/>            | 4     |
| **CAPICOM \_ CERT \_ INFO \_ ISSUER \_ UPN**           | Gibt den UPN des Zertifikatausstellers zurück. Eingeführt in CAPICOM 2.0.<br/>      | 5     |
| **DNS-NAME DES \_ SUBJEKTS FÜR CAPICOM-ZERTIFIKATINFORMATIONEN \_ \_ \_ \_**    | Gibt den DNS-Namen des Zertifikatsubjekts zurück. Eingeführt in CAPICOM 2.0.<br/>       | 6     |
| **CAPICOM \_ CERT \_ INFO \_ ISSUER \_ DNS \_ NAME**     | Gibt den DNS-Namen des Zertifikatausstellers zurück. Eingeführt in CAPICOM 2.0.<br/> | 7     |



## <a name="remarks"></a>Hinweise

Der **CAPICOM \_ CERT \_ INFO TYPE-Enumerationstyp \_** wird von der [**Certificate.GetInfo-Methode**](certificate-getinfo.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




