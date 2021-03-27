---
description: Im folgenden finden Sie Informationen zu den Optionen, die beim Anpassen von Desktop-App-Kacheln für Windows 8 zu beachten sind. dazu zählen das Entwerfen von Desktop-App-Kacheln für den neuen Startbildschirm und das Auswählen der Einstiegspunkte, die auf dem Startbildschirm
ms.assetid: EF5182A2-09B2-46F2-B55E-4BD212CC1F7F
title: Desktop-App-Kacheln auf dem Start Bildschirm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fcc5475732926300e2125ae9e97ea2d188bc468
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "104350979"
---
# <a name="desktop-app-tiles-on-the-start-screen"></a>Desktop-App-Kacheln auf dem Start Bildschirm

Im folgenden finden Sie Informationen zu den Optionen, die beim Anpassen von Desktop-App-Kacheln für Windows 8 zu beachten sind. dazu zählen das Entwerfen von Desktop-App-Kacheln für den neuen Startbildschirm und das Auswählen der Einstiegspunkte, die auf dem Startbildschirm

## <a name="design-your-tile-for-the-start-screen"></a>Entwerfen der Kachel für den Start Bildschirm

Sie können zwei Aspekte Ihrer Desktop-App-Kacheln anpassen: den APP-Namen und das Symbol. Die Hintergrundfarbe wird von der ausgewählten Hintergrundfarbe des Benutzers abgeleitet und kann nicht Programm gesteuert angepasst werden.

![Entwurfs Leit Faden für App-Kacheln](images/tiles-desktop-1.png)

Do: vermeiden Sie das Abschneiden des Anwendungs namens. Desktop Kacheln, die an den Start Bildschirm angeheftet sind, können bis zu zwei Zeilen Text in jeder Zeile oder ungefähr zehn Zeichen umfassen (obwohl dies von der Benutzeroberflächen Sprache abhängt). Daher sollten Sie versuchen, den Anwendungsnamen so kurz wie möglich zu halten, um das Abschneiden zu vermeiden.

Do: Stellen Sie Symbole für die vier unterstützten Start Bildschirm-Skalierungs Werte bereit, um sicherzustellen, dass Ihre Symbole für alle Formfaktoren kurz aussehen.



| Skalieren | Kachel Größe (in Pixel) | Verwendete Symbolgröße (in Pixel) |
|-------|-----------------------|----------------------------|
| 80 %   | 120 x 120             | 48 x 48                    |
| 100 %  | 150 x 150             | 64 x 64                    |
| 140%  | 210 x 210             | 96 x 96                    |
| 180%  | 270 x 270             | 128 x 128                  |



 

Do: akzeptieren Sie die Entwurfs Prinzipien von Microsoft. Das neue Erscheinungsbild für Symbole ist flach. Wenn Sie also Symbole für Windows Store-Apps für Ihre Desktop-App imitieren möchten, sollten Sie Schlag Schatten usw. in Erwägung ziehen.

Nicht: vermeiden Sie die Verwendung von Farben. Obwohl Windows Store-App-Symbole manchmal Mono-Tisch sind, empfehlen wir die Verwendung von Farbsymbolen für Desktop-Apps. Dadurch können Desktop Anwendungen auf der Taskleiste und von anderen Desktop-App-Kacheln auf dem Start Bildschirm unterschieden werden, da die Hintergrundfarbe der Desktop Kacheln nicht angepasst werden kann. Verwenden Sie mehr satte Farben.

## <a name="decide-the-right-entry-points-to-include-in-the-start-screen"></a>Festlegen der richtigen Einstiegspunkte, die auf dem Start Bildschirm enthalten sein sollen

Do: Fügen Sie eine Verknüpfung pro App auf dem Start Bildschirm hinzu, wenn die APP installiert wird. Dadurch wird sichergestellt, dass Benutzer Ihre APP direkt über den Start Bildschirm oder durchsuchen starten können. Wenn Sie keine Verknüpfung auf dem Start Bildschirm einschließen, wird die APP schwer zu starten. Fügen Sie insbesondere keine Verknüpfung auf dem Desktop hinzu. Benutzern wird der Startbildschirm angezeigt, wenn Sie sich zum ersten Mal anmelden. das Platzieren einer Verknüpfung nur auf dem Desktop ist nicht so effektiv wie die Aufnahme auf den Startbildschirm.

![Diagramm, das ein Raster mit einer Anwendungs Kachel, Dimensionen und "Segoe U I semilight" anzeigt, um die verwendete Schriftart anzugeben.](images/tiles-desktop-2.png)

Nicht: Geben Sie nicht mehrere Verknüpfungen zur gleichen APP an. Sie haben z. b. keine zwei Verknüpfungen, mit denen eine app in zwei verschiedenen Modi gestartet wird, z. b. eine für Windows Internet Explorer und eine für Internet Explorer ohne Add-ons.

Do: minimieren Sie die Anzahl der Kacheln, die im Rahmen der Installation hinzugefügt werden. Es empfiehlt sich, andere Einstiegspunkte für die überflüssigen apps verfügbar zu machen. Anstatt z. b. eine separate Einstellungs-APP mit einer Konsolen-App einzuschließen, greifen Sie über eine Funktion in der Konsolen-App auf die Einstellungen zu.

Nicht: Fügen Sie keine Verknüpfungen zu den folgenden Elementen auf dem Start Bildschirm hinzu:

-   Uninstaller. Benutzer können über das Element "Programme" in der Systemsteuerung auf "Uninstaller" zugreifen.
-   Hilfedateien. Fügen Sie Hilfe Themen direkt in Ihre APP ein.
-   App-Einstellungen und-Optionen. Fügen Sie die Benutzeroberfläche zum Konfigurieren von Einstellungen für eine APP innerhalb der APP oder zum Erstellen eines System Steuerungs Elements hinzu.
-   Websites. Geben Sie entsprechende Links zu Informationen wie Hilfe-und technischen Support Websites direkt in Ihrer APP an.
-   The. Assistenten und andere einmalige Konfigurationsaufgaben sollten innerhalb der APP gestartet werden.

Nicht: Erstellen Sie keine Verknüpfungen zu Features oder Funktionen, die in der APP selbst gestartet werden können. Spracheinstellungen können z. b. über eine beliebige Microsoft Office-App konfiguriert werden, sodass es nicht erforderlich ist, dass auf dem Start Bildschirm auch ein separater Einstiegspunkt für die Spracheinstellungen vorhanden ist.

Nicht: Erstellen Sie keine Verknüpfungen zu Elementen, die keine ausführbaren Dateien sind. Tastenkombinationen, die nicht ausführbaren Dateien zugeordnet sind, z. b. Verknüpfungen, die Websites oder Hilfedateien starten, werden aus dem Start Bildschirm herausgefiltert.

Gehen Sie wie folgt vor, wenn Sie eine Suite von apps anstelle einer einzelnen App installieren, fügen Sie eine Verknüpfung für jede app in der Sammlung hinzu. Wie bereits erwähnt, sollten Sie keine Verknüpfungen zu sekundären Funktionen wie Hilfe Informationen, Hilfsprogramme und Einstellungen erstellen. Diese Funktionalität sollte in den relevanten apps der Sammlung enthalten sein.

Do: Erstellen Sie einen Produktordner auf einer einzelnen Ebene für Sammlungen, die drei oder mehr Kacheln enthalten. In der App-Ansicht des Start Bildschirms, auf die über den Charm "Suche" zugegriffen werden kann, werden Anwendungen nach dem Ordner der obersten Ebene gruppiert. Wählen Sie einen beschreibenden, aber präzisen Ordnernamen aus. Es werden drei Wörter oder weniger empfohlen. Beachten Sie, dass während der App-Ansicht Kacheln gruppiert werden und der Ordnername angezeigt wird. dieser Name ist nicht sichtbar, wenn eine Kachel an den Start Bildschirm angeheftet ist, sodass Sie Ihre Kachel Namen ausreichend beschreiben.

Nicht: Erstellen Sie keinen Produktordner, wenn die Sammlung nur eine einzige Verknüpfung enthält. Platzieren Sie die Verknüpfung im Start Ordner der obersten Ebene.

Gehen Sie wie folgt vor, wenn Sie eine Suite von mehr als drei apps installieren, sollten Sie berücksichtigen, ob eine dieser Apps für sekundäre, unregelmäßige Verwendung und nicht an den Start Bildschirm angeheftet werden soll. Wenn dies der Fall ist, können diese Kacheln gemäß der obigen Anleitung vollständig entfernt und in einer primären App gestartet werden. Wenn Sie die Kacheln nicht entfernen können, können Sie Sie über den Start Bildschirm lösen. Auf diese Weise werden die Verknüpfungen weiterhin in der Ansicht " **alle apps** " angezeigt, aber nicht in der Start Seite des Benutzers.

Um eine APP-Verknüpfung hinzuzufügen, ohne Sie an den Start Bildschirm anzuhepten, legen Sie die folgende Eigenschaft für die Verknüpfung fest: System. appusermodel. startpinoption = 1. Der symbolische Name für 1 ist appusermodel \_ startpinoption \_ nopinoninstall.

Dadurch wird verhindert, dass die Verknüpfung auf dem Start Bildschirm angezeigt wird, Sie kann jedoch weiterhin in der Ansicht " **alle apps** " und in den Suchergebnissen angezeigt werden. Nur der Benutzer kann vorhandene Verknüpfungen lösen, sodass Sie diese Eigenschaft während der Installation oder unmittelbar nach dem Platzieren der APP auf dem Datenträger festlegen müssen.

Nicht: Erstellen Sie keine Kachel für einen Host oder eine Laufzeit für Anwendungen wie Silverlight oder Java. Geben Sie in der Systemsteuerung einen Einstiegspunkt für die Deinstallation des Frameworks an.

 

 



