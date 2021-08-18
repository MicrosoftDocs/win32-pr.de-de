---
description: Beheben ActiveX Kompatibilitätsproblemen bei der Installation für Standardbenutzer
ms.assetid: 4199521A-58E6-4475-9B95-A724AB52969A
title: Beheben ActiveX Kompatibilitätsproblemen bei der Installation für Standardbenutzer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31dbcf8dfddd7e35a8a446f4b73dd1e5324cbe4695590511fa1cb220700b2c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994770"
---
# <a name="fixing-activex-installation-compatibility-issues-for-standard-users"></a>Beheben ActiveX Kompatibilitätsproblemen bei der Installation für Standardbenutzer

Um eine sichere Desktopumgebung zu entwickeln, müssen Sie die Bedrohungen durch schädliche ActiveX steuern und ein angemessenes Maß an Anwendungskompatibilität in Ihrer Umgebung bereitstellen. Ein *ActiveX-Steuerelement* ist ein Teil des ausführbaren Codes (in der Regel eine OCX-Datei, die in einer Schränkdatei gepackt ist), die installiert wird und durch Windows Internet Explorer. Sie können ActiveX Erstellen von Steuerelementen erstellen, um Webanwendungen Funktionen hinzuzufügen, die Sie nicht einfach mithilfe von HTML-Standardcode oder einem einfachen Skript erreichen können.

Die Installation von ActiveX-Steuerelementen wird zu einem Kompatibilitätsproblem, wenn die Migration zu Windows 7 einen Wechsel zu Standardbenutzern einschließt. Diese Art von Übergang ist eine gängige bewährte Methode, bei der IT-Experten ihre Umgebung in ein [Standardbenutzerkonto verschieben.](https://support.microsoft.com/hub/4338813/windows-help) Dieser Übergang ist keine Voraussetzung für die Bereitstellung Windows Internet Explorer 8.

## <a name="activex-control-installation"></a>ActiveX Steuern der Installation

ActiveX-Steuerelemente verfügen über ein einfaches Bereitstellungsmodell zum Herunterladen und Ausführen. ActiveX Steuerelemente werden installiert und durch  das HTML-Objektelement ausgeführt. Das **CODEBASE-Attribut** für dieses Element teilt Internet Explorer (mithilfe einer URL) mit, wo das Steuerelement erhalten werden soll, wenn es noch nicht auf dem Computer des Benutzers installiert ist. In diesem Fall lädt Internet Explorer das zugeordnete Installationspaket herunter, führt eine Vertrauensüberprüfung für das Objekt durch und fordert den Benutzer auf, die Installationsberechtigung in Internet Explorer.

Während der Installation wird das Steuerelement auf der Renderingseite registriert und ausgeführt. Nachdem das Steuerelement installiert wurde, können alle Standardbenutzer das Steuerelement ausführen. Dieser einfache Verteilungs- und Ausführungsmechanismus bietet eine einfache Möglichkeit, Ihre Komponenten an Benutzer Ihrer Webanwendung zu verteilen. Standardkontobenutzer können jedoch keine computerspezifischen ActiveX installieren und benötigen möglicherweise Administratorrechte, um die Installation abzuschließen.

## <a name="activex-installer-service-axis"></a>ActiveX Installer-Dienst (AXIS)

Mit ActiveX Installer Service (AXIS) können Sie ActiveX-Steuerelemente bereitstellen, indem Sie Gruppenrichtlinie Computern in einer Organisation verwenden. Sie können AXIS mithilfe Gruppenrichtlinie konfigurieren, die Sie mithilfe des Gruppenrichtlinien-Verwaltungskonsole (GPMC) oder des Editor für lokale Gruppenrichtlinien.

Es gibt zwei Richtlinieneinstellungen für AXIS:

-   Die Richtlinieneinstellung Genehmigte Installationsstandorte für ActiveX-Steuerelemente besteht aus einer Liste von genehmigten Installationsstandorten, die von AXIS verwendet werden, um zu bestimmen, ob ein ActiveX installiert werden kann.
-   Die ActiveX-Installationsrichtlinie für Standorte in der Richtlinieneinstellung Vertrauenswürdige Zonen gibt an, wie Zonen für vertrauenswürdige Standorte zum Installieren von ActiveX werden können.

Wenn eine Website versucht, ein ActiveX-Steuerelement zu installieren, überprüft die ACHSE, ob die URL der Website in der Liste der genehmigten Installationsstandorte oder als Teil der Zone der vertrauenswürdigen Standorte aufgeführt ist. Wenn sich der Standort in einer dieser Listen befindet, stellt axis sicher, dass der Standort die von der Richtlinie festgelegten Anforderungen erfüllt. Wenn die Website und das ActiveX-Steuerelement alle Anforderungen der Richtlinieneinstellungen erfüllen, wird das Steuerelement installiert. Weitere Informationen finden Sie unter [Verwalten des ActiveX-Installationsdiensts](/previous-versions/windows/it-pro/windows-7/dd631688(v=ws.10)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mit Kompatibilitätsansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
