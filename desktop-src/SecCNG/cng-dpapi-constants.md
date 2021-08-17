---
description: Die folgenden Konstanten werden von der CNG-Datenschutz-API verwendet.
ms.assetid: 4E43FAA9-7D6F-43DB-A998-189411E0AB4C
title: CNG DPAPI-Konstanten (NCryptprotect.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1afc589afa113250728b46639b7cd47442034f7b3bc82264099f334919a94c76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908798"
---
# <a name="cng-dpapi-constants"></a>CNG DPAPI-Konstanten

Die folgenden Konstanten werden von der CNG-Datenschutz-API verwendet.

<dl> <dt>

<span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**NCRYPT \_ DESCR \_ DELIMITER \_ UND**
</dt> <dd> <dl> <dt>

L" UND "
</dt> <dt>



Kann verwendet werden, um eine Schutzdeskriptorzeichenfolge für ein AND-Trennzeichen zu testen.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**NCRYPT \_ DESCR \_ EQUAL**
</dt> <dd> <dl> <dt>

L"="
</dt> <dt>



Kann verwendet werden, um eine Schutzbeschreibungszeichenfolge auf ein Gleichheitszeichen zu testen.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**NCRYPT \_ DESCR \_ DELIMITER \_ ODER**
</dt> <dd> <dl> <dt>

L" OR "
</dt> <dt>



Kann verwendet werden, um eine Schutzdeskriptorzeichenfolge für ein OR-Trennzeichen zu testen.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**NCRYPT \_ KEY \_ PROTECTION \_ ALGORITHM \_ LOCAL**
</dt> <dd> <dl> <dt>

„LOCAL“
</dt> <dt>



Der LOCAL-Schutzdeskriptor schützt Inhalte für die Anmeldesitzung, den aktuellen Benutzer oder den lokalen Computer, wie durch die folgenden Konstanten identifiziert:

-   **NCRYPT \_ KEY PROTECTION – LOKALE \_ \_ \_ ANMELDUNG**
-   **LOKALER NCRYPT \_ KEY \_ \_ \_ PROTECTION-BENUTZER**
-   **LOKALER NCRYPT \_ KEY \_ \_ \_ PROTECTION-COMPUTER**


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**NCRYPT \_ KEY \_ PROTECTION \_ ALGORITHM \_ SDDL**
</dt> <dd> <dl> <dt>

"SDDL"
</dt> <dt>



Schützt Inhalte in einer SDDL-Zeichenfolge (Security Descriptor Definition Language), die Sicherheitsbeschreibungsinformationen enthält.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**NCRYPT \_ KEY \_ PROTECTION \_ ALGORITHM \_ SID**
</dt> <dd> <dl> <dt>

"SID"
</dt> <dt>



Der SID-Schutzdeskriptor enthält eine Gruppen- oder Prinzipalidentität.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**NCRYPT \_ KEY \_ PROTECTION \_ ALGORITHM \_ WEBCREDENTIALS**
</dt> <dd> <dl> <dt>

"WEBCREDENTIALS"
</dt> <dt>



Schützt vor den Anmeldeinformationen eines Webkontos eines Benutzers.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**NCRYPT \_ KEY PROTECTION – LOKALE \_ \_ \_ ANMELDUNG**
</dt> <dd> <dl> <dt>

"Logon"
</dt> <dt>



Schützt Inhalte in der aktuellen Anmeldesitzung. Benutzer können die geschützten Inhalte nach dem Abmelden oder Neustart nicht entschlüsseln.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**LOKALER NCRYPT \_ KEY \_ \_ \_ PROTECTION-COMPUTER**
</dt> <dd> <dl> <dt>

"machine"
</dt> <dt>



Schützt Inhalte auf dem lokalen Computer. Alle Benutzer auf dem lokalen Computer können den geschützten Inhalt entschlüsseln.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**LOKALER NCRYPT \_ KEY \_ \_ \_ PROTECTION-BENUTZER**
</dt> <dd> <dl> <dt>

"user"
</dt> <dt>



Schützt Inhalte in der aktuellen Benutzersitzung. Nur dieser Benutzer auf dem lokalen Computer kann den geschützten Inhalt entschlüsseln.


</dt> </dl> </dd> <dt>

<span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**MS \_ KEY \_ \_ PROTECTION-ANBIETER**
</dt> <dd> <dl> <dt>

"Microsoft Key Protection Provider"
</dt> <dt>



Stellt den Microsoft-Schlüsselschutzanbieter dar, der Formate unterstützt, die durch die folgenden Konstanten dargestellt werden:

-   **NCRYPT \_ KEY \_ PROTECTION \_ ALGORITHM \_ SID**
-   **NCRYPT \_ KEY \_ PROTECTION \_ ALGORITHM \_ LOCAL**
-   **NCRYPT \_ KEY \_ PROTECTION \_ ALGORITHM \_ SDDL**


</dt> </dl> </dd> <dt>

<span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**\_ \_ \_ WINDOWS-CLIENTSCHLÜSSELSCHUTZANBIETER \_**
</dt> <dd> <dl> <dt>

"Windows Clientschlüsselschutzanbieter"
</dt> <dt>



Stellt den Microsoft-Schlüsselschutzanbieter dar, der nur auf dem Client verfügbar ist und Formate unterstützt, die durch die folgenden Konstanten dargestellt werden:

-   **NCRYPT \_ KEY \_ PROTECTION \_ ALGORITHM \_ WEBCREDENTIALS**


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>NCryptprotect.h</dt> </dl> |



 

 




