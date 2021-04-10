---
title: App-Manifest (ausführbare Datei)
description: App-Manifest (ausführbare Datei)
ms.assetid: F46F33A6-0B2F-4086-9C6D-4AD43C26BCD3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de6f5a1d26af4b8ac6314655013ed56275bf7d73
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104039735"
---
# <a name="app-executable-manifest"></a>App-Manifest (ausführbare Datei)

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>BESCHREIBUNG

Der Kompatibilitäts Abschnitt des in Windows eingeführten App-Manifests (ausführbare Datei) unterstützt das Betriebssystem bei der Ermittlung der Windows-Versionen, für die eine APP entworfen wurde. Außerdem ermöglicht das App-Manifest Windows, das von der APP erwartete Verhalten basierend auf der Version von Windows, die die APP als Ziel hat, bereitzustellen.

Im Kompatibilitäts Abschnitt des Manifests können Windows neue Verhaltensweisen für neu erstellte Software bereitstellen und gleichzeitig die Kompatibilität vorhandener Software beibehalten. In diesem Abschnitt wird Windows auch bei zukünftigen Versionen von Windows mehr Kompatibilität bereitgestellt. Beispielsweise wird eine APP, die Unterstützung nur für Windows 8 im Kompatibilitäts Abschnitt deklariert, weiterhin Windows 8-Verhalten in zukünftigen Versionen von Windows empfangen.

## <a name="manifestation"></a>Ausstrahlung

Apps ohne Kompatibilitäts Abschnitt in ihrem Manifest haben standardmäßig Windows Vista-Verhalten unter Windows 7 und Windows 8 und zukünftigen Windows-Versionen. Beachten Sie, dass diese Manifestressourcen von Windows XP und Windows Vista ignoriert werden und keine Auswirkung darauf besteht.

Diese Windows-Komponenten bieten unterschiedliche Verhaltensweisen auf der Grundlage des Kompatibilitäts Abschnitts:

**Remote Prozedur Aufruf (RPC)-Standard Thread Pool**

-   Windows 8 und Windows 7: um die Skalierbarkeit zu verbessern und die Thread Anzahl zu reduzieren, wechselt der RPC zum NT-Thread Pool (Standard Pool). Für Windows Vista hat RPC einen privaten Thread Pool verwendet:

    -   Für Binärdateien, die für Windows 7 und spätere Versionen von Windows kompiliert wurden, wird der Standard Pool verwendet.
    -   Wenn \_ RpcMgmtEnableDedicatedThreadPool aufgerufen wird, bevor eine RPC-API aufgerufen wird, wird der private Thread Pool verwendet (Vista-Verhalten).
    -   Wenn ich \_ RpcMgmtEnableDedicatedThreadPool nach einem RPC-Aufruf aufgerufen wird, wird der Standard Pool verwendet \_ . i RpcMgmtEnableDedicatedThreadPool gibt den Fehler 1764 zurück, und der angeforderte Vorgang wird nicht unterstützt.

-   Windows Vista (Standard): für Binärdateien, die für Windows Vista und frühere Versionen von Windows kompiliert wurden, wird der private Pool verwendet.

**DirectDraw-Sperre**

-   Windows 8 und Windows 7: für Windows 7 und höhere Versionen des Betriebssystems manifestierte Apps können die Lock-API in ddraw nicht aufrufen, um den primären Desktop-Video Puffer zu sperren. Dies führt zu einem Fehler, und es wird ein NULL-Zeiger für das primäre Replikat zurückgegeben. Dieses Verhalten wird auch dann erzwungen, wenn Desktopfenster-Manager Komposition nicht aktiviert ist. Apps, deren Kompatibilität für Windows 7 und höher deklariert wurde, dürfen den primären Video Puffer nicht zum renderingsperren sperren.
-   Windows Vista (Standard): Apps können eine Sperre für den primären Video Puffer erhalten, da ältere apps von diesem Verhalten abhängig sind. Wenn Sie die app ausführen, wird Desktopfenster-Manager deaktiviert.

**DirectDraw-Bitblock Übertragung (BitBLT) zum primären Replikat ohne Clipping-Fenster**

-   Windows 8 und Windows 7: für Windows 7 und höhere Versionen von Windows dargestellte apps werden daran gehindert, ein BitBlt für den primären Desktop-Video Puffer ohne clippingfenster auszuführen. Dies führt zu einem Fehler, und der BitBLT-Bereich wird nicht gerendert. Windows erzwingt dieses Verhalten auch dann, wenn Sie Desktopfenster-Manager Komposition nicht aktivieren. Apps, deren Kompatibilität für Windows 7 und höher deklariert wurde, müssen ein BitBLT in einem clippingfenster ausführen.
-   Windows Vista (Standard): apps müssen in der Lage sein, ein BitBLT-Element ohne clippingfenster auf das primäre Replikat auszuführen, da Legacy-apps von diesem Verhalten abhängig sind. Wenn Sie diese APP ausführen, wird die Desktopfenster-Manager deaktiviert.

**Ge-verlappedresult-API**

-   Windows 8 und Windows 7: löst eine Racebedingung aus, bei der eine Multithread-APP, die **gedeverlappedresult** verwendet, zurückgeben kann, ohne das Ereignis in der überlappenden Struktur zurückzusetzen. Dadurch wird der nächste Aufrufe dieser Funktion vorzeitig zurückgegeben.
-   Windows Vista (Standard): stellt das Verhalten mit der Racebedingung bereit, von der Apps möglicherweise abhängig sind. Apps, die dieses Race vor dem Windows 7-Verhalten vermeiden müssen, sollten auf das überlappende Ereignis warten und bei Signalisierung gedeverlappedresult mit bwait = = false aufrufen.

**Status von shelldesigns im Modus mit hohem Kontrast**

-   Windows 8: gibt den tatsächlichen Themenstatus für im Modus mit hohem Kontrast zurück.
-   Windows 7: gibt das Design im Modus mit hohem Kontrast als nicht verfügbar zurück, da DWM noch immer eingeschaltet ist.
-   Windows Vista (Standard): gibt das Design im Modus mit hohem Kontrast als nicht verfügbar zurück, da DWM noch immer aktiviert ist.

**Shell IPersistFile:: Save-Methode**

-   Windows 8: cshelllink:: Save bestimmt jetzt, ob der IPersistFile-Handler mit einem relativen Pfad Argument aufgerufen wird, und schlägt den Aufruf fehl, wenn dies der Fall ist.

    Die [öffentliche Dokumentation](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) , die dieses Verhalten beschreibt, gibt an, dass das Pfad Argument ein absoluter Pfad sein muss:

-   Windows 7 und früher (Standard): cshelllink:: Save bestimmt nicht, ob der IPersistFile-Handler eine relative Pfad Überprüfung sendet und ermöglicht, dass apps weiterhin mit absoluten oder relativen Pfaden arbeiten können.

**Programmkompatibilitäts-Assistent (PCA)**

-   Windows 8: apps mit dem Kompatibilitäts Abschnitt erhalten keine PCA-Entschärfung.
-   Windows 7: apps mit dem Kompatibilitäts Abschnitt werden auf mögliche Kompatibilitätsprobleme bei Windows 8-Änderungen nachverfolgt (in diesem Dokument beschrieben).
-   Windows Vista (Standard): apps, die in bestimmten Situationen nicht ordnungsgemäß installiert werden oder während der Laufzeit abstürzen, erhalten die PCA-Entschärfung. Weitere Informationen finden Sie im Abschnitt "Resources" (Ressourcen).

## <a name="leveraging-feature-capabilities"></a>Nutzen von Featurefunktionen

Aktualisieren Sie das App-Manifest mit den neuesten Kompatibilitätsinformationen für die Betriebssystemunterstützung. In diesem Abschnitt werden die Ergänzungen des Manifests beschrieben:

**Namespace:** Compatibility. v1 (xmlns = "urn: Schemas-Microsoft-com: Compatibility. v1" >)

**Abschnitts Name:** Kompatibilität (neuer Abschnitt)

**SupportedOS:** GUID des unterstützten Betriebssystems: die GUIDs, die den unterstützten Betriebssystemen zugeordnet sind:

-   {e2011457-1546-43c5-a5fe-008deee3d3f0}

    für **Windows Vista**: Dies ist der Standardwert für den switchbackkontext.

-   {35138b9a-5d96-4f BD-8e2d-a2440225b93a}

    für **Windows 7**: apps, die diesen Wert im App-Manifest festlegen, erhalten das Windows 7-Verhalten.

-   {4a2b28e3-53b9-4441-ba9c-d69d4a4a6e38}

    für **Windows 8**: apps, die diesen Wert im Anwendungs Manifest festlegen, erhalten das Windows 8-Verhalten.

Microsoft generiert und veröffentlicht GUIDs für zukünftige Windows-Versionen nach Bedarf.

Ein XML-Beispiel für ein aktualisiertes Manifest:

> [!Note]  
> Beim Attribut-und Tagnamen im App-Manifest wird die Groß-/Kleinschreibung beachtet.

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
    <application> 
        <!--The ID below indicates app support for Windows Vista -->
        <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates app support for Windows 7 -->
        <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--The ID below indicates app support for Windows 8 -->
        <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
    </application> 
</compatibility>
</assembly>
```



Die GUIDs für alle Betriebssysteme im vorherigen Beispiel bieten Unterstützung auf der Basis von. Apps, die mehrere Plattformen unterstützen, benötigen für jede Plattform keine separaten Manifeste.

## <a name="tests"></a>Tests

Eine APP kann mehrere unterstützte Betriebssystem-IDs angeben. Sie sollten eine unterstützte Betriebssystem-ID hinzufügen, wenn Sie die APP auf diesem Betriebssystem getestet oder getestet haben. Diese Einträge werden von Windows Vista und früheren Betriebssystemversionen nicht beachtet. Ab Windows 7 wählt Windows die höchste Versions-GUID im Manifest bis zur laufenden Windows-Version aus und unterstützt die APP auf dieser Ebene. So überprüfen Sie, ob die APP mit dem neuen Kompatibilitäts Abschnitt des App-Manifests funktioniert:

1.  Testen Sie die APP mit dem neuen Kompatibilitäts Abschnitt und SupportedOS ID = {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}, um sicherzustellen, dass die APP mit dem aktuellen Windows 8-Verhalten ordnungsgemäß funktioniert.
2.  Testen Sie die APP mit dem neuen Kompatibilitäts Abschnitt und SupportedOS ID = {35138b9a-5d96-4fbd-8e2d-a2440225f93a}, um sicherzustellen, dass die APP unter Verwendung des Windows 7-Verhaltens ordnungsgemäß funktioniert.
3.  Testen Sie die APP mit dem neuen Kompatibilitäts Abschnitt und SupportedOS ID = {e2011457-1546-43c5-a5fe-008deee3d3f0}, um sicherzustellen, dass die APP mit dem Windows Vista-Verhalten ordnungsgemäß funktioniert.

## <a name="resources"></a>Ressourcen

-   [Queryactctxw-Funktion](../sbscs/application-manifests.md)
-   [UAC-Manifest](/previous-versions/bb756929(v=msdn.10))
-   [Anwendungs Manifeste für Windows-Anwendungen](../sbscs/application-manifests.md)
-   [Desktopfenster-Manager (DWM)](../dwm/dwm-overview.md)
-   [Aktualisierung des Kontext Konflikts](https://support.microsoft.com/kb/978637)
-   [Programmkompatibilitäts-Assistent](/previous-versions/bb756937(v=msdn.10))

 

 