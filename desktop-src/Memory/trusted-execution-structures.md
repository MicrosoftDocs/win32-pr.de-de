---
description: 'Die folgenden Strukturen werden bei der Arbeit mit Enklaven verwendet, die zum Erstellen vertrauenswürdiger Ausführungs Umgebungen verwendet werden:'
ms.assetid: 61F99132-E947-4EA4-86A0-914CE316B53A
title: Vertrauenswürdige Ausführungs Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d934ec26f9973697b987bf3a816e95d94ea591
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356683"
---
# <a name="trusted-execution-structures"></a>Vertrauenswürdige Ausführungs Strukturen

Die folgenden Strukturen werden bei der Arbeit mit Enklaven verwendet, die zum Erstellen vertrauenswürdiger Ausführungs Umgebungen verwendet werden:

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                         | BESCHREIBUNG                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Enclave \_ Create \_ Info \_ SGX**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_sgx)<br/>                      | Enthält architekturspezifische Informationen, die zum Erstellen einer Enclave verwendet werden, wenn der Enclave-Typ der **Enclave- \_ Typ \_ SGX** ist, der eine Enclave für die Architektur Erweiterung von Intel Software Guard Extensions (SGX) angibt.<br/>     |
| [**Enclave \_ Create \_ Info- \_ VSB**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_vbs)<br/>                      | Enthält architekturspezifische Informationen, die zum Erstellen einer Enclave verwendet werden, wenn der Enclave-Typ " **Enclave \_ Type \_ VSB**" ist, der eine virtualisierungsbasierte Sicherheits-Enclave (VSB) angibt.<br/>                                       |
| [**Enclave- \_ Identität**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_identity)<br/>                                      | Beschreibt die Identität des primären Moduls einer Enclave. <br/>                                                                                                                                                                 |
| [**Enclave- \_ Informationen**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_information)<br/>                                | Enthält Informationen über die derzeit ausgeführte Enclave.<br/>                                                                                                                                                                  |
| [**Enclave \_ Init \_ Info \_ SGX**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_sgx)<br/>                          | Enthält architekturspezifische Informationen, die zum Initialisieren einer Enclave verwendet werden, wenn der Enclave-Typ der **Enclave- \_ Typ \_ SGX** ist, der eine Enclave für die Architektur Erweiterung von Intel Software Guard Extensions (SGX) angibt.<br/> |
| [**Enclave \_ Init \_ Info- \_ VSB**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_vbs)<br/>                          | Enthält architekturspezifische Informationen, die zum Initialisieren einer Enclave verwendet werden, wenn der Enclave-Typ " **Enclave \_ Type \_ VSB**" ist, der eine virtualisierungsbasierte Sicherheits-Enclave (VSB) angibt.<br/>                                   |
| [**Bild \_ Enclave \_ CONFIG32**](/windows/desktop/api/winnt/ns-winnt-image_enclave_config32)<br/>                         | Definiert das Format der Enclave-Konfiguration für Systeme, die 32-Bit-Windows ausführen.<br/>                                                                                                                                          |
| [**Bild \_ Enclave \_ CONFIG64**](/previous-versions/windows/desktop/legacy/mt844244(v=vs.85))<br/>                         | Definiert das Format der Enclave-Konfiguration für Systeme, die 64-Bit-Windows ausführen.<br/>                                                                                                                                          |
| [**Bild \_ Enclave- \_ Import**](/windows/desktop/api/winnt/ns-winnt-image_enclave_import)<br/>                             | Definiert einen Eintrag im Array von Bildern, den eine Enclave importieren kann.<br/>                                                                                                                                                           |
| [**VSB- \_ Enclave- \_ Bericht**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report)<br/>                                 | Beschreibt das Format der signierten Anweisung, die in einem Bericht enthalten ist, der durch Aufrufen der [**envegetattestationreport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) -Funktion generiert wurde.<br/>                                                     |
| [**VSB- \_ Enclave- \_ Berichts \_ Modul**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_module)<br/>                  | Beschreibt ein Modul, das für die Enclave geladen wurde.<br/>                                                                                                                                                                                   |
| [**VSB- \_ Enclave- \_ Berichts- \_ pkg- \_ Header**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_pkg_header)<br/>         | Beschreibt den Inhalt eines Berichts, der durch Aufrufen der [**envegetattestationreport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) -Funktion generiert wird.<br/>                                                                                     |
| [**VSB- \_ Enclave- \_ berichtsvardata- \_ \_ Header**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_vardata_header)<br/> | Beschreibt das Format eines Variablen Datenblocks, der in einem Bericht enthalten ist, der von der [**envegetattestationreport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) -Funktion generiert wird.<br/>                                                          |



 

 

 
