---
title: Wiedergabe eines Geräts
description: Wiedergabe eines Geräts
ms.assetid: 48d83e06-9e6e-498b-ad9b-0b66f235db25
keywords:
- MCI_PLAY Befehl
- MCIAVI-Wiedergabefenster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9efc06b3d5f33dfb798aa4c47bf7d5a7a8bab45842de1da170c860d2a4a5f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372641"
---
# <a name="playing-a-device"></a>Wiedergabe eines Geräts

Der [**Befehl play**](play.md) ([**MCI \_ PLAY**](mci-play.md)) beginnt mit der Wiedergabe eines Geräts. Ohne Flags beginnt dieser Befehl mit der Wiedergabe von der aktuellen Position und wird so lange ausgeführt, bis der Befehl unterbrochen wird oder bis das Ende des Mediums oder der Datei erreicht ist. Nach der Wiedergabe befindet sich die aktuelle Position am Ende des Mediums. Sie können auch den [**Suchbefehl**](seek.md) ([**MCI \_ SEEK**](mci-seek.md)) verwenden, um die aktuelle Position zu ändern.

Die meisten Geräte, die den **Wiedergabebefehl** unterstützen, unterstützen auch die Flags "from" (MCI FROM) und \_ "to" (MCI \_ TO). Diese Flags geben die Position an, an der das Gerät gestartet und die Wiedergabe beenden soll. Der folgende Befehl gibt beispielsweise mithilfe der [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) einen CD-Audiodaten datenträger vom Anfang des ersten Titels wieder:


```C++
mciSendString("play cdaudio from 0", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



Einige Gerätetypen erweitern diesen Befehl, um die Funktionen eines bestimmten Geräts auszunutzen. Der Befehl [](play.md) play für den **Gerätetyp videodisc** enthält beispielsweise die Flags "fast" (MCI \_ VD \_ PLAY \_ FAST), "slow" (MCI \_ VD PLAY SLOW) und \_ \_ "scan" (MCI \_ VD PLAY \_ \_ SCAN).

> [!Note]  
> Die einheiten, die dem Positionswert zugewiesen sind, hängen vom vom Gerät verwendeten Zeitformat ab. Jedes Gerät hat ein Standardzeitformat, aber Sie sollten das Zeitformat mithilfe des Befehls [**set**](set.md) ([**MCI \_ SET**](mci-set.md)) angeben, bevor Sie Befehle ausführen, die Positionswerte verwenden.

 

## <a name="playing-an-avi-file"></a>Wiedergabe einer AVI-Datei

Videodateien in Windows aus mindestens zwei übereinander verwebten Datenströmen: einem Videodatenstrom (13) und einem Audiostream. Sie können diese audio-video interleaved (AVI)-Dateien mithilfe von MCI-Befehlen problemlos wiederverspielen. In den folgenden Abschnitten wird die Wiedergabe von AVI-Dateien erläutert.

## <a name="setting-up-an-mciavi-playback-window"></a>Einrichten eines MCIAVI-Wiedergabefensters

Ihre Anwendung kann die folgenden Optionen angeben, um das Wiedergabefenster für die Wiedergabe einer AVI-Datei zu definieren:

-   Verwenden Sie das Standard-Popupfenster des MCIAVI-Treibers.
-   Geben Sie ein übergeordnetes Fenster und einen Fensterstil an, die der MCIAVI-Treiber zum Erstellen des Wiedergabefensters verwenden kann.
-   Geben Sie ein Wiedergabefenster an, das der MCIAVI-Treiber für die Wiedergabe verwenden soll.
-   Geben Sie die AVI-Datei auf einer Vollbildanzeige wieder.

Wenn In Ihrer Anwendung keine Fensteroptionen angegeben werden, erstellt der MCIAVI-Treiber ein Standardfenster für die Wiedergabe der Sequenz. Der Treiber erstellt dieses Wiedergabefenster für den befehl [**open**](open.md) ([**MCI \_ OPEN**](mci-open.md)), zeigt das Fenster jedoch erst an, wenn Ihre Anwendung einen Befehl sendet, um das Fenster anzuzeigen oder die Datei wiedergeben. Dieses Standardwiedergabefenster ist ein Popupfenster mit einem Größenrahmen, einer Titelleiste, einem dichten Rahmen, einem Fenstermenü und einer Schaltfläche Minimieren. 

Ihre Anwendung kann auch ein übergeordnetes Fensterhandel und ein Fensterformat angeben, wenn sie den Befehl **"Öffnen"** aus gibt. In diesem Fall erstellt der MCIAVI-Treiber anstelle des Standard-Popupfensters ein Fenster, das auf diesen Spezifikationen basiert. Ihre Anwendung kann einen beliebigen Fensterstil angeben, der für die [CreateWindow-Funktion verfügbar](/windows/win32/api/winuser/nf-winuser-createwindowa) ist. Stile, die ein übergeordnetes Fenster erfordern, z. B. WS \_ CHILD, sollten ein übergeordnetes Fensterhand handle enthalten.

Ihre Anwendung kann auch ein eigenes Fenster erstellen und das Handle für den MCIAVI-Treiber mithilfe des Befehls [**window**](window.md) ([**MCI \_ WINDOW**](mci-window.md)) verwenden. Der MCIAVI-Treiber verwendet dieses Fenster, anstatt ein eigenes zu erstellen.

Wenn der MCIAVI-Treiber das Wiedergabefenster erstellt oder ein Fensterhand handle von Ihrer Anwendung erhält, wird das Fenster erst angezeigt, wenn die Anwendung die Sequenz wiedergeben oder einen Befehl zum Anzeigen des Fensters sendet. Ihre Anwendung kann den Befehl **window verwenden,** um das Fenster ohne Wiedergabe der Sequenz anzuzeigen. Beispielsweise zeigt der folgende Befehl das Fenster mit [**mciSendString an:**](/previous-versions//dd757161(v=vs.85))


```C++
mciSendString("window movie state show", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



In diesem Beispiel ist "movie" ein Alias für das Digitalvideogerät.

Ihre Anwendung kann auch eine AVI-Datei im Vollbildmodus wiederverspielen. Ändern Sie den Befehl play [**(**](play.md) [**MCI \_ PLAY**](mci-play.md)) mit dem Flag "Fullscreen" (MCI \_ MCIAVI \_ PLAY FULLSCREEN), um den Vollbildmodus \_ wieder anzuzeigen. Wenn Ihre Anwendung dieses Flag verwendet, verwendet der MCIAVI-Treiber ein 320- bis 240-Pixel-Vollbildformat für die Wiedergabe der Sequenz. Der folgende Befehl gibt z. B. die geöffnete Datei im Vollbildmodus wieder (mit "movie" als Alias):


```C++
mciSendString("play movie fullscreen", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



## <a name="changing-the-playback-state-for-an-avi-file"></a>Ändern des Wiedergabezustands für eine AVI-Datei

Ihre Anwendung kann den [**Suchbefehl**](seek.md) ([**MCI \_ SEEK**](mci-seek.md)) verwenden, um die aktuelle Position an den Anfang, das Ende oder eine beliebige Position in einer AVI-Datei zu verschieben. Es gibt zwei Suchmodi für den MCIAVI-Treiber: genau und ungenau. Ihre Anwendung kann den Suchmodus mithilfe des Befehls [**set**](set.md) ([**MCI \_ SET**](mci-set.md)) ändern. Wenn Sie **set** "seek exactly on" verwenden, sucht der MCIAVI-Treiber genau den Rahmen, den Ihre Anwendung angibt. Dies kann zu einer Verzögerung führen, wenn die Datei zeitlich komprimiert ist und Ihre Anwendung keinen Keyframe an gibt. Wenn Sie **set** "seek exactly off" verwenden, sucht der MCIAVI-Treiber nach dem nächstgelegenen Keyframe in einer temporal komprimierten Datei.

Mit einigen MCI-Befehlen kann Ihre Anwendung die Wiedergabe einer AVI-Datei auf andere Weise ändern. Beispielsweise wird eine AVI-Datei standardmäßig mit normaler Geschwindigkeit abspielt, aber Ihre Anwendung kann diese Geschwindigkeit erhöhen oder verringern, indem sie das Flag "speed" mit dem **Set-Befehl** verwendet. Bei AVI-Dateien ist ein Geschwindigkeitswert von 1000 typisch. Daher kann Ihre Anwendung den Befehlssatz **"Movie** speed 500" verwenden, um einen Film mit halber typischer Geschwindigkeit wieder zu spielen. Alternativ kann die  Sequenz mit der festgelegten "Filmgeschwindigkeit 2000" doppelt so schnell wie gewohnt abspielt werden.

Mit [**dem Befehl setaudio**](setaudio.md) ([**MCI \_ SETAUDIO**](mci-setaudio.md)) kann Ihre Anwendung den Audioteil einer AVI-Datei steuern. Ihre Anwendung kann Audio während der Wiedergabe stummschalten oder bei mehreren Audiostreamdateien den audiostream auswählen, der abgespielt wird.

Der MCIAVI-Treiber verfügt über ein Dialogfeld, um einige seiner Wiedergabeoptionen zu steuern. Zu den optionen, die dem Benutzer zur Verfügung stehen, gehören das Auswählen der fensterorientierten Wiedergabe oder der Vollbildwiedergabe, das Auswählen des Suchmodus und das Zoomen des Bilds. In Ihrer Anwendung kann MCIAVI dieses Dialogfeld mithilfe des Befehls [**configure**](configure.md) ([**MCI \_ CONFIGURE**](mci-configure.md)) anzeigen.

## <a name="stream-handlers"></a>Streamhandler

Die Daten in einer AVI-Datei werden als eine Reihe von Datenströmen behandelt. Eine AVI-Datei enthält in der Regel einen Audio- und Videostream, und es kann auch einen benutzerdefinierten Stream geben, der Text oder einige andere benutzerdefinierte Daten enthält. Der MCIAVI-Treiber kann verschiedene Handler für diese Datenströme verwenden. Weitere Informationen zu benutzerdefinierten AVI-Dateien finden Sie unter [Benutzerdefinierte Datei- und Streamhandler.](custom-file-and-stream-handlers.md)

 

 