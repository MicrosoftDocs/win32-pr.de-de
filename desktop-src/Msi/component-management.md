---
description: Durch die Windows Installer werden die Gesamtbetriebskosten (TCO) Ihrer Anwendungen reduziert, indem die Kunden die Verwaltung und Wartung von Anwendungskomponenten während des Setups und der Laufzeit erhöhen.
ms.assetid: fbb139e3-c81b-44fc-9e92-bada0be02862
title: Verwaltung von Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeff6c25556879429330170ec8190b1296576517
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363566"
---
# <a name="component-management"></a>Verwaltung von Komponenten

Durch die Windows Installer werden die Gesamtbetriebskosten (TCO) Ihrer Anwendungen reduziert, indem die Kunden die Verwaltung und Wartung von Anwendungskomponenten während des Setups und der Laufzeit erhöhen. Die-Installations Datenbank verfolgt, welche Anwendungen eine bestimmte Komponente erfordern, welche Dateien die einzelnen Komponenten enthalten, wo jede Datei auf dem System installiert ist und wo sich die Quell Komponenten befinden. Dies ermöglicht es Entwicklern, Pakete zu erstellen, die die folgenden Vorteile bieten:

-   Höhere Resilienz von Anwendungen. Verwenden Sie das Installationsprogramm, um beschädigte Komponenten zu erkennen und neu zu installieren, ohne Setup erneut ausführen zu müssen. Das Installationsprogramm überprüft den Pfad einer Komponente zur Laufzeit. Dadurch werden Anwendungen von der Abhängigkeit von statischen Dateipfaden befreit, die sich häufig zwischen den Computern unterscheiden und auf fehlende Komponenten verweisen können. Weitere Informationen finden Sie unter [Resilienz](resiliency.md).
-   Installation nach Bedarf. Diese Featuregruppe wird nicht während des Setups installiert, sondern in der Datenbank so angegeben, dass Sie Just-in-Time zur Verwendung installiert werden soll, wenn Sie in Zukunft von der Anwendung benötigt wird. Benutzer müssen das Setup nicht erneut ausführen. Weitere Informationen finden Sie unter [Installation bei Bedarf](installation-on-demand.md).
-   Ankündigung von Verknüpfungen zu Features, Anwendungen oder ganzen Produkten in der Benutzeroberfläche. Benutzer können diese Bedarfs gesteuert mithilfe der Tastenkombinationen installieren. Benutzer können Features, Anwendungen oder gesamte Produkte auch Bedarfs gesteuert entfernen. Weitere Informationen finden Sie unter [Ankündigung.](advertisement.md)
-   Installations Anpassung. Ein Administrator kann Transformationen auf die Datenbank anwenden, die die Installation für eine bestimmte Benutzergruppe anpassen. Weitere Informationen finden Sie unter [Anpassung](customization.md).
-   Einfachere Bereitstellung von Anwendungs Updates. Verwenden Sie das Installationsprogramm, um Ihre Produkte zu aktualisieren. Weitere Informationen finden Sie unter [Patching und Upgrades](patching-and-upgrades.md).
-   Featureverknüpfungs Anzeige. Der Installer zeigt Verknüpfungen zu Features an, die lokal mit Verknüpfungen zu Features ausgeführt werden, die Remote ausgeführt werden. Da in der Installations Datenbank der Lauf Kontext der einzelnen Features angegeben ist, können Benutzern nach Bedarf sichtbar äquivalente Einstiegspunkte angezeigt werden.
-   Behalten Sie nutzungsmetriken für Features bei. Entwickler können ein Installationspaket bereitstellen, das die Verwendungs Anzahl eines Features von allen Client Anwendungen beibehält und nicht verwendete Komponenten entfernt.
-   Integrieren Sie-Installationen. Entwickler können die Komponenten Verwaltungsfunktionen des Installers in Ihre Anwendungen integrieren, indem Sie ein Installationspaket erstellen und die [installerfunktionen](installer-functions.md) in Ihrem Anwendungscode verwenden. In der folgenden Abbildung wird eine Anwendung veranschaulicht, die die Installation eines Features anfordert.

    ![Anwendung, die Funktions Installation anfordert. ](images/over1.png)

 

 



