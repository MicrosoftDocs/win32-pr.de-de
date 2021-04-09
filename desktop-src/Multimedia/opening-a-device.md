---
title: Öffnen eines Geräts
description: Öffnen eines Geräts
ms.assetid: d4881d32-e8b7-45e6-b00b-b4cd69b738f1
keywords:
- MCI_OPEN-Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd975b0dd5004fb4b1209003568b7fd5901cfc4e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038839"
---
# <a name="opening-a-device"></a>Öffnen eines Geräts

Bevor Sie ein Gerät verwenden, müssen Sie es mit dem [**geöffneten**](open.md) Befehl ([**MCI \_ Open**](mci-open.md)) initialisieren. Mit diesem Befehl wird der Treiber in den Arbeitsspeicher geladen (sofern er nicht bereits geladen wurde), und der Geräte Bezeichner wird abgerufen, den Sie zum Identifizieren des Geräts in nachfolgenden MCI-Befehlen verwenden. Sie sollten den Rückgabewert der Funktion " [**mciSendString**](/previous-versions//dd757161(v=vs.85)) " oder " [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) " überprüfen, bevor Sie einen neuen Geräte Bezeichner verwenden, um sicherzustellen, dass der Bezeichner gültig ist. (Sie können auch einen Geräte Bezeichner mithilfe der Funktion " [**mcigetdebug Eid**](/previous-versions//dd757156(v=vs.85)) " abrufen.)

Wie bei allen MCI-befehlsnachrichten verfügt **MCI \_ Open** über eine zugeordnete Struktur. Diese Strukturen werden manchmal als *Parameter Blöcke* bezeichnet. Die Standardstruktur für **MCI \_ Open** ist [**MCI \_ Open- \_ Parser**](mci-open-parms.md). Bestimmte Geräte (z. b. *Wellenform* und *Overlay*) haben erweiterte Strukturen (z. b. [**MCI \_ Wave \_ Open \_**](mci-wave-open-parms.md) -Parameter und [**MCI- \_ Oly- \_ Open \_**](mci-ovly-open-parms.md)-Parameter), um zusätzliche optionale Parameter zu bieten. Wenn Sie diese zusätzlichen Parameter nicht benötigen, können Sie die MCI-Struktur mit **\_ offenen \_ para** Metern mit einem beliebigen MCI-Gerät verwenden.

Die Anzahl der Geräte, die Sie öffnen können, ist nur durch die Menge des verfügbaren Arbeitsspeichers beschränkt.

## <a name="using-an-alias"></a>Verwenden eines Alias

Wenn Sie ein Gerät öffnen, können Sie das Flag "Alias" verwenden, um einen Geräte Bezeichner für das Gerät anzugeben. Mit diesem Flag können Sie eine kurze Geräte-ID für Verbund Geräte mit langen Dateinamen zuweisen, und Sie können mehrere Instanzen derselben Datei oder eines Geräts öffnen.

Der folgende Befehl weist z. b. den Geräte Bezeichner "birdcall" dem langen Dateinamen "C: \\ nabunds \\ Sounds \\ mockmtng" zu. Wave


