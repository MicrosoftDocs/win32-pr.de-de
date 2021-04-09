---
description: Eine Berechtigung ist das Recht eines Kontos (z. b. ein Benutzer-oder Gruppenkonto), um verschiedene System Vorgänge auf dem lokalen Computer auszuführen, z. b. das Herunterfahren des Systems, das Laden von Gerätetreibern oder das Ändern der Systemzeit.
ms.assetid: fe6aae0f-93eb-4aba-a6ac-45e71c251c51
title: Rechte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cccedffdf5786da07dd2cfd77c3de428ee15ba94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959067"
---
# <a name="privileges"></a>Rechte

Eine [*Berechtigung*](/windows/desktop/SecGloss/p-gly) ist das Recht eines Kontos (z. b. ein Benutzer-oder Gruppenkonto), um verschiedene System Vorgänge auf dem lokalen Computer auszuführen, z. b. das Herunterfahren des Systems, das Laden von Gerätetreibern oder das Ändern der Systemzeit. Die Berechtigungen unterscheiden sich von Zugriffsrechten auf zwei Arten:

-   Berechtigungen steuern den Zugriff auf Systemressourcen und systembezogene Aufgaben, während Zugriffsrechte den Zugriff auf Sicherungs [fähige Objekte](securable-objects.md)steuern.
-   Ein Systemadministrator weist Benutzer-und Gruppenkonten Berechtigungen zu, während das System den Zugriff auf ein Sicherungs fähiges Objekt basierend auf den in den ACEs in der DACL des Objekts gewährten Zugriffsrechten gewährt oder verweigert.

Jedes System verfügt über eine Konto Datenbank, in der die Berechtigungen von Benutzer-und Gruppenkonten gespeichert sind. Wenn sich ein Benutzer anmeldet, erstellt das System ein [Zugriffs Token](access-tokens.md) , das eine Liste der Benutzerberechtigungen enthält, einschließlich derjenigen, die dem Benutzer oder Gruppen, denen der Benutzer angehört, erteilt wurden. Beachten Sie, dass die Berechtigungen nur für den lokalen Computer gelten. ein Domänen Konto kann auf verschiedenen Computern über unterschiedliche Berechtigungen verfügen.

Wenn der Benutzer versucht, einen privilegierten Vorgang auszuführen, prüft das System das Zugriffs Token des Benutzers, um zu bestimmen, ob der Benutzer die erforderlichen Berechtigungen besitzt. wenn dies der Fall ist, wird überprüft, ob die Berechtigungen aktiviert sind. Wenn der Benutzer diese Tests nicht durchführt, führt das System den Vorgang nicht aus.

Um die in einem Zugriffs Token gespeicherten Berechtigungen zu ermitteln, müssen Sie die [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) -Funktion aufrufen, die auch angibt, welche Berechtigungen aktiviert sind. Die meisten Berechtigungen sind standardmäßig deaktiviert.

Die Windows-API definiert einen Satz von Zeichen folgen Konstanten, wie z. b. den Namen des SE-Zugriffstokens, \_ \_ um die verschiedenen Berechtigungen zu identifizieren. Diese Konstanten sind auf allen Systemen identisch und in Winnt. h definiert. Eine Tabelle der von Windows definierten Berechtigungen finden Sie unter [Berechtigungs Konstanten](authorization-constants.md). Allerdings verwenden die Funktionen, die die Berechtigungen in einem Zugriffs Token abrufen und anpassen, den [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) -Typ, um Berechtigungen zu identifizieren. Die **LUID** -Werte für eine Berechtigung können sich von einem Computer zu einem anderen und von einem Start zum anderen auf demselben Computer unterscheiden. Verwenden Sie die [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) -Funktion, um die aktuelle **LUID** zu erhalten, die einer der Zeichen folgen Konstanten entspricht. Verwenden Sie die [**lookupprivilegilegename**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) -Funktion, um eine **LUID** in die entsprechende Zeichen folgen Konstante zu konvertieren.

Das System stellt eine Reihe von anzeigen Amen bereit, mit denen die einzelnen Berechtigungen beschrieben werden. Diese sind nützlich, wenn Sie eine Beschreibung der Berechtigung für den Benutzer anzeigen müssen. Verwenden Sie die [**lookupprivilegedisplayname**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegedisplaynamea) -Funktion, um eine Beschreibungs Zeichenfolge abzurufen, die der Zeichen folgen Konstante für eine Berechtigung entspricht. Auf Systemen, die US-Englisch verwenden, lautet der Anzeige Name für die \_ Berechtigung "SE SYSTEMTIME \_ Name" z. b. "Systemzeit ändern".

Sie können die [**privilegecheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) -Funktion verwenden, um zu bestimmen, ob ein Zugriffs Token einen angegebenen Berechtigungs Satz enthält. Dies ist in erster Linie für Server Anwendungen nützlich, die die Identität eines Clients annehmen.

Ein Systemadministrator kann Verwaltungs Tools, wie z. b. Benutzer-Manager, verwenden, um Berechtigungen für Benutzer-und Gruppenkonten hinzuzufügen oder zu entfernen. Administratoren können die Funktionen der [*lokalen Sicherheits Autorität (Local Security Authority*](/windows/desktop/SecGloss/l-gly) , LSA) Programm gesteuert verwenden, um mit Berechtigungen zu arbeiten. Die Funktionen " [**lsaaddaccounschghts**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) " und " [**lsaremuveaccountrghts**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaremoveaccountrights) " fügen Berechtigungen zu einem Konto hinzu oder entfernen Sie. Die [**lsaenumerateaccounselghts**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountrights) -Funktion Listet die Berechtigungen auf, die von einem angegebenen Konto gehalten werden. Die [**lsaenumerateaccountenwithuserright**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright) -Funktion Listet die Konten auf, die eine angegebene Berechtigung enthalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Autorisierungs Konstanten](authorization-constants.md)
</dt> <dt>

[Aktivieren und Deaktivieren von Berechtigungen in C++](enabling-and-disabling-privileges-in-c--.md)
</dt> </dl>

 

 
