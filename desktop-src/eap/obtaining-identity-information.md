---
title: Abrufen von Identitätsinformationen
description: Der Hersteller, der das Authentifizierungsprotokoll implementiert, kann auch eine Funktions Schnittstelle bereitstellen, die anfängliche identifizierende Informationen für den Benutzer erhält, der die Authentifizierung anfordert.
ms.assetid: 773c9fdb-c810-4cea-afed-df6484a9c9c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9519da9d66937fd25245fe78f12ef34c3c0ad8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038831"
---
# <a name="obtaining-identity-information"></a>Abrufen von Identitätsinformationen

Der Hersteller, der das Authentifizierungsprotokoll implementiert, kann auch eine Funktions Schnittstelle bereitstellen, die anfängliche identifizierende Informationen für den Benutzer erhält, der die Authentifizierung anfordert.

Der Anbieter sollte die folgenden Funktionen implementieren.

-   [**Raseapgetidentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity)
-   [**Raseapfrememory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

Diese Funktionen können in derselben DLL wie das Authentifizierungsprotokoll oder in einer separaten dll implementiert werden. Außerdem unterstützt die dll, die die Identitäts Funktionen implementiert, möglicherweise mehr als ein Authentifizierungsprotokoll. Der Pfad zur DLL für diese Funktionen wird im RAS-Registrierungs Wert " [ \_ EAP \_ valueName \_ Identity](authentication-protocol-registry-values.md) " unter dem Schlüssel für das Authentifizierungsprotokoll gespeichert. Weitere Informationen zum Erstellen dieses Registrierungs Werts finden Sie unter [EAP-Installation](eap-installation.md).

Die [**raseapgetidentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) -Funktion zeigt in der Regel eine Benutzeroberfläche (User Interface, UI) an, um Identitätsinformationen für den Benutzer abzurufen. Wenn der *dwFlags* -Parameter jedoch das RAS- \_ EAP- \_ Flag "nicht interaktiv" enthält \_ \_ , sollte **raseapgetidentity** keine Benutzeroberfläche anzeigen.

Wenn [**raseapgetidentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) eine Benutzeroberfläche anzeigt, muss die Benutzeroberfläche [**WM- \_ Befehls**](../menurc/wm-command.md) Nachrichten unterstützen, bei denen der Wert von [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))(*wParam*) gleich IDCANCEL ist.

Der Authentifizierungsdienst ruft [**raseapgetidentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) auf, wenn der [RAS- \_ EAP \_ valueName den \_ \_ namedlg](authentication-protocol-registry-values.md) -Wert aufruft, der sich in der Registrierung für dieses EAP befindet, auf 0 (null) festgelegt ist. Wenn RAS- \_ EAP- \_ valueName " \_ \_ namedlg aufrufen" nicht vorhanden ist oder vorhanden und auf 1 festgelegt ist, zeigt der Authentifizierungsdienst das Standard Dialogfeld "Systembenutzer Name" an.

Zusätzlich zu RAS- \_ EAP \_ valueName \_ Aufrufen von \_ namedlg kann der EAP-Anbieter einen zugehörigen Wert erstellen, der [RAS- \_ EAP \_ valueName \_ \_ pwddlg](authentication-protocol-registry-values.md)in der Registrierung aufruft. Wenn dieser Wert vorhanden und auf 0 (null) festgelegt ist, zeigt der Dienst nicht das Standard Dialogfeld "System Kennwort" an. Dieser Wert ist hilfreich, wenn eine biometrische Methode implementiert wird, z. b. eine Fingerabdruck Überprüfung, um den Benutzer zu authentifizieren. Wenn der RAS \_ -EAP \_ -valueName " \_ \_ namedlg" aufruft und "RAS \_ EAP valueName" den Wert "0" (null) aufruft \_ \_ \_ , könnte eine Identitäts Benutzeroberfläche verwendet werden, um die Identitäts-und biometrischen Informationen abzurufen. Wenn jedoch nur der RAS- \_ EAP- \_ valueName " \_ \_ pwddlg" auf 0 (null) aufzurufen, ruft der Authentifizierungsdienst " [**raseapgetidentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity)" nicht auf. In diesem Fall können Sie die [interaktive Benutzeroberfläche](interactive-user-interface.md) zum Abrufen der biometrischen Informationen verwenden.

Weitere Informationen zu diesen Registrierungs Werten finden Sie unter [Registrierungs Werte für das Authentifizierungsprotokoll](authentication-protocol-registry-values.md).

Die Informationen, die von [**raseapgetidentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) abgerufen werden, werden während des Aufrufes von [**raseapbegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))an das Authentifizierungsprotokoll übermittelt. Auf die Informationen wird von den **pszidentity** -und **puserdata** -Membern der [**PPP- \_ EAP- \_ Eingabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) Struktur verwiesen. Um diese Informationen in der Registrierung auf dem Client Computer zu speichern, sollte das Authentifizierungsprotokoll die Informationen im Parameter " *Peer Output* " von " [**raseapmakemess Age**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))" zurückgeben.

Nach dem Aufruf von [**raseapbegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))ruft der Authentifizierungsdienst [**raseapfreememory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) auf, um den von diesen Daten belegten Arbeitsspeicher freizugeben. Daher sollte das Authentifizierungsprotokoll die Informationen während des Aufrufens von **raseapbegin** in einen privaten Speicherpuffer kopieren.

 

 