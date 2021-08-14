---
description: 'Die folgenden Strukturen werden bei der Arbeit mit Enclaves verwendet, die zum Erstellen vertrauenswürdiger Ausführungsumgebungen verwendet werden:'
ms.assetid: 61F99132-E947-4EA4-86A0-914CE316B53A
title: Vertrauenswürdige Ausführungsstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9349c8c4e4c04ecc664ccab668abe55cdca1e1720b6fa17fd35bb7139f53f19c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386251"
---
# <a name="trusted-execution-structures"></a>Vertrauenswürdige Ausführungsstrukturen

Die folgenden Strukturen werden bei der Arbeit mit Enclaves verwendet, die zum Erstellen vertrauenswürdiger Ausführungsumgebungen verwendet werden:

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                         | BESCHREIBUNG                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ENCLAVE \_ CREATE \_ INFO \_ SGX**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_sgx)<br/>                      | Enthält architekturspezifische Informationen zum Erstellen einer Enclave, wenn der **Enclave-Typ ENCLAVE \_ TYPE \_ SGX** ist, der eine Enclave für die Intel Software Guard Extensions-Architekturerweiterung (SGX) angibt.<br/>     |
| [**ENCLAVE \_ CREATE \_ INFO \_ VBS**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_vbs)<br/>                      | Enthält architekturspezifische Informationen zum Erstellen einer Enclave, wenn der **Enclavetyp ENCLAVE \_ TYPE \_ VBS** ist, der eine Virtualisierungsbasierte Sicherheits-Enclave (VBS) angibt.<br/>                                       |
| [**ENCLAVE-IDENTITÄT \_**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_identity)<br/>                                      | Beschreibt die Identität des primären Moduls einer Enclave. <br/>                                                                                                                                                                 |
| [**ENCLAVE-INFORMATIONEN \_**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_information)<br/>                                | Enthält Informationen zur derzeit ausgeführten Enclave.<br/>                                                                                                                                                                  |
| [**ENCLAVE \_ INIT \_ INFO \_ SGX**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_sgx)<br/>                          | Enthält architekturspezifische Informationen, die zum Initialisieren einer Enclave verwendet werden, wenn der **Enclave-Typ ENCLAVE \_ TYPE \_ SGX** ist, der eine Enclave für die Intel Software Guard Extensions -Architekturerweiterung (SGX) angibt.<br/> |
| [**ENCLAVE \_ INIT \_ INFO \_ VBS**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_vbs)<br/>                          | Enthält architekturspezifische Informationen, die zum Initialisieren einer Enclave verwendet werden, wenn der **Enclave-Typ ENCLAVE \_ TYPE \_ VBS** ist, der eine Virtualisierungsbasierte Sicherheits-Enclave (VBS) angibt.<br/>                                   |
| [**IMAGE \_ ENCLAVE \_ CONFIG32**](/windows/desktop/api/winnt/ns-winnt-image_enclave_config32)<br/>                         | Definiert das Format der Enclave-Konfiguration für Systeme, auf denen 32-Bit-Windows.<br/>                                                                                                                                          |
| [**IMAGE \_ ENCLAVE \_ CONFIG64**](/previous-versions/windows/desktop/legacy/mt844244(v=vs.85))<br/>                         | Definiert das Format der Enclave-Konfiguration für Systeme mit 64-Bit-Windows.<br/>                                                                                                                                          |
| [**\_IMAGE-ENCLAVE-IMPORT \_**](/windows/desktop/api/winnt/ns-winnt-image_enclave_import)<br/>                             | Definiert einen Eintrag im Array von Bildern, die eine Enclave importieren kann.<br/>                                                                                                                                                           |
| [**\_VBS-ENCLAVE-BERICHT \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report)<br/>                                 | Beschreibt das Format der signierten Anweisung, die in einem Bericht enthalten ist, der durch Aufrufen der [**EnclaveGetAttestationReport-Funktion generiert**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) wird.<br/>                                                     |
| [**VBS \_ ENCLAVE-BERICHTSMODUL \_ \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_module)<br/>                  | Beschreibt ein Modul, das für die Enclave geladen wurde.<br/>                                                                                                                                                                                   |
| [**PKG-HEADER \_ FÜR VBS-ENCLAVE-BERICHT \_ \_ \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_pkg_header)<br/>         | Beschreibt den Inhalt eines Berichts, der durch Aufrufen der [**EnclaveGetAttestationReport-Funktion generiert**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) wird.<br/>                                                                                     |
| [**\_VARDATA-HEADER FÜR VBS-ENCLAVE-BERICHT \_ \_ \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_vardata_header)<br/> | Beschreibt das Format eines Variablendatenblocks, der in einem Bericht enthalten ist, der von der [**EnclaveGetAttestationReport-Funktion**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) generiert wird.<br/>                                                          |



 

 

 
