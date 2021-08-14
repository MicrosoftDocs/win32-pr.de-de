---
description: Definiert die Bedingungen, für die eine Zertifikatkette überprüft werden soll.
ms.assetid: 87df623c-5661-4325-8dd6-393ce2e44066
title: CAPICOM_CHECK_FLAG -Enumeration (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CHECK_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 4b9fbc5ec1717acbd32c70ea3467465daf47de5d41af794a5164f44174a602d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772512"
---
# <a name="capicom_check_flag-enumeration"></a>CAPICOM \_ CHECK \_ FLAG-Enumeration

Der **CAPICOM \_ CHECK \_ FLAG-Enumerationstyp** definiert die Bedingungen, auf die eine Zertifikatskette überprüft werden soll.

## <a name="members"></a>Member



| Member                                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Wert      |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ CHECK \_ NONE**                        | Es wird keine Gültigkeitsprüfung durchgeführt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 0x00000000 |
| **CAPICOM \_ CHECK \_ TRUSTED \_ ROOT**               | Sucht nach einem vertrauenswürdigen Stamm der Zertifikatkette.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | 0x00000001 |
| **GÜLTIGKEIT DER \_ \_ CAPICOM-ÜBERPRÜFUNGSZEIT \_**              | Überprüft die Gültigkeit aller Zertifikate in der Kette.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | 0x00000002 |
| **CAPICOM \_ CHECK \_ SIGNATURE \_ VALIDITY**         | Überprüft auf gültige Signaturen für alle Zertifikate in der Kette.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 0x00000004 |
| **CAPICOM \_ CHECK \_ ONLINE \_ REVOCATION \_ STATUS**  | Überprüft den Sperrstatus aller Zertifikate in der Kette mithilfe von Zertifikatsperrlisten (Certificate Revocation Lists, CRLs), die online verfügbar sind. Zertifikatsperrlisten werden mithilfe der CRL-Verteilungspunkterweiterung (CRL Distribution Point, CDP) im Zertifikat heruntergeladen. <br/> Wenn die Zertifikatsperrliste heruntergeladen wurde und noch nicht abgelaufen ist, verwendet CAPICOM sie und geht nicht online. Wenn eine Zertifikatsperrliste nicht heruntergeladen wurde oder veraltet ist, geht CAPICOM online, um zu versuchen, die Zertifikatsperrliste herunterzuladen.<br/> Dieses Flag wird ignoriert, wenn auch CAPICOM \_ CHECK OFFLINE REVOCATION STATUS angegeben \_ \_ \_ wird.<br/> | 0x00000008 |
| **CAPICOM \_ CHECK \_ OFFLINE \_ REVOCATION \_ STATUS** | Überprüft den Sperrstatus aller Zertifikate in der Kette nur mithilfe von Offline-CRLs. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              | 0x00000010 |
| **CAPICOM \_ CHECK \_ COMPLETE \_ CHAIN**             | Überprüft die gesamte Kette. Eingeführt in CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | 0x00000020 |
| **CAPICOM \_ CHECK \_ NAME \_ CONSTRAINTS**           | Überprüft Namenseinschränkungen. Eingeführt in CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | 0x00000040 |
| **CAPICOM \_ CHECK \_ BASIC \_ CONSTRAINTS**          | Überprüft grundlegende Einschränkungen. Eingeführt in CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | 0x00000080 |
| **CAPICOM \_ CHECK \_ NESTED \_ VALIDITY \_ PERIOD**    | Überprüft die geschachtelte Gültigkeit. Eingeführt in CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | 0x00000100 |
| **CAPICOM \_ CHECK \_ ONLINE \_ ALL**                 | Überprüft alle Bedingungen außer CAPICOM \_ CHECK \_ OFFLINE REVOCATION \_ \_ STATUS. Sperrprüfungen werden für alle Zertifikate in der Kette mit Ausnahme des Stammzertifikats ausgeführt. Eingeführt in CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                               | 0x000001EF |
| **CAPICOM \_ CHECK \_ OFFLINE \_ ALL**                | Überprüft alle Bedingungen außer CAPICOM \_ CHECK \_ ONLINE REVOCATION \_ \_ STATUS. Sperrprüfungen werden für alle Zertifikate in der Kette mit Ausnahme des Stammzertifikats ausgeführt. Eingeführt in CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                | 0x000001F7 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




