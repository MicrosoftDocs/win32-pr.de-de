---
description: Definiert, welche Informationen von einem Zertifikat abgefragt werden sollen.
ms.assetid: b603c06b-e6d4-4d5d-92b2-3b4f5b93478a
title: CAPICOM_CERT_INFO_TYPE-Enumeration (CAPICOM. h)
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
ms.openlocfilehash: 8e38bb8940645bbefecb3822bce8de8c2e0eb902
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360418"
---
# <a name="capicom_cert_info_type-enumeration"></a>CAPICOM \_ CERT \_ - \_ Infotyp-Enumeration

Der Typ " **CAPICOM \_ CERT \_ Info \_ Type** Enumeration" definiert, welche Informationen von einem Zertifikat abgefragt werden sollen.

## <a name="members"></a>Member



| Member                                         | BESCHREIBUNG                                                                                  | Wert |
|------------------------------------------------|----------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ CERT \_ Info \_ Subject \_ Simple \_ Name** | Gibt den anzeigen amen des Zertifikats Antragstellers zurück.<br/>                              | 0     |
| **Name der von CAPICOM \_ CERT \_ Info \_ Aussteller \_ einfacher \_**  | Gibt den anzeigen amen des Zertifikats Ausstellers zurück.<br/>                        | 1     |
| **Name der "CAPICOM \_ CERT \_ Info \_ Subject \_ Email \_ "**  | Gibt die e-Mail-Adresse des Zertifikat Antragstellers zurück.<br/>                             | 2     |
| **Name der \_ \_ \_ Aussteller \_ -e-Mail \_ des CAPICOM-Zertifikats**   | Gibt die e-Mail-Adresse des Zertifikats Ausstellers zurück.<br/>                       | 3     |
| **Antragsteller \_ - \_ \_ \_ UPN für CAPICOM CERT Info**          | Gibt den UPN des Zertifikat Antragstellers zurück. Eingeführt in CAPICOM 2,0.<br/>            | 4     |
| **-UPN des CAPICOM \_ CERT \_ Info- \_ Ausstellers \_**           | Gibt den UPN des Zertifikats Ausstellers zurück. Eingeführt in CAPICOM 2,0.<br/>      | 5     |
| **"CAPICOM \_ CERT \_ Info \_ Subject \_ DNS \_ Name"**    | Gibt den DNS-Namen des Zertifikat Antragstellers zurück. Eingeführt in CAPICOM 2,0.<br/>       | 6     |
| **Name des CAPICOM \_ CERT \_ Info-Aussteller- \_ \_ DNS \_**     | Gibt den DNS-Namen des Zertifikats Ausstellers zurück. Eingeführt in CAPICOM 2,0.<br/> | 7     |



## <a name="remarks"></a>Bemerkungen

Der-Enumerationstyp des **CAPICOM- \_ CERT- \_ \_ Typs** wird von der [**Certificate. GetInfo**](certificate-getinfo.md) -Methode verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




