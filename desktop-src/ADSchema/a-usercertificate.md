---
title: X509-Cert-Attribut
description: Enthält die der-codierten X. 509v3-Zertifikate, die für den Benutzer ausgestellt wurden. Beachten Sie, dass diese Eigenschaft die Zertifikate des öffentlichen Schlüssels enthält, die für diesen Benutzer vom Microsoft-Zertifikat Dienst ausgestellt wurden.
ms.assetid: bdd6b9a4-c402-462c-be2c-8e7e582a899a
ms.tgt_platform: multiple
keywords:
- AD-Schema für X509-Cert-Attribut
- userCertificate-Attribut AD-Schema
topic_type:
- apiref
api_name:
- X509-Cert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa6f0dfb5acc25890361a124e52b8b24958915f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480207"
---
# <a name="x509-cert-attribute"></a>X509-Cert-Attribut

Enthält die der-codierten X. 509v3-Zertifikate, die für den Benutzer ausgestellt wurden. Beachten Sie, dass diese Eigenschaft die Zertifikate des öffentlichen Schlüssels enthält, die für diesen Benutzer vom Microsoft-Zertifikat Dienst ausgestellt wurden.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| CN                | X509-Cert                                                                                                               |
| LDAP-Display-Name | userCertificate                                                                                                         |
| Size              | Dieses Attribut erfordert ca. 4 KB für jedes von der Zertifizierungsstelle ausgegebene Schlüssel Wiederherstellungs-Agent-Zertifikat mithilfe der KRA-Instanz. |
| Berechtigung aktualisieren  | Domänen Administrator                                                                                                    |
| Aktualisierungshäufigkeit  | Jedes Mal, wenn ein Zertifikat ausgestellt wird.                                                                                      |
| Attribute-Id      | 2.5.4.36                                                                                                                |
| System-ID-GUID    | bf967a7f-0de6-11d0-a285-00aa003049e2                                                                                    |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)                                                                   |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                     |
| MAPI-Id                | 0x8c6a                                                                                 |
| System-Only            | False                                                                                  |
| Ist-einwertig       | False                                                                                  |
| Ist indiziert             | False                                                                                  |
| Im globalen Katalog      | Richtig                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| In verwendete Klassen        | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8c6a                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                              |
| Ist-einwertig       | False                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                              |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**MS-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8c6a                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                              |
| Ist-einwertig       | False                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                              |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**MS-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8c6a                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                              |
| Ist-einwertig       | False                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                              |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**MS-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8c6a                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                              |
| Ist-einwertig       | False                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                              |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**MS-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8c6a                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                              |
| Ist-einwertig       | False                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                              |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**MS-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Benutzer**](c-user.md)<br/> |



 

 





