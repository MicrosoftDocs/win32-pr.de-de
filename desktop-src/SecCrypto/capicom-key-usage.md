---
description: Die CAPICOM \_ KEY \_ USAGE-Enumeration definiert die Verwendungsmöglichkeiten eines Schlüssels. Eingeführt in CAPICOM 2.0.
ms.assetid: 7143567b-5882-44a3-ae30-fb8965fb7997
title: CAPICOM_KEY_USAGE-Enumeration (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_USAGE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: bb477ee12b33c3d32fd2c48a56831dc2f56244b1e8a564cd2d0482e6e4a5d5bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772425"
---
# <a name="capicom_key_usage-enumeration"></a>CAPICOM \_ KEY \_ USAGE-Enumeration

Die **CAPICOM \_ KEY \_ USAGE-Enumeration** definiert die Verwendungsmöglichkeiten eines Schlüssels. Eingeführt in CAPICOM 2.0.

## <a name="members"></a>Member



| Member                                      | Beschreibung                                                                                                                      | Wert      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|------------|
| **\_VERWENDUNG DES CAPICOM DIGITAL SIGNATURE \_ \_ KEY \_** | Der Schlüssel kann zum Erstellen einer digitalen Signatur verwendet werden.<br/>                                                                    | 0x00000080 |
| **\_VERWENDUNG VON CAPICOM-NICHTABWEISUNGSSCHLÜSSELN \_ \_ \_**   | Der Schlüssel kann für [*die Nichtabrufbarkeit*](../secgloss/n-gly.md)verwendet werden.<br/> | 0x00000040 |
| **VERWENDUNG DES \_ CAPICOM-SCHLÜSSELSCHLÜSSELS \_ \_ \_**  | Der Schlüssel kann zum Verschlüsseln eines Schlüssels verwendet werden.<br/>                                                                                 | 0x00000020 |
| **NUTZUNG DES \_ CAPICOM-DATENSCHLÜSSELS \_ \_ \_** | Der Schlüssel kann zum Verschlüsseln von Daten verwendet werden.<br/>                                                                                  | 0x00000010 |
| **NUTZUNG DES SCHLÜSSELS DER \_ CAPICOM-SCHLÜSSELVEREINBARUNG \_ \_ \_**     | Der Schlüssel kann für die Schlüsselvereinbarung verwendet werden.<br/>                                                                                | 0x00000008 |
| **\_VERWENDUNG DES CAPICOM-SCHLÜSSELZERTIFIKAT-SIGNSCHLÜSSELS \_ \_ \_ \_**    | Der Schlüssel kann zum Signieren von Schlüsselzertifikaten verwendet werden. Dieser Wert entspricht der VERWENDUNG DES CAPICOM \_ OFFLINE \_ CRL \_ SIGN \_ \_ KEY.<br/> | 0x00000004 |
| **\_VERWENDUNG DES CAPICOM-OFFLINE-SPERRLISTEN-ANMELDESCHLÜSSELS \_ \_ \_ \_** | Der Schlüssel kann zum Signieren von Schlüsselzertifikaten verwendet werden. Dieser Wert entspricht der VERWENDUNG VON CAPICOM \_ KEY \_ CERT \_ SIGN \_ \_ KEY.<br/>    | 0x00000002 |
| **\_VERWENDUNG DES CAPICOM-SPERRLISTEN-ANMELDESCHLÜSSELS \_ \_ \_**          | Der Schlüssel kann zum Signieren verwendet werden.<br/>                                                                                      | 0x00000002 |
| **CAPICOM \_ ENCIPHER \_ ONLY \_ KEY \_ USAGE**     | Der Schlüssel kann nur zum Verschlüsseln verwendet werden.<br/>                                                                                  | 0x00000001 |
| **CAPICOM: \_ \_ NUR \_ \_ SCHLÜSSELVERWENDUNG ENTSCHLÜSSELN**     | Der Schlüssel kann nur zum Entschlüsseln verwendet werden.<br/>                                                                                  | 0x00008000 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
