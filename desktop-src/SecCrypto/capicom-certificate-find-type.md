---
description: Der-Enumerationstyp "CAPICOM \_ Certificate \_ Find \_ Type" definiert den Typ der Suchkriterien, die zum Suchen nach bestimmten Zertifikaten verwendet werden. Dieser Enumerationstyp wurde in CAPICOM 2,0 eingeführt.
ms.assetid: d71436e5-d921-4b84-8028-301d8fc4aedb
title: CAPICOM_CERTIFICATE_FIND_TYPE-Enumeration (CAPICOM. h)
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
ms.openlocfilehash: c5c867b230ba2045d97619d7f55e257bd7803b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358253"
---
# <a name="capicom_certificate_find_type-enumeration"></a>CAPICOM \_ - \_ \_ Zertifikattyp-Enumeration

Der-Enumerationstyp " **CAPICOM \_ Certificate \_ Find \_ Type** " definiert den Typ der Suchkriterien, die zum Suchen nach bestimmten Zertifikaten verwendet werden. Dieser Enumerationstyp wurde in CAPICOM 2,0 eingeführt.

## <a name="members"></a>Member



| Member                                                | BESCHREIBUNG                                                                                                                                 | Wert |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM- \_ Zertifikat \_ Suche SHA1- \_ \_ Hash**            | Gibt Zertifikate zurück, die einem angegebenen SHA1-Hash entsprechen.<br/>                                                                             | 0     |
| **CAPICOM-Zertifikat suchantrags Teller \_ \_ \_ \_ Name**         | Gibt Zertifikate zurück, deren Antragsteller Name dem angegebenen Antragsteller Namen genau oder teilweise entspricht.<br/>                                   | 1     |
| **CAPICOM- \_ Zertifikat \_ Suchen des \_ Aussteller \_ namens**          | Gibt Zertifikate zurück, deren Aussteller Name exakt oder teilweise mit einem angegebenen Aussteller Namen übereinstimmt.<br/>                                     | 2     |
| **CAPICOM- \_ Zertifikat \_ \_ \_ suchstammname**            | Gibt Zertifikate zurück, deren Stamm Antragsteller Name exakt oder teilweise mit einem angegebenen Stamm Antragsteller Namen übereinstimmt.<br/>                         | 3     |
| **CAPICOM- \_ Zertifikat \_ Suchen \_ Vorlagen \_ Name**        | Gibt Zertifikate zurück, deren Vorlagen Name mit einem angegebenen Vorlagen Namen übereinstimmt.<br/>                                                      | 4     |
| **CAPICOM- \_ Zertifikat \_ Suche- \_ Erweiterung**             | Gibt Zertifikate zurück, die eine Erweiterung aufweisen, die mit einer angegebenen Erweiterung übereinstimmt.<br/>                                                  | 5     |
| **CAPICOM- \_ Zertifikat für \_ \_ Erweiterte \_ Eigenschaft suchen**    | Gibt Zertifikate mit einer erweiterten Eigenschaft zurück, deren Eigenschaften Bezeichner mit einem angegebenen Eigenschaften Bezeichner übereinstimmt.<br/>           | 6     |
| **CAPICOM- \_ Zertifikat \_ Suche- \_ Anwendungs \_ Richtlinie**   | Gibt Zertifikate im Speicher zurück, die entweder über eine erweiterte Schlüssel Verwendungs Erweiterung oder-Eigenschaft in Kombination mit einem Verwendungs Bezeichner verfügen.<br/> | 7     |
| **CAPICOM- \_ Zertifikat Zertifikat \_ \_ \_ Richtlinie suchen**   | Gibt Zertifikate zurück, die eine angegebene Richtlinien OID enthalten.<br/>                                                                          | 8     |
| **zulässige Zeit für CAPICOM- \_ Zertifikat \_ Suche \_ \_ gültig**           | Gibt Zertifikate zurück, deren Zeit gültig ist.<br/>                                                                                        | 9     |
| **Das CAPICOM- \_ Zertifikat ist \_ \_ \_ \_ noch nicht \_ gültig.** | Gibt Zertifikate zurück, deren Zeit noch nicht gültig ist.<br/>                                                                                | 10    |
| **Zeit für das CAPICOM- \_ Zertifikat ist \_ \_ \_ abgelaufen.**         | Gibt Zertifikate zurück, deren Zeit abgelaufen ist.<br/>                                                                                     | 11    |
| **CAPICOM- \_ Zertifikat \_ Suche \_ Schlüssel \_ Verwendung**            | Gibt Zertifikate zurück, die einen Schlüssel enthalten, der in der angegebenen Weise verwendet werden kann.<br/>                                                  | 12    |



## <a name="remarks"></a>Bemerkungen

Der-Enumerationstyp " **CAPICOM \_ Certificate \_ Find \_ Type** " wird von der Certificate [**. Find**](certificates-find.md) -Methode verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




