---
title: Öffnen eines Geräts
description: Öffnen eines Geräts
ms.assetid: d4881d32-e8b7-45e6-b00b-b4cd69b738f1
keywords:
- MCI_OPEN Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34408cef4e85ed7200b91c610e60ca546ff488ce5ad45edee12159a664f319fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802317"
---
# <a name="opening-a-device"></a>Öffnen eines Geräts

Bevor Sie ein Gerät verwenden, müssen Sie es mit dem [**Befehl open**](open.md) ([**MCI \_ OPEN**](mci-open.md)) initialisieren. Dieser Befehl lädt den Treiber in den Arbeitsspeicher (sofern er noch nicht geladen ist) und ruft den Gerätebezeichner ab, den Sie zum Identifizieren des Geräts in nachfolgenden MCI-Befehlen verwenden. Überprüfen Sie den Rückgabewert der [**mciSendString-**](/previous-versions//dd757161(v=vs.85)) oder [**mciSendCommand-Funktion,**](/previous-versions//dd757160(v=vs.85)) bevor Sie einen neuen Gerätebezeichner verwenden, um sicherzustellen, dass der Bezeichner gültig ist. (Sie können einen Gerätebezeichner auch mithilfe der [**mciGetDeviceID-Funktion**](/previous-versions//dd757156(v=vs.85)) abrufen.)

Wie alle MCI-Befehlsmeldungen verfügt **MCI \_ OPEN** über eine zugeordnete Struktur. Diese Strukturen werden manchmal als *Parameterblöcke* bezeichnet. Die Standardstruktur für **MCI \_ OPEN** ist [**MCI \_ OPEN \_ PARMS.**](mci-open-parms.md) Bestimmte Geräte (z. B. *Wellenform* und *Überlagerung)* verfügen über erweiterte Strukturen (z. B. [**MCI \_ WAVE OPEN \_ \_ PARMS**](mci-wave-open-parms.md) und [**MCI \_ OVLY \_ OPEN \_ PARMS),**](mci-ovly-open-parms.md)um zusätzliche optionale Parameter aufzunehmen. Sofern Sie diese zusätzlichen Parameter nicht verwenden müssen, können Sie die **MCI \_ OPEN \_ PARMS-Struktur** mit jedem MCI-Gerät verwenden.

Die Anzahl der geöffneten Geräte ist nur durch die Menge des verfügbaren Arbeitsspeichers beschränkt.

## <a name="using-an-alias"></a>Verwenden eines Alias

Wenn Sie ein Gerät öffnen, können Sie das Flag "alias" verwenden, um einen Gerätebezeichner für das Gerät anzugeben. Mit diesem Flag können Sie einen kurzen Gerätebezeichner für Verbundgeräte mit langen Dateinamen zuweisen und mehrere Instanzen derselben Datei oder desselben Geräts öffnen.

Der folgende Befehl weist beispielsweise den Gerätebezeichner "birdcall" dem langen Dateinamen C zu: \\ NABIRDS \\ SOUNDS \\ MOCKMTNG. Wav:


```C++
mciSendString(
    "open c:\nabirds\sounds\mockmtng.wav type waveaudio alias birdcall", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



In der Befehlsmeldungsschnittstelle geben Sie einen Alias an, indem Sie den **lpstrAlias-Member** der [**MCI \_ OPEN \_ PARMS-Struktur**](mci-open-parms.md) verwenden.

## <a name="specifying-a-device-type"></a>Angeben eines Gerätetyps

Wenn Sie ein Gerät öffnen, können Sie das Flag "type" verwenden, um auf einen Gerätetyp und nicht auf einen bestimmten Gerätetreiber zu verweisen. Im folgenden Beispiel wird die Waveform-Audiodatei C: \\ WINDOWS \\ CHIMES geöffnet. WAV (mit dem Flag "type" zum Angeben des **Waveaudio-Gerätetyps)** und weist den Alias "Chimes" zu:


```C++
mciSendString(
    "open c:\windows\chimes.wav type waveaudio alias chimes", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



In der Befehlsmeldungsschnittstelle wird die Funktionalität des Flags "type" vom **lpstrDeviceType-Member** der [**MCI \_ OPEN \_ PARMS-Struktur**](mci-open-parms.md) bereitgestellt.

## <a name="simple-and-compound-devices"></a>Einfache und zusammengesetzte Geräte

MCI klassifiziert Gerätetreiber als *zusammengesetzte* oder *einfache*. Treiber für Verbundgeräte erfordern den Namen einer Datendatei für die Wiedergabe. Treiber für einfache Geräte nicht.

Zu den einfachen Geräten gehören **cdaudio-** und **videodisc-Geräte.** Es gibt zwei Möglichkeiten, einfache Geräte zu öffnen:

-   Geben Sie einen Zeiger auf eine auf NULL endende Zeichenfolge an, die den Gerätenamen aus der Registrierung oder der SYSTEM.INI-Datei enthält.

    Beispielsweise können Sie ein **videodisc-Gerät** mit dem folgenden Befehl öffnen:


```C++
    mciSendString("open videodisc", lpszReturnString, 
        lstrlen(lpszReturnString), NULL);
```



In diesem Fall ist "videodisc" der Gerätename aus der Registrierung oder der \[ mci-Abschnitt \] von SYSTEM.INI.

-   Geben Sie den tatsächlichen Namen des Gerätetreibers an. Das Öffnen eines Geräts mithilfe des Gerätetreiberdateinamens macht die Anwendung gerätespezifisch und kann verhindern, dass die Anwendung ausgeführt wird, wenn sich die Systemkonfiguration ändert. Wenn Sie einen Dateinamen verwenden, müssen Sie nicht den vollständigen Pfad oder die Dateinamenerweiterung angeben. MCI geht davon aus, dass treiber sich in einem Systemverzeichnis befinden und über die verfügen. DRV-Dateinamenerweiterung.

Verbundgeräte umfassen **Waveaudio-** und **Sequencergeräte.** Die Daten für ein verbundes Gerät werden manchmal als *Geräteelement* bezeichnet. Dieses Dokument bezieht sich jedoch im Allgemeinen auf diese Daten als Datei, obwohl die Daten in einigen Fällen möglicherweise nicht als Datei gespeichert werden.

Es gibt drei Möglichkeiten, ein Verbundgerät zu öffnen:

-   Geben Sie nur den Gerätenamen an. Auf diese Weise können Sie ein verbundes Gerät öffnen, ohne einen Dateinamen zuzuordnen. Die meisten zusammengesetzten Geräte verarbeiten nur die [**Befehle MCI**](capability.md) [**\_ GETDEVCAPS**](mci-getdevcaps.md)und [**Close**](close.md) [**(MCI \_ CLOSE),**](mci-close.md)wenn sie auf diese Weise geöffnet werden.
-   Geben Sie nur den Dateinamen an. Der Gerätename wird anhand der Zuordnungen in der Registrierung bestimmt.
-   Geben Sie den Dateinamen und den Gerätenamen an. MCI ignoriert die Einträge in der Registrierung und öffnet den angegebenen Gerätenamen.

Um eine Datendatei einem bestimmten Gerät zuzuordnen, können Sie den Dateinamen und den Gerätenamen angeben. Mit dem folgenden Befehl wird beispielsweise das **Waveaudio-Gerät** mit dem Dateinamen MYVOICE geöffnet. Snd:


```C++
mciSendString("open myvoice.snd type waveaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



In der Befehlszeichenfolgen-Schnittstelle können Sie die Gerätenamensspezifikation auch mithilfe des alternativen Ausrufezeichenformats abkürzen, wie mit dem [**open-Befehl**](open.md) dokumentiert.

## <a name="opening-a-device-using-the-filename-extension"></a>Öffnen eines Geräts mithilfe der Dateinamenerweiterung

Wenn der Befehl [**open**](open.md) ([**MCI \_ OPEN**](mci-open.md)) nur den Dateinamen angibt, verwendet MCI die Dateinamenerweiterung, um das entsprechende Gerät aus der Liste in der Registrierung oder im \[ Abschnitt mci-Erweiterungen \] der SYSTEM.INI-Datei auszuwählen. Die Einträge im \[ Abschnitt mci-Erweiterungen \] verwenden das folgende Format:

*Gerätename der \_ Dateinamenerweiterung*  =  *\_*

MCI verwendet implizit *den \_ Gerätenamen,* wenn die Erweiterung gefunden wird und wenn im **befehl open** kein Gerätename angegeben wurde.

Das folgende Beispiel zeigt einen typischen \[ \] mci-Erweiterungsabschnitt:


```C++
[mci extensions]
wav=waveaudio
mid=sequencer
rmi=sequencer
```



Mithilfe dieser Definitionen öffnet MCI das **Waveaudio-Gerät,** wenn der folgende Befehl ausgegeben wird:


```C++
mciSendString("open train.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="new-data-files"></a>Neue Datendateien

Um eine neue Datendatei zu erstellen, geben Sie einfach einen leeren Dateinamen an. MCI speichert eine neue Datei erst, wenn Sie sie mit dem Befehl [**save**](save.md) ([**MCI \_ SAVE**](mci-save.md)) speichern. Beim Erstellen einer neuen Datei müssen Sie einen Gerätealias mit dem [**befehl open**](open.md) ([**MCI \_ OPEN**](mci-open.md)) einschließen.

Im folgenden Beispiel wird eine neue **waveaudio-Datei** geöffnet, die Aufzeichnung gestartet und beendet, die Datei gespeichert und geschlossen:


```C++
mciSendString("open new type waveaudio alias capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("record capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("stop capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("save capture orca.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="sharable-devices"></a>Sharable Devices

Mit dem Flag "sharable" (MCI \_ OPEN \_ SHAREABLE) des [**open**](open.md) -Befehls [**(MCI \_ OPEN**](mci-open.md)) können mehrere Anwendungen gleichzeitig auf dasselbe Gerät (oder die gleiche Datei) und die gleiche Geräteinstanz zugreifen. Wenn Ihre Anwendung ein Gerät oder eine Datei als trennbar öffnet, können andere Anwendungen auch darauf zugreifen, indem sie es als trennbar öffnen. Das freigegebene Gerät oder die datei gibt jeder Anwendung die Möglichkeit, die Parameter zu ändern, die ihren Betriebszustand bestimmen. Jedes Mal, wenn ein Gerät oder eine Datei als trennbar geöffnet wird, gibt MCI einen eindeutigen Gerätebezeichner zurück, obwohl die Bezeichner auf dieselbe Instanz verweisen.

Wenn Ihre Anwendung ein Gerät oder eine Datei öffnet, ohne anzugeben, dass es trennbar ist, kann keine andere Anwendung darauf zugreifen, bis Ihre Anwendung es schließt. Wenn ein Gerät nur eine geöffnete Instanz unterstützt, schlägt der **Open-Befehl** fehl, wenn Sie das Trennzeichen angeben.

Wenn Ihre Anwendung ein Gerät öffnet und angibt, dass es trennbar ist, sollte Ihre Anwendung keine Annahmen über den Zustand dieses Geräts treffen. Ihre Anwendung muss möglicherweise Änderungen kompensieren, die von anderen Anwendungen vorgenommen wurden, die auf das Gerät zugreifen.

Die meisten Verbunddateien sind nicht trennbar. Sie können jedoch mehrere Dateien öffnen, oder Sie können eine einzelne Datei mehrmals öffnen. Wenn Sie eine einzelne Datei mehrmals öffnen, erstellt MCI jeweils eine unabhängige Instanz, wobei jede Instanz einen eindeutigen Betriebsstatus aufweist.

Wenn Sie mehrere Instanzen einer Datei öffnen, müssen Sie jedem einen eindeutigen Gerätebezeichner zuweisen. Sie können wie im folgenden Abschnitt beschrieben einen Alias verwenden, um jeder Datei einen eindeutigen Namen zuzuweisen.

 

 