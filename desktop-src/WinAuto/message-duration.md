---
title: Nachrichtenduration-Parameter
description: Anwendungen verwenden in der Regel Popup Fenster, um dem Benutzer kurz wichtige Benachrichtigungs Meldungen anzuzeigen. Eine Anwendung erstellt das Fenster, zeigt es für eine von der Anwendung definierte Dauer an und zerstört das Fenster dann.
ms.assetid: a3f7a8d8-78e7-4fb0-8ee2-bd9341857153
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2a99a43ace763da94944da334b0865c768cc920
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390443"
---
# <a name="message-duration-parameter"></a>Nachrichtenduration-Parameter

Anwendungen verwenden in der Regel Popup Fenster, um dem Benutzer kurz wichtige Benachrichtigungs Meldungen anzuzeigen. Eine Anwendung erstellt das Fenster, zeigt es für eine von der Anwendung definierte Dauer an und zerstört das Fenster dann.

Da Benutzer mit Sehbehinderung oder Cognitive-Bedingungen möglicherweise mehr Zeit zum Lesen von Benachrichtigungs-Popups benötigen, sollten Anwendungen die Dauer nicht hart codieren. Stattdessen sollte eine Anwendung die Dauer basierend auf dem Wert des **SPI \_ getmessageduration** -System Parameters festlegen. Verwenden Sie zum Abrufen dieses Parameters die [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion.

Hilfstechnologieanwendungen können die Nachrichten Dauer auf der Grundlage von Benutzereingaben festlegen, indem Sie den Systemparameter **SPI \_ setmessageduration** festlegen.

 

 