---
description: .
ms.assetid: f022374d-ea3f-477f-9b59-3188b775ed64
title: Anwendungsmanifest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf4fd1ae8a9f66dafbe65a3db09dd014dbef31e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366213"
---
# <a name="application-manifest"></a>Anwendungsmanifest

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkungen von Features

 **Schweregrad** -niedrig  
**Häufigkeit** -niedrig  





## <a name="description"></a>BESCHREIBUNG

Mit Windows 7 wird ein neuer Abschnitt im Anwendungs Manifest mit dem Namen "Kompatibilität" eingeführt. In diesem Abschnitt können Windows die Versionen von Windows ermitteln, für die eine Anwendung konzipiert wurde, und Windows das Verhalten bereitstellen, das die Anwendung basierend auf der Windows-Version erwartet, auf die die Anwendung ausgerichtet ist.

Im Kompatibilitäts Abschnitt können Windows neuen, von Entwicklern erstellten Software neuen Verhalten bereitstellen und gleichzeitig die Kompatibilität vorhandener Software beibehalten. In diesem Abschnitt wird Windows auch bei zukünftigen Versionen von Windows mehr Kompatibilität bereitgestellt. Beispielsweise wird eine Anwendung, die die Unterstützung nur für Windows 7 im Kompatibilitäts Abschnitt deklariert, weiterhin Windows 7-Verhalten in zukünftigen Versionen von Windows empfangen.

## <a name="manifestation-of-change"></a>Darstellung der Änderung

Anwendungen ohne Kompatibilitäts Abschnitt in ihrem Manifest erhalten standardmäßig Windows Vista-Verhalten unter Windows 7 und zukünftigen Windows-Versionen. Beachten Sie, dass Windows XP und Windows Vista diesen Manifest-Abschnitt ignorieren und keine Auswirkung auf diese haben.

Die folgenden Windows-Komponenten bieten unterschiedliche Verhaltensweisen auf der Grundlage des Kompatibilitäts Abschnitts in Windows 7:

**RPC-Standard Thread Pool**

-   **Windows 7:** Um die Skalierbarkeit zu verbessern und die Thread Anzahl zu reduzieren, wechselt der RPC zum NT-Thread Pool (Standard Pool). Für Windows Vista hat RPC einen privaten Thread Pool verwendet.
    -   Für Binärdateien, die für Win7 kompiliert werden, wird der Standard Pool verwendet.
    -   Wenn \_ RpcMgmtEnableDedicatedThreadPool aufgerufen wird, bevor eine RPC-API aufgerufen wird, wird der private Thread Pool verwendet (Vista-Verhalten).
    -   Wenn ich \_ RpcMgmtEnableDedicatedThreadPool nach einem RPC-Aufruf aufgerufen wird, wird der Standard Pool verwendet. i \_ RpcMgmtEnableDedicatedThreadPool gibt den Fehler 1764 zurück, und der angeforderte Vorgang wird nicht unterstützt.
-   **Windows Vista (Standard):** Für Binärdateien, die für Windows Vista und niedriger kompiliert werden, wird der private Pool verwendet.

**DirectDraw-Sperre**

-   **Windows 7:** Für Windows 7 manifestierte Anwendungen können die Lock-API in ddraw nicht aufrufen, um den primären Desktop-Video Puffer zu sperren. Dies führt zu einem Fehler, und für das primäre Replikat wird ein **null** -Zeiger zurückgegeben. Dieses Verhalten wird auch dann erzwungen, wenn Desktopfenster-Manager Komposition nicht aktiviert ist. Windows 7-kompatible Anwendungen dürfen den primären Video Puffer nicht zum renderingsperren sperren.
-   **Windows Vista (Standard):** Anwendungen können eine Sperre für den primären Video Puffer erhalten, da ältere Anwendungen von diesem Verhalten abhängig sind. Wenn Sie die Anwendung ausführen, wird Desktopfenster-Manager deaktiviert.

**DirectDraw-Bitblock Übertragung (BLT) zum primären Replikat ohne Clipping-Fenster**

-   **Windows 7:** Anwendungen, die für Windows 7 angezeigt werden, werden daran gehindert, BLT auf dem primären Desktop-Video Puffer ohne clippingfenster auszuführen. Dies führt zu einem Fehler, und der BLT-Bereich wird nicht gerendert. Windows erzwingt dieses Verhalten auch dann, wenn Sie Desktopfenster-Manager Komposition nicht aktivieren. Windows 7-kompatible Anwendungen müssen in ein clippingfenster geändert werden.
-   **Windows Vista (Standard):** Anwendungen müssen in der Lage sein, BLT zum primären Replikat ohne Clipping-Fenster zu haben, da ältere Anwendungen von diesem Verhalten abhängig sind. Wenn Sie diese Anwendung ausführen, wird der Desktopfenster-Manager deaktiviert.

**Ge-verlappedresult-API**

-   **Windows 7:** Löst eine Racebedingung auf, bei der eine Multithread-APP, die gezu verlappedresult verwendet, zurückgegeben werden kann, ohne das Ereignis in der überlappenden Struktur zurückzusetzen, wodurch der nächste Aufrufe dieser Funktion vorzeitig zurückgegeben wird.
-   **Windows Vista (Standard):** Stellt das Verhalten mit der Racebedingung bereit, von der Anwendungen möglicherweise abhängig sind. Anwendungen, die dieses Race vor dem Windows 7-Verhalten vermeiden möchten, sollten auf das überlappende Ereignis warten und, wenn signalisiert, gefliverlappedresult mit bwait = = **false** aufrufen.

**Programmkompatibilitäts-Assistent (PCA)**

-   **Windows 7:** Anwendungen mit Kompatibilitäts Abschnitt erhalten keine PCA-Entschärfung.
-   **Windows Vista (Standard):** Anwendungen, die unter bestimmten Umständen nicht ordnungsgemäß installiert werden oder während der Laufzeit abstürzen, erhalten die PCA-Entschärfung. Weitere Informationen finden Sie im Abschnitt "Reference".

## <a name="leveraging-feature-capabilities"></a>Nutzen von Featurefunktionen

Aktualisieren Sie das Anwendungs Manifest mit den neuesten Kompatibilitätsinformationen für die Betriebssystemunterstützung. In diesem Abschnitt werden die Ergänzungen des Manifests beschrieben:

-   **Namespace:** Compatibility. v1 (xmlns = "urn: Schemas-Microsoft-com: Compatibility. v1" >)

-   **Abschnitts Name:** Kompatibilität (neuer Abschnitt)

-   **SupportedOS:** GUID des unterstützten Betriebssystems: die GUIDs, die den unterstützten Betriebssystemen zugeordnet sind:

    -   {e2011457-1546-43c5-a5fe-008deee3d3f0} für Windows Vista: Dies ist der Standardwert für den switchbackkontext.
    -   {35138b9a-5d96-4sbd-8e2d-a2440225t93a} für Windows 7: Anwendungen, die diesen Wert im Anwendungs Manifest festlegen, erhalten das Windows 7-Verhalten.

    > [!Note]  
    > Microsoft generiert und veröffentlicht GUIDs für zukünftige Windows-Versionen nach Bedarf.

     

Im folgenden finden Sie ein Beispiel für ein aktualisiertes Manifest.

> [!Note]  
> Bei den Attribut-und Tagnamen im Anwendungs Manifest wird die Groß-/Kleinschreibung beachtet.

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?> 
  <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--The ID below indicates application support for Windows Vista --> 
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates application support for Windows 7 --> 
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/> 
      </application> 
    </compatibility>
  </assembly>
```



Der Wert für das Hinzufügen von GUIDs für beide Betriebssysteme im obigen Beispiel ist die Bereitstellung einer Unterstützung von Unterstützung. Anwendungen, die beide Plattformen unterstützen, benötigen für jede Plattform keine separaten Manifeste.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Tests der Kompatibilität, Leistung, Zuverlässigkeit und Benutzerfreundlichkeit

1.  Testen Sie die Anwendung mit dem neuen Kompatibilitäts Abschnitt `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` , und stellen Sie sicher, dass die Anwendung mit dem aktuellen Windows 7-Verhalten ordnungsgemäß funktioniert.
2.  Testen Sie die Anwendung mit dem neuen Kompatibilitäts Abschnitt und `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (bzw. ohne diesen Abschnitt vollständig), um sicherzustellen, dass die Anwendung mit dem Windows Vista-Verhalten unter Windows 7 ordnungsgemäß funktioniert.

## <a name="known-issues"></a>Bekannte Probleme

**Kontext** Konflikt Eine Anwendung wird in einem Windows Vista-Kontext statt in einem Windows 7-Kontext auf einem Computer ausgeführt, auf dem eine x64-Edition von Windows 7 oder Windows Server 2008 R2 ausgeführt wird.

**Lösung** Updates sind verfügbar, um dies für alle unterstützten x64-basierten Versionen von Windows 7 und Windows Server 2008 R2 sowie für alle unterstützten Itanium-basierten Versionen von Windows Server 2008 R2 zu beheben. Wechseln Sie zur Microsoft-Support Seite für [KB 978637: eine Anwendung wird in einem Windows Vista-Kontext statt in einem Windows 7-Kontext auf einem Computer ausgeführt, auf dem eine x64-Edition von Windows 7 oder Windows Server 2008 R2 ausgeführt wird](https://support.microsoft.com/kb/978637) , um weitere Informationen zu erhalten und die richtige Version für Ihr System herunterzuladen.

**Absturz Abbild Diagnose blockiert**

**Lösung** Wechseln Sie zur Microsoft-Support Seite für [KB 976038: Ausnahmen, die von einer Anwendung ausgelöst werden, die in einer 64-Bit-Version von Windows ausgeführt wird, werden](https://support.microsoft.com/kb/976038) bei zusätzlichen Details ignoriert.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [**Queryactctxw-Funktion**](/windows/win32/api/winbase/nf-winbase-queryactctxw)
-   [UAC-Manifest](/previous-versions/bb756929(v=msdn.10))
-   [Anwendungs Manifeste für Windows-Anwendungen](../sbscs/application-manifests.md)
-   [Desktopfenster-Manager (DWM)](../dwm/dwm-overview.md)
-   [Aktualisierung des Kontext Konflikts](https://support.microsoft.com/kb/978637)

 

 
