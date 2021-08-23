---
description: Eine Berechtigung ist das Recht eines Kontos, z. B. eines Benutzer- oder Gruppenkontos, verschiedene systembezogene Vorgänge auf dem lokalen Computer durchzuführen, z. B. das Herunterfahren des Systems, das Laden von Gerätetreibern oder das Ändern der Systemzeit.
ms.assetid: fe6aae0f-93eb-4aba-a6ac-45e71c251c51
title: Rechte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c0289ea66f4c1d2f94cb74112a1160dd93cc873125ae5183bd6a6fab5834b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118912136"
---
# <a name="privileges"></a>Rechte

Eine [](/windows/desktop/SecGloss/p-gly) Berechtigung ist das Recht eines Kontos, z. B. eines Benutzer- oder Gruppenkontos, verschiedene systembezogene Vorgänge auf dem lokalen Computer durchzuführen, z. B. das Herunterfahren des Systems, das Laden von Gerätetreibern oder das Ändern der Systemzeit. Berechtigungen unterscheiden sich von Zugriffsrechten auf zwei Arten:

-   Berechtigungen steuern den Zugriff auf Systemressourcen und systembezogene Aufgaben, während Zugriffsrechte den Zugriff auf [sicherungsfähige Objekte steuern.](securable-objects.md)
-   Ein Systemadministrator weist Benutzer- und Gruppenkonten Berechtigungen zu, während das System den Zugriff auf ein sicherungsfähiges Objekt basierend auf den Zugriffsrechten gewährt, die in den ACEs in der DACL des Objekts gewährt werden.

Jedes System verfügt über eine Kontodatenbank, in der die Berechtigungen von Benutzer- und Gruppenkonten gespeichert werden. Wenn sich ein Benutzer anmeldet, erzeugt das System ein Zugriffstoken, das eine Liste der Berechtigungen des Benutzers enthält, einschließlich der Berechtigungen, die dem Benutzer oder Gruppen gewährt werden, zu denen der Benutzer gehört. [](access-tokens.md) Beachten Sie, dass die Berechtigungen nur für den lokalen Computer gelten. Ein Domänenkonto kann auf verschiedenen Computern unterschiedliche Berechtigungen haben.

Wenn der Benutzer versucht, einen privilegierten Vorgang durchzuführen, überprüft das System das Zugriffstoken des Benutzers, um zu bestimmen, ob der Benutzer über die erforderlichen Berechtigungen verfügt. In diesem Grund wird überprüft, ob die Berechtigungen aktiviert sind. Wenn der Benutzer diese Tests nicht bestanden hat, führt das System den Vorgang nicht aus.

Um die in einem Zugriffstoken gehaltenen Berechtigungen zu bestimmen, rufen Sie die [**GetTokenInformation-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) auf, die auch angibt, welche Berechtigungen aktiviert sind. Die meisten Berechtigungen sind standardmäßig deaktiviert.

Die Windows-API definiert einen Satz von Zeichenfolgenkonst konstanten, z. B. SE \_ ASSIGNPRIMARYTOKEN NAME, um die \_ verschiedenen Berechtigungen zu identifizieren. Diese Konstanten sind auf allen Systemen identisch und werden in Winnt.h definiert. Eine Tabelle mit den berechtigungen, die durch Windows definiert werden, finden Sie unter [Privilege Constants](authorization-constants.md). Die Funktionen, die die Berechtigungen in einem Zugriffstoken abrufen und anpassen, verwenden jedoch den [**LUID-Typ,**](/windows/desktop/api/Winnt/ns-winnt-luid) um Berechtigungen zu identifizieren. Die **LUID-Werte** für eine Berechtigung können sich von Computer zu Computer und von Start zu Computer unterscheiden. Verwenden Sie die [**LookupPrivilegeValue-Funktion,**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) um die aktuelle **LUID** zu erhalten, die einer der Zeichenfolgenkonst constants entspricht. Verwenden Sie [**die LookupPrivilegeName-Funktion,**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) um eine **LUID** in die entsprechende Zeichenfolgenkonst constant zu konvertieren.

Das System bietet eine Reihe von Anzeigenamen, die die einzelnen Berechtigungen beschreiben. Diese sind nützlich, wenn Sie dem Benutzer eine Beschreibung einer Berechtigung anzeigen müssen. Verwenden Sie [**die LookupPrivilegeDisplayName-Funktion,**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegedisplaynamea) um eine Beschreibungszeichenfolge abzurufen, die der Zeichenfolgenkonst constant für eine Berechtigung entspricht. Auf Systemen, die us-amerikanisches Englisch verwenden, ist der Anzeigename für die SE \_ SYSTEMTIME \_ NAME-Berechtigung beispielsweise "Systemzeit ändern".

Sie können die [**PrivilegeCheck-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) verwenden, um zu bestimmen, ob ein Zugriffstoken einen angegebenen Berechtigungssatz enthält. Dies ist in erster Linie für Serveranwendungen nützlich, die die Identität eines Clients angenommen haben.

Ein Systemadministrator kann Verwaltungstools wie User Manager verwenden, um Berechtigungen für Benutzer- und Gruppenkonten hinzuzufügen oder zu entfernen. Administratoren können programmgesteuert die Funktionen der lokalen Sicherheitsstelle [*(Local Security Authority,*](/windows/desktop/SecGloss/l-gly) LSA) verwenden, um mit Berechtigungen zu arbeiten. Die [**Funktionen LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) und [**LsaRemoveAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaremoveaccountrights) fügen einem Konto Berechtigungen hinzu oder entfernen diese. Die [**LsaEnumerateAccountRights-Funktion**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountrights) enumeriert die Berechtigungen eines angegebenen Kontos. Die [**LsaEnumerateAccountsWithUserRight-Funktion**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright) enumeriert die Konten, die über eine angegebene Berechtigung verfügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Autorisierungskonst constants](authorization-constants.md)
</dt> <dt>

[Aktivieren und Deaktivieren von Berechtigungen in C++](enabling-and-disabling-privileges-in-c--.md)
</dt> </dl>

 

 
