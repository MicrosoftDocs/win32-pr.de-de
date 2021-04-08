---
description: .
ms.assetid: 4199521A-58E6-4475-9B95-A724AB52969A
title: Beheben von Kompatibilitätsproblemen der ActiveX-Installation für Standard Benutzer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e50ed2aa9e428164e39b377b65c418d82df1e5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761436"
---
# <a name="fixing-activex-installation-compatibility-issues-for-standard-users"></a>Beheben von Kompatibilitätsproblemen der ActiveX-Installation für Standard Benutzer

Zum Entwickeln einer sicheren Desktopumgebung müssen Sie die Bedrohungen durch böswillige ActiveX-Steuerelemente mindern und eine angemessene Anwendungs Kompatibilität in Ihrer Umgebung bereitstellen. Ein *ActiveX-Steuer* Element ist ein Teil des ausführbaren Codes (in der Regel eine OCX-Datei, die in einer CAB-Datei verpackt ist), die über Windows Internet Explorer installiert und ausgeführt wird. Sie können ActiveX-Steuerelemente erstellen, um Webanwendungen Funktionen hinzuzufügen, die Sie nicht ohne weiteres mithilfe von HTML-Standard Code oder einem einfachen Skript erreichen können.

Die Installation von ActiveX-Steuerelementen wird zu einem Kompatibilitätsproblem, wenn die Migration zu Windows 7 einen Wechsel zu Standardbenutzern einschließt. Diese Art des Übergangs ist eine gängige bewährte Vorgehensweise, bei der IT-Experten ihre Umgebung in ein [Standardbenutzer Konto](https://support.microsoft.com/hub/4338813/windows-help)verschieben. Dieser Übergang ist keine Voraussetzung für die Bereitstellung von Windows Internet Explorer 8.

## <a name="activex-control-installation"></a>ActiveX-Steuerelement Installation

ActiveX-Steuerelemente verfügen über ein einfaches Download-und Ausführungs Bereitstellungs Modell. ActiveX-Steuerelemente werden installiert und durch das HTML- **Objekt** Element ausgeführt. Das **CodeBase** -Attribut in diesem Element weist Internet Explorer (mithilfe einer URL) an, wo das Steuerelement zu finden ist, wenn es nicht bereits auf dem Computer des Benutzers installiert ist. In diesem Fall lädt Internet Explorer das zugehörige Installationspaket herunter, führt die Überprüfung der Vertrauenswürdigkeit für das Objekt durch und fordert den Benutzer zur Installation der Berechtigung in Internet Explorer auf.

Während der Installation wird das-Steuerelement von der renderingseite registriert und ausgeführt. Nachdem das-Steuerelement installiert wurde, können alle Standardbenutzer das-Steuerelement ausführen. Dieser einfache Verteilungs-und Ausführungs Mechanismus bietet eine einfache Möglichkeit, ihre Komponenten an Benutzer Ihrer Webanwendung zu verteilen. Benutzer mit Standardkonten können ActiveX-Steuerelemente auf dem Computer jedoch nicht direkt installieren und benötigen möglicherweise Administratorrechte, um die Installation abzuschließen.

## <a name="activex-installer-service-axis"></a>ActiveX-Installations Dienst (Achse)

Mit dem ActiveX-Installations Dienst (Axis) können Sie ActiveX-Steuerelemente bereitstellen, indem Sie Gruppenrichtlinie auf Computern in einer Organisation verwenden. Sie können die Achse Gruppenrichtlinie Einstellungen konfigurieren, die Sie mithilfe der Gruppenrichtlinien-Verwaltungskonsole (GPMC) oder der Editor für lokale Gruppenrichtlinien ändern können.

Es gibt zwei Richtlinien Einstellungen für die-Achse:

-   Die Richtlinien Einstellung genehmigte Installations Standorte für ActiveX-Steuerelemente besteht aus einer Liste genehmigter Installations Standorte, die die-Achse verwendet, um zu bestimmen, ob ein ActiveX-Steuerelement installiert werden kann.
-   Die Richtlinien Einstellung ActiveX-Installations Richtlinie für Sites in vertrauenswürdigen Zonen gibt an, wie Zone vertrauenswürdiger Sites zum Installieren von ActiveX-Steuerelementen verwendet werden kann.

Wenn eine Website versucht, ein ActiveX-Steuerelement zu installieren, überprüft die Achse, ob die URL der Website in der Liste der genehmigten Installations Sites oder als Teil der Zone der vertrauenswürdigen Sites aufgeführt ist. Wenn der Standort in einer dieser Listen aufgeführt ist, stellt die Achse sicher, dass die Site die von der Richtlinie definierten Anforderungen erfüllt. Wenn die Website und das ActiveX-Steuerelement alle Anforderungen der Richtlinieneinstellungen erfüllen, wird das Steuerelement installiert. Weitere Informationen finden Sie unter [Verwalten des ActiveX-Installationsdiensts](/previous-versions/windows/it-pro/windows-7/dd631688(v=ws.10)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
