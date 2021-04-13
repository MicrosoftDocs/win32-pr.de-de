---
title: TSB-Funktionen
description: TSB bietet die folgenden Funktionen.
ms.assetid: df2d3e36-0a27-4cc0-bcb2-709eb6bedeac
keywords:
- TPM-Basisdienste-TSB, Functions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1b34f2dfbe18ef2230838ff4ba9ec2241d3cc2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390683"
---
# <a name="tbs-functions"></a>TSB-Funktionen

TSB bietet die folgenden Funktionen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                       | BESCHREIBUNG                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Tbsi- \_ Kontext \_ Erstellung**](/windows/desktop/api/Tbs/nf-tbs-tbsi_context_create)<br/>                            | Erstellt ein Kontext Handle, das verwendet werden kann, um Befehle an TSB zu übergeben.<br/>                                                                               |
| [**Tbsi-Nachweis \_ \_ \_ aus \_ Protokoll erstellen**](/previous-versions/windows/desktop/legacy/dn455155(v=vs.85))<br/> | Erstellt einen Nachweis durch Extrahieren eines Trust Point aus einem TCG-Protokoll.<br/>                                                                                |
| [**Tbsi \_ getdebug**](/windows/desktop/api/Tbs/nf-tbs-tbsi_getdeviceinfo)<br/>                                | Ruft die Version des TPM auf dem Computer ab.<br/>                                                                                                  |
| [**Tbsi \_ Get Besitzer Authentifizierung \_**](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_ownerauth)<br/>                               | Ruft die Besitzer Autorisierung des TPM ab, wenn die Informationen in der lokalen Registrierung verfügbar sind. <br/>                                             |
| [**Tbsi \_ get \_ TCG- \_ Protokoll**](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_tcg_log)<br/>                                  | Ruft das aktuellste Windows-Start Konfigurations Protokoll (wbcl) ab, das auch als TCG-Protokoll bezeichnet wird.<br/>                                                  |
| [**Tbsi \_ get \_ TCG \_ log \_ Ex**](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_tcg_log_ex)<br/>                           | Ruft das Windows-Start Konfigurations Protokoll (wbcl), das auch als TCG-Protokoll bezeichnet wird, vom angegebenen Typ ab.<br/>                                          |
| [**Tbsi \_ get \_ TCG- \_ Protokolle**](/previous-versions/windows/desktop/legacy/dn455156(v=vs.85))<br/>                                | Holen Sie sich ein oder mehrere Windows-Start Konfigurations Protokolle (wbcl), die auch als TCG-Protokolle bezeichnet werden.<br/>                                                        |
| [**\_Physischer \_ Anwesenheits \_ Befehl in tbsi**](/windows/desktop/api/Tbs/nf-tbs-tbsi_physical_presence_command)<br/>     | Übergibt einen physischen Anwesenheits-ACPI-Befehl über TSB an den Treiber.<br/>                                                                               |
| [**Tbsi-Nachweis \_ widerrufen \_**](/windows/desktop/api/Tbs/nf-tbs-tbsi_revoke_attestation)<br/>                     | Erklärt das PCRs für ungültig, wenn der Elam-Treiber eine Richtlinien Verletzung erkennt (z. b. ein Rootkit).<br/>                                                     |
| [**Tbsip \_ - \_ Befehle Abbrechen**](/windows/desktop/api/Tbs/nf-tbs-tbsip_cancel_commands)<br/>                        | Bricht alle ausstehenden Befehle für den angegebenen Kontext ab.<br/>                                                                                      |
| [**Tbsip- \_ Kontext \_ Schließen**](/windows/desktop/api/Tbs/nf-tbs-tbsip_context_close)<br/>                            | Schließt ein Kontext Handle, das Ressourcen freigibt, die dem Kontext in TSB zugeordnet sind, und schließt das Bindungs handle, das für die Kommunikation mit TSB verwendet wird.<br/> |
| [**Tbsip-Befehl zum über \_ Mitteln \_**](/windows/desktop/api/Tbs/nf-tbs-tbsip_submit_command)<br/>                          | Übermittelt einen Trusted Platform Module (TPM)-Befehl an TPM-Basisdienste (TSB) zur Verarbeitung.<br/>                                                       |



 

 

