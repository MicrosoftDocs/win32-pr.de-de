---
description: Erläutert das Ändern von Berechtigungen in einem Token mithilfe der Funktionen "" "" "" "" "" "" "" "" "" ""
ms.assetid: b8e47d04-07c1-4d57-8209-6b0c397476e5
title: Ändern von Berechtigungen in einem Token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8b77d966acf90db101269b77a767550bcae3ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366167"
---
# <a name="changing-privileges-in-a-token"></a>Ändern von Berechtigungen in einem Token

Sie können die Berechtigungen entweder in einem primären oder einem Identitätswechsel Token auf zwei Arten ändern:

-   Aktivieren oder deaktivieren Sie Berechtigungen mithilfe der Funktion "- [**tokenprivilegien**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) ".
-   Einschränken oder Entfernen von Berechtigungen mithilfe der [**Funktion "**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) " von "".

[](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) "" "" "" "" "" "" "" "" "". Es können nur vorhandene Berechtigungen aktiviert werden, die zurzeit deaktiviert sind, oder vorhandene Berechtigungen deaktivieren, die derzeit aktiviert sind. Beispiele finden Sie unter [aktivieren und Deaktivieren von Berechtigungen in C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).

Informationen zum Zuweisen von Berechtigungen zu einem Benutzerkonto finden Sie unter [Zuweisen von Berechtigungen zu einem Konto](assigning-privileges-to-an-account.md).

" [**Kreaterestrictedtoken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) " verfügt über umfangreichere Funktionen wie folgt:

-   Entfernen einer Berechtigung. Beachten Sie, dass das Entfernen einer Berechtigung nicht mit der Deaktivierung einer Berechtigung identisch ist. Nachdem eine Berechtigung aus einem Token entfernt wurde, kann Sie nicht wieder zurückgesetzt werden.
-   Das Deny-only-Attribut wird an SIDs im Token angefügt. Dies hat den Effekt, dass bestimmte Gruppen oder Konten nicht zulässig sind, z. b. wenn die Gruppe "jeder" den Lösch Zugriff auf eine bestimmte Datei verweigert. Weitere Informationen zum Einschränken von SIDs finden Sie unter [SID-Attribute in einem Zugriffs Token](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token).
-   Angeben einer Liste mit einschränkenden SIDs im Token. Informationen zum Einschränken von SIDs finden Sie unter [Eingeschränkte Token](/windows/desktop/SecAuthZ/restricted-tokens).

 

 
