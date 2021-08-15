---
description: Im Folgenden finden Sie Informationen zu Optionen, die beim Anpassen von Desktop-App-Kacheln für Windows 8 zu berücksichtigen sind, z. B. zum Entwerfen von Desktop-App-Kacheln für die neue Startbildschirm und zum Auswählen der Einstiegspunkte, die in der Startbildschirm.
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

Im Folgenden finden Sie Informationen zu Optionen, die beim Anpassen von Desktop-App-Kacheln für Windows 8 zu berücksichtigen sind, z. B. zum Entwerfen von Desktop-App-Kacheln für die neue Startbildschirm und zum Auswählen der Einstiegspunkte, die in der Startbildschirm.

## <a name="design-your-tile-for-the-start-screen"></a>Entwerfen Sie Ihre Kachel für die Startbildschirm

Sie können zwei Aspekte Ihrer Desktop-App-Kacheln anpassen: den App-Namen und das Symbol. Die Hintergrundfarbe wird von der vom Benutzer gewählten Hintergrundfarbe abgeleitet und ist nicht programmgesteuert anpassbar.

![Anleitung zum Entwerfen von App-Kacheln.](images/tiles-desktop-1.png)

DO: Vermeiden Sie das Abschneiden des Anwendungsnamens. Desktopkacheln, die an die Startbildschirm angeheftet sind, können bis zu zwei Textzeilen pro Zeile oder etwa zehn Zeichen aufnehmen (obwohl dies von der Benutzeroberflächensprache abhängt). Versuchen Sie daher, den Anwendungsnamen kurz genug zu halten, um Kürzungen zu vermeiden.

DO: Geben Sie Symbole für die vier unterstützten Startbildschirm an, um sicherzustellen, dass Ihre Symbole bei allen Formfaktoren klar aussehen.



| Skalieren | Kachelgröße (in Pixel) | Verwendete Symbolgröße (in Pixel) |
|-------|-----------------------|----------------------------|
| 80 %   | 120 x 120             | 48 x 48                    |
| 100%  | 150 x 150             | 64 x 64                    |
| 140%  | 210 x 210             | 96 x 96                    |
| 180%  | 270 x 270             | 128 x 128                  |



 

DO: Nutzen Sie die Entwurfsprinzipien von Microsoft. Das neue Aussehen und Verhalten für Symbole ist flach. Wenn Sie also Windows Store App-Symbole für Ihre Desktop-App imitieren möchten, sollten Sie schlagschatten lassen und so weiter.

NICHT: Vermeiden Sie nicht die Verwendung von Farbe. Obwohl Windows Store App-Symbole manchmal monotone sind, empfehlen wir die Verwendung von Farbsymbolen für Desktop-Apps. Dies hilft, Desktopanwendungen auf der Taskleiste und von anderen Desktop-App-Kacheln im Startbildschirm zu unterscheiden, da die Hintergrundfarbe von Desktopkacheln nicht angepasst werden kann. Erwägen Sie die Verwendung von farbenerhättigten Farben.

## <a name="decide-the-right-entry-points-to-include-in-the-start-screen"></a>Entscheiden Sie sich für die richtigen Einstiegspunkte, die in die Startbildschirm

DO: Fügen Sie eine Verknüpfung pro App im Startbildschirm, wenn die App installiert wird. Dadurch wird sichergestellt, dass Benutzer Ihre App direkt über die Startbildschirm oder über die Suche starten können. Wenn Sie keine Verknüpfung in den Startbildschirm, wird es schwierig, Ihre App zu starten. Fügen Sie insbesondere keine Verknüpfung nur auf dem Desktop hinzu. Benutzer sehen die Startbildschirm, wenn sie sich zum ersten Mal anmelden. Daher ist es nicht so effektiv, eine Verknüpfung nur auf dem Desktop zu platzieren, als sie in die Startbildschirm.

![Diagramm, das das Raster mit einer Anwendungkachel, Dimensionen und "Segoe U I Semilight" zeigt, um die verwendete Schriftart anzugeben.](images/tiles-desktop-2.png)

NICHT: Stellen Sie nicht mehrere Verknüpfungen für dieselbe App zur Verfügung. Verfügen Sie beispielsweise nicht über zwei Tastenkombinationen, die eine App in zwei verschiedenen Modi starten, z. B. eine für Windows Internet Explorer und eine für Internet Explorer ohne Add-Ons.

DO: Minimieren Sie die Anzahl der Kacheln, die im Rahmen der Installation hinzugefügt werden. Erwägen Sie, andere Einstiegspunkte für die unnentsprichtigen Apps verfügbar zu machen. Anstatt z. B. eine separate Einstellungen-App mit einer Konsolen-App zu verwenden, greifen Sie über ein Feature in der Konsolen-App auf die Einstellungen zu.

