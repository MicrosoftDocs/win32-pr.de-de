---
description: Die Startseite des Eigenschaftenblatts, das von der EditSecurity-Funktion angezeigt wird. Sie können auch die CreateSecurityPage-Funktion verwenden, um eine grundlegende Sicherheitseigenschaftenseite zu erstellen, die in Ihr eigenes Eigenschaftenblatt eingefügt werden soll.
ms.assetid: 6623fe7e-e91d-49c7-9ad0-7791c178d12b
title: Eigenschaftenseite "Grundlegende Sicherheit"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8628b0b096e24a3a7baef94f5ab9913c2cd89825bb15bf6b19d18cd81d1033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783707"
---
# <a name="basic-security-property-page"></a>Eigenschaftenseite "Grundlegende Sicherheit"

Die Eigenschaftenseite "Grundlegende Sicherheit" ist die Startseite des Eigenschaftenblatts, das von der [**Funktion EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity) angezeigt wird. Sie können auch die [**CreateSecurityPage-Funktion**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) verwenden, um eine grundlegende Sicherheitseigenschaftenseite zu erstellen, die in Ihr eigenes Eigenschaftenblatt eingefügt werden soll.

Auf der Eigenschaftenseite wird eine Liste der Vertrauensnehmer angezeigt, die in den [*Zugriffssteuerungseinträgen (ACEs)*](/windows/desktop/SecGloss/a-gly) der [*DACL (Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) des Objekts benannt sind. [](trustees.md) Die Seite enthält auch eine Liste der Zugriffsrechte, die vom -Objekt unterstützt werden. Wenn der Benutzer einen Namen aus der Liste der Vertrauensnehmer auswählt, geben die Kontrollkästchen neben jedem Zugriffsrecht die Rechte an, die für diesen Vertrauensnehmer zugelassen oder verweigert werden. Der Benutzer kann dann die Kontrollkästchen aktivieren oder deaktivieren, um die Zugriffsrechte des Vertrauensnehmers zu ändern. Der Benutzer kann der Liste auch Vertrauensnehmer hinzufügen oder daraus entfernen.

Auf der Eigenschaftenseite "Grundlegende Sicherheit" können keine komplexen ACEs wie [objektspezifische ACEs](object-specific-aces.md)oder ACE-Vererbungsinformationen angezeigt werden. Damit der Benutzer solche Informationen anzeigen oder bearbeiten kann, können Sie eine Schaltfläche **Erweitert** auf der Seite "Grundlegende Sicherheit" einfügen. Der Benutzer kann auf die Schaltfläche **Erweitert** klicken, um ein [erweitertes Sicherheitseigenschaftenblatt](advanced-security-property-sheet.md)anzuzeigen. Dieses Eigenschaftenblatt verfügt über Eigenschaftenseiten, mit denen der Benutzer die [*Systemzugriffssteuerungsliste*](/windows/desktop/SecGloss/s-gly) (SACL) des Objekts bearbeiten, den Besitzer des Objekts ändern oder die DACL des Objekts erweitert bearbeiten kann. Um die Schaltfläche **Erweitert** anzuzeigen, legen Sie das SI \_ ADVANCED-Flag in der [**SI OBJECT \_ \_ INFO-Struktur**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) fest, die von Ihrer [**ISecurityInformation::GetObjectInformation-Implementierung**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) zurückgegeben wird.

Sie können den **PszPageTitle-Member** der [**SI OBJECT \_ \_ INFO-Struktur**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) verwenden, um den Titel der Eigenschaftenseite "Grundlegende Sicherheit" anzugeben. Der Standardtitel lautet **Sicherheit.**

 

 
