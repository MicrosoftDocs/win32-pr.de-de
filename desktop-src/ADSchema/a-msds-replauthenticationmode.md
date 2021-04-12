---
title: ms-DS-repl-Authentication-Mode-Attribut
description: Das ms-DS-repl-Authentication-Mode-Attribut wird verwendet, um anzugeben, welche Authentifizierungsmethode zum Authentifizieren von Replikations Partnern verwendet wird.
ms.assetid: b7e77b40-7aa7-4990-93fd-c8068e35fcf9
ms.tgt_platform: multiple
keywords:
- AD-Schema für das Attribut "ms-DS-repl-Authentication-Mode"
- AD-Schema für das msDS-ReplAuthenticationMode-Attribut
topic_type:
- apiref
api_name:
- ms-DS-Repl-Authentication-Mode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b88c7e3223b946b56962b710b036ee6e0c36dc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480359"
---
# <a name="ms-ds-repl-authentication-mode-attribute"></a>ms-DS-repl-Authentication-Mode-Attribut

Das **ms-DS-repl-Authentication-Mode** -Attribut wird verwendet, um anzugeben, welche Authentifizierungsmethode zum Authentifizieren von Replikations Partnern verwendet wird. Dieses Attribut gilt für die Konfigurations Partition einer ADAM-Instanz.

Die folgenden Werte sind die möglichen Werte für dieses Attribut.

| Wert        | Authentifizierungsmethode                          | BESCHREIBUNG                                                                                                                                                                    |
|--------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0<br/> | Aushandlungsdurchsatz<br/>             | Alle ADAM-Instanzen im Konfigurationssatz verwenden denselben Kontonamen und dasselbe Kennwort wie das Adam-Dienst Konto.<br/>                                                 |
| 1<br/> | Ausgehandelt<br/>                          | Zuerst wird versucht, die Kerberos-Authentifizierung (mit Dienstprinzipalnamen) auszuführen. Falls diese nicht erfolgreich ist, wird versucht, eine NTLM-Authentifizierung auszuführen. Wenn NTLM ausfällt, werden die ADAM-Instanzen nicht repliziert.<br/> |
| 2<br/> | Gegenseitige Authentifizierung mithilfe von Kerberos<br/> | Kerberos-Authentifizierung mithilfe von Dienstprinzipalnamen (SPN) erforderlich. Wenn die Kerberos-Authentifizierung fehlschlägt, werden die ADAM-Instanzen nicht repliziert.<br/>                |



 

In der folgenden Tabelle sind die programmgesteuerten Bezeichner für die Werte dieses Attributs enthalten.

| Wert        | Bezeichner (von NTDSAPI. h)                                               |
|--------------|---------------------------------------------------------------------------|
| 0<br/> | **Adam \_ repl \_ Authentication \_ Mode \_ aushandeln \_ Pass- \_ through**<br/> |
| 1<br/> | **Adam \_ repl- \_ Authentifizierungs \_ Modus- \_ Aushandlung**<br/>                |
| 2<br/> | **die \_ \_ gegenseitige Authentifizierung des Adam repl-Authentifizierungs \_ Modus ist \_ \_ \_ erforderlich.**<br/>   |



 



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ms-DS-repl-Authentifizierungsmodus       |
| LDAP-Display-Name | msDS-ReplAuthenticationMode          |
| Size              | \-                                   |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1861              |
| System-ID-GUID    | 6e124d4f -1a3b-4cc6-8e09-4a54c81b1d50 |
| Syntax            | [**Enumeration**](s-enumeration.md) |



## <a name="implementations"></a>Implementierungen

-   [**Adam**](#adam)

## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|-----------------------------------------------------|
| Link-ID                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | False                                               |
| Ist-einwertig       | Richtig                                                |
| Ist indiziert             | False                                               |
| Im globalen Katalog      | False                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| In verwendete Klassen        | [**Konfiguration**](c-configuration.md)<br/> |



 

 





