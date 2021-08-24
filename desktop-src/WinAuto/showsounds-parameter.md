---
title: Anzeigen von Sounds (und Audiobeschreibungsflag)
description: Dieses Thema enthält Informationen zu einem Parameter, der angibt, ob eine Anwendung eine visuelle Warnung oder hinweise bereitstellen soll, wenn sie Sound verwendet, um wichtige Informationen zu übermitteln.
ms.assetid: 7b316892-76ff-48b3-bf67-34dea2e63936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbf32dfacdf1dc0b8ed3bc51c986ae572e43300263565254ad6b3a48a981beb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734320"
---
# <a name="show-sounds-and-audio-description-flag"></a>Anzeigen von Sounds (und Audiobeschreibungsflag)

Dieses Thema enthält Informationen zu einem Parameter, der angibt, ob eine Anwendung eine visuelle Warnung oder hinweise bereitstellen soll, wenn sie Sound verwendet, um wichtige Informationen zu übermitteln. Sie enthält auch Informationen zu einem Flag, das angibt, ob eine Anwendung eine Audiobeschreibung für visuelle Elemente bereitstellen soll.

## <a name="show-sounds-parameter"></a>Sounds-Parameter anzeigen

Der Show Sounds-Parameter gibt an, ob der Benutzer möchte, dass Anwendungen alle wichtigen Informationen in visueller Form präsentieren.

Der Benutzer steuert die Einstellung des Show Sounds-Parameters mithilfe der Center für erleicherte Bedienung in Systemsteuerung oder einer anderen Anwendung zum Anpassen der Umgebung. Anwendungen verwenden die **SPI \_ GETSHOWSOUNDS-** und **SPI \_ SETSHOWSOUNDS-Flags** mit der [**SystemParametersInfo-Funktion,**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) um den Show Sounds-Parameter zu erhalten und fest zu legen. Alternativ können Anwendungen das **SM \_ SHOWSOUNDS-Flag** mit der [**GetSystemMetrics-Funktion**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) verwenden, um den Status des Show Sounds-Parameters zu bestimmen.

Die Bestimmung des Zustands des Show Sounds-Parameters ist nur für Anwendungen erforderlich, die in der Regel wichtige Informationen allein durch Sound präsentieren würden. Anwendungen sollten Unterstützung für Show Sounds bereitstellen, wenn sie Sounds auf eine der folgenden Arten verwenden:

-   Um Informationen zu vermitteln, die für den Betrieb der Anwendung wichtig sind.
-   Um den Benutzer zu warnen, dass wichtige Informationen visuell dargestellt werden. Wenn dies der Fall ist, obwohl die Informationen visuell dargestellt werden, hat der Sound die zusätzliche Funktion, die Aufmerksamkeit des Benutzers zu gewinnen.

Geeignete visuelle Feedbackformulare können die Software für Benutzer, die sich nicht allein auf Sound verlassen können, wesentlich funktionstüchtiger machen. Das Design des visuellen Feedbacks ist anwendungsspezifisch und hängt von den Informationen ab, die dem Benutzer präsentiert werden. Um beispielsweise die Aufmerksamkeit des Benutzers zu gewinnen, wenn neue elektronische E-Mails eintreffen, kann die Anwendung ihr Fenster blinken oder sogar den gesamten Bildschirm blinken lassen. Wenn die Anwendung in der Regel einen Sound gibt, um anzugeben, dass der Benutzer versucht, einen unzulässigen Vorgang durchzuführen, kann sie auch eine entsprechende Meldung in der Statuszeile anzeigen oder die [**MessageBox-Funktion**](/windows/desktop/api/winuser/nf-winuser-messagebox) verwenden, um eine bestimmte Fehlermeldung anzuzeigen. Wenn die Anwendung in der Regel so konzipiert ist, dass sie Soundtitel mit Bedeutung wiedererlangt, z. B. digitalisierter Sprache, kann sie auch ein Untertitelfenster mit demselben Text anzeigen.

Die redundante Verwendung akustischer und visueller Warnungen wurde gezeigt, um die Benutzerfreundlichkeit von Softwareanwendungen zu erhöhen. Der Parameter show sounds ist eine Anforderung für visuelles Feedback, aber seine Verwendung schränkt eine Anwendung nicht auf die visuelle Darstellung von Informationen ein. Benutzer sollten visuelles Feedback anfordern können, unabhängig davon, ob sie auch hörbares Feedback wünschen.

## <a name="audio-description-flag"></a>Audiobeschreibungsflag

Anwendungen verwenden die **\_ SPI-Flags GETAUDIODESCRIPTION** und **SPI \_ SETAUDIODESCRIPTION** mit der [**SystemParametersInfo-Funktion,**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) um Audiobeschreibungen zu aktivieren oder zu deaktivieren. Es ist zwar möglich, dass Benutzer, die sehbehindert sind, audio in Videoinhalten hören, aber es gibt viele Aktionen in Videos, die nicht über entsprechende Audiodaten verfügen. Eine spezifische Audiobeschreibung, was in einem Video geschieht, hilft diesen Benutzern, den Inhalt besser zu verstehen. Mit diesem Flag können Sie Audiobeschreibungen in den Sprachen aktivieren oder deaktivieren, in denen sie bereitgestellt werden.

 

 