---
title: CA-Certificate-DN-Attribut
description: Vollständiger Distinguished Name vom Zertifizierungsstellenzertifikat.
ms.assetid: 51d1a9f8-d3d7-4ac9-b029-fa66b6799820
ms.tgt_platform: multiple
keywords:
- AD-Schema des CA-Certificate-DN-Attributs
- cACertificateDN-Attribut-AD-Schema
topic_type:
- apiref
api_name:
- CA-Certificate-DN
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02a3e77e19ebc8cb0f9277e529a2d249bb53f60260e121823082524d9bed1b46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022668"
---
# <a name="ca-certificate-dn-attribute"></a>CA-Certificate-DN-Attribut

Vollständiger Distinguished Name vom Zertifizierungsstellenzertifikat.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | CA-Certificate-DN                           |
| Ldap-Anzeigename | cACertificateDN                             |
| Size              | \-                                          |
| Aktualisieren von Berechtigungen  | \-                                          |
| Updatehäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.697                      |
| System-ID-GUID    | 963d2740-48be-11d1-a9c3-0000f80367c1        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                         |
| System-Only            | Falsch                                                                                                                                      |
| Ist einwertig       | Richtig                                                                                                                                       |
| Ist indiziert             | Falsch                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | \-                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                         |
| System-Only            | Falsch                                                                                                                                      |
| Ist einwertig       | Richtig                                                                                                                                       |
| Ist indiziert             | Falsch                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | \-                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                         |
| System-Only            | Falsch                                                                                                                                      |
| Ist einwertig       | Richtig                                                                                                                                       |
| Ist indiziert             | Falsch                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | \-                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                         |
| System-Only            | Falsch                                                                                                                                      |
| Is-Single-Valued       | Richtig                                                                                                                                       |
| Ist indiziert             | Falsch                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | \-                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                         |
| System-Only            | Falsch                                                                                                                                      |
| Is-Single-Valued       | Richtig                                                                                                                                       |
| Ist indiziert             | Falsch                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | \-                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                         |
| System-Only            | Falsch                                                                                                                                      |
| Is-Single-Valued       | Richtig                                                                                                                                       |
| Ist indiziert             | Falsch                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | \-                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> |



 

 





