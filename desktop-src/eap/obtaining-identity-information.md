---
title: Abrufen von Identitätsinformationen
description: Der Anbieter, der das Authentifizierungsprotokoll implementiert, kann auch eine Funktionsschnittstelle bereitstellen, die anfängliche identifizierende Informationen für den Benutzer erhält, der die Authentifizierung an fordert.
ms.assetid: 773c9fdb-c810-4cea-afed-df6484a9c9c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46245b22a5538fc347ba735620270b7bbc1071574852305adc6b3881202ae317
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605820"
---
# <a name="obtaining-identity-information"></a>Abrufen von Identitätsinformationen

Der Anbieter, der das Authentifizierungsprotokoll implementiert, kann auch eine Funktionsschnittstelle bereitstellen, die anfängliche identifizierende Informationen für den Benutzer erhält, der die Authentifizierung an fordert.

Der Anbieter sollte die folgenden Funktionen implementieren.

-   [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity)
-   [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

Diese Funktionen können in derselben DLL wie das Authentifizierungsprotokoll oder in einer separaten DLL implementiert werden. Außerdem unterstützt die DLL, die die Identitätsfunktionen implementiert, möglicherweise mehr als ein Authentifizierungsprotokoll. Der Pfad zur DLL für diese Funktionen wird im [Registrierungswert RAS \_ EAP \_ VALUENAME \_ IDENTITY](authentication-protocol-registry-values.md) unter dem Schlüssel für das Authentifizierungsprotokoll gespeichert. Weitere Informationen zum Erstellen dieses Registrierungswerts finden Sie unter [EAP-Installation.](eap-installation.md)

Die [**RasEapGetIdentity-Funktion**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) zeigt in der Regel eine Benutzeroberfläche an, um Identitätsinformationen für den Benutzer zu erhalten. Wenn der *dwFlags-Parameter* jedoch das FLAG RAS \_ EAP FLAG NON INTERACTIVE enthält, sollte \_ \_ \_ **RasEapGetIdentity** keine Benutzeroberfläche anzeigen.

Wenn [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) eine Benutzeroberfläche zeigt, muss die Benutzeroberfläche [**WM \_ COMMAND-Meldungen**](../menurc/wm-command.md) unterstützen, bei denen der Wert von [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))(*wParam*) gleich IDCANCEL ist.

Der Authentifizierungsdienst ruft [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) auf, wenn der [WERT VON RAS \_ EAP \_ VALUENAME INVOKE \_ \_ NAMEDLG,](authentication-protocol-registry-values.md) der sich in der Registrierung für diesen EAP befindet, auf 0 (null) festgelegt ist. Wenn RAS \_ EAP VALUENAME INVOKE NAMEDLG nicht vorhanden oder vorhanden ist und auf 1 festgelegt ist, zeigt der Authentifizierungsdienst das Dialogfeld Standardbenutzername des Systems \_ \_ \_ an.

Zusätzlich zum RAS EAP VALUENAME INVOKE NAMEDLG kann der EAP-Anbieter in der Registrierung den zugehörigen Wert \_ \_ RAS \_ \_ [ \_ EAP \_ VALUENAME INVOKE \_ \_ PWDDLG](authentication-protocol-registry-values.md)erstellen. Wenn dieser Wert vorhanden ist und auf 0 (null) festgelegt ist, zeigt der Dienst das Standarddialogfeld für Systemkennwort nicht an. Dieser Wert ist nützlich, wenn Sie eine biometrische Methode implementieren, z. B. einen Fingerabdruckscan, um den Benutzer zu authentifizieren. Wenn sowohl der RAS EAP VALUENAME INVOKE NAMEDLG- als auch der \_ \_ RAS \_ \_ \_ EAP \_ VALUENAME INVOKE \_ \_ PWDDLG-Wert 0 (null) sind, kann eine Identitätsbenutzeroberfläche verwendet werden, um sowohl die Identität als auch biometrische Informationen zu erhalten. Wenn jedoch nur RAS EAP VALUENAME INVOKE PWDDLG 0 (null) ist, ruft der Authentifizierungsdienst \_ \_ \_ \_ [**RasEapGetIdentity nicht auf.**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) In diesem Fall können Sie die interaktive Benutzeroberfläche [verwenden,](interactive-user-interface.md) um die biometrischen Informationen zu erhalten.

Weitere Informationen zu diesen Registrierungswerten finden Sie unter [Authentication Protocol Registry Values](authentication-protocol-registry-values.md).

Die von [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) erhaltenen Informationen werden während des Aufrufs von [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))an das Authentifizierungsprotokoll übergeben. Auf die Informationen wird von den **PszIdentity-** und **pUserData-Membern** der [**\_ ORGANISATIONS-EAP \_ INPUT-Struktur**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) verwiesen. Um diese Informationen in der Registrierung auf dem Clientcomputer zu speichern, sollte das Authentifizierungsprotokoll die Informationen im *pEapOutput-Parameter* von [**RasEapMakeMessage zurückgeben.**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))

Nach dem Aufruf von [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))ruft der Authentifizierungsdienst [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) auf, um den von diesen Daten belegten Arbeitsspeicher frei zu geben. Daher sollte das Authentifizierungsprotokoll die Informationen während des Aufrufs von **RasEapBegin** in einen privaten Speicherpuffer kopieren.

 

 