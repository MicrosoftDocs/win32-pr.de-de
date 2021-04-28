---
description: Beheben von Kompatibilitätsproblemen bei der ActiveX-Installation für Standardbenutzer
ms.assetid: 4199521A-58E6-4475-9B95-A724AB52969A
title: Beheben von Kompatibilitätsproblemen bei der ActiveX-Installation für Standardbenutzer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e88b26ebd0c6e4887a8a304aeab725b176ee04a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116408"
---
# <a name="fixing-activex-installation-compatibility-issues-for-standard-users"></a>Beheben von Kompatibilitätsproblemen bei der ActiveX-Installation für Standardbenutzer

Um eine sichere Desktopumgebung zu entwickeln, müssen Sie die Bedrohungen durch schädliche ActiveX-Steuerelemente mindern und ein angemessenes Maß an Anwendungskompatibilität in Ihrer Umgebung bereitstellen. Ein *ActiveX-Steuerelement* ist ein ausführbarer Code (in der Regel eine OCX-Datei, die in einer Cab-Datei gepackt ist), die installiert und über Windows Internet Explorer ausgeführt wird. Sie können ActiveX-Steuerelemente erstellen, um Webanwendungen Funktionen hinzuzufügen, die Sie nicht einfach mit html-Standardcode oder einem einfachen Skript erreichen können.

Die Installation von ActiveX-Steuerelementen wird zu einem Kompatibilitätsproblem, wenn die Migration zu Windows 7 einen Wechsel zu Standardbenutzern einschließt. Diese Art von Übergang ist eine gängige bewährte Methode, bei der IT-Experten ihre Umgebung in ein [Standardbenutzerkonto](https://support.microsoft.com/hub/4338813/windows-help)verschieben. Dieser Übergang ist für die Bereitstellung von Windows Internet Explorer 8 nicht erforderlich.

## <a name="activex-control-installation"></a>Installation des ActiveX-Steuerelements

ActiveX-Steuerelemente verfügen über ein einfaches Bereitstellungsmodell zum Herunterladen und Ausführen. ActiveX-Steuerelemente werden installiert und durch das **HTML-Objektelement** ausgeführt. Das **CODEBASE-Attribut** für dieses Element teilt Internet Explorer (mithilfe einer URL) mit, wo das Steuerelement abzurufen ist, wenn es nicht bereits auf dem Computer des Benutzers installiert ist. In diesem Fall lädt Internet Explorer das zugehörige Installationspaket herunter, führt eine Vertrauensüberprüfung für das Objekt durch und fordert den Benutzer zur Eingabe der Installationsberechtigung in Internet Explorer auf.

Während der Installation wird das Steuerelement auf der Renderingseite registriert und ausgeführt. Nach der Installation des Steuerelements können alle Standardbenutzer das Steuerelement ausführen. Dieser einfache Verteilungs- und Ausführungsmechanismus bietet eine einfache Möglichkeit, Ihre Komponenten an Benutzer Ihrer Webanwendung zu verteilen. Benutzer von Standardkonten können activeX-Steuerelemente jedoch nicht direkt pro Computer installieren, und sie benötigen möglicherweise Administratorrechte, um die Installation abzuschließen.

## <a name="activex-installer-service-axis"></a>ActiveX Installer Service (AXIS)

Mit dem ActiveX-Installerdienst (AXIS) können Sie ActiveX-Steuerelemente mithilfe Gruppenrichtlinie Computern in einer Organisation bereitstellen. Sie können AXIS konfigurieren, indem Gruppenrichtlinie, die Sie ändern können, indem Sie die Gruppenrichtlinien-Verwaltungskonsole (GPMC) oder die Editor für lokale Gruppenrichtlinien.

Es gibt zwei Richtlinieneinstellungen für AXIS:

-   Die Richtlinieneinstellung Genehmigte Installationsstandorte für ActiveX-Steuerelemente besteht aus einer Liste von genehmigten Installationsstandorten, mit denen AXIS bestimmt, ob ein ActiveX-Steuerelement installiert werden kann.
-   Die Richtlinieneinstellung ActiveX-Installationsrichtlinie für Standorte in vertrauenswürdigen Zonen gibt an, wie Zonen für vertrauenswürdige Standorte zum Installieren von ActiveX-Steuerelementen verwendet werden können.

Wenn eine Website versucht, ein ActiveX-Steuerelement zu installieren, überprüft axis, ob die URL der Website in der Liste der genehmigten Installationsstandorte oder als Teil der Zone der vertrauenswürdigen Standorte aufgeführt ist. Wenn sich der Standort in einer dieser Listen befindet, stellt axis sicher, dass der Standort die von der Richtlinie festgelegten Anforderungen erfüllt. Wenn die Website und das ActiveX-Steuerelement alle Anforderungen der Richtlinieneinstellungen erfüllen, wird das Steuerelement installiert. Weitere Informationen finden Sie unter [Verwalten des ActiveX-Installationsdiensts](/previous-versions/windows/it-pro/windows-7/dd631688(v=ws.10)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mit Kompatibilitätsansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
