---
title: X509-Cert-Attribut
description: Enthält die DER-codierten X.509v3-Zertifikate, die für den Benutzer ausgestellt wurden. Beachten Sie, dass diese Eigenschaft die Öffentlichen Schlüsselzertifikate enthält, die diesem Benutzer vom Microsoft-Zertifikatdienst ausgestellt wurden.
ms.assetid: bdd6b9a4-c402-462c-be2c-8e7e582a899a
ms.tgt_platform: multiple
keywords:
- X509-Cert AD-Schema
- AD-Schema des userCertificate-Attributs
topic_type:
- apiref
api_name:
- X509-Cert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0d6d95ab05047c19ba978a02957dca3870c2f93cf26b323bd6aa55c2f35472a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644590"
---
# <a name="x509-cert-attribute"></a>X509-Cert-Attribut

Enthält die DER-codierten X.509v3-Zertifikate, die für den Benutzer ausgestellt wurden. Beachten Sie, dass diese Eigenschaft die Öffentlichen Schlüsselzertifikate enthält, die diesem Benutzer vom Microsoft-Zertifikatdienst ausgestellt wurden.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| CN                | X509-Cert                                                                                                               |
| Ldap-Anzeigename | userCertificate                                                                                                         |
| Size              | Dieses Attribut erfordert ca. 4 KB für jedes Key Recovery Agent-Zertifikat, das von der Zertifizierungsstelle mithilfe der ZERTIFIZIERUNG-Instanz ausgestellt wird. |
| Aktualisieren von Berechtigungen  | Domänenadministrator                                                                                                    |
| Updatehäufigkeit  | Jedes Mal, wenn ein Zertifikat ausgestellt wird.                                                                                      |
| Attribute-Id      | 2.5.4.36                                                                                                                |
| System-Id-Guid    | bf967a7f-0de6-11d0-a285-00aa003049e2                                                                                    |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)                                                                   |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                     |
| MAPI-Id                | 0x8C6A                                                                                 |
| System-Only            | False                                                                                  |
| Is-Single-Valued       | False                                                                                  |
| Ist indiziert             | False                                                                                  |
| Im globalen Katalog      | True                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| In verwendete Klassen        | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                              |
| Is-Single-Valued       | False                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                              |
| Im globalen Katalog      | True                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                              |
| Is-Single-Valued       | False                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                              |
| Im globalen Katalog      | True                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                              |
| Ist einwertig       | False                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                              |
| Im globalen Katalog      | True                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                              |
| Ist einwertig       | False                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                              |
| Im globalen Katalog      | True                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                              |
| Ist einwertig       | False                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                              |
| Im globalen Katalog      | True                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Benutzer**](c-user.md)<br/> |



 

 





