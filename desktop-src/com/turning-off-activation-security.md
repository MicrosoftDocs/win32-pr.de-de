---
title: Deaktivieren der Aktivierungs Sicherheit
description: Deaktivieren der Aktivierungs Sicherheit
ms.assetid: 3474f8ad-f041-4886-ad39-ff0603c5c69e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da3ebd7cc03d79fc38fbafe3bc652efc3499437
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391060"
---
# <a name="turning-off-activation-security"></a>Deaktivieren der Aktivierungs Sicherheit

Normalerweise werden bei der Aktivierung die Standard Sicherheitseinstellungen verwendet. Sie können die Aktivierungs Sicherheit jedoch steuern, indem Sie eine [**coauthinfo**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) -Struktur angeben, die ein Member der [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) -Struktur ist, die an die Aktivierungs Funktionen übermittelt wird. Wenn der Client eine Authentifizierungs Ebene der RPC- \_ C- \_ authn- \_ Ebene \_ None in der **coauthinfo** -Struktur angibt, wird die Authentifizierung nicht versucht. Andernfalls wird eine sichere Aktivierung versucht, und wenn die Authentifizierung fehlschlägt, schlägt die Aktivierung fehl.

Wenn der Client keine explizite [**coauthinfo**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) -Struktur angibt und stattdessen den Zeiger auf **null** festlegt, versucht com, den Client zu authentifizieren. Wenn der Client nicht authentifiziert werden kann, prüft com die Sicherheits Beschreibung der Startberechtigung, um festzustellen, ob eine DACL mit **null** oder eine ACL vorhanden ist, die den Zugriff auf alle Benutzer zulässt. Wenn diese Überprüfung erfolgreich ist, wird der Server gestartet. Daher kann selbst dann, wenn der Client keine **coauthinfo**-Struktur angibt, eine unsichere Aktivierung erfolgen, wenn der Server dies zulässt.

> [!Note]  
> Damit nicht authentifizierte Netzwerk Benutzer eine COM-Anwendung ausführen können, müssen die Anwendungs Rollen den anonymen Benutzer einschließen. Ab Windows Server 2003 ist der anonyme Benutzer standardmäßig nicht in der Gruppe "jeder" enthalten.

 

Warum soll ein Client die Aktivierungs Sicherheit explizit deaktivieren, auch wenn die unsichere Aktivierung letztendlich stattfindet, wenn der Server Sie zulässt? Aufgrund der expliziten Deaktivierung der Aktivierungs Sicherheit wird die Leistung erhöht, wenn der Client keine Sicherheitsüberprüfungen mehr wünscht oder benötigt.

Es müssen die folgenden Schritte ausgeführt werden, um die Aktivierungs Sicherheit explizit zu deaktivieren:

-   Der Client muss \_ \_ \_ \_ in der [**coauthinfo**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) -Struktur, die Mitglied der [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) -Struktur ist, die der Aktivierungsfunktion bereitgestellt wird, eine Authentifizierungs Ebene von RPC C authn Level None angeben.
-   Der Client muss \_ \_ \_ \_ in der [**coauthinfo**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) -Struktur, die ein Member der [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) -Struktur ist, die für die Aktivierungsfunktion bereitgestellt wird, eine Identitätswechsel Ebene der RPC-C-IMP-Ebene angeben. Wenn dieser Wert nicht erfolgreich ist, wird der RPC \_ S- \_ Server nicht verfügbar sein \_ .
-   Der Server muss **alle** Benutzer für die **Standard Start Berechtigungen** angeben. Die empfohlene Vorgehensweise zum Ausführen dieser Aufgabe ist die Verwendung Dcomcnfg.exe wie folgt:
    1.  Führen Sie "Dcomcnfg.exe" aus.
    2.  Wählen Sie auf der Seite **Anwendungen** die Anwendung aus, die den Server darstellt. Klicken Sie auf die Schaltfläche **Eigenschaften** (oder Doppelklicken Sie auf die ausgewählte Anwendung).
    3.  Klicken Sie auf der Eigenschaften Seite **Sicherheit** auf die Schaltfläche **benutzerdefinierte Start Berechtigungen verwenden** .
    4.  Klicken Sie im Bereich **Start Berechtigungen** auf die Schaltfläche **Bearbeiten** .
    5.  Klicken Sie im Dialogfeld **Berechtigungen für Registrierungs Wert** auf die Schaltfläche **Hinzufügen** .
    6.  Wählen Sie im Listenfeld den Eintrag für **alle** aus.
    7.  Wählen Sie im Listenfeld **Zugriffstyp** die Option **Start zulassen** aus.
    8.  Klicken Sie auf die Schaltfläche **OK** .

> [!Note]  
> In Windows Server 2003 enthält die Authentifizierungsfunktion für die COM+-Systemanwendung den Wert eoac- \_ deaktivierte \_ AAA. Dieser Wert, der Aktivierungen von Aktivierungen durch aktivierte Aktivierungen deaktiviert, wird beim Starten der Systemanwendung im [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) -Befehl verwendet. Wenn Sie die Authentifizierungsfunktion auf eoac \_ deaktivieren, \_ kann eine Anwendung, die unter einem privilegierten Konto (z. b. LocalSystem) ausgeführt wird, verhindern, dass Ihre Identität verwendet wird, um nicht vertrauenswürdige Komponenten zu starten.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ausschalten der Rückruf Sicherheit](turning-off-call-security.md)
</dt> </dl>

 

 