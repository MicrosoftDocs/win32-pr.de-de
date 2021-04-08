---
title: Anpassen des Plug-Ins für die Benutzeroberfläche
description: Anpassen des Plug-Ins für die Benutzeroberfläche
ms.assetid: d961ed18-ba14-45af-90d3-b1e38dc53180
keywords:
- Windows Media Player-Plug-ins, anpassen
- Plug-ins, anpassen
- Plug-Ins für die Benutzeroberfläche, anpassen
- UI-Plug-ins, anpassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4572c4ce5102443c3100ddd20719fe17fe62ffc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037371"
---
# <a name="customizing-the-ui-plug-in"></a>Anpassen des Plug-Ins für die Benutzeroberfläche

An diesem Punkt ist Ihr Projekt bereit für die Anpassung. Sie können die vom Assistenten generierte Implementierung der **iwmppluginui** -Schnittstelle ändern, Sie können der **cpluginwindow** -Klasse eine Benutzeroberfläche hinzufügen, und Sie können eine Eigenschaften Seite in der **cpropertydialog** -Klasse implementieren. Wenn das Plug-in für das Lauschen auf Windows Media Player-Ereignisse konfiguriert ist, werden vom Assistenten standardmäßige oder leere Implementierungen aller erforderlichen Ereignishandler generiert, die Sie ebenfalls ändern oder erstellen.

Der Typ des Plug-ins und die von ihm unterstützten Funktionen werden durch einen Wert angezeigt, der in der Windows-Registrierung gespeichert ist. Der Assistent generiert eine Datei mit der Dateinamenerweiterung RGS, die die Informationen enthält, mit denen das Plug-in registriert werden soll. Der "Funktionen"-Wert in dieser Datei ist die dezimale Entsprechung eines booleschen Werts oder der Plug-in-Typkonstanten und Plug-in-Flags, die in "wmpplug. h" definiert sind. Obwohl dieser Wert durch die Optionen bestimmt wird, die Sie im Assistenten auswählen, müssen Sie ihn ändern, wenn Sie ein Plug-in mit mehreren Voreinstellungen erstellen möchten oder eine, an die Medienelemente oder Wiedergabelisten gesendet werden können.

Wenn Sie Ihren Plug-in-Code ändern und erweitern, können Sie die dll erstellen und registrieren, damit Sie Ihr Plug-in in Windows Media Player testen können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aufbau eines UI-Plug-ins**](building-a-ui-plug-in.md)
</dt> </dl>

 

 




