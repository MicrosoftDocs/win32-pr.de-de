---
title: Wiedergeben eines Geräts
description: Wiedergeben eines Geräts
ms.assetid: 48d83e06-9e6e-498b-ad9b-0b66f235db25
keywords:
- MCI_PLAY-Befehl
- MCIAVI-Wiedergabe Fenster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73d8b6539e842a1ffa632ed1efae5c2c8d3cda1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948740"
---
# <a name="playing-a-device"></a>Wiedergeben eines Geräts

Der [**Wiedergabe**](play.md) Befehl ([**MCI \_ Play**](mci-play.md)) beginnt mit der Wiedergabe eines Geräts. Ohne Flags startet dieser Befehl von der aktuellen Position aus und wird wiedergegeben, bis der Befehl unterbrochen wird oder bis das Ende des Mediums oder der Datei erreicht ist. Nach der Wiedergabe befindet sich die aktuelle Position am Ende des Mediums. Sie können auch den Befehl [**Seek**](seek.md) ([**MCI \_ Seek**](mci-seek.md)) verwenden, um die aktuelle Position zu ändern.

Die meisten Geräte, die den **Play** -Befehl unterstützen, unterstützen auch die Flags "from" (MCI \_ from) und "to" (MCI \_ to). Diese Flags geben die Position an, an der das Gerät gestartet und beendet werden soll. Der folgende Befehl gibt z. b. eine CD-Audiodatenträger ab dem Anfang der ersten Spur mit der [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion ein:


```C++
mciSendString("play cdaudio from 0", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



Einige Gerätetypen erweitern diesen Befehl, um die Funktionen eines bestimmten Geräts auszunutzen. Beispielsweise umfasst der [**Wiedergabe**](play.md) Befehl für den Geräte Datentyp " **Video Disk** " die Flags "fast" (MCI VD Play \_ \_ \_ fast), "langsam" (MCI \_ VD \_ Play \_ Slow) und "Scan" (MCI \_ VD \_ Play \_ Scan).

> [!Note]  
> Die dem Positionswert zugewiesenen Einheiten hängen von dem vom Gerät verwendeten Zeitformat ab. Jedes Gerät weist ein Standardzeit Format auf, Sie sollten jedoch das Zeitformat mithilfe des Befehls [**Set**](set.md) ([**MCI \_ set**](mci-set.md)) angeben, bevor Sie Befehle ausgeben, die Positionswerte verwenden.

 

## <a name="playing-an-avi-file"></a>Abspielen einer AVI-Datei

Videodateien in Windows bestehen aus mindestens zwei verschachtelten Datenströmen: einem Videodaten Strom (bildlich) und einem Audiodatenstrom. Sie können diese überlappenden Audiodateien (AVI) problemlos mithilfe von MCI-Befehlen abspielen. In den folgenden Abschnitten wird das Abspielen von AVI-Dateien erläutert

## <a name="setting-up-an-mciavi-playback-window"></a>Einrichten eines MCIAVI-Wiedergabe Fensters

Die Anwendung kann die folgenden Optionen angeben, um das Wiedergabe Fenster zum Abspielen einer AVI-Datei zu definieren:

-   Verwenden Sie das Standard-Popup Fenster des MCIAVI-Treibers.
-   Geben Sie ein übergeordnetes Fenster und eine Fenster Formatvorlage an, mit denen der MCIAVI-Treiber das Wiedergabe Fenster erstellen kann.
-   Geben Sie ein Wiedergabe Fenster für den MCIAVI-Treiber an, der für die Wiedergabe verwendet wird.
-   Geben Sie die AVI-Datei auf einer voll Bild Anzeige wieder.

Wenn die Anwendung keine Fenster Optionen angibt, erstellt der MCIAVI-Treiber ein Standardfenster für die Wiedergabe der Sequenz. Der Treiber erstellt dieses Wiedergabe Fenster für den [**geöffneten**](open.md) Befehl ([**MCI \_ Open**](mci-open.md)), zeigt jedoch erst das Fenster an, wenn die Anwendung einen Befehl sendet, um das Fenster anzuzeigen oder die Datei wiederzugeben. Dieses Standard Wiedergabe Fenster ist ein Popup Fenster mit einem Größen Anpassungsrahmen, einer Titelleiste, einem dicken Rahmen, einem **Fenster** Menü und einer Minimieren-Schaltfläche.

Die Anwendung kann auch ein übergeordnetes Fenster Handle und einen Fenster Stil angeben, wenn der Befehl zum **Öffnen** ausgegeben wird. In diesem Fall erstellt der MCIAVI-Treiber ein Fenster auf der Grundlage dieser Spezifikationen anstelle des standardmäßigen Popup Fensters. Die Anwendung kann einen beliebigen Fenster Stil angeben, der für die Funktion "up [Window](/windows/win32/api/winuser/nf-winuser-createwindowa) " verfügbar ist. Stile, die ein übergeordnetes Fenster erfordern, z. b. untergeordnete WS-Elemente \_ , sollten ein übergeordnetes Fenster Handle enthalten.

Die Anwendung kann auch ein eigenes Fenster erstellen und das Handle für den MCIAVI-Treiber über den [**Fenster**](window.md) Befehl ([**MCI- \_ Fenster**](mci-window.md)) bereitstellen. Der MCIAVI-Treiber verwendet dieses Fenster, anstatt einen eigenen zu erstellen.

Wenn der MCIAVI-Treiber das Wiedergabe Fenster erstellt oder ein Fenster Handle von der Anwendung abruft, wird das Fenster erst angezeigt, nachdem die Anwendung die Sequenz abgespielt oder einen Befehl zum Anzeigen des Fensters gesendet hat. Die Anwendung kann den **Fenster** Befehl verwenden, um das Fenster anzuzeigen, ohne die Sequenz zu spielen. Beispielsweise wird mit dem folgenden Befehl das Fenster mithilfe von " [**mciSendString**](/previous-versions//dd757161(v=vs.85))" angezeigt:


```C++
mciSendString("window movie state show", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



In diesem Beispiel ist "Movie" ein Alias für das Digital-Video-Gerät.

Die Anwendung kann auch einen voll Bildschirm der AVI-Datei abspielen. Um den voll Bildschirm wiederzugeben, ändern Sie den Befehl [**Play**](play.md) ([**MCI \_ Play**](mci-play.md)) mit dem Flag "fullscreen" (MCI \_ MCIAVI \_ Play \_ fullscreen). Wenn Ihre Anwendung dieses Flag verwendet, verwendet der MCIAVI-Treiber ein 320-und 240-Pixel-Vollbildformat zum Abspielen der Sequenz. Beispielsweise wird mit dem folgenden Befehl der voll Bildschirm der geöffneten Datei (mit "Movie" als Alias) abgespielt:


```C++
mciSendString("play movie fullscreen", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



## <a name="changing-the-playback-state-for-an-avi-file"></a>Ändern des Wiedergabe Zustands für eine AVI-Datei

Die Anwendung kann den [**Seek**](seek.md) -Befehl ([**MCI \_ Seek**](mci-seek.md)) verwenden, um die aktuelle Position an den Anfang, das Ende oder an eine beliebige Position in einer AVI-Datei zu verschieben. Es gibt zwei Suchmodi für den MCIAVI-Treiber: genau und ungenau. Die Anwendung kann den Suchmodus mithilfe des Befehls [**Set**](set.md) ([**MCI \_ set**](mci-set.md)) ändern. Wenn Sie **Set** "Seek very on" verwenden, sucht der MCIAVI-Treiber genau nach dem Frame, der von der Anwendung angegeben wird. Dies kann zu einer Verzögerung führen, wenn die Datei temporlig komprimiert ist und die Anwendung keinen Keyframe angibt. Wenn Sie **Set** "Seek genau aus" verwenden, sucht der MCIAVI-Treiber den nächsten Keyframe in einer Temporale komprimierten Datei.

Einige MCI-Befehle ermöglichen der Anwendung, die Wiedergabe einer AVI-Datei auf andere Weise zu ändern. Beispielsweise wird eine AVI-Datei standardmäßig mit der normalen Geschwindigkeit abgespielt, aber Ihre Anwendung kann diese Geschwindigkeit erhöhen oder verringern, indem Sie das Flag "Geschwindigkeit" mit dem **Set** -Befehl verwenden. Für AVI-Dateien ist ein Geschwindigkeitswert von 1000 typisch. Damit ein Film mit der Hälfte seiner typischen Geschwindigkeit wiedergegeben werden kann, kann die Anwendung den Befehls **Satz** "Filmgeschwindigkeit 500" verwenden. Sie können auch **Set** "Movie Speed 2000" verwenden, um die Sequenz mit der doppelten Geschwindigkeit wiederzugeben.

Der [**setaudiobefehl**](setaudio.md) ([**MCI \_ setaudiobefehl**](mci-setaudio.md)) ermöglicht der Anwendung die Steuerung des Audioteils einer AVI-Datei. Die Anwendung kann Audiodaten während der Wiedergabe stumm schalten oder bei mehreren audiostreamdateien den wiedergegebenen Audiostream auswählen.

Der MCIAVI-Treiber verfügt über ein Dialogfeld, in dem einige der Wiedergabe Optionen gesteuert werden können. Zu den Optionen, die für den Benutzer verfügbar sind, gehören das Auswählen der Fenster orientierten oder der Vollbildwiedergabe, das Auswählen des Suchmodus und das Zoomen des Bilds. In Ihrer Anwendung kann MCIAVI dieses Dialogfeld mithilfe des Befehls [**configure**](configure.md) ([**MCI \_ configure**](mci-configure.md)) anzeigen.

## <a name="stream-handlers"></a>Datenstrom Handler

Die Daten in einer AVI-Datei werden als eine Reihe von Streams behandelt. Eine AVI-Datei enthält in der Regel einen Audiostream und einen Videostream, und es kann auch ein benutzerdefinierter Stream vorhanden sein, der Text oder andere benutzerdefinierte Daten enthält. Der MCIAVI-Treiber kann verschiedene Handler für diese Datenströme verwenden. Weitere Informationen zu benutzerdefinierten AVI-Dateien finden Sie unter [Custom File and Stream Handlers](custom-file-and-stream-handlers.md).

 

 