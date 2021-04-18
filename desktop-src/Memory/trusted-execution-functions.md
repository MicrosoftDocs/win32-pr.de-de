---
description: 'Die folgenden Funktionen werden bei der Arbeit mit Enklaven verwendet, die zum Erstellen von vertrauenswürdigen Ausführungs Umgebungen verwendet werden:'
ms.assetid: DF6CDEE1-CAAA-429C-9939-DDC844302027
title: Vertrauenswürdige Ausführungs Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b1bd2411d0448346f0a8afcca870c26b4a61ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357376"
---
# <a name="trusted-execution-functions"></a>Vertrauenswürdige Ausführungs Funktionen

Die folgenden Funktionen werden bei der Arbeit mit Enklaven verwendet, die zum Erstellen von vertrauenswürdigen Ausführungs Umgebungen verwendet werden:

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                               | BESCHREIBUNG                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Callenclave**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-callenclave)<br/>                                       | Ruft eine Funktion innerhalb einer Enclave auf. <br/>                                                                                                                                                                                |
| [**"Kreateenclave"**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave)<br/>                                   | Erstellt eine neue nicht initialisierte Enclave. Eine Enclave ist ein isolierter Code Bereich und Daten innerhalb des Adressraums für eine Anwendung. Nur Code, der innerhalb der Enclave ausgeführt wird, kann auf Daten innerhalb desselben Enclave zugreifen.<br/> |
| [**Deleteenclave**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-deleteenclave)<br/>                                   | Löscht die angegebene Enclave.<br/>                                                                                                                                                                                      |
| [**Envegetattestationreport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport)<br/>       | Ruft einen Enclave-Nachweis Bericht ab, der die aktuelle Enclave beschreibt und von der Autorität signiert ist, die für den Typ der Enclave zuständig ist. <br/>                                                              |
| [**Envegetenclaveinformation**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetenclaveinformation)<br/>     | Ruft Informationen über die derzeit ausgeführte Enclave ab.<br/>                                                                                                                                                             |
| [**Envesealdata**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavesealdata)<br/>                               | Generiert eine verschlüsselte Binary Large Object (BLOB) aus Daten, die aus der Registrierung entfernt wurden.<br/>                                                                                                                                             |
| [**Enveunversiegedaten**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclaveunsealdata)<br/>                           | Entschlüsselt einen verschlüsselten Binary Large Object (BLOB).<br/>                                                                                                                                                                   |
| [**Enveverifyattestationreport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclaveverifyattestationreport)<br/> | Überprüft einen Nachweis Bericht, der auf dem aktuellen System generiert wurde. <br/>                                                                                                                                           |
| [**Initializeenclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-initializeenclave)<br/>                           | Initialisiert eine Enclave, die Sie erstellt und mit Daten geladen haben.<br/>                                                                                                                                                       |
| [**Isenvetypesupportiert**](/windows/desktop/api/enclaveapi/nf-enclaveapi-isenclavetypesupported)<br/>                 | Ruft ab, ob der angegebene Typ von Enclave unterstützt wird.<br/>                                                                                                                                                       |
| [**Loadenclavedata**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata)<br/>                               | Lädt Daten in eine nicht initialisierte Enclave, die Sie durch Aufrufen von [**createenclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave)erstellt haben.<br/>                                                                                                        |
| [**Loadenclaveimage**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-loadenclaveimagew)<br/>                             | Lädt ein Bild und alle zugehörigen Importe in eine Enclave.<br/>                                                                                                                                                              |
| [**Terminateenclave**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-terminateenclave)<br/>                             | Beendet die Ausführung der Threads, die innerhalb einer Enclave ausgeführt werden.<br/>                                                                                                                                               |



 

 

 




