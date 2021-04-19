---
description: Definiert, welche Zertifikate in einer Kette gespeichert werden.
ms.assetid: 6f9e28e6-b01f-4803-8259-8ab73abeecf8
title: CAPICOM_CERTIFICATE_INCLUDE_OPTION-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_INCLUDE_OPTION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 45ea9ccf7d3a43e325073f04e28bbd392fa34998
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361332"
---
# <a name="capicom_certificate_include_option-enumeration"></a>CAPICOM \_ Certificate \_ include- \_ Option-Enumeration

Der " **CAPICOM \_ Certificate \_ include \_ Option** "-Enumerationstyp definiert, welche Zertifikate in einer Kette gespeichert werden. Dieser Enumerationstyp wurde in CAPICOM 2,0 eingeführt.

## <a name="members"></a>Member



| Member                                                 | BESCHREIBUNG                                                                           | Wert |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|-------|
| **CAPICOM- \_ Zertifikats \_ include- \_ Kette \_ mit Ausnahme von \_ root** | Speichert alle Zertifikate in der Kette mit Ausnahme der Stamm Entität.<br/> | 0     |
| **CAPICOM- \_ Zertifikat \_ einschließlich \_ ganzer \_ Kette**        | Speichert die komplette Zertifikatskette.<br/>                                      | 1     |
| **CAPICOM- \_ Zertifikat \_ schließt \_ nur End- \_ Entität \_ ein.**   | Speichert nur das Endentitäts Zertifikat.<br/>                                     | 2     |



## <a name="remarks"></a>Bemerkungen

Der Enumerationstyp " **CAPICOM \_ Certificate \_ include \_ Option** " wird von der [**Certificate. Save**](certificate-save.md) -Methode verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




