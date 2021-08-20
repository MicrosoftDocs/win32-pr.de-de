---
description: Die Startseite des Eigenschaftenblatts, das von der EditSecurity-Funktion angezeigt wird. Sie können auch die CreateSecurityPage-Funktion verwenden, um eine grundlegende Sicherheitseigenschaftsseite zum Einfügen in Ihr eigenes Eigenschaftenblatt zu erstellen.
ms.assetid: 6623fe7e-e91d-49c7-9ad0-7791c178d12b
title: Eigenschaftenseite "Basic Security"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8628b0b096e24a3a7baef94f5ab9913c2cd89825bb15bf6b19d18cd81d1033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783707"
---
# <a name="basic-security-property-page"></a>Eigenschaftenseite "Basic Security"

Die Grundlegende Sicherheitseigenschaftsseite ist die Startseite des Eigenschaftenblatts, das von der [**EditSecurity-Funktion angezeigt**](/windows/desktop/api/Aclui/nf-aclui-editsecurity) wird. Sie können auch die [**CreateSecurityPage-Funktion**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) verwenden, um eine grundlegende Sicherheitseigenschaftsseite zum Einfügen in Ihr eigenes Eigenschaftenblatt zu erstellen.

Auf der Eigenschaftenseite wird eine Liste der Vertrauenshänder angezeigt, die in den [Zugriffssteuerungseinträgen](trustees.md) (ACCESS [*Control Entries,*](/windows/desktop/SecGloss/a-gly) ACEs) der DACL [*(Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) des Objekts benannt sind. Die Seite enthält auch eine Liste der Zugriffsrechte, die vom -Objekt unterstützt werden. Wenn der Benutzer einen Namen aus der Liste der Vertrauenshänder auswählt, geben die Kontrollkästchen neben jedem Zugriffsrecht die Rechte an, die für diesen Vertrauenshänder zugelassen oder verweigert werden. Der Benutzer kann dann die Kontrollkästchen aktivieren oder löschen, um die Zugriffsrechte des Vertrauenshänders zu ändern. Der Benutzer kann der Liste auch Vertrauenshänder hinzufügen oder daraus entfernen.

Auf der Grundlegenden Sicherheitseigenschaftsseite können keine komplexen ACEs wie [objektspezifische ACEs](object-specific-aces.md)oder ACE-Vererbungsinformationen angezeigt werden. Um dem Benutzer das Anzeigen oder Bearbeiten solcher  Informationen zu ermöglichen, können Sie auf der Seite "Grundlegende Sicherheit" die Schaltfläche Erweitert hinzufügen. Der Benutzer kann auf die Schaltfläche **Erweitert klicken,** um ein [erweitertes Sicherheitseigenschaftsblatt anzuzeigen.](advanced-security-property-sheet.md) Dieses Eigenschaftenblatt enthält Eigenschaftenseiten, mit denen der [](/windows/desktop/SecGloss/s-gly) Benutzer die Systemzugriffssteuerungsliste (SACL) des Objekts bearbeiten, den Besitzer des Objekts ändern oder die DACL des Objekts erweitert bearbeiten kann. Um die Schaltfläche **Erweitert anzuzeigen,** legen Sie das SI ADVANCED-Flag in der SI OBJECT INFO-Struktur fest, die von Ihrer \_ [**ISecurityInformation::GetObjectInformation-Implementierung zurückgegeben**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) wird. [**\_ \_**](/windows/desktop/api/Aclui/ns-aclui-si_object_info)

Sie können das **pszPageTitle-Member** der [**SI OBJECT \_ \_ INFO-Struktur**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) verwenden, um den Titel der Grundlegenden Sicherheitseigenschaftsseite anzugeben. Der Standardtitel ist **Security**.

 

 
