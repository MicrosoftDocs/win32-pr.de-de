---
description: Definiert die CAPICOM-Eigenschaftenbezeichner.
ms.assetid: faf10018-3ed8-4de6-9838-c553626f6dd7
title: CAPICOM_PROPID-Enumeration (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_PROPID
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 6d99c823d5396d2b8ece4484fa8888dff19b7898fb7d3b6ebedc5841b85c7e80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772266"
---
# <a name="capicom_propid-enumeration"></a>CAPICOM \_ PROPID-Enumeration

Die **CAPICOM \_ PROPID-Enumeration** definiert die CAPICOM-Eigenschaftsbezeichner.

## <a name="members"></a>Member



| Member                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                | Wert      |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ PROPID \_ UNKNOWN**                           | Der Typ der Eigenschaft ist nicht bekannt.<br/>                                                                                                                                                                                                                                          | 0          |
| **CAPICOM \_ PROPID \_ KEY \_ PROV \_ HANDLE**                 | Ein Handle für einen Schlüsselcontainer innerhalb eines [*Kryptografiedienstanbieters (Cryptographic Service Provider,*](../secgloss/c-gly.md) CSP).<br/>                                                                                        | 1          |
| **CAPICOM \_ PROPID \_ KEY \_ PROV \_ INFO**                   | Informationen zu einem Schlüsselcontainer in einem CSP.<br/>                                                                                                                                                                                                                                 | 2          |
| **CAPICOM \_ PROPID \_ SHA1 \_ HASH**                        | Ein SHA1-Hashobjekt.<br/>                                                                                                                                                                                                                                                             | 3          |
| **CAPICOM \_ PROPID \_ HASH \_ PROP**                        | Die Eigenschaften eines Hashobjekts.<br/>                                                                                                                                                                                                                                                | 3          |
| **CAPICOM \_ PROPID \_ MD5 \_ HASH**                         | Ein MD5-Hashobjekt.<br/>                                                                                                                                                                                                                                                             | 4          |
| **CAPICOM \_ PROPID \_ KEY \_ CONTEXT**                      | Der [*Schlüsselkontext*](../secgloss/c-gly.md).<br/>                                                                                                                                                                                                | 5          |
| **SPEZIFIKATION DES \_ CAPICOM-PROPID-SCHLÜSSELS \_ \_**                         | Die Spezifikationen für einen Schlüssel.<br/>                                                                                                                                                                                                                                                   | 6          |
| **CAPICOM \_ PROPID \_ IE30 \_ RESERVIERT**                    | Informationen darüber, ob das Objekt in Internet Explorer 3.0 reserviert ist.<br/>                                                                                                                                                                                                      | 7          |
| **CAPICOM \_ PROPID \_ PUBKEY \_ HASH \_ RESERVIERT**            | Informationen darüber, ob der Hash des öffentlichen Schlüssels reserviert ist.<br/>                                                                                                                                                                                                               | 8          |
| **CAPICOM \_ PROPID \_ ENHKEY \_ USAGE**                     | Eine erweiterte Schlüsselverwendung (Enhanced [*Key Usage,*](../secgloss/e-gly.md) EKU).<br/>                                                                                                                                                              | 9          |
| **CAPICOM \_ PROPID \_ CTL \_ USAGE**                        | Verwendung einer [*Zertifikatvertrauensliste*](../secgloss/c-gly.md) (Certificate Trust List, CTL).<br/>                                                                                                                                             | 9          |
| **CAPICOM \_ PROPID \_ SPEICHERORT DES NÄCHSTEN \_ UPDATES \_**            | Der Speicherort des nächsten Updates der [*Zertifikatsperrliste*](../secgloss/c-gly.md) (Certificate Revocation List, CRL).<br/>                                                                                               | 10         |
| **ANZEIGENAME DER \_ CAPICOM-PROPID \_ \_**                    | Ein für Menschen lesbarer Name.<br/>                                                                                                                                                                                                                                                          | 11         |
| **CAPICOM \_ PROPID \_ \_ PVK-DATEI**                         | Eine Datei, die einen privaten Schlüssel enthält.<br/>                                                                                                                                                                                                                                             | 12         |
| **CAPICOM \_ PROPID \_ DESCRIPTION**                       | Eine lesbare Beschreibung.<br/>                                                                                                                                                                                                                                                   | 13         |
| **CAPICOM \_ PROPID \_ ACCESS \_ STATE**                     | Der Zustand des Zugriffs.<br/>                                                                                                                                                                                                                                                        | 14         |
| **CAPICOM \_ PROPID \_ SIGNATURE \_ HASH**                   | Ein Hash der Signatur.<br/>                                                                                                                                                                                                                                                        | 15         |
| **CAPICOM \_ \_ PROPID-SMARTCARDDATEN \_ \_**                 | Smartcarddaten.<br/>                                                                                                                                                                                                                                                                | 16         |
| **CAPICOM \_ PROPID \_ EFS**                               | Ein [*verschlüsselndes Dateisystem*](../secgloss/e-gly.md) (EFS).<br/>                                                                                                                                                  | 17         |
| **CAPICOM \_ PROPID \_ FORTEZZA \_ DATA**                    | Daten, die mit den kryptografischen Protokollen und Algorithmen des [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST) erstellt wurden.<br/> | 18         |
| **CAPICOM \_ PROPID \_ ARCHIVED**                          | Informationen darüber, ob das Objekt archiviert wird.<br/>                                                                                                                                                                                                                               | 19         |
| **CAPICOM \_ PROPID \_ KEY \_ IDENTIFIER**                   | Ein Schlüsselbezeichner.<br/>                                                                                                                                                                                                                                                               | 20         |
| **CAPICOM \_ PROPID \_ AUTO \_ ENROLL**                      | Informationen zur automatischen Registrierung für ein Zertifikat.<br/>                                                                                                                                                                                                                                  | 21         |
| **CAPICOM \_ PROPID \_ PUBKEY \_ ALG \_ PARA**                 | Parameter für einen Algorithmus mit öffentlichem Schlüssel.<br/>                                                                                                                                                                                                                                          | 22         |
| **CAPICOM \_ PROPID \_ – ZERTIFIKATÜBERGREIFENDE \_ \_ \_ DIST-PUNKTE**         | Informationen, die zum Aktualisieren dynamischer zertifikatübergreifender Zertifikate verwendet werden.<br/>                                                                                                                                                                                                                          | 23         |
| **CAPICOM \_ PROPID \_ ISSUER \_ PUBLIC \_ KEY \_ MD5 \_ HASH**    | Der MD5-Hash des öffentlichen Schlüssels des Ausstellers.<br/>                                                                                                                                                                                                                                        | 24         |
| **CAPICOM \_ PROPID \_ SUBJECT \_ PUBLIC \_ KEY \_ MD5 \_ HASH**   | Der MD5-Hash des öffentlichen Schlüssels des Antragstellers.<br/>                                                                                                                                                                                                                                       | 25         |
| **CAPICOM \_ \_ PROPID-REGISTRIERUNG**                        | Informationen zur Registrierung des Zertifikats.<br/>                                                                                                                                                                                                                                 | 26         |
| **CAPICOM \_ PROPID \_ DATE \_ STAMP**                       | Ein Datumsstempel.<br/>                                                                                                                                                                                                                                                                   | 27         |
| **MD5-HASH DER SERIENNUMMER DES \_ CAPICOM-PROPID-AUSSTELLERS \_ \_ \_ \_ \_** | Der MD5-Hash der Seriennummer des Ausstellers.<br/>                                                                                                                                                                                                                                     | 28         |
| **CAPICOM \_ PROPID \_ SUBJECT \_ NAME \_ MD5 \_ HASH**          | Der MD5-Hash des Antragstellernamens.<br/>                                                                                                                                                                                                                                             | 29         |
| **\_ \_ ERWEITERTE \_ \_ FEHLERINFORMATIONEN ZU CAPICOM PROPID**             | Erweiterte Informationen zu einem Fehler.<br/>                                                                                                                                                                                                                                            | 30         |
| **CAPICOM \_ PROPID \_ RENEWAL**                           | Informationen zur Erneuerung einer [*Zertifizierungsstelle.*](../secgloss/c-gly.md)<br/>                                                                                                                     | 64         |
| **CAPICOM \_ PROPID \_ ARCHIVED \_ KEY \_ HASH**               | Ein archivierter Hash eines Schlüssels.<br/>                                                                                                                                                                                                                                                      | 65         |
| **CAPICOM \_ PROPID \_ FIRST \_ RESERVIERT**                   | Informationen zur ersten Reservierung.<br/>                                                                                                                                                                                                                                        | 66         |
| **CAPICOM \_ PROPID \_ LAST \_ RESERVED**                    | Informationen zur letzten Reservierung.<br/>                                                                                                                                                                                                                                  | 0x00007FFF |
| **CAPICOM \_ PROPID \_ FIRST \_ USER**                       | Informationen zum ersten Benutzer.<br/>                                                                                                                                                                                                                                               | 0x00008000 |
| **CAPICOM \_ PROPID \_ LAST \_ USER**                        | Informationen zum letzten Benutzer.<br/>                                                                                                                                                                                                                                         | 0x0000FFFF |



## <a name="remarks"></a>Hinweise

Diese Enumeration wird von den folgenden CAPICOM-Eigenschaften verwendet:

-   [**ExtendedProperty.PropID**](extendedproperty-propid.md)
-   [**ExtendedProperties.Remove**](extendedproperties-remove.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
