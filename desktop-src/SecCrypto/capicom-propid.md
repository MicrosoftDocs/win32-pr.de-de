---
description: Definiert die CAPICOM-Eigenschaften Bezeichner.
ms.assetid: faf10018-3ed8-4de6-9838-c553626f6dd7
title: CAPICOM_PROPID-Enumeration (CAPICOM. h)
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
ms.openlocfilehash: d817262b869ef694c2cf9ff5b1e577840c3168a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359317"
---
# <a name="capicom_propid-enumeration"></a>CAPICOM- \_ PROPID-Enumeration

Die **CAPICOM \_ PROPID** -Enumeration definiert die CAPICOM-Eigenschaften Bezeichner.

## <a name="members"></a>Member



| Member                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                | Wert      |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ PROPID \_ unbekannt**                           | Der Typ der Eigenschaft ist nicht bekannt.<br/>                                                                                                                                                                                                                                          | 0          |
| **CAPICOM \_ PROPID \_ Key \_ Prov \_ handle**                 | Ein Handle für einen Schlüssel Container in einem [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP).<br/>                                                                                        | 1          |
| **Proxy Informationen zu CAPICOM \_ PROPID \_ Key \_ \_**                   | Informationen zu einem Schlüssel Container innerhalb eines CSP.<br/>                                                                                                                                                                                                                                 | 2          |
| **CAPICOM \_ PROPID \_ SHA1- \_ Hash**                        | Ein SHA1-Hash Objekt.<br/>                                                                                                                                                                                                                                                             | 3          |
| **CAPICOM \_ PROPID- \_ Hash- \_ Prop**                        | Die Eigenschaften eines Hash Objekts.<br/>                                                                                                                                                                                                                                                | 3          |
| **CAPICOM \_ PROPID \_ MD5- \_ Hash**                         | Ein MD5-Hash Objekt.<br/>                                                                                                                                                                                                                                                             | 4          |
| **CAPICOM- \_ PROPID- \_ Schlüssel \_ Kontext**                      | Der Schlüssel [*Kontext*](../secgloss/c-gly.md).<br/>                                                                                                                                                                                                | 5          |
| **CAPICOM- \_ PROPID- \_ Schlüssel \_ Spezifikation**                         | Die Spezifikationen für einen Schlüssel.<br/>                                                                                                                                                                                                                                                   | 6          |
| **CAPICOM \_ PROPID \_ IE30 \_ reserviert**                    | Informationen dazu, ob das Objekt in Internet Explorer 3,0 reserviert ist.<br/>                                                                                                                                                                                                      | 7          |
| **CAPICOM \_ PROPID \_ Pubkey- \_ Hash \_ reserviert**            | Informationen dazu, ob der Hash des öffentlichen Schlüssels reserviert ist.<br/>                                                                                                                                                                                                               | 8          |
| **CAPICOM \_ PROPID \_ enhkey- \_ Verwendung**                     | [*Erweiterte Schlüssel Verwendung (Enhanced Key Usage*](../secgloss/e-gly.md) , EKU).<br/>                                                                                                                                                              | 9          |
| **Verwendung von CAPICOM \_ PROPID \_ CTL \_**                        | Eine CTL ( [*Certificate Trust List*](../secgloss/c-gly.md) )-Verwendung.<br/>                                                                                                                                             | 9          |
| **CAPICOM \_ PROPID \_ Nächster \_ Update \_ Speicherort**            | Der Speicherort des nächsten Updates der [*Zertifikat Sperr Liste*](../secgloss/c-gly.md) .<br/>                                                                                               | 10         |
| **CAPICOM- \_ PROPID-Anzeige \_ \_ Name**                    | Ein lesbarer Name.<br/>                                                                                                                                                                                                                                                          | 11         |
| **CAPICOM \_ PROPID \_ PVK- \_ Datei**                         | Eine Datei, die einen privaten Schlüssel enthält.<br/>                                                                                                                                                                                                                                             | 12         |
| **CAPICOM- \_ PROPID- \_ Beschreibung**                       | Eine lesbare Beschreibung.<br/>                                                                                                                                                                                                                                                   | 13         |
| **CAPICOM- \_ PROPID- \_ Zugriffs \_ Status**                     | Der Status des Zugriffs.<br/>                                                                                                                                                                                                                                                        | 14         |
| **CAPICOM- \_ PROPID- \_ Signatur \_ Hash**                   | Ein Hash der Signatur.<br/>                                                                                                                                                                                                                                                        | 15         |
| **CAPICOM \_ PROPID \_ \_ Smartcard- \_ Daten**                 | Smartcarddaten.<br/>                                                                                                                                                                                                                                                                | 16         |
| **CAPICOM \_ PROPID \_ EFS**                               | Ein- [*verschlüsselndes Dateisystem*](../secgloss/e-gly.md) (EFS).<br/>                                                                                                                                                  | 17         |
| **CAPICOM \_ PROPID \_ Fortezza- \_ Daten**                    | Daten, die mit den kryptografischen Protokollen und Algorithmen erstellt werden, die im Besitz des [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST) sind.<br/> | 18         |
| **CAPICOM- \_ PROPID \_ archiviert**                          | Informationen dazu, ob das Objekt archiviert wird.<br/>                                                                                                                                                                                                                               | 19         |
| **CAPICOM- \_ PROPID- \_ Schlüssel \_ Bezeichner**                   | Ein Schlüssel Bezeichner.<br/>                                                                                                                                                                                                                                                               | 20         |
| **PDB-Registrierung für \_ CAPICOM \_ \_**                      | Informationen zur automatischen Registrierung für ein Zertifikat.<br/>                                                                                                                                                                                                                                  | 21         |
| **CAPICOM \_ PROPID \_ Pubkey \_ ALG \_ para**                 | Parameter für einen Algorithmus für öffentliche Schlüssel.<br/>                                                                                                                                                                                                                                          | 22         |
| **CAPICOM \_ PROPID- \_ Kreuz \_ Zertifikat-dist- \_ \_ Punkte**         | Informationen, die zum Aktualisieren dynamischer Kreuz Zertifikate verwendet werden.<br/>                                                                                                                                                                                                                          | 23         |
| **MD5- \_ Hash des \_ \_ öffentlichen \_ Schlüssels \_ \_ des CAPICOM PROPID-Ausstellers**    | Der MD5-Hash des öffentlichen Schlüssels des Ausstellers.<br/>                                                                                                                                                                                                                                        | 24         |
| **MD5- \_ Hash des \_ \_ öffentlichen \_ Schlüssels \_ \_ für CAPICOM PROPID**   | Der MD5-Hash des öffentlichen Schlüssels des Antragstellers.<br/>                                                                                                                                                                                                                                       | 25         |
| **CAPICOM- \_ PROPID-Registrierung \_**                        | Informationen zur Registrierung des Zertifikats.<br/>                                                                                                                                                                                                                                 | 26         |
| **CAPICOM- \_ PROPID- \_ Datums \_ Stempel**                       | Ein Datumsstempel.<br/>                                                                                                                                                                                                                                                                   | 27         |
| **\_ \_ \_ Serien \_ Nummer \_ MD5- \_ Hash des CAPICOM PROPID-Ausstellers** | Der MD5-Hash der Seriennummer des Ausstellers.<br/>                                                                                                                                                                                                                                     | 28         |
| **MD5-Hash des CAPICOM PROPID-Antragsteller \_ \_ \_ namens \_ \_**          | Der MD5-Hash des Antragsteller namens.<br/>                                                                                                                                                                                                                                             | 29         |
| **Erweiterte CAPICOM \_ PROPID- \_ \_ Fehler \_ Informationen**             | Erweiterte Informationen zu einem Fehler.<br/>                                                                                                                                                                                                                                            | 30         |
| **CAPICOM- \_ PROPID- \_ Erneuerung**                           | Informationen zur Erneuerung einer [*Zertifizierungs*](../secgloss/c-gly.md)Stelle.<br/>                                                                                                                     | 64         |
| **der CAPICOM- \_ PROPID- \_ Hash für archivierte \_ Schlüssel \_**               | Ein archivierter Hash eines Schlüssels.<br/>                                                                                                                                                                                                                                                      | 65         |
| **CAPICOM \_ PROPID \_ zuerst \_ reserviert**                   | Informationen zur ersten Reservierung.<br/>                                                                                                                                                                                                                                        | 66         |
| **die CAPICOM- \_ PROPID ist \_ zuletzt \_ reserviert.**                    | Informationen über die letzte Reservierung.<br/>                                                                                                                                                                                                                                  | 0x00007fff |
| **CAPICOM \_ PROPID, \_ erster \_ Benutzer**                       | Informationen zum ersten Benutzer.<br/>                                                                                                                                                                                                                                               | 0x00008000 |
| **der CAPICOM- \_ PROPID- \_ Letzte \_ Benutzer**                        | Informationen zum aktuellen Benutzer.<br/>                                                                                                                                                                                                                                         | 0X0000FFFF |



## <a name="remarks"></a>Bemerkungen

Diese Enumeration wird von den folgenden CAPICOM-Eigenschaften verwendet:

-   [**ExtendedProperty. PROPID**](extendedproperty-propid.md)
-   [**ExtendedProperties. Remove**](extendedproperties-remove.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
