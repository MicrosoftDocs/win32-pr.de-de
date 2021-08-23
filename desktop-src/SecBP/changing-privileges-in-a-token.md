---
description: Erläutert, wie Berechtigungen in einem Token mithilfe der Funktionen AdjustTokenPrivileges und CreateRestrictedToken geändert werden.
ms.assetid: b8e47d04-07c1-4d57-8209-6b0c397476e5
title: Ändern von Berechtigungen in einem Token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c511ca66c5d4739057f5ea75cae589ee97e849f659002a612e7d22fd6be8eecb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622750"
---
# <a name="changing-privileges-in-a-token"></a>Ändern von Berechtigungen in einem Token

Sie können die Berechtigungen in einem primären Token oder einem Identitätswechseltoken auf zwei Arten ändern:

-   Aktivieren oder deaktivieren Sie Berechtigungen mithilfe der [**Funktion AdjustTokenPrivileges.**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges)
-   Beschränken oder entfernen Sie Berechtigungen mithilfe der [**CreateRestrictedToken-Funktion.**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken)

[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) kann dem Token keine Berechtigungen hinzufügen oder daraus entfernen. Sie kann nur vorhandene Berechtigungen aktivieren, die derzeit deaktiviert sind, oder vorhandene Berechtigungen deaktivieren, die derzeit aktiviert sind. Beispiele finden Sie unter [Aktivieren und Deaktivieren von Berechtigungen in C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).

Informationen zum Zuweisen von Berechtigungen zu einem Benutzerkonto finden Sie unter [Zuweisen von Berechtigungen zu einem Konto.](assigning-privileges-to-an-account.md)

[**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) verfügt über umfangreichere Funktionen wie folgt:

-   Entfernen einer Berechtigung. Beachten Sie, dass das Entfernen einer Berechtigung nicht mit dem Deaktivieren einer Berechtigung identisch ist. Nachdem eine Berechtigung aus einem Token entfernt wurde, kann sie nicht mehr zurückgesetzt werden.
-   Anfügen des Attributs "Nur verweigern" an SIDs im Token. Dies hat zur Folge, dass bestimmte Gruppen oder Konten verweigert werden, z. B. das Verweigern des Löschzugriffs auf eine bestimmte Datei durch die Gruppe Jeder. Weitere Informationen zum Einschränken von SIDs finden Sie unter [SID-Attribute in einem Zugriffstoken.](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token)
-   Angeben einer Liste mit einschränkungenden SIDs im Token. Informationen zum Einschränken von SIDs finden Sie unter [Eingeschränkte Token.](/windows/desktop/SecAuthZ/restricted-tokens)

 

 