NICHT: Verwenden Sie keine Verknüpfungen zu den folgenden Elementen auf dem Startbildschirm:

-   Deinstallationen. Benutzer können auf Deinstallationen über das Element Programme in der Systemsteuerung.
-   Hilfedateien. Schließen Sie Hilfethemen direkt in Ihre App ein.
-   App-Einstellungen und -Optionen. Fügen Sie die Benutzeroberfläche ein, um Einstellungen für eine App in der App zu konfigurieren oder ein Systemsteuerung zu erstellen.
-   Websites. Stellen Sie alle entsprechenden Links zu Informationen wie Hilfe- und technischen Support-Websites direkt in Ihrer App zur Verfügung.
-   Assistenten. Assistenten und andere einmalige Konfigurationsaufgaben sollten innerhalb der App gestartet werden.

NICHT: Erstellen Sie keine Verknüpfungen zu Features oder Funktionen, die aus der App selbst gestartet werden können. Beispielsweise kann Language Einstellungen aus jeder Microsoft Office-App konfiguriert werden, sodass es nicht erforderlich ist, auch einen separaten Einstellungen-Einstiegspunkt auf dem Startbildschirm.

NICHT: Erstellen Sie keine Verknüpfungen zu Elementen, die keine ausführbaren Dateien sind. Verknüpfungen, die nicht ausführbaren Dateien wie Verknüpfungen zum Starten von Websites oder Hilfedateien zuordnen, werden aus dem Startbildschirm.

DO: Wenn Sie eine Suite von Apps statt einer einzelnen App installieren, fügen Sie für jede App in der Suite eine Verknüpfung hinzu. Vermeiden Sie wie oben erwähnt das Erstellen von Verknüpfungen mit sekundären Funktionen wie Hilfeinformationen, Hilfsprogrammen und Einstellungen. Diese Funktionalität sollte in den relevanten Apps der Suite enthalten sein.

DO: Erstellen Sie einen Produktordner auf einer ebene für Sammlungen, die drei oder mehr Kacheln enthalten. In der Ansicht Apps der Startbildschirm, auf die über den Charm Suchen zugegriffen werden kann, werden Anwendungen nach ihrem Ordner der obersten Ebene gruppiert. Wählen Sie einen aussagekräftigen, aber präzisen Ordnernamen aus. Es werden drei Wörter oder weniger empfohlen. Beachten Sie, dass dieser Name nicht sichtbar ist, wenn eine Kachel an die Startbildschirm angeheftet wird, sodass Ihre Kachelnamen ausreichend beschreibend sind, während die Ansicht Apps Kacheln auflistet und den Ordnernamen zeigt.

NICHT: Erstellen Sie keinen Produktordner, wenn Ihre Suite nur eine einzige Verknüpfung enthält. Platzieren Sie die Verknüpfung im Ordner Start der obersten Ebene.

DO: Wenn Sie eine Suite mit mehr als drei Apps installieren, sollten Sie überlegen, ob eine dieser Apps für sekundäre, unregelmäßigere Verwendung geeignet ist und nicht an die Startbildschirm. Falls ja, können diese Kacheln gemäß der obigen Anleitung vollständig entfernt und aus einer primären App heraus gestartet werden. Wenn Sie die Kacheln nicht entfernen können, ziehen Sie in Betracht, sie aus dem Startbildschirm. Auf diese Weise werden die Tastenkombinationen weiterhin in der Ansicht Alle **Apps** angezeigt, sind aber nicht unübersichtlich für Startbildschirm.

Um eine App-Verknüpfung hinzuzufügen, ohne sie an den Startbildschirm zu heften, legen Sie die folgende Eigenschaft für die Verknüpfung fest: System.AppUserModel.StartPinOption = 1. Der symbolische Name für 1 ist APPUSERMODEL \_ STARTPINOPTION \_ NOPINONINSTALL.

Dadurch wird verhindert, dass die Verknüpfung auf dem Startbildschirm angezeigt wird, sie kann jedoch weiterhin in der Ansicht Alle **Apps** und in den Suchergebnissen angezeigt werden. Nur der Benutzer kann vorhandene Verknüpfungen entfernen, daher müssen Sie diese Eigenschaft während der Installation oder unmittelbar nach dem Platzieren der App auf dem Datenträger festlegen.

NICHT: Erstellen Sie keine Kachel für einen Host oder eine Runtime für Anwendungen wie Silverlight oder Java. Stellen Sie einen Einstiegspunkt zum Deinstallieren des Frameworks in "Programme hinzufügen/entfernen" und einen beliebigen Einstellungseinstiegspunkt in Systemsteuerung.

 

 



