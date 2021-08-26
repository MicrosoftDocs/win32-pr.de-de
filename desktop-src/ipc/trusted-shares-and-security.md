---
description: Netzwerk-DDE verwendet vertrauenswürdige Freigaben und Sicherheitsdeskriptoren, um den Zugriff auf Freigaben zu steuern.
ms.assetid: a22d9fc6-a0c9-442f-b278-1271cfbc636b
title: Vertrauenswürdige Freigaben und Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22bed3b520597f6cabe95929d2ee5bf9c29af6bb6c524d2aa136f4c86392cbb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014680"
---
# <a name="trusted-shares-and-security"></a>Vertrauenswürdige Freigaben und Sicherheit

\[Netzwerk-DDE wird nicht mehr unterstützt. Nddeapi.dll ist auf Windows Vista vorhanden, aber alle Funktionsaufrufe geben NDDE \_ NICHT \_ IMPLEMENTIERT zurück.\]

Netzwerk-DDE verwendet vertrauenswürdige Freigaben und Sicherheitsdeskriptoren, um den Zugriff auf Freigaben zu steuern.

## <a name="trusted-shares"></a>Vertrauenswürdige Freigaben

Wenn ein Clientbenutzer von einem Remotecomputer aus eine Verbindung mit einer DDE-Freigabe herstellt, akzeptiert Netzwerk-DDE die Anforderung nur, wenn die folgenden Anweisungen zutreffen:

-   Der Benutzer, der die Freigabe erstellt hat, hat der Freigabe durch Aufrufen von [**NDdeSetTrustedShare den vertrauenswürdigen Status gewährt.**](nddesettrustedshare.md) Nur der Ersteller der Freigabe kann der Freigabe den vertrauenswürdigen Status gewähren. Nicht einmal ein Administrator kann einer DDE-Freigabe, die von einem anderen Benutzer erstellt wurde, den vertrauenswürdigen Status gewähren.
-   Der Benutzer, der die Freigabe erstellt hat, ist derzeit beim Servercomputer angemeldet.

Durch das Gewähren des vertrauenswürdigen Status zu einer Freigabe wird die Freigabe der Liste der vertrauenswürdigen Freigaben des angemeldeten Benutzers im DSDM hinzugefügt. Dadurch wird eine Vertrauensstellung zwischen dem Server und seinen Clients erstellt. Sobald eine DDE-Freigabe den Status "Vertrauenswürdig" hat, können Clients eine Verbindung mit ihr herstellen, solange der Benutzer, der die Freigabe erstellt hat, angemeldet ist. Wenn der Client von einem Remotecomputer aus eine Verbindung mit der Freigabe herstellt, akzeptiert der Netzwerk-DDE die Anforderung nur, wenn die Freigabe in der Liste der vertrauenswürdigen Freigaben des angemeldeten Benutzers im DSDM aufgeführt ist.

## <a name="security"></a>Sicherheit

Netzwerk-DDE führt eine zusätzliche Sicherheitsüberprüfung durch, wenn der Client Daten oder einen Link an fordert. Es wird überprüft, ob der Server dem Remotebenutzer die erforderliche Berechtigung für den Vorgang erteilt hat. Der Server steuert den Zugriff auf die Freigabe über den *pSD-Parameter* der [**NDdeShareAdd-Funktion.**](nddeshareadd.md) Dieser Parameter gibt den Sicherheitsdeskriptor an. Wenn dieser Parameter **NULL ist,** erstellt die Funktion einen Standardsicherheitsdeskriptor, der dem Ersteller der Freigabe Vollzugriff gewährt und allen anderen Benutzern Lese- und Linkberechtigungen erteilt. Um einzelnen Benutzern oder Benutzergruppen zusätzliche Berechtigungen zu gewähren oder zu verweigern, erstellen und verwenden Sie einen Sicherheitsdeskriptor. Weitere Informationen zu Sicherheitsdeskriptoren finden Sie unter [**Access Control**](/windows/desktop/SecAuthZ/access-control).

Um die Sicherheitsbeschreibung für eine vorhandene DDE-Freigabe zu erhalten, rufen Sie die [**NDdeGetShareSecurity-Funktion**](nddegetsharesecurity.md) auf. Sie können die Informationen bearbeiten und dann den Sicherheitsdeskriptor für die Freigabe aktualisieren, indem Sie die [**NDdeSetShareSecurity-Funktion**](nddesetsharesecurity.md) verwenden.

 

 