```C++
mciSendString(
    "open c:\nabirds\sounds\mockmtng.wav type waveaudio alias birdcall", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



In der befehlsnachrichten Schnittstelle geben Sie einen Alias an, indem Sie den **lpstraualias** -Member der [**geöffneten MCI-Struktur \_ Öffnen \_**](mci-open-parms.md) .

## <a name="specifying-a-device-type"></a>Angeben eines Gerätetyps

Wenn Sie ein Gerät öffnen, können Sie das Flag "Type" verwenden, um auf einen Gerätetyp und nicht auf einen bestimmten Gerätetreiber zu verweisen. Im folgenden Beispiel wird die Waveform-Audiodatei C: \\ Windows- \\ Chimes geöffnet. WAV (mit dem Flag "Type", um den **waveaudiogerätetyp** anzugeben) und weist den Alias "Chimes" zu:


```C++
mciSendString(
    "open c:\windows\chimes.wav type waveaudio alias chimes", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



In der befehlsnachrichten Schnittstelle wird die Funktionalität des "Type"-Flags durch das **lpstraudevicetype** -Element der [**MCI \_ Open \_**](mci-open-parms.md) -Parameterstruktur bereitgestellt.

## <a name="simple-and-compound-devices"></a>Einfache und Verbund Geräte

MCI klassifiziert Gerätetreiber als *Verbund* oder *einfach*. Treiber für Verbund Geräte erfordern den Namen einer Datendatei für die Wiedergabe. Treiber für einfache Geräte nicht.

Einfache Geräte sind **CDAudio** -und **Videodisk** -Geräte. Es gibt zwei Möglichkeiten, um einfache Geräte zu öffnen:

-   Geben Sie einen Zeiger auf eine NULL-terminierte Zeichenfolge an, die den Gerätenamen aus der Registrierung oder der SYSTEM.INI Datei enthält.

    Beispielsweise können Sie ein **Videodisk** -Gerät mit dem folgenden Befehl öffnen:


```C++
    mciSendString("open videodisc", lpszReturnString, 
        lstrlen(lpszReturnString), NULL);
```



In diesem Fall ist "Videodisk" der Gerätename aus der Registrierung oder der \[ MCI- \] Abschnitt der SYSTEM.INI.

-   Geben Sie den tatsächlichen Namen des Gerätetreibers an. Wenn Sie ein Gerät mit dem Gerätetreiber-Dateinamen öffnen, wird die Anwendung jedoch gerätespezifisch, und die Ausführung der Anwendung kann verhindert werden, wenn sich die Systemkonfiguration ändert. Wenn Sie einen Dateinamen verwenden, müssen Sie nicht den kompletten Pfad oder die Dateinamenerweiterung angeben. MCI geht davon aus, dass sich Treiber in einem System Verzeichnis befinden und über verfügen. DRV-Dateinamenerweiterung.

Verbund Geräte umfassen **waveaudiogeräte** und **Sequencer** -Geräte. Die Daten für ein Verbund Gerät werden manchmal als *Geräte Element* bezeichnet. Dieses Dokument bezieht sich jedoch im Allgemeinen auf diese Daten als Datei, auch wenn die Daten in einigen Fällen nicht als Datei gespeichert werden.

Es gibt drei Möglichkeiten, ein Verbund Gerät zu öffnen:

-   Geben Sie nur den Gerätenamen an. Auf diese Weise können Sie ein Verbund Gerät öffnen, ohne einen Dateinamen zuzuordnen. Bei den meisten Verbund Geräten werden nur die [**Funktionen**](capability.md) ([**MCI \_ getdevcaps**](mci-getdevcaps.md)) und [**Close**](close.md) ([**MCI \_ Close**](mci-close.md)) verarbeitet, wenn Sie auf diese Weise geöffnet werden.
-   Geben Sie nur den Dateinamen an. Der Gerätename wird aus den Zuordnungen in der Registrierung ermittelt.
-   Geben Sie den Dateinamen und den Gerätenamen an. MCI ignoriert die Einträge in der Registrierung und öffnet den angegebenen Gerätenamen.

Wenn Sie einer Datendatei ein bestimmtes Gerät zuordnen möchten, können Sie den Dateinamen und den Gerätenamen angeben. Der folgende Befehl öffnet z. b. das **Waveaudiogerät** mit dem Dateinamen myvoice. SND


```C++
mciSendString("open myvoice.snd type waveaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



In der Befehls Zeichenfolgen-Schnittstelle können Sie auch die Geräte namens Spezifikation mit dem alternativen Ausrufezeichen Format abkürzen, wie mit dem [**Open**](open.md) -Befehl dokumentiert.

## <a name="opening-a-device-using-the-filename-extension"></a>Öffnen eines Geräts mithilfe der Dateinamenerweiterung

Wenn der Befehl [**Öffnen**](open.md) ([**MCI \_ geöffnet**](mci-open.md)) nur den Dateinamen angibt, verwendet MCI die Dateinamenerweiterung, um das entsprechende Gerät aus der Liste in der Registrierung oder im \[ Abschnitt MCI-Erweiterungen \] der SYSTEM.INI Datei auszuwählen. Die Einträge im \[ Abschnitt MCI- \] Erweiterungen verwenden die folgende Form:

*Dateiname \_ Erweiterung*  =  *Geräte \_ Name*

MCI verwendet implizit den *Geräte \_ Namen* , wenn die Erweiterung gefunden wird und ein Gerätename nicht im Befehl " **Öffnen** " angegeben wurde.

Das folgende Beispiel zeigt einen typischen \[ MCI-Erweiterungs \] Abschnitt:


```C++
[mci extensions]
wav=waveaudio
mid=sequencer
rmi=sequencer
```



Mithilfe dieser Definitionen öffnet MCI das **Waveaudiogerät** , wenn der folgende Befehl ausgegeben wird:


```C++
mciSendString("open train.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="new-data-files"></a>Neue Datendateien

Geben Sie einfach einen leeren Dateinamen an, um eine neue Datendatei zu erstellen. MCI speichert eine neue Datei erst, wenn Sie Sie mit dem Befehl [**Speichern**](save.md) ([**MCI- \_ Speicher**](mci-save.md)) speichern. Beim Erstellen einer neuen Datei müssen Sie einen Gerätealias mit dem [**geöffneten**](open.md) Befehl ([**MCI \_ Open**](mci-open.md)) einschließen.

Im folgenden Beispiel wird eine neue **waveaudiodatei** geöffnet, die Aufzeichnung gestartet und beendet und anschließend die Datei gespeichert und geschlossen:


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



## <a name="sharable-devices"></a>Sharable-Geräte

Mit dem Flag "sharable" (MCI \_ Open \_ share able) des [**geöffneten**](open.md) Befehls ([**MCI \_ Open**](mci-open.md)) können mehrere Anwendungen gleichzeitig auf das gleiche Gerät (oder die gleiche Datei) und die Geräte Instanz zugreifen. Wenn Ihre Anwendung ein Gerät oder eine Datei als frei stellbar öffnet, können auch andere Anwendungen darauf zugreifen, indem Sie Sie als Sharable öffnen. Das freigegebene Gerät oder die freigegebene Datei gibt jeder Anwendung die Möglichkeit, die Parameter zu ändern, die den Betriebszustand steuern. Jedes Mal, wenn ein Gerät oder eine Datei als Sharable geöffnet wird, gibt MCI einen eindeutigen Geräte Bezeichner zurück, auch wenn die Bezeichner auf dieselbe Instanz verweisen.

Wenn Ihre Anwendung ein Gerät oder eine Datei öffnet, ohne anzugeben, dass Sie freigegeben werden kann, kann keine andere Anwendung darauf zugreifen, bis Sie von der Anwendung geschlossen wird. Wenn ein Gerät nur eine geöffnete Instanz unterstützt, schlägt der Befehl " **Öffnen** " fehl, wenn Sie das freigegeben-Flag angeben.

Wenn Ihre Anwendung ein Gerät öffnet und angibt, dass Sie freigegeben werden kann, sollte Ihre Anwendung keine Annahmen über den Status dieses Geräts treffen. Die Anwendung muss möglicherweise Änderungen vornehmen, die von anderen Anwendungen, die auf das Gerät zugreifen, vorgenommen werden.

Die meisten Verbund Dateien können nicht freigegeben werden. Sie können jedoch mehrere Dateien öffnen oder eine einzelne Datei mehrmals öffnen. Wenn Sie eine einzelne Datei mehrmals öffnen, erstellt MCI jeweils eine unabhängige Instanz, wobei jede Instanz einen eindeutigen Betriebsstatus aufweist.

Wenn Sie mehrere Instanzen einer Datei öffnen, müssen Sie jedem eine eindeutige Gerätekennung zuweisen. Sie können einen Alias verwenden, wie im folgenden Abschnitt beschrieben, um für jede Datei einen eindeutigen Namen zuzuweisen.

 

 