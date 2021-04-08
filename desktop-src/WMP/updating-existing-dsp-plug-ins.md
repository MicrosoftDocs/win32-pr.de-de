---
title: Aktualisieren vorhandener DSP-Plug-ins
description: Aktualisieren vorhandener DSP-Plug-ins
ms.assetid: 0525030e-eb30-41a0-8191-4a5727736857
keywords:
- Windows Media Player-Plug-ins, digitale Signalverarbeitung (DSP)
- Plug-ins, digitale Signalverarbeitung (DSP)
- Plug-Ins für die digitale Signalverarbeitung, aktualisieren
- DSP-Plug-ins, aktualisieren
- Versionen von Windows Media Player, DSP-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393cde356e0d86bb920825e731bb12ee0b7c2818
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723472"
---
# <a name="updating-existing-dsp-plug-ins"></a>Aktualisieren vorhandener DSP-Plug-ins

DSP-Plug-ins, die vor der Veröffentlichung des Windows Media Player 11 SDK erstellt wurden, funktionieren möglicherweise nicht erwartungsgemäß, wenn Windows Media Player 11 unter Windows Vista ausgeführt wird. Um sicherzustellen, dass Kunden, die Windows Media Player 11 unter Windows Vista ausführen, die Plug-Ins verwenden können, müssen Sie einige Änderungen an Ihrem DSP-Plug-in-Code vornehmen, das Projekt neu kompilieren und das aktualisierte Plug-in an Ihre Kunden verteilen.

Projekte, die mit der neuesten Version des Assistenten für Windows Media Player-Plug-Ins erstellt werden, enthalten die erforderlichen Updates. Weitere [Informationen finden Sie unter Updates für den DSP-Plug-in-Assistenten für Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md). (Es empfiehlt sich, den Assistenten auszuführen, um ein neues Beispiel Projekt zu erstellen und dann ein Tool wie Windiff.exe zu verwenden, das in Visual Studio zur Verfügung steht, um die Unterschiede zwischen dem Beispielcode und dem Produktionscode zu untersuchen.)

An allen vorhandenen DSP-Plug-Ins müssen Sie drei wesentliche Änderungen vornehmen:

-   Ändern der Art und Weise, wie das Plug-in registriert wird. Ihr vorhandenes Plug-in registriert das Threading Modell wahrscheinlich als "Apartment". Windows Media Player 11 unter Windows Vista erfordert, dass DSP-Plug-ins das Threading Modell als "beides" registrieren. Sie können dieses Problem beheben, indem Sie den Threading Modell Wert in der Datei " *ProjectName*. RGS" wie folgt ändern:

    ```C++
    val ThreadingModel = s 'Both'
    
    ```

    

    > [!Note]  
    > Durch Angeben des Threading Modells als "both" wird jede Serialisierung entfernt, die com für Aufrufe von benutzerdefinierten Schnittstellen bereitstellt. Wenn Sie benutzerdefinierte Schnittstellen aus mehreren Threads aufrufen, müssen Sie diese Serialisierung selbst bereitstellen.

     

    Windows Media Player 11 stellt sicher, dass Aufrufe der DMO-Schnittstellen ordnungsgemäß serialisiert werden.

    1.  Fügen Sie die folgenden Befehle hinzu [: wmpregisterplayerplayerplayerplayerplayerplayerplayerplayerplayerplayerplug](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) -in mit einem neuen Plug-in-Typ: [](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) WMP \_ PlugInType \_ DSP \_ oudeberproc in DllRegisterServer und DllUnregisterServer in der Datei *projectnamedll*. cpp. Weitere Informationen finden Sie auf den Referenzseiten für diese Methoden.
    2.  Erstellen und verteilen Sie eine Proxy-/Stub-DLL, um das COM-Marshalling einer beliebigen benutzerdefinierten Schnittstelle zu ermöglichen, die von der Plug-in-Klasse implementiert oder erstellt wird. Eine benutzerdefinierte Schnittstelle ist eine beliebige proprietäre Schnittstelle, die Sie für die Verwendung durch das Plug-in-Objekt definieren und implementieren. Dies schließt die benutzerdefinierte Schnittstelle ein, die von der Eigenschaften Seite verwendet wird, wenn Sie eine solche bereitgestellt haben, kann jedoch auch Schnittstellen enthalten, die eine Verbindung mit Benutzeroberflächen-Plug-ins herstellen Ein Beispiel für eine benutzerdefinierte Schnittstelle, die vom Plug-in-Assistenten erstellt wurde, ist *iprojectname*. Beispiele für Schnittstellen, die keine benutzerdefinierten Schnittstellen sind, sind **imediaobject** und **iwmppluginenable**.

Wenn Ihr DSP-Plug-in Audioprozesse verarbeitet, müssen Sie auch Unterstützung für die folgenden neuen Audioformate hinzufügen:

-   "Wave \_ Format \_ IEEE \_ float"
-   Das Wave- \_ Format ist \_ erweiterbar mit dem unter Format "ksdataformat"- \_ Untertyp \_ IEEE \_ float.

Wenn Ihr DSP-Plug-in Video verarbeitet, müssen Sie Unterstützung für das NV12-Videoformat hinzufügen.

Ein Beispiel für die Verarbeitung dieser Format Typen finden Sie im Beispiel für das Audio-oder Video DSP-Plug-in, das vom Assistenten erstellt wird.

## <a name="about-the-proxystub-project"></a>Informationen zum Proxy-/Stubprojekt

Möglicherweise ist die einfachste Möglichkeit, ein Proxy-/Stub-DLL-Projekt für Ihr DSP-Plug-in zu erstellen, den DSP-Plug-in-Assistenten auszuführen. Dadurch wird ein Beispiel für ein Proxy-/Stubprojekt erstellt, das Sie ändern können, um mit vorhandenem Code zu arbeiten. Sie müssen die folgenden Änderungen vornehmen:

1.  Entfernen Sie alle vorhandenen Definitionen für Ihre benutzerdefinierten Schnittstellen aus Ihrem Code. Der DSP-Plug-in-Assistent aus dem Windows Media Player 10 SDK hat z. b. die *iprojectname* -Schnittstellen Definition in der Datei " *ProjectName*. h" mithilfe des Schlüssel Worts " **Interface** " erstellt.
2.  Definieren Sie die benutzerdefinierten Schnittstellen in der IDL-Datei des Proxy-/stubprojekts.
3.  Erstellen Sie das Proxy-/Stubprojekt vor dem Hauptprojekt. Sie können Visual Studio so konfigurieren, dass dies automatisch geschieht, wenn beide Projekte Teil derselben Projekt Mappe sind.
4.  Der mittlerer l-Compiler erstellt eine neue Header Datei mit einem Namen im Format *ProjectName* \_ h.h. Sie müssen diesen Header in das Hauptprojekt (in *ProjectName*. h) einschließen. Sie enthält die Definitionen für Ihre benutzerdefinierten Schnittstellen.

## <a name="distributing-the-updated-plug-in"></a>Das aktualisierte Plug-in wird verteilt.

Sie können das aktualisierte Plug-in genau so wie in der Vergangenheit auf den Computern Ihrer Benutzer installieren. Sie müssen jetzt jedoch auch die Proxy-/Stub-DLL verteilen und registrieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Übersicht über den DSP-Plug-in-Entwickler**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




