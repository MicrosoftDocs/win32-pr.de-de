---
description: Die Startseite des Eigenschaften Blatts, das von der EditSecurity-Funktion angezeigt wird. Sie können auch die Funktion "kreatesecuritypage" verwenden, um eine grundlegende Sicherheitseigenschaften Seite zu erstellen, die in Ihr eigenes Eigenschaften Blatt eingefügt werden kann.
ms.assetid: 6623fe7e-e91d-49c7-9ad0-7791c178d12b
title: Grundlegende Sicherheit (Eigenschaften Seite)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f839058d8cd9c9a4c9d1a20dab96620d1e731d23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130421"
---
# <a name="basic-security-property-page"></a>Grundlegende Sicherheit (Eigenschaften Seite)

Die Eigenschaften Seite grundlegende Sicherheit ist die Startseite des Eigenschaften Blatts, das von der [**EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity) -Funktion angezeigt wird. Sie können auch die Funktion " [**kreatesecuritypage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) " verwenden, um eine grundlegende Sicherheitseigenschaften Seite zu erstellen, die in Ihr eigenes Eigenschaften Blatt eingefügt werden kann.

Auf der Eigenschaften Seite wird eine Liste der [Treuhänder](trustees.md) angezeigt, die in den [*Zugriffs Steuerungs Einträgen (Access Control Entries*](/windows/desktop/SecGloss/a-gly) , ACEs) der [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) des Objekts benannt sind. Die Seite enthält außerdem eine Liste der Zugriffsrechte, die vom-Objekt unterstützt werden. Wenn der Benutzer einen Namen aus der Liste der Vertrauens nehmer auswählt, geben die Kontrollkästchen neben den einzelnen Zugriffsrechten die Rechte an, die für den Vertrauens nehmer zugelassen oder verweigert werden. Der Benutzer kann dann die Kontrollkästchen aktivieren oder deaktivieren, um die Zugriffsrechte des Vertrauens nehmers zu ändern. Der Benutzer kann auch Treuhänder in der Liste hinzufügen oder entfernen.

Auf der Eigenschaften Seite grundlegende Sicherheit können keine komplexen ACEs angezeigt werden, z. b. [objektspezifische ACEs](object-specific-aces.md)oder ACE-Vererbungs Informationen. Um dem Benutzer zu ermöglichen, solche Informationen anzuzeigen oder zu bearbeiten, können Sie eine Schaltfläche " **erweitert** " auf der Seite "grundlegende Sicherheit" einschließen. Der Benutzer kann auf die Schaltfläche **erweitert** klicken, um ein [Eigenschaften Blatt für die erweiterte Sicherheit](advanced-security-property-sheet.md)anzuzeigen. Dieses Eigenschaften Blatt verfügt über Eigenschaften Seiten, die es dem Benutzer ermöglichen, die [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL) des Objekts zu bearbeiten, den Besitzer des Objekts zu ändern oder eine erweiterte Bearbeitung der DACL des Objekts auszuführen. Um die Schaltfläche **erweitert** anzuzeigen, legen Sie das Flag "Si \_ Advanced" in der Si-Objekt Informationsstruktur fest, die von Ihrer [**ISecurityInformation:: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) -Implementierung zurückgegeben wurde. [**\_ \_**](/windows/desktop/api/Aclui/ns-aclui-si_object_info)

Sie können den **pszpagetitle** -Member der [**Si- \_ Objekt \_ Informations**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) Struktur verwenden, um den Titel der Standard-Sicherheitseigenschaften Seite anzugeben. Der Standard Titel ist **Sicherheit**.

 

 
