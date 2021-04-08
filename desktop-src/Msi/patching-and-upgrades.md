---
description: Da ein Installationspaket die Dateien, aus denen eine Anwendung besteht, sowie die für die Installation benötigten Informationen enthalten kann, können Windows Installer zum Aktualisieren der Anwendung verwendet werden.
ms.assetid: da946739-9efc-4bf0-8a9a-6f6ead3c4a34
title: Patchen und Upgrades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cee185461ac14c8eac336a5af0c1315eb5e027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959800"
---
# <a name="patching-and-upgrades"></a>Patchen und Upgrades

Da ein Installationspaket die Dateien, aus denen eine Anwendung besteht, sowie die für die Installation benötigten Informationen enthalten kann, können Windows Installer zum Aktualisieren der Anwendung verwendet werden. Der Installer kann die Informationen in den folgenden Teilen des Installationspakets aktualisieren:

-   Die MSI-Datei.
-   Die Dateien der Anwendung.
-   Die Windows Installer Registrierungsinformationen.

Der Typ des Updates kann durch die Änderungen gekennzeichnet werden, die das Update an den Produktcode, die Produktversion und den Paketcode der Anwendung vornimmt. Die Produktversion der Anwendung wird in der [**ProductVersion**](productversion.md) -Eigenschaft gespeichert. Der Produktcode der Anwendung wird in der [**ProductCode**](productcode.md) -Eigenschaft gespeichert. Der [Paketcode](package-codes.md) der Anwendung wird in der [**Zusammenfassungs Eigenschaft "Revisionsnummer**](revision-number-summary.md) " gespeichert.

Ein Update, das die Anwendung in ein anderes Produkt ändert, ist erforderlich, um den [**ProductCode**](productcode.md) der Anwendung zu ändern. Weitere Informationen dazu, welche Updates das Ändern von **ProductCode** erfordern, finden Sie [unter Ändern des Produktcodes](changing-the-product-code.md). Das Update kann die [**ProductVersion**](productversion.md) ändern und den **ProductCode** unverändert lassen, wenn in zukünftigen Versionen der Anwendung zwischen den aktualisierten und nicht aktualisierten Versionen des aktuellen Produkts unterschieden werden muss. Der [Paket Code](package-codes.md) identifiziert das Installationspaket eindeutig und sollte immer geändert werden, wenn bei Update oder Upgrade alle Informationen im Installationspaket geändert werden.

Bei der Entscheidung, ob die Produktversion geändert werden soll, sollten Sie überlegen, ob zukünftige Versionen der Anwendung zwischen den aktualisierten und nicht aktualisierten Versionen des aktuellen Produkts unterscheiden müssen. Um die Differenzierung in Zukunft zu gewährleisten, sollte anstelle eines [kleinen Updates](small-updates.md)ein [kleineres Upgrade](minor-upgrades.md) verwendet werden.

-   Wenn die MSI-Datei und die Anwendungs Dateien von einem Update geändert werden, die [**ProductCode**](productcode.md) -Eigenschaft oder die [**ProductVersion**](productversion.md) -Eigenschaft jedoch nicht geändert wird, wird Sie als [kleines Update](small-updates.md)bezeichnet.
-   Wenn das Update die [**ProductVersion**](productversion.md)ändert, der [**ProductCode**](productcode.md)jedoch nicht geändert wird, wird es als [geringfügige Aktualisierung](minor-upgrades.md)bezeichnet.
-   Wenn die Installation des Updates in ein völlig anderes Produkt geändert wird, muss sich der [**ProductCode**](productcode.md) ändern, und das Update wird als [großes Upgrade](major-upgrades.md)bezeichnet.

> [!Note]  
> Um die Differenzierung von Versionen des aktuellen Produkts in Zukunft zu gewährleisten, sollte anstelle eines [kleinen Updates](small-updates.md)ein [kleineres Upgrade](minor-upgrades.md) verwendet werden.

 

In der folgenden Tabelle werden die verschiedenen Update Typen zusammengefasst.



| Art des Updates                       | ProductCode | ProductVersion | BESCHREIBUNG                                                                                                                                                                                                                                                                                                           |
|--------------------------------------|-------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Kleines Update](small-updates.md)    | Keine Änderung   | Keine Änderung      | Ein Update für eine oder zwei Dateien, die zu klein sind, um das Ändern der [**ProductVersion**](productversion.md)zu rechtfertigen. Der Paketcode in der [**Zusammenfassungs Eigenschaft der Revisionsnummer**](revision-number-summary.md) ändert sich. Kann als vollständiges Installationspaket oder als [Patchpaket](patch-packages.md)ausgeliefert werden. |
| [Geringfügige Aktualisierung](minor-upgrades.md)  | Keine Änderung   | Geändert        | Ein kleines Update, das Änderungen erheblich macht, um das Ändern der [**ProductVersion**](productversion.md) -Eigenschaft zu rechtfertigen. Kann als vollständiges Installationspaket oder als [Patchpaket](patch-packages.md)ausgeliefert werden.                                                                                                |
| [Wichtige Upgrades](major-upgrades.md) | Geändert     | Geändert        | Ein umfassendes Update des Produkts, das eine Änderung in der [**ProductCode**](productcode.md) -Eigenschaft garantiert. Als [Patchpaket](patch-packages.md) oder als vollständiges Produkt Installationspaket ausgeliefert.                                                                                                             |



 

