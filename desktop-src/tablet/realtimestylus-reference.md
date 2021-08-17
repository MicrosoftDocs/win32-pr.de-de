---
description: Ermöglicht den Zugriff auf die Stiftereignisse, die von Stift- oder Touchdigisierern kommen.
ms.assetid: a239b53c-7fc9-4211-962a-6cfbe0be4e4c
title: RealTimeStylus-Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05518658a7bca01090e72cbe68d23b98d5ffffed14b2d8d091fa8c884e9f7c0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091460"
---
# <a name="realtimestylus-reference"></a>RealTimeStylus-Referenz

Ermöglicht den Zugriff auf die Stiftereignisse, die von Stift- oder Touchdigisierern kommen.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [RealTimeStylus-Klassen und -Schnittstellen](realtimestylus-classes-and-interfaces.md)
-   [RealTimeStylus-Enumerationen](realtimestylus-enumerations.md)
-   [RealTimeStylus-Strukturen](realtimestylus-structures.md)

## <a name="remarks"></a>Hinweise

Dieses Objekt implementiert die [**IRealTimeStylus-COM-Schnittstelle.**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance-Methode**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) in C++ instanziiert werden.

Sie können Daten vollständig steuern, dynamisch rendern, ändern und sogar aus dem Paketstream innerhalb der synchronen und asynchronen Plug-Ins des [**RealTimeStylus-Klassenobjekts**](realtimestylus-class.md) löschen.

Der Echtzeit-Stift bietet eine Möglichkeit, ein **InkCollecting-Objekt** zu erstellen, das singlethreadig ist und sich im Ui-Thread der Anwendung befindet. Dieses **InkCollecting-Objekt** greifen auf die Echtzeit-Stiftdaten aus der Warteschlange zu. Ein **InkCollecting-Objekt** in Verbindung mit einem Echtzeit-Stift ermöglicht die Bearbeitung der Auswahl in Echtzeit und die Echtzeitbearbeitung der gesammelten Ink-Daten. Weitere Informationen finden Sie unter Zugreifen auf und [Bearbeiten von Stifteingaben.](accessing-and-manipulating-stylus-input.md)

Verwenden Sie [**das RealTimeStylus-Klassenobjekt,**](realtimestylus-class.md) um direkt mit dem Tablettstiftdatenstrom zu interagieren oder das Inking in Echtzeit zu blockieren. Verwenden Sie das [**InkCollector-Klassenobjekt,**](inkcollector-class.md) [**das InkOverlay-Klassenobjekt,**](inkoverlay-class.md) das [Steuerelement InkPicture Control](inkpicture-control-reference.md) oder das Steuerelement [InkEdit Control,](inkedit-control-reference.md) wenn das Standardverhalten dieser Objekte das von Ihnen benötigte Verhalten bietet.

Die Echtzeit-Stiftereignisse befinden sich auf einem bestimmten Fensterhandpunkt innerhalb eines bestimmten Fenstereingaberechtecks. RealTimeStylusService kann Stiftdaten an mehrere [**RealTimeStylus Class-Objekte**](realtimestylus-class.md) senden. Jedes **RealTimeStylus-Klassenobjekt** empfängt Stiftdaten für einen bestimmten Abschnitt eines Fensters basierend auf der definierten [**IRealTimeStylus::WindowInputRectangle-Eigenschaft**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) für dieses **RealTimeStylus-Klassenobjekt.** Das **RealTimeStylus-Klassenobjekt** ruft die Stiftdaten ab und verarbeitet diese dann über eine Liste synchroner und asynchroner Plug-Ins.

Der Unterschied zwischen den synchronen Plug-Ins und den asynchronen Plug-Ins liegt in dem Thread, in dem sie ausgeführt werden, und der aufrufenden Sequenz. Synchrone Plug-Ins werden von dem Thread aufgerufen, in dem das [**RealTimeStylus-Klassenobjekt**](realtimestylus-class.md) ausgeführt wird. Jedes **Mal, wenn das RealTimeStylus-Klassenobjekt** instanziiert wird, wird ein Ausführungsthread instanziiert. Synchrone Plug-Ins werden für diesen neuen Thread ausgeführt, der für die Instanz des **RealTimeStylus-Klassenobjekts instanziiert** wird. Asynchrone Plug-Ins werden über die Benutzeroberfläche oder den Anwendungsthread aufgerufen, nachdem der Paketstream von den synchronen Plug-Ins verarbeitet und in der Ausgabewarteschlange gespeichert wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IDynamicRenderer-Schnittstelle**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)
</dt> <dt>

[**Istylussyncplugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[**Istylusasyncplugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)
</dt> </dl>

 

 
