---
description: Die folgenden Konstanten werden von der CNG-Datenschutz-API verwendet.
ms.assetid: 4E43FAA9-7D6F-43DB-A998-189411E0AB4C
title: CNG-DPAPI-Konstanten (ncryptprotect. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece376a0b7282f26ef933b249a1356b2d012d438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484291"
---
# <a name="cng-dpapi-constants"></a>CNG-DPAPI-Konstanten

Die folgenden Konstanten werden von der CNG-Datenschutz-API verwendet.

<dl> <dt>

<span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**ncrypt \_ descr \_ -Trennzeichen \_ und**
</dt> <dd> <dl> <dt>

L "und"
</dt> <dt>



Kann verwendet werden, um eine Schutz Deskriptorzeichenfolge für ein-und-Trennzeichen zu testen.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**ncrypt \_ descr \_ gleich**
</dt> <dd> <dl> <dt>

L "="
</dt> <dt>



Kann verwendet werden, um eine Schutz Deskriptorzeichenfolge für ein Gleichheitszeichen zu testen.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**ncrypt- \_ descr- \_ Trennzeichen \_ oder**
</dt> <dd> <dl> <dt>

L "or"
</dt> <dt>



Kann verwendet werden, um eine Schutz Deskriptorzeichenfolge für ein-oder-Trennzeichen zu testen.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**ncrypt- \_ Schlüssel \_ Schutz \_ Algorithmus \_ lokal**
</dt> <dd> <dl> <dt>

„LOCAL“
</dt> <dt>



Der lokale Schutz Deskriptor schützt Inhalte für die Anmelde Sitzung, den aktuellen Benutzer oder den lokalen Computer, wie durch die folgenden Konstanten identifiziert:

-   **lokale Anmeldung mit NCrypt- \_ Schlüssel \_ Schutz \_ \_**
-   **ncrypt- \_ Schlüssel \_ Schutz \_ lokaler \_ Benutzer**
-   **ncrypt- \_ Schlüssel \_ Schutz- \_ lokaler \_ Computer**


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**ncrypt- \_ Schlüssel \_ Schutz \_ Algorithmus \_ SDDL**
</dt> <dd> <dl> <dt>

SDDL
</dt> <dt>



Schützt Inhalte in einer SDDL-Zeichenfolge (Security Deskriptor Definition Language), die Sicherheits Deskriptorinformationen enthält.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**ncrypt- \_ Schlüssel \_ Schutz Algorithmus- \_ \_ sid**
</dt> <dd> <dl> <dt>

SID
</dt> <dt>



Der SID-Schutz Deskriptor enthält eine Gruppen-oder Prinzipal Identität.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**webanmelde Informationen für den NCrypt- \_ Schlüssel \_ Schutz \_ Algorithmus \_**
</dt> <dd> <dl> <dt>

"Webanmelde Informationen"
</dt> <dt>



Schützt die Anmelde Informationen für das Webkonto eines Benutzers.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**lokale Anmeldung mit NCrypt- \_ Schlüssel \_ Schutz \_ \_**
</dt> <dd> <dl> <dt>

Melden
</dt> <dt>



Schützt Inhalte in der aktuellen Anmelde Sitzung. Benutzer können den geschützten Inhalt nach dem Abmelden oder Neustart nicht entschlüsseln.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**ncrypt- \_ Schlüssel \_ Schutz- \_ lokaler \_ Computer**
</dt> <dd> <dl> <dt>

Computer
</dt> <dt>



Schützt Inhalt auf dem lokalen Computer. Alle Benutzer auf dem lokalen Computer können den geschützten Inhalt entschlüsseln.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**ncrypt- \_ Schlüssel \_ Schutz \_ lokaler \_ Benutzer**
</dt> <dd> <dl> <dt>

Bedienungs
</dt> <dt>



Schützt Inhalt in der aktuellen Benutzersitzung. Nur dieser Benutzer auf dem lokalen Computer ist in der Lage, den geschützten Inhalt zu entschlüsseln.


</dt> </dl> </dd> <dt>

<span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**MS- \_ Schlüssel \_ Schutz \_ Anbieter**
</dt> <dd> <dl> <dt>

"Microsoft Key Protection Provider"
</dt> <dt>



Stellt den Microsoft-Schlüsselschutz Anbieter dar, der Formate unterstützt, die durch die folgenden Konstanten dargestellt werden:

-   **ncrypt- \_ Schlüssel \_ Schutz Algorithmus- \_ \_ sid**
-   **ncrypt- \_ Schlüssel \_ Schutz \_ Algorithmus \_ lokal**
-   **ncrypt- \_ Schlüssel \_ Schutz \_ Algorithmus \_ SDDL**


</dt> </dl> </dd> <dt>

<span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**Windows- \_ Client- \_ Schlüssel \_ Schutz \_ Anbieter**
</dt> <dd> <dl> <dt>

"Windows-Client-Schlüsselschutz Anbieter"
</dt> <dt>



Stellt den Microsoft-Schlüsselschutz Anbieter dar, der nur auf dem Client verfügbar ist und die durch die folgenden Konstanten dargestellten Formate unterstützt:

-   **webanmelde Informationen für den NCrypt- \_ Schlüssel \_ Schutz \_ Algorithmus \_**


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Ncryptprotect. h</dt> </dl> |



 

 