> [!Note]  
> Der Windows Installer kann eine Anwendung oder ein Update für alle Benutzer eines Computers (Computer bezogen) oder für einen bestimmten Benutzer (kontextbezogen), abhängig von den Zugriffsberechtigungen des Benutzers, dem Wert der Eigenschaft " [**ALLUSERS**](allusers.md) " und der Version des Betriebssystems installieren. Anwendungsentwickler sollten in Erwägung gezogen werden, in welchen Kontext Updates installiert werden. Wenn sich die Kontexte der Anwendung und des Updates unterscheiden, wird die Anwendung möglicherweise nicht erwartungsgemäß aktualisiert.

 

Benutzer können ein Update auf eine Anwendung durch erneutes Installieren eines Windows Installer Pakets für die Anwendung durchsetzen. Beachten Sie, dass [kleinere Upgrades](minor-upgrades.md) auf die gleiche Weise wie bei [kleinen Updates](small-updates.md)angewendet werden können. Weitere Informationen zum Aktualisieren einer Anwendung durch eine Neuinstallation der Anwendung finden Sie in den folgenden Abschnitten:

-   [Anwenden von kleinen Updates durch Neuinstallation des Produkts](applying-small-updates-by-reinstalling-the-product.md)
-   [Anwenden von größeren Upgrades durch Installieren des Produkts](applying-major-upgrades-by-installing-the-product.md)

Ein Update für eine Anwendung kann Benutzern als Windows Installer Patch-Paket bereitgestellt werden. Ein Patch kann eine vollständige Datei oder nur die Datei Bits enthalten, die erforderlich sind, um einen Teil einer Datei zu aktualisieren. Dies bedeutet, dass der Benutzer einen Upgradepatch herunterladen kann, der wesentlich kleiner als das gesamte Produkt ist, und der Benutzeranpassungen durch das Upgrade beibehält. Beachten Sie, dass [kleinere Upgrades](minor-upgrades.md) auf die gleiche Weise wie bei [kleinen Updates](small-updates.md)angewendet werden können. Weitere Informationen zum Aktualisieren einer Anwendung mithilfe eines Patches finden Sie in den folgenden Abschnitten:

-   [Patchen](patching.md)
-   [Erstellen eines kleinen Update-Patches](creating-a-small-update-patch.md)
-   [Anwenden von kleinen Updates durch Patchen der lokalen Installation des Produkts](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
-   [Anwenden von kleinen Updates durch Patchen eines administrativen Abbilds](applying-small-updates-by-patching-an-administrative-image.md)
-   [Anwenden von größeren Upgrades durch Patchen der lokalen Installation des Produkts](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)

 

 



