---
title: Aktualisieren vorhandener DSP-Plug-Ins
description: Aktualisieren vorhandener DSP-Plug-Ins
ms.assetid: 0525030e-eb30-41a0-8191-4a5727736857
keywords:
- Windows Media Player Plug-Ins, digitale Signalverarbeitung (DSP)
- Plug-Ins, digitale Signalverarbeitung (DSP)
- Plug-Ins für die digitale Signalverarbeitung, Aktualisieren
- DSP-Plug-Ins, Aktualisieren
- Versionen von Windows Media Player,DSP-Plug-Ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725a7a752206f4d321af9deb106df82c40b677dd719182660c5940cac4788244
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122730"
---
# <a name="updating-existing-dsp-plug-ins"></a>Aktualisieren vorhandener DSP-Plug-Ins

DSP-Plug-Ins, die vor der Veröffentlichung des Windows Media Player 11 SDK erstellt wurden, funktionieren möglicherweise nicht wie erwartet, wenn Windows Media Player 11 unter Windows Vista ausgeführt wird. Um sicherzustellen, dass Kunden, die Windows Media Player 11 unter Windows Vista ausführen, Ihre Plug-Ins verwenden können, müssen Sie einige Änderungen am DSP-Plug-In-Code vornehmen, Ihr Projekt neu kompilieren und das aktualisierte Plug-In an Ihre Kunden verteilen.

Projekte, die mit der neuesten Version des Windows Media Player-Plug-In-Assistenten erstellt wurden, enthalten die erforderlichen Updates. Weitere [Informationen finden Sie unter Updates des DSP-Plug-In-Assistenten Windows Media Player 11.](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md) (Es ist eine gute Idee, den Assistenten zum Erstellen eines neuen Beispielprojekts zu verwenden und dann ein Tool wie Windiff.exe zu verwenden, das im Visual Studio enthalten ist, um die Unterschiede zwischen dem Beispielcode und Ihrem Produktionscode zu untersuchen.)

Es gibt drei Hauptänderungen, die Sie an vorhandenen DSP-Plug-Ins vornehmen müssen:

-   Ändern Sie die Art und Weise, in der das Plug-In registriert wird. Ihr vorhandenes Plug-In registriert das Threadingmodell wahrscheinlich als "Apartment". Windows Media Player 11 auf Windows Vista ausgeführt wird, müssen DSP-Plug-Ins das Threadingmodell als "Beide" registrieren. Sie können dies beheben, indem Sie den Wert des Threadingmodells in der RGS-Datei ihres Projektnamens wie folgt ändern:

    ```C++
    val ThreadingModel = s 'Both'
    
    ```

    

    > [!Note]  
    > Wenn Sie das Threadingmodell als "Beide" angeben, werden alle Serialisierungen entfernt, die COM für Aufrufe benutzerdefinierter Schnittstellen bietet. Wenn Sie ihre benutzerdefinierten Schnittstellen von mehreren Threads aufrufen, müssen Sie diese Serialisierung selbst bereitstellen.

     

    Windows Media Player 11 stellt sicher, dass Aufrufe DMO Schnittstellen ordnungsgemäß serialisiert werden.

    1.  Fügen Sie Aufrufe von [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) und [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin mit](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) einem neuen Plug-In-Typ hinzu: WMP \_ PLUGINTYPE \_ DSP \_ OUTOFPROC in DllRegisterServer und DllUnregisterServer in Ihrer CPP-Datei *projectnamedll.* Weitere Informationen zu diesen Methoden finden Sie auf den Referenzseiten.
    2.  Erstellen und verteilen Sie eine Proxy-/Stub-DLL, um das COM-Marshalling beliebiger benutzerdefinierter Schnittstellen zu ermöglichen, die in der Plug-In-Klasse implementiert oder erstellt wurden. Eine benutzerdefinierte Schnittstelle ist jede proprietäre Schnittstelle, die Sie für die Verwendung durch das Plug-In-Objekt definieren und implementieren. Dies schließt die benutzerdefinierte Schnittstelle ein, die von Ihrer Eigenschaftenseite verwendet wird, wenn Sie eine bereitgestellt haben, kann aber auch Schnittstellen enthalten, die z. B. eine Verbindung mit Benutzeroberflächen-Plug-Ins herstellen. Ein Beispiel für eine benutzerdefinierte Schnittstelle, die vom Plug-In-Assistenten erstellt wurde, ist *Iprojectname.* Beispiele für Schnittstellen, die keine benutzerdefinierten Schnittstellen sind, sind **IMediaObject** und **IWMPPluginEnable.**

Wenn Ihr DSP-Plug-In Audio verarbeitet, müssen Sie auch Unterstützung für die folgenden neuen Audioformate hinzufügen:

-   \_WAVE-FORMAT \_ IEEE \_ FLOAT
-   WAVE \_ FORMAT \_ EXTENSIBLE mit dem Unterformat KSDATAFORMAT \_ SUBTYPE IEEE \_ \_ FLOAT.

Wenn Ihr DSP-Plug-In Videos verarbeitet, müssen Sie Unterstützung für das NV12-Videoformat hinzufügen.

Ein Beispiel für die Verarbeitung dieser Formattypen finden Sie im Beispiel-DSP-Plug-In für Audio oder Video, das der Assistent erstellt.

## <a name="about-the-proxystub-project"></a>Informationen zum Proxy/Stub-Project

Die einfachste Möglichkeit, ein Proxy-/Stub-DLL-Projekt für Ihr DSP-Plug-In zu erstellen, ist die Ausführung des DSP-Plug-In-Assistenten. Dadurch wird ein Beispielproxy-/Stubprojekt erstellt, das Sie ändern können, um mit ihrem vorhandenen Code zu arbeiten. Sie müssen die folgenden Änderungen vornehmen:

1.  Entfernen Sie alle vorhandenen Definitionen für Ihre benutzerdefinierten Schnittstellen aus dem Code. Beispielsweise hat der DSP-Plug-In-Assistent aus dem Windows Media Player 10 SDK die *Iprojectname-Schnittstellendefinition* in der *Projektnamen-H-Datei* mithilfe des Schlüsselworts **interface** erstellt.
2.  Definieren Sie Ihre benutzerdefinierten Schnittstellen in der IDL-Datei des Proxy-/Stubprojekts.
3.  Erstellen Sie das Proxy-/Stubprojekt vor Dem Hauptprojekt. Sie können Visual Studio dies automatisch konfigurieren, wenn beide Projekte Teil derselben Projektmappe sind.
4.  Der MIDL-Compiler erstellt eine neue Headerdatei mit einem Namen im Format *Projektname* \_ h.h. Sie müssen diesen Header in Das Hauptprojekt (in *Projektname .h)* enthalten. Sie enthält die Definitionen für Ihre benutzerdefinierten Schnittstellen.

## <a name="distributing-the-updated-plug-in"></a>Verteilen des aktualisierten Plug-Ins

Sie können das aktualisierte Plug-In genau wie in der Vergangenheit auf den Computern Ihrer Benutzer installieren. Jetzt müssen Sie jedoch auch die Proxy-/Stub-DLL verteilen und registrieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Übersicht über DSP-Plug-In-Entwickler**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




