---
description: Übersicht über die Verwendung von Gesten.
ms.assetid: 5bc80086-7acf-4f86-a9fb-a663de489f8b
title: Verwenden von Gesten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c267cff446d1bb6d092ba50bde21c1b3e25184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958899"
---
# <a name="using-gestures"></a>Verwenden von Gesten

Die Tablet PC-Plattform bietet die Microsoft Gestenerkennung zum unterstützen von Anwendungs Gesten. Eine Liste der Gesten, die von der Gestenerkennung von Microsoft unterstützt werden, finden Sie in der Tabelle mit Anwendungs Gesten in der [**applicationgesten**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) -Enumeration. Der Tablet PC unterstützt auch System Gesten. Eine Liste der System Gesten, die vom Tablet PC unterstützt werden, finden Sie in der Tabelle mit System Gesten in der [**systemgesten**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) -Enumeration.

## <a name="microsoft-gesture-recognizer"></a>Gestenerkennung von Microsoft

Sie können die Microsoft Gestenerkennung mithilfe der [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) -Eigenschaft des [**InkCollector**](inkcollector-class.md) -Objekts, des [**InkOverlay**](inkoverlay-class.md) -Objekts oder des [InkPicture](inkpicture-control-reference.md) -Steuer Elements verwenden. Wenn Sie die **CollectionMode** -Eigenschaft auf den gemischten Modus (**inkandgesten**) oder den Modus "nur Gesten" (**GestureOnly**) festlegen, werden frei Hand Eingaben standardmäßig an die Microsoft Gestenerkennung weitergeleitet. Sie können die Microsoft Gestenerkennung mit dem [InkEdit](inkedit-control-reference.md) -Steuerelement verwenden, indem Sie die Eigenschaft [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) auf **inkandgesten** festlegen. Sie können auch die Gestenerkennung mit dem [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) -Objekt verwenden, indem Sie einer der zugehörigen Plug-in-Auflistungen ein [**GestureRecognizer**](gesturerecognizer-class.md) -Objekt hinzufügen.

Wenn die Gesten, die Sie verwenden möchten, jedoch nicht von der aktuellen Version der Gestenerkennung von Microsoft unterstützt werden, können Sie Ihre eigene Erkennung erstellen und in Verbindung mit der Microsoft-Gestenerkennung verwenden. Dies ermöglicht die vollständige Unterstützung der Gesten in Ihrer Anwendung.

Der Tablet PC verwendet einen Stift für einige oder alle Eingaben. Dadurch ist es sehr einfach, frei Hand Eingaben zu schreiben. Die Tablet PC-Plattform bietet eine Architektur für Stift Eingaben, die eine mehrstufige Struktur von Gesten unterstützt. Gesten und Zuordnung werden definiert, um dem Benutzer das Schreiben und aufrufen erweiterter Gesten auf neuen Oberflächen zu ermöglichen und gleichzeitig Gesten zu reservieren, die herkömmliche Maus Meldungen anderer Windows-basierter Anwendungen aufrufen.

Die Tablet PC-Plattform führt zwei Ebenen von Gesten ein: System Gesten, auch als Systemereignisse bezeichnet und Anwendungs Gesten. Die Pen-Architektur unterstützt sowohl System-als auch Anwendungs Gesten. Anwendungen mit nur einem Strich und mehreren Strichen werden unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungs Gesten](application-gestures.md)
</dt> <dt>

[Gesten Flicks](flicks-gestures.md)
</dt> <dt>

[System Gesten](system-gestures.md)
</dt> </dl>

 

 



