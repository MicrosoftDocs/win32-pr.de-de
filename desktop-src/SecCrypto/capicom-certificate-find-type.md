---
description: Der CAPICOM \_ CERTIFICATE \_ FIND \_ TYPE-Enumerationstyp definiert den Typ der Suchkriterien, die zum Suchen nach bestimmten Zertifikaten verwendet werden. Dieser Enumerationstyp wurde in CAPICOM 2.0 eingeführt.
ms.assetid: d71436e5-d921-4b84-8028-301d8fc4aedb
title: CAPICOM_CERTIFICATE_FIND_TYPE -Enumeration (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_FIND_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: fb10b9289ae094f27fe29c3f2723d639eccc029aa7e5512833ac7e859c5c36ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772695"
---
# <a name="capicom_certificate_find_type-enumeration"></a>CAPICOM \_ CERTIFICATE \_ FIND \_ TYPE-Enumeration

Der **CAPICOM \_ CERTIFICATE FIND \_ TYPE-Enumerationstyp \_** definiert den Typ der Suchkriterien, die zum Suchen nach bestimmten Zertifikaten verwendet werden. Dieser Enumerationstyp wurde in CAPICOM 2.0 eingeführt.

## <a name="members"></a>Member



| Member                                                | Beschreibung                                                                                                                                 | Wert |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ CERTIFICATE \_ FIND \_ SHA1 \_ HASH**            | Gibt Zertifikate zurück, die mit einem angegebenen SHA1-Hash übereinstimmen.<br/>                                                                             | 0     |
| **CAPICOM \_ CERTIFICATE \_ FIND \_ SUBJECT \_ NAME**         | Gibt Zertifikate zurück, deren Betreffname genau oder teilweise mit einem angegebenen Betreffnamen entspricht.<br/>                                   | 1     |
| **CAPICOM \_ CERTIFICATE \_ FIND \_ ISSUER \_ NAME**          | Gibt Zertifikate zurück, deren Ausstellername einem angegebenen Ausstellernamen genau oder teilweise entspricht.<br/>                                     | 2     |
| **CAPICOM \_ CERTIFICATE FIND ROOT NAME (STAMMNAME DES CAPICOM-ZERTIFIKATS \_ \_ \_ SUCHEN)**            | Gibt Zertifikate zurück, deren Name des Stammsubjekts genau oder teilweise mit einem angegebenen Stammsubjektnamen entspricht.<br/>                         | 3     |
| **CAPICOM \_ CERTIFICATE \_ FIND \_ TEMPLATE \_ NAME**        | Gibt Zertifikate zurück, deren Vorlagenname einem angegebenen Vorlagennamen entspricht.<br/>                                                      | 4     |
| **CAPICOM \_ CERTIFICATE \_ FIND \_ EXTENSION**             | Gibt Zertifikate zurück, die über eine Erweiterung verfügen, die einer angegebenen Erweiterung entspricht.<br/>                                                  | 5     |
| **CAPICOM \_ CERTIFICATE \_ FIND \_ EXTENDED \_ PROPERTY**    | Gibt Zertifikate zurück, die über eine erweiterte Eigenschaft verfügen, deren Eigenschaftenbezeichner einem angegebenen Eigenschaftenbezeichner entspricht.<br/>           | 6     |
| **CAPICOM \_ CERTIFICATE \_ FIND \_ APPLICATION \_ POLICY**   | Gibt Zertifikate im Speicher zurück, die entweder über eine erweiterte Schlüsselverwendungserweiterung oder -eigenschaft in Kombination mit einem Nutzungsbezeichner verfügen.<br/> | 7     |
| **CAPICOM \_ CERTIFICATE \_ FIND \_ CERTIFICATE \_ POLICY**   | Gibt Zertifikate zurück, die eine angegebene Richtlinien-OID enthalten.<br/>                                                                          | 8     |
| **CAPICOM \_ CERTIFICATE \_ FIND \_ TIME \_ VALID**           | Gibt Zertifikate zurück, deren Zeit gültig ist.<br/>                                                                                        | 9     |
| **CAPICOM \_ CERTIFICATE \_ FIND \_ TIME \_ NOT \_ YET \_ VALID** | Gibt Zertifikate zurück, deren Zeit noch nicht gültig ist.<br/>                                                                                | 10    |
| **CAPICOM \_ CERTIFICATE \_ FIND \_ TIME \_ EXPIRED**         | Gibt Zertifikate zurück, deren Zeit abgelaufen ist.<br/>                                                                                     | 11    |
| **CAPICOM \_ CERTIFICATE \_ FIND \_ KEY \_ USAGE**            | Gibt Zertifikate zurück, die einen Schlüssel enthalten, der auf die angegebene Weise verwendet werden kann.<br/>                                                  | 12    |



## <a name="remarks"></a>Hinweise

Der **CAPICOM \_ CERTIFICATE FIND \_ TYPE-Enumerationstyp \_** wird von der [**Certificates.Find-Methode**](certificates-find.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




