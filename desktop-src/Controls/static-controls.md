---
title: Statisches Steuerelement
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit statischen Steuerelementen verwendet werden. Ein statisches Steuerelement ist ein Steuerelement, mit dem eine Anwendung Informationstext und Grafiken für den Benutzer bereitstellen kann, die in der Regel keine Antwort erfordern.
ms.assetid: vs|controls|~\controls\staticcontrols\staticcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62c8c5b554dad8c6f3c18d0c1ceb9300dde57b20
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039692"
---
# <a name="static-control"></a>Statisches Steuerelement

Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit statischen Steuerelementen verwendet werden. Ein *statisches Steuer* Element ist ein Steuerelement, mit dem eine Anwendung Informationstext und Grafiken für den Benutzer bereitstellen kann, die in der Regel keine Antwort erfordern.

### <a name="overviews"></a>Übersichten



| Thema                                              | Inhalte                                                              |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [Informationen zu statischen Steuerelementen](about-static-controls.md) | In diesem Thema wird erläutert, wie statische Steuerelemente verwendet werden.<br/>         |
| [Statische Steuerelement Stile](static-control-styles.md) |                                                                       |
| [Verwenden statischer Steuerelemente](using-static-controls.md) | Dieses Thema enthält ein Beispiel, das ein statisches-Steuerelement verwendet.<br/> |



 

### <a name="messages"></a>Meldungen



| Thema                                 | Inhalte                                                                                                                                                                        |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**STM- \_ getIcon**](stm-geticon.md)   | Eine Anwendung sendet die [**STM \_ GetIcon**](stm-geticon.md) -Nachricht, um ein Handle für das Symbol abzurufen, das einem statischen Steuerelement mit dem SS-Symbolstil zugeordnet ist \_ . <br/> |
| [**STM \_ GetImage**](stm-getimage.md) | Eine Anwendung sendet eine [**STM \_ GetImage**](stm-getimage.md) -Nachricht zum Abrufen eines Handles zum Bild (Symbol oder Bitmap), das einem statischen Steuerelement zugeordnet ist. <br/>          |
| [**STM \_ -Ziel**](stm-seticon.md)   | Eine Anwendung sendet die [**STM \_ SetIcon**](stm-seticon.md) -Nachricht, um ein Symbol einem Symbol Steuerelement zuzuordnen. <br/>                                                     |
| [**STM- \_ Zeitrahmen**](stm-setimage.md) | Eine Anwendung sendet eine [**STM \_ SetImage**](stm-setimage.md) -Nachricht, um ein neues Bild einem statischen Steuerelement zuzuordnen.<br/>                                                |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                           | Inhalte                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_angeklickte STN](stn-clicked.md)                 | Der [ \_ angeklickte STN](stn-clicked.md) -Benachrichtigungs Code wird gesendet, wenn der Benutzer auf ein statisches Steuerelement mit dem SS-Benachrichtigungs Stil klickt [**\_**](static-control-styles.md) Das übergeordnete Fenster des Steuer Elements empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.<br/>                                                                                                                                                                  |
| [STN- \_ dblclk](stn-dblclk.md)                   | Der [STN \_ dblclk](stn-dblclk.md) -Benachrichtigungs Code wird gesendet, wenn der Benutzer auf ein statisches Steuerelement mit dem SS-Benachrichtigungs Stil doppelklickt. **\_** Das übergeordnete Fenster des Steuer Elements empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.<br/>                                                                                                                                                                                          |
| [STN \_ Deaktivieren](stn-disable.md)                 | Der [STN \_ ](stn-disable.md) -Deaktivierungs Benachrichtigungs Code wird gesendet, wenn ein statisches Steuerelement deaktiviert wird. Das statische Steuerelement muss über den SS-Benachrichtigungs Stil verfügen, um diesen Benachrichtigungs Code zu erhalten. **\_** Das übergeordnete Fenster des Steuer Elements empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.<br/>                                                                                                                                            |
| [STN \_ aktivieren](stn-enable.md)                   | Der [STN \_ ](stn-enable.md) -Benachrichtigungs Code aktivieren wird gesendet, wenn ein statisches Steuerelement aktiviert ist. Das statische Steuerelement muss über den SS-Benachrichtigungs Stil verfügen, um diesen Benachrichtigungs Code zu erhalten. **\_** Das übergeordnete Fenster des Steuer Elements empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.<br/>                                                                                                                                               |
| [**WM \_ ctlcolorstatic**](wm-ctlcolorstatic.md) | Ein statisches Steuerelement oder ein Schreib geschütztes oder deaktiviertes Bearbeitungs Steuerelement sendet die [**WM \_ ctlcolorstatic**](wm-ctlcolorstatic.md) -Meldung an das übergeordnete Fenster, wenn das Steuerelement gezeichnet werden soll. Wenn Sie auf diese Meldung reagieren, kann das übergeordnete Fenster den angegebenen Gerätekontext Handle verwenden, um die Text-und Hintergrundfarben des statischen Steuer Elements festzulegen. <br/> Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion. <br/> |



 

 

