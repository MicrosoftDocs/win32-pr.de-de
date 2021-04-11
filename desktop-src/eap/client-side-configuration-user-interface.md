---
title: Client-Side Konfigurations Benutzeroberfläche
description: Der Hersteller, der das Authentifizierungsprotokoll implementiert, kann auch eine Konfigurations Benutzeroberfläche (UI) für das Protokoll bereitstellen.
ms.assetid: 956a7ad6-1fd5-4938-aa2f-4de646dfd6c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d7296f6afd8fd84f287b6c2c7085e5ed92685f5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314888"
---
# <a name="client-side-configuration-user-interface"></a>Client-Side Konfigurations Benutzeroberfläche

Der Hersteller, der das Authentifizierungsprotokoll implementiert, kann auch eine Konfigurations Benutzeroberfläche (UI) für das Protokoll bereitstellen. Die Konfigurations Benutzeroberfläche kann in derselben DLL wie das Authentifizierungsprotokoll oder in einer separaten dll implementiert werden. Außerdem unterstützt die dll, die die Konfigurations Benutzeroberfläche implementiert, möglicherweise mehr als ein Authentifizierungsprotokoll. Der Pfad zu der DLL für die Konfigurations Benutzeroberfläche wird im RAS- \_ Registrierungs Wert "EAP \_ valueName \_ configui" unter dem Schlüssel für das Authentifizierungsprotokoll gespeichert. Weitere Informationen zum Erstellen dieses Registrierungs Werts finden Sie unter [EAP-Installation](eap-installation.md).

Die DLL für die Benutzeroberfläche der Konfiguration sollte Einstiegspunkte für die folgenden Funktionen exportieren:

[**Raseapinvokeconfigui**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeconfigui)

[**Raseapfrememory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

Wenn der Benutzer einen Konfigurationseintrag für eine bestimmte Verbindung erstellt, und zwar unabhängig davon, ob für einen RAS-oder einen drahtlosen Client, kann der Benutzer das Authentifizierungsprotokoll auswählen, das der Dienst für diesen Eintrag verwenden soll. Wenn das Authentifizierungsprotokoll konfigurierbar ist, ruft der Dienst [**raseapinvokeconfigui**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeconfigui) auf, um die Konfigurations Benutzeroberfläche aufzurufen. Die Konfigurations Benutzeroberfläche speichert die von **raseapinvokeconfigui** zurückgegebenen Konfigurationsinformationen im Konfigurationseintrag.

Die Konfigurationsinformationen sollten für alle Benutzer auf dem Client Computer generisch sein. Informationen, die für einen bestimmten Benutzer oder Benutzer spezifisch sind, dürfen nicht im Eintrag gespeichert werden. Das Authentifizierungsprotokoll sollte benutzerspezifische Informationen mithilfe der [Identitäts Funktionen](obtaining-identity-information.md) oder [interaktiven Benutzeroberfläche](interactive-user-interface.md)abrufen. Das Authentifizierungsprotokoll kann diese Informationen in der Registrierung speichern, indem es an den Authentifizierungsdienst im " *Peer Output* "-Parameter von " [**raseapmakemess Age**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))" übergeben wird.

Die Konfigurationsinformationen sollten auch nicht spezifisch für den aktuellen Computer sein. Er sollte von Computer zu Computer portierbar sein.

Wenn der Authentifizierungsdienst die [**raseapbegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) -Funktion für das Authentifizierungsprotokoll aufruft, übergibt er eine [**PPP- \_ EAP- \_ Eingabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) Struktur, die einen Zeiger auf die Konfigurationsinformationen enthält. Nachdem der Aufruf von **raseapbegin** abgeschlossen ist, ruft der Authentifizierungsdienst [**raseapfreememory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) auf, um den von den Konfigurationsinformationen belegten Arbeitsspeicher freizugeben. Daher sollte das Authentifizierungsprotokoll die Konfigurationsinformationen während des Aufrufens von **raseapbegin** in einen privaten Arbeitsspeicher Puffer kopieren.

Der Anbieter kann einen Wert unter dem Registrierungsschlüssel für das Authentifizierungsprotokoll hinzufügen, das die Standard Konfigurationsinformationen für das Protokoll angibt. Der Anbieter kann auch einen Wert hinzufügen, der angibt, ob der Benutzer beim Erstellen eines Telefonbucheintrags Konfigurationsinformationen eingeben muss. Weitere Informationen finden Sie unter [Registrierungs Werte für das Authentifizierungsprotokoll](authentication-protocol-registry-values.md).

 

 