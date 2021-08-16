---
description: Im Folgenden finden Sie Informationen zu den Optionen, die beim Anpassen von Desktop-App-Kacheln für Windows 8 berücksichtigt werden müssen, einschließlich des Entwurfs von Desktop-App-Kacheln für die neue Startbildschirm und der Auswahl der Einstiegspunkte, die in der Startbildschirm angezeigt werden sollen.
ms.assetid: EF5182A2-09B2-46F2-B55E-4BD212CC1F7F
title: Desktop-App-Kacheln auf dem Startbildschirm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44ed35bd5c8405301e872ef54774914d625e1fc06c6a9fc3c26965e130301eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861221"
---
# <a name="desktop-app-tiles-on-the-start-screen"></a>Desktop-App-Kacheln auf dem Startbildschirm

Im Folgenden finden Sie Informationen zu den Optionen, die beim Anpassen von Desktop-App-Kacheln für Windows 8 berücksichtigt werden müssen, einschließlich des Entwurfs von Desktop-App-Kacheln für die neue Startbildschirm und der Auswahl der Einstiegspunkte, die in der Startbildschirm angezeigt werden sollen.

## <a name="design-your-tile-for-the-start-screen"></a>Entwerfen Der Kachel für die Startbildschirm

Sie können zwei Aspekte Ihrer Desktop-App-Kacheln anpassen: den App-Namen und das Symbol. Die Hintergrundfarbe wird von der ausgewählten Hintergrundfarbe des Benutzers abgeleitet und ist nicht programmgesteuert anpassbar.

![Leitfaden zum Entwerfen von App-Kacheln.](images/tiles-desktop-1.png)

DO: Vermeiden Sie das Abschneiden Ihres Anwendungsnamens. Desktopkacheln, die an die Startbildschirm angeheftet sind, können bis zu zwei Textzeilen pro Zeile oder etwa zehn Zeichen aufnehmen (obwohl dies von der Benutzeroberflächensprache abhängt). Versuchen Sie daher, den Anwendungsnamen kurz genug zu halten, um abgeschnittene Daten zu vermeiden.

DO: Geben Sie Symbole für die vier unterstützten Startbildschirm Skalierungswerte an, um sicherzustellen, dass Ihre Symbole für alle Formfaktoren präzise aussehen.



| Skalieren | Kachelgröße (in Pixel) | Verwendete Symbolgröße (in Pixel) |
|-------|-----------------------|----------------------------|
| 80 %   | 120 x 120             | 48 x 48                    |
| 100 %  | 150 x 150             | 64 x 64                    |
| 140%  | 210 x 210             | 96 x 96                    |
| 180%  | 270 x 270             | 128 x 128                  |



 

DO: Nutzen Sie die Microsoft-Entwurfsprinzipien. Das neue Aussehen und Aussehen von Symbolen ist flach. Wenn Sie also Windows Store App-Symbole für Ihre Desktop-App imitieren möchten, ziehen Sie in Betracht, Fallschatten zu erstellen usw.

NICHT: Vermeiden Sie nicht die Verwendung von Farben. Während Windows Store App-Symbole manchmal monokolonisch sind, empfehlen wir die Verwendung von Farbsymbolen für Desktop-Apps. Dadurch können Desktopanwendungen auf der Taskleiste und von anderen Desktop-App-Kacheln im Startbildschirm unterschieden werden, da die Hintergrundfarbe von Desktopkacheln nicht angepasst werden kann. Erwägen Sie die Verwendung von stärker überlasteten Farben.

## <a name="decide-the-right-entry-points-to-include-in-the-start-screen"></a>Entscheiden Sie die richtigen Einstiegspunkte, die in die Startbildschirm

DO: Fügen Sie eine Verknüpfung pro App im Startbildschirm hinzu, wenn die App installiert ist. Dadurch wird sichergestellt, dass Benutzer Ihre App direkt über die Startbildschirm oder über die Suche starten können. Wenn Sie keine Verknüpfung in den Startbildschirm einfügen, ist ihr Start schwierig. Fügen Sie insbesondere keine Verknüpfung nur auf dem Desktop hinzu. Benutzer sehen die Startbildschirm, wenn sie sich zum ersten Mal anmelden. Daher ist es nicht so effektiv, eine Verknüpfung nur auf dem Desktop zu platzieren, als sie in die Startbildschirm einzuschlussen.

![Diagramm, das das Raster mit einer Anwendungkachel, Dimensionen und "Segoe U I Semilight" zeigt, um die verwendete Schriftart anzugeben.](images/tiles-desktop-2.png)

NICHT: Stellen Sie nicht mehrere Verknüpfungen für dieselbe App bereit. Verwenden Sie beispielsweise keine zwei Tastenkombinationen, die eine App in zwei verschiedenen Modi starten, z. B. eine für Windows Internet Explorer und eine für Internet Explorer ohne Add-Ons.

