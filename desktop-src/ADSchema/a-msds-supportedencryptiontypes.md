---
title: ms-DS-Supported-Encryption-Types-Attribut
description: Die verschlüsselungsalgorithmen, die von Benutzer-, Computer- oder Vertrauenskonten unterstützt werden. Hinweis Das KDC verwendet diese Informationen beim Generieren eines Diensttickets für dieses Konto.
ms.assetid: 6f9055a9-531e-4f4b-8703-aca5531a3bcb
ms.tgt_platform: multiple
keywords:
- AD-Schema des Attributs ms-DS-Supported-Encryption-Types
- AD-Schema des msDS-SupportedEncryptionTypes-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Supported-Encryption-Types
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d092061dfebcea8e9a0e4f4a060010e16102108d1e2e74f05e6df2db706141
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544340"
---
# <a name="ms-ds-supported-encryption-types-attribute"></a>ms-DS-Supported-Encryption-Types-Attribut

Die verschlüsselungsalgorithmen, die von Benutzer-, Computer- oder Vertrauenskonten unterstützt werden.

> [!Note]  
> Das KDC verwendet diese Informationen beim Generieren eines Diensttickets für dieses Konto. Dienste und Computer können dieses Attribut für ihre jeweiligen Konten in Active Directory automatisch aktualisieren und benötigen daher Schreibzugriff auf dieses Attribut.

 



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ms-DS-Supported-Encryption-Types     |
| Ldap-Anzeigename | msDS-SupportedEncryptionTypes        |
| Size              | \-                                   |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1963              |
| System-Id-Guid    | 20119867-1d04-4ab7-9371-cfc3d5df0afd |
| Syntax            | [**Enumeration**](s-enumeration.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | False                                                                                  |
| Is-Single-Valued       | True                                                                                   |
| Ist indiziert             | False                                                                                  |
| Im globalen Katalog      | False                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| In verwendete Klassen        | [**Trusted-Domain**](c-trusteddomain.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | False                                                                                  |
| Is-Single-Valued       | True                                                                                   |
| Ist indiziert             | False                                                                                  |
| Im globalen Katalog      | False                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| In verwendete Klassen        | [**Trusted-Domain**](c-trusteddomain.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | False                                                                                  |
| Is-Single-Valued       | True                                                                                   |
| Ist indiziert             | False                                                                                  |
| Im globalen Katalog      | False                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| In verwendete Klassen        | [**Trusted-Domain**](c-trusteddomain.md)<br/> [**Benutzer**](c-user.md)<br/> |



 

 





