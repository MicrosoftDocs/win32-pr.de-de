---
title: Sounds anzeigen (und audiobeschreibungs-Flag)
description: Dieses Thema enthält Informationen über einen Parameter, der angibt, ob eine Anwendung eine visuelle Warnung oder einen Hinweis bereitstellen soll, wenn Sound zum vermitteln wichtiger Informationen verwendet wird.
ms.assetid: 7b316892-76ff-48b3-bf67-34dea2e63936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d01e3fda902c23c86279a9a4d75889ebfeff4d55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341531"
---
# <a name="show-sounds-and-audio-description-flag"></a>Sounds anzeigen (und audiobeschreibungs-Flag)

Dieses Thema enthält Informationen über einen Parameter, der angibt, ob eine Anwendung eine visuelle Warnung oder einen Hinweis bereitstellen soll, wenn Sound zum vermitteln wichtiger Informationen verwendet wird. Außerdem werden Informationen zu einem Flag bereitgestellt, das angibt, ob eine Anwendung eine Audiobeschreibung für visuelle Elemente bereitstellen soll.

## <a name="show-sounds-parameter"></a>Sounds-Parameter anzeigen

Der Show Sounds-Parameter gibt an, ob der Benutzer möchten, dass die Anwendungen alle wichtigen Informationen im visuellen Formular darstellen.

Der Benutzer steuert die Einstellung des Parameters Show Sounds mithilfe der Easy of Access Center in der Systemsteuerung oder einer anderen Anwendung für die Anpassung der Umgebung. Anwendungen verwenden die **SPI \_ getshowsounds** -und **SPI \_ setshowsounds** -Flags mit der [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion, um den Show Sounds-Parameter zu erhalten und festzulegen. Alternativ können Anwendungen das **SM \_ ShowSounds** -Flag mit der [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) -Funktion verwenden, um den Status des Show Sounds-Parameters zu bestimmen.

Die Bestimmung des Status des Show Sounds-Parameters ist nur für Anwendungen erforderlich, die in der Regel wichtige Informationen nur mit Sound darstellen. Anwendungen sollten Show Sounds-Unterstützung bieten, wenn Sie Sounds auf eine der folgenden Arten verwenden:

-   Zum vermitteln von Informationen, die für den Betrieb der Anwendung wichtig sind.
-   , Um den Benutzer darüber zu informieren, dass wichtige Informationen visuell dargestellt werden. Wenn dies der Fall ist, auch wenn die Informationen visuell dargestellt werden, verfügt der Sound über die zusätzliche Funktion, die dem Benutzer Aufmerksamkeit geschenkt hat.

Mit den entsprechenden visuellen Feedback Formularen kann die Software für Benutzer, die sich nicht allein auf Sound verlassen können, viel besser funktionieren. Der Entwurf des visuellen Feedbacks ist anwendungsspezifisch und hängt von den Informationen ab, die dem Benutzer angezeigt werden. Wenn Sie z. b. die Aufmerksamkeit des Benutzers beim Eintreffen neuer elektronischer e-Mails gewinnen möchten, kann die Anwendung das Fenster oder sogar den gesamten Bildschirm blinken. Wenn die Anwendung in der Regel den Sound angibt, um anzugeben, dass der Benutzer versucht, einen ungültigen Vorgang auszuführen, könnte Sie auch eine entsprechende Meldung in der Statuszeile anzeigen oder die [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) -Funktion verwenden, um eine bestimmte Fehlermeldung anzuzeigen. Wenn die Anwendung in der Regel für die Wiedergabe von Sound Stichen konzipiert ist, die Bedeutung haben, wie z. b. die digitalisierte Sprache, könnte Sie auch ein Beschriftungs Fenster mit demselben Text anzeigen

Die redundante Verwendung von akustischen und visuellen Warnungen wurde gezeigt, um die Nutzbarkeit von Softwareanwendungen zu verbessern. Der Show Sounds-Parameter ist eine Anforderung für visuelles Feedback, aber seine Verwendung schränkt eine Anwendung nicht auf die visuelle Darstellung von Informationen ein. Benutzer sollten in der Lage sein, visuelles Feedback anzufordern, unabhängig davon, ob Sie auch ein hörbares Feedback wünschen.

## <a name="audio-description-flag"></a>Audiobeschreibungs-Flag

Anwendungen verwenden die **SPI \_ getaudiodescription** -und **SPI \_ setaudiodescription** -Flags mit der [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion, um Audiobeschreibungen zu aktivieren oder zu deaktivieren. Es ist zwar möglich, dass Benutzer, denen die Audioinhalte in Videoinhalten angezeigt werden, die Audioinhalte in Videoinhalten aber sehr viel zu tun haben, wenn Sie nicht über das entsprechende Audiomaterial verfügen. Mit der spezifischen Audiobeschreibung, was in einem Video geschieht, können diese Benutzer den Inhalt besser verstehen. Dieses Flag ermöglicht Ihnen das Aktivieren oder Deaktivieren von Audiobeschreibungen in den Sprachen, die in bereitgestellt werden.

 

 