---
description: Definiert die Namen der erweiterten Schlüssel Verwendung, die darauf basieren, wo Sie verwendet werden können.
ms.assetid: 78f9f9cb-46e7-4f81-a16e-503750a0d743
title: CAPICOM_EKU-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EKU
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: e1d2f4f435fa31df00b87e20254aad57b690b047
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359371"
---
# <a name="capicom_eku-enumeration"></a>CAPICOM- \_ EKU-Enumeration

Der **CAPICOM- \_ EKU** -Enumerationstyp definiert die Namen der erweiterten Schlüssel Verwendung, die darauf basieren, wo Sie verwendet werden können.

## <a name="members"></a>Member



| Member                                     | BESCHREIBUNG                                                                                                                                                 | Wert |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **Weitere CAPICOM- \_ EKU \_ other**                    | Das Zertifikat verfügt über in der lokalen Richtlinie definierte Verwendung. Diese wird verwendet, wenn die erforderliche EKU nicht vordefiniert ist und der OID-Wert von der Anwendung festgelegt werden muss.<br/> | 0     |
| **CAPICOM- \_ EKU- \_ Server Authentifizierung \_**             | Das Zertifikat kann zum Authentifizieren eines Servers verwendet werden.<br/>                                                                                                | 1     |
| **CAPICOM- \_ EKU- \_ Client Authentifizierung \_**             | Das Zertifikat kann zum Authentifizieren eines Clients verwendet werden.<br/>                                                                                                | 2     |
| **CAPICOM- \_ EKU- \_ Code \_ Signatur**            | Das Zertifikat kann verwendet werden, um eine digitale Signatur zu erstellen.<br/>                                                                                           | 3     |
| **CAPICOM \_ EKU \_ -e-Mail- \_ Schutz**        | Zertifikat kann für den e-Mail-Schutz verwendet werden.<br/>                                                                                                    | 4     |
| **CAPICOM \_ EKU \_ Smartcard- \_ Anmeldung**         | Das Zertifikat kann für die Smartcard-Anmeldung verwendet werden. Eingeführt in CAPICOM 2,0.<br/>                                                                         | 5     |
| **CAPICOM- \_ EKU- \_ verschlüsselndes \_ Datei \_ System** | Das Zertifikat kann für EFS verwendet werden. Eingeführt in CAPICOM 2,0.<br/>                                                                                      | 6     |



## <a name="remarks"></a>Bemerkungen

Der **\_ EKU** -Enumerationstyp CAPICOM wird von der [**EKU verwendet. Name**](eku-name.md) -Eigenschaft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




