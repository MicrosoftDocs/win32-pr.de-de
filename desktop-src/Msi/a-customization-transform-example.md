---
description: In diesem Beispiel wird veranschaulicht, wie eine Anpassungs Transformation verwendet werden kann, um Funktionen zu deaktivieren und neue Ressourcen hinzuzufügen.
ms.assetid: 028b1d01-3b66-4640-98f9-ca33f90ca516
title: Beispiel für eine Anpassungs Transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ea655d1187b0271aba7ea56a46bacf95f5fb40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367887"
---
# <a name="a-customization-transform-example"></a>Beispiel für eine Anpassungs Transformation

In diesem Beispiel wird veranschaulicht, wie eine Anpassungs Transformation verwendet werden kann, um Funktionen zu deaktivieren und neue Ressourcen hinzuzufügen.

Ein Administrator kann eine Funktion dauerhaft deaktivieren, indem eine Anpassungs Transformation verwendet wird, um eine 0 in die Spalte Ebene der [Funktions Tabelle](feature-table.md)einzugeben. Die Anwendung der Anpassungs Transformation verhindert dann die Installation und Anzeige dieses Features, auch wenn der Benutzer eine vollständige Installation über die Benutzeroberfläche auswählt oder die Eigenschaft [**ADDLOCAL**](addlocal.md) in der Befehlszeile auf alle festgelegt hat. Eine Erläuterung der Installations Ebene finden Sie unter [Featuretabelle](feature-table.md) und [**INSTALLLEVEL**](installlevel.md) -Eigenschaft.

Die zum Anpassen einer Anwendung benötigten Ressourcen können mithilfe einer Anpassungs Transformation bereitgestellt werden, um eine oder mehrere neue Komponenten hinzuzufügen. Die Transformation muss eine oder mehrere neue Features hinzufügen, die diese neuen Komponenten enthalten. Informationen zu den Regeln, die beim Bereitstellen von Ressourcen wie Dateien, Registrierungs Schlüsseln oder Verknüpfungen befolgt werden sollten, finden Sie unter [Verwenden von Transformationen zum Hinzufügen von Ressourcen](using-transforms-to-add-resources.md).

In diesem Beispiel wird veranschaulicht, wie eine [Transformation](transforms.md) erstellt wird, um die Installation der in [einem Installations Beispiel](an-installation-example.md)beschriebenen Anwendung anzupassen. Das ursprüngliche Installationspaket installiert alle Features der Beispielanwendung, einschließlich des featuretors, das Benutzern ermöglicht, Eintritts Informationen für die rote Park-Arena anzuzeigen. Einige Benutzergruppen benötigen nur die Anwendungs Features, die Informationen zur Ereignis Planung enthalten, und benötigen die Gate-Funktion nicht. Diese Gruppen müssen auch eine spezielle Telefonliste erhalten. Die Transformation muss daher zwei Dinge tun: 1) passen Sie die Installation so an, dass diese Gruppe nur die benötigten Anwendungs Features erhält und 2) die erforderlichen Ressourcen für die neue Telefonliste bereitstellen.

Ein Beispiel für eine minimale Benutzeroberfläche für dieses Beispiel wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md) als Datei Uisample.msi bereitgestellt. Wenn Sie über das SDK verfügen, haben Sie Zugriff auf alle Tools und Daten, die erforderlich sind, um das Beispiel Installationspaket, die Benutzeroberfläche und die Anpassungs Transformation zu reproduzieren.

Die Anpassungs Transformation verfügt über die folgenden Spezifikationen:

-   Die Anpassungs Transformation ist in die MNP2000.msi Datei eingebettet, um sicherzustellen, dass Sie immer mit der Installations Datenbank verfügbar ist.
-   Wenn Sie MNP2000.msi mit der Anpassungs Transformation installieren, werden das Gate-Feature, die untergeordneten Funktionen der Gate-Funktion oder eine der Komponenten der Gate-Funktion nicht installiert, auch wenn der Benutzer den gesamten Installationstyp auswählt.
-   Andere Anwendungen können einige oder alle Komponenten des Gate-Features gemeinsam nutzen. Die Installationspakete dieser Anwendungen können alle Komponenten auf dem Computer des Benutzers installieren.
-   Wenn Sie MNP2000.msi mit der Anpassungs Transformation entfernen, werden keine der von anderen Anwendungen installierten Gate-Komponenten entfernt.
-   Wenn Sie MNP2000.msi mit der Anpassungs Transformation installieren, werden auch ein neues Feature der obersten Ebene, die Telefon \_ Liste und eine neue Komponente (Telefon) installiert, für die die Installation der Ressource Phone.txt erforderlich ist. Der Benutzer greift \_ über eine Verknüpfung im Menü Verzeichnis auf das Feature "Telefonliste" zu.

[Fortsetzen](customizing-an-original-database.md)

 

 



