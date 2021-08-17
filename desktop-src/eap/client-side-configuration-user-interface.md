---
title: Client-Side Configuration Benutzeroberfläche
description: Der Anbieter, der das Authentifizierungsprotokoll implementiert, kann auch eine Benutzeroberfläche für die Konfiguration für das Protokoll bereitstellen.
ms.assetid: 956a7ad6-1fd5-4938-aa2f-4de646dfd6c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13c8b067ba65312edea412ba532620e029912088e9cc61885626f8a13f5a2834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117804"
---
# <a name="client-side-configuration-user-interface"></a>Client-Side Configuration Benutzeroberfläche

Der Anbieter, der das Authentifizierungsprotokoll implementiert, kann auch eine Benutzeroberfläche für die Konfiguration für das Protokoll bereitstellen. Die Konfigurationsoberfläche kann in derselben DLL wie das Authentifizierungsprotokoll oder in einer separaten DLL implementiert werden. Außerdem unterstützt die DLL, die die Konfigurationsoberfläche implementiert, möglicherweise mehr als ein Authentifizierungsprotokoll. Der Pfad zur DLL für die Konfigurationsbenutzeroberfläche wird im RAS \_ EAP \_ VALUENAME \_ CONFIGUI-Registrierungswert unter dem Schlüssel für das Authentifizierungsprotokoll gespeichert. Weitere Informationen zum Erstellen dieses Registrierungswerts finden Sie unter [EAP-Installation.](eap-installation.md)

Die DLL für die Benutzeroberfläche der Konfiguration sollte Einstiegspunkte für die folgenden Funktionen exportieren:

[**RasEapInvokeConfigUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeconfigui)

[**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

Wenn der Benutzer einen Konfigurationseintrag für eine bestimmte Verbindung erstellt , unabhängig davon, ob es sich um einen RAS- oder Drahtlosclient handelt, kann der Benutzer das Authentifizierungsprotokoll auswählen, das der Dienst mit diesem Eintrag verwenden soll. Wenn das Authentifizierungsprotokoll konfigurierbar ist, ruft der Dienst [**RasEapInvokeConfigUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeconfigui) auf, um die Konfigurationsbenutzeroberfläche aufzurufen. Die Konfigurationsbenutzeroberfläche speichert die Konfigurationsinformationen, die von **RasEapInvokeConfigUI** zurückgegeben werden, im Konfigurationseintrag.

Die Konfigurationsinformationen sollten für alle Benutzer auf dem Clientcomputer generisch sein. Informationen, die für einen bestimmten Benutzer oder bestimmte Benutzer spezifisch sind, sollten nicht im Eintrag gespeichert werden. Das Authentifizierungsprotokoll sollte mithilfe der [Identitätsfunktionen](obtaining-identity-information.md) oder der [interaktiven Benutzeroberfläche](interactive-user-interface.md)benutzerspezifische Informationen abrufen. Das Authentifizierungsprotokoll kann diese Informationen in der Registrierung speichern, indem es sie an den Authentifizierungsdienst im *pEapOutput-Parameter* von [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))übergibt.

Die Konfigurationsinformationen sollten auch nicht spezifisch für den aktuellen Computer sein. Er sollte von Computer zu Computer portierbar sein.

Wenn der Authentifizierungsdienst die [**RasEapBegin-Funktion**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) für das Authentifizierungsprotokoll aufruft, übergibt er eine [**EMAILS \_ EAP \_ INPUT-Struktur,**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) die einen Zeiger auf die Konfigurationsinformationen enthält. Nach Abschluss des Aufrufs von **RasEapBegin** ruft der Authentifizierungsdienst [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) auf, um den von den Konfigurationsinformationen belegten Arbeitsspeicher freizugeben. Daher sollte das Authentifizierungsprotokoll die Konfigurationsinformationen während des Aufrufs von **RasEapBegin** in einen privaten Speicherpuffer kopieren.

Der Anbieter kann unter dem Registrierungsschlüssel für das Authentifizierungsprotokoll einen Wert hinzufügen, der Standardkonfigurationsinformationen für das Protokoll angibt. Der Anbieter kann auch einen Wert hinzufügen, der angibt, ob der Benutzer beim Erstellen eines Telefonbucheintrags Konfigurationsinformationen eingeben muss. Weitere Informationen finden Sie unter [Authentication Protocol Registry Values](authentication-protocol-registry-values.md).

 

 