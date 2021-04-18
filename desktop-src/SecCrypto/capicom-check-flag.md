---
description: Definiert die Bedingungen, für die eine Zertifikat Kette geprüft werden soll.
ms.assetid: 87df623c-5661-4325-8dd6-393ce2e44066
title: CAPICOM_CHECK_FLAG-Enumeration (CAPICOM. h)
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
ms.openlocfilehash: 47b6168fb87ebbb65b07eadfe9adaf488934e252
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368298"
---
# <a name="capicom_check_flag-enumeration"></a>CAPICOM- \_ Check- \_ Flag-Enumeration

Der Enumerationstyp " **CAPICOM- \_ \_ checkflag** " definiert die Bedingungen, für die eine Zertifikat Kette überprüft werden soll.

## <a name="members"></a>Member



| Member                                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Wert      |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM- \_ Überprüfung nicht \_**                        | Keine Gültigkeits Überprüfung erfolgt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 0x00000000 |
| **CAPICOM- \_ Überprüfung \_ vertrauenswürdiger Stamm \_**               | Überprüft, ob ein vertrauenswürdiger Stamm der Zertifikat Kette besteht.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | 0x00000001 |
| **\_ \_ Gültigkeitsdauer für CAPICOM-Prüfung \_**              | Überprüft die Gültigkeitsdauer aller Zertifikate in der Kette.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | 0x00000002 |
| **CAPICOM- \_ Überprüfung der \_ Signatur \_ Gültigkeit**         | Prüft auf gültige Signaturen für alle Zertifikate in der Kette.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 0x00000004 |
| **CAPICOM \_ \_ -Online \_ Sperr \_ Status überprüfen**  | Überprüft den Sperr Status aller Zertifikate in der Kette mithilfe der Online verfügbaren Zertifikat Sperr Listen (CRLs). CRLs werden mithilfe der CDP-Erweiterung (CRL Distribution Point) im Zertifikat heruntergeladen. <br/> Wenn die CRL heruntergeladen wurde und noch nicht abgelaufen ist, wird Sie von CAPICOM verwendet und nicht online geschaltet. Wenn eine Zertifikat Sperr Liste nicht heruntergeladen wurde oder veraltet ist, wechselt CAPICOM zum Versuch, die CRL herunterzuladen.<br/> Dieses Flag wird ignoriert, wenn der Status der CAPICOM- \_ Überprüfung im \_ Offline Modus \_ \_ ebenfalls angegeben ist.<br/> | 0x00000008 |
| **CAPICOM- \_ Überprüfung des \_ Offline Sperr \_ \_ Status** | Überprüft den Sperr Status aller Zertifikate in der Kette, die ausschließlich offline-CRLs verwenden. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              | 0x00000010 |
| **CAPICOM- \_ Überprüfung, \_ komplette \_ Kette**             | Überprüft die gesamte Kette. Eingeführt in CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | 0x00000020 |
| **Einschränkungen für "CAPICOM \_ Check \_ Name" \_**           | Überprüft namens Einschränkungen. Eingeführt in CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | 0x00000040 |
| **grundeinschränkungen für CAPICOM- \_ Überprüfung \_ \_**          | Überprüft grundlegende Einschränkungen. Eingeführt in CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | 0x00000080 |
| **Überprüfung der in der zwischen \_ Zeit überprüfen \_ \_ \_**    | Überprüft die eingesterte Gültigkeit. Eingeführt in CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | 0x00000100 |
| **CAPICOM \_ \_ Online \_ alle überprüfen**                 | Überprüft alle Bedingungen außer CAPICOM \_ Check \_ Offline-Sperr \_ \_ Status. Sperr Überprüfungen werden für alle Zertifikate in der Kette mit Ausnahme des Stamm Zertifikats durchgeführt. Eingeführt in CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                               | 0x000001ef |
| **CAPICOM \_ - \_ Prüfung \_ alle Offline**                | Überprüft alle Bedingungen außer CAPICOM \_ Check \_ Online-Sperr \_ \_ Status. Sperr Überprüfungen werden für alle Zertifikate in der Kette mit Ausnahme des Stamm Zertifikats durchgeführt. Eingeführt in CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                | 0x000001, f |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




