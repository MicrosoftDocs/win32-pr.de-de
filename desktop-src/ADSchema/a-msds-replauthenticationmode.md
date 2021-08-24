---
title: ms-DS-Repl-Authentication-Mode-Attribut
description: Das Attribut ms-DS-Repl-Authentication-Mode wird verwendet, um anzugeben, welche Authentifizierungsmethode zum Authentifizieren von Replikationspartnern verwendet wird.
ms.assetid: b7e77b40-7aa7-4990-93fd-c8068e35fcf9
ms.tgt_platform: multiple
keywords:
- MS-DS-Repl-Authentication-Mode-Attribut AD-Schema
- AD-Schema des msDS-ReplAuthenticationMode-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Repl-Authentication-Mode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff624a9b7a1d1f678c748f79d3193b0b4b287026de1a669896c3e25d69f27ab0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803540"
---
# <a name="ms-ds-repl-authentication-mode-attribute"></a>ms-DS-Repl-Authentication-Mode-Attribut

Das **Attribut ms-DS-Repl-Authentication-Mode** wird verwendet, um anzugeben, welche Authentifizierungsmethode zum Authentifizieren von Replikationspartnern verwendet wird. Dieses Attribut gilt für die Konfigurationspartition einer ADAM-Instanz.

Die folgenden Werte sind die möglichen Werte für dieses Attribut.

| Wert        | Authentifizierungsmethode                          | BESCHREIBUNG                                                                                                                                                                    |
|--------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0<br/> | Aushandlungsdurchsatz<br/>             | Alle ADAM-Instanzen im Konfigurationssatz verwenden einen identischen Kontonamen und ein Kennwort wie das ADAM-Dienstkonto.<br/>                                                 |
| 1<br/> | Ausgehandelt<br/>                          | Zuerst wird versucht, die Kerberos-Authentifizierung (mit Dienstprinzipalnamen) auszuführen. Falls diese nicht erfolgreich ist, wird versucht, eine NTLM-Authentifizierung auszuführen. Wenn NTLM ausfällt, werden die ADAM-Instanzen nicht repliziert.<br/> |
| 2<br/> | Gegenseitige Authentifizierung mithilfe von Kerberos<br/> | Kerberos-Authentifizierung mithilfe von Dienstprinzipalnamen (SPN) erforderlich. Wenn bei der Kerberos-Authentifizierung ein Fehler auftritt, werden die ADAM-Instanzen nicht repliziert.<br/>                |



 

Die folgende Tabelle enthält die programmgesteuerten Bezeichner für die Werte dieses Attributs.

| Wert        | Bezeichner (aus Ntdsapi.h)                                               |
|--------------|---------------------------------------------------------------------------|
| 0<br/> | **ADAM \_ REPL \_ AUTHENTICATION \_ MODE \_ NEGOTIATE \_ PASS \_ THROUGH**<br/> |
| 1<br/> | **ADAM \_ REPL \_ AUTHENTICATION \_ MODE \_ NEGOTIATE**<br/>                |
| 2<br/> | **ADAM \_ REPL \_ AUTHENTICATION \_ MODE \_ MUTUAL \_ AUTH \_ REQUIRED**<br/>   |



 



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ms-DS-Repl-Authentication-Mode       |
| Ldap-Anzeigename | msDS-ReplAuthenticationMode          |
| Size              | \-                                   |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1861              |
| System-Id-Guid    | 6e124d4f-1a3f-4cc6-8e09-4a54c81b1d50 |
| Syntax            | [**Enumeration**](s-enumeration.md) |



## <a name="implementations"></a>Implementierungen

-   [**Adam**](#adam)

## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|-----------------------------------------------------|
| Link-ID                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | False                                               |
| Is-Single-Valued       | True                                                |
| Ist indiziert             | False                                               |
| Im globalen Katalog      | False                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| In verwendete Klassen        | [**Konfiguration**](c-configuration.md)<br/> |



 

 





