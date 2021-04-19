---
description: Die "CAPICOM \_ Key Usage"- \_ Enumeration definiert die Methoden, mit denen ein Schlüssel verwendet werden kann. Eingeführt in CAPICOM 2,0.
ms.assetid: 7143567b-5882-44a3-ae30-fb8965fb7997
title: CAPICOM_KEY_USAGE-Enumeration (CAPICOM. h)
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
ms.openlocfilehash: 1d44c7f3ecf35ddeb55dd96e5513261691010990
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359352"
---
# <a name="capicom_key_usage-enumeration"></a>CAPICOM- \_ Schlüssel \_ Verwendungs Enumeration

Die " **CAPICOM \_ Key \_ Usage** "-Enumeration definiert die Methoden, mit denen ein Schlüssel verwendet werden kann. Eingeführt in CAPICOM 2,0.

## <a name="members"></a>Member



| Member                                      | BESCHREIBUNG                                                                                                                      | Wert      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|------------|
| **Verwendung von CAPICOM \_ Digital \_ Signature \_ Key \_** | Der Schlüssel kann verwendet werden, um eine digitale Signatur zu erstellen.<br/>                                                                    | 0x00000080 |
| **Verwendung von CAPICOM- \_ nicht \_ Ablehnungs \_ Schlüsseln \_**   | Der Schlüssel kann für die [*Nichtabstreitbarkeit*](../secgloss/n-gly.md)verwendet werden.<br/> | 0x00000040 |
| **Verwendung des CAPICOM- \_ Schlüssel \_ Verschlüsselungs \_ Schlüssels \_**  | Der Schlüssel kann verwendet werden, um einen Schlüssel zu verschlüsseln.<br/>                                                                                 | 0x00000020 |
| **Verwendung des CAPICOM- \_ Daten \_ Verschlüsselungs \_ Schlüssels \_** | Der Schlüssel kann zum Verschlüsseln von Daten verwendet werden.<br/>                                                                                  | 0x00000010 |
| **Verwendung von CAPICOM \_ Key \_ Agreement \_ Key \_**     | Der Schlüssel kann für die Schlüssel Übereinstimmung verwendet werden.<br/>                                                                                | 0x00000008 |
| **Verwendung von CAPICOM \_ Key \_ CERT \_ Sign \_ Key \_**    | Der Schlüssel kann zum Signieren von Schlüsselzertifikaten verwendet werden. Dieser Wert entspricht der Verwendung von CAPICOM- \_ Offline- \_ CRL- \_ Signatur \_ Schlüsseln \_ .<br/> | 0x00000004 |
| **Verwendung von CAPICOM- \_ Offline- \_ CRL- \_ Signatur \_ Schlüsseln \_** | Der Schlüssel kann zum Signieren von Schlüsselzertifikaten verwendet werden. Dieser Wert entspricht der Verwendung von CAPICOM \_ Key \_ CERT \_ Sign \_ Key \_ .<br/>    | 0x00000002 |
| **Verwendung von CAPICOM- \_ CRL- \_ Signatur \_ Schlüsseln \_**          | Der Schlüssel kann zum Signieren verwendet werden.<br/>                                                                                      | 0x00000002 |
| **nur CAPICOM- \_ \_ \_ Schlüssel \_ Verwendung**     | Der Schlüssel kann nur zum Verschlüsseln verwendet werden.<br/>                                                                                  | 0x00000001 |
| **nur CAPICOM \_ Decipher \_ \_ Key \_ Usage**     | Der Schlüssel kann nur zum Entschlüsseln verwendet werden.<br/>                                                                                  | 0x00008000 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