DO: Minimieren Sie die Anzahl der Kacheln, die im Rahmen der Installation hinzugefügt werden. Erwägen Sie, andere Einstiegspunkte für die überflüssigen Apps verfügbar zu machen. Anstatt z. B. eine separate Einstellungen-App mit einer Konsolen-App zu verwenden, greifen Sie über ein Feature in der Konsolen-App auf die Einstellungen zu.

NICHT: Setzen Sie keine Verknüpfungen zu den folgenden Elementen auf dem Startbildschirm:

-   Deinstallationen. Benutzer können über das Element Programme im Systemsteuerung auf Deinstallationen zugreifen.
-   Hilfedateien. Fügen Sie Hilfethemen direkt in Ihre App ein.
-   App-Einstellungen und -Optionen. Schließen Sie die Benutzeroberfläche ein, um Einstellungen für eine App innerhalb der App zu konfigurieren, oder erstellen Sie ein Systemsteuerung Element.
-   Websites. Stellen Sie geeignete Links zu Informationen wie Hilfe- und technischen Supportwebsites direkt in Ihrer App bereit.
-   Assistenten. Assistenten und andere einmalige Konfigurationsaufgaben sollten innerhalb der App gestartet werden.

NICHT: Erstellen Sie keine Verknüpfungen zu Features oder Funktionen, die innerhalb der App selbst gestartet werden können. Beispielsweise kann Language Einstellungen von jeder Microsoft Office-App konfiguriert werden, sodass es nicht erforderlich ist, auch einen separaten Language Einstellungen-Einstiegspunkt auf dem Startbildschirm zu haben.

NICHT: Erstellen Sie keine Verknüpfungen zu Elementen, die keine ausführbaren Dateien sind. Verknüpfungen, die nicht ausführbaren Dateien zugeordnet sind, z. B. Verknüpfungen, die Websites oder Hilfedateien starten, werden aus dem Startbildschirm herausgefiltert.

DO: Wenn Sie eine Suite von Apps anstelle einer einzelnen App installieren, fügen Sie eine Verknüpfung für jede App in der Suite hinzu. Vermeiden Sie wie oben erwähnt das Erstellen von Verknüpfungen mit sekundären Funktionen wie Hilfeinformationen, Hilfsprogrammen und Einstellungen. Diese Funktionalität sollte in den relevanten Apps der Suite enthalten sein.

DO: Erstellen Sie einen Einebenen-Produktordner für Sammlungen, die drei oder mehr Kacheln enthalten. In der Ansicht Apps des Startbildschirm, auf das über den Search-Charm zugegriffen werden kann, werden Anwendungen nach ihrem Ordner der obersten Ebene gruppiert. Wählen Sie einen beschreibenden, aber präzisen Ordnernamen aus. es werden drei oder weniger Wörter empfohlen. Beachten Sie, dass in der Ansicht Apps Kacheln gruppiert und der Ordnername angezeigt wird, dieser Name jedoch nicht sichtbar ist, wenn eine Kachel an die Startbildschirm angeheftet ist. Machen Sie die Namen Ihrer Kacheln daher ausreichend beschreibend.

NICHT: Erstellen Sie keinen Produktordner, wenn Ihre Suite nur eine einzige Verknüpfung enthält. Platzieren Sie Ihre Verknüpfung im Ordner Start der obersten Ebene.

DO: Berücksichtigen Sie bei der Installation einer Suite mit mehr als drei Apps, ob eine dieser Apps für die sekundäre, unregelmäßigere Verwendung vorgesehen ist und nicht an die Startbildschirm angeheftet werden sollte. Wenn ja, können diese Kacheln möglicherweise gemäß den obigen Anweisungen vollständig entfernt und innerhalb einer primären App gestartet werden. Wenn Sie die Kacheln nicht entfernen können, sollten Sie sie aus dem Startbildschirm entfernen. Auf diese Weise werden die Tastenkombinationen weiterhin in der Ansicht **Alle Apps** angezeigt, aber die Startbildschirm des Benutzers sind nicht überladen.

Um eine App-Verknüpfung hinzuzufügen, ohne sie an die Startbildschirm anzuheften, legen Sie die folgende Eigenschaft für die Verknüpfung fest: System.AppUserModel.StartPinOption = 1. Der symbolische Name für 1 lautet APPUSERMODEL \_ STARTPINOPTION \_ NOCHILDNINSTALL.

Dadurch wird verhindert, dass die Verknüpfung auf dem Startbildschirm angezeigt wird, aber sie kann weiterhin in der Ansicht **Alle Apps** und in den Suchergebnissen angezeigt werden. Nur der Benutzer kann vorhandene Verknüpfungen lösen. Daher müssen Sie diese Eigenschaft während der Installation oder unmittelbar nach dem Platzieren der App auf dem Datenträger festlegen.

NICHT: Erstellen Sie keine Kachel für einen Host oder eine Runtime für Anwendungen wie Silverlight oder Java. Geben Sie unter Software einen Einstiegspunkt zum Deinstallieren des Frameworks an, und geben Sie einen beliebigen Einstellungseinstiegspunkt in Systemsteuerung an.

 

 



