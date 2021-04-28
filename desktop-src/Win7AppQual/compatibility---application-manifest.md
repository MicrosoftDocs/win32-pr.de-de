---
description: Anwendungsmanifest
ms.assetid: f022374d-ea3f-477f-9b59-3188b775ed64
title: Anwendungsmanifest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c52b8eb2af87c271151be3d7989f50b2903084
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088588"
---
# <a name="application-manifest"></a>Anwendungsmanifest

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** – Windows 7  
**Server** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkung von Features

 **Schweregrad:** Niedrig  
**Häufigkeit** – Niedrig  





## <a name="description"></a>BESCHREIBUNG

Windows 7 führt einen neuen Abschnitt im Anwendungsmanifest namens "Kompatibilität" ein. Dieser Abschnitt hilft Windows bei der Bestimmung der Windows-Versionen, für die eine Anwendung entwickelt wurde, und ermöglicht Es Windows, das Verhalten zu bieten, das die Anwendung basierend auf der Windows-Version erwartet, auf die die Anwendung ausgerichtet ist.

Im Abschnitt Kompatibilität kann Windows neues Verhalten für neue, vom Entwickler erstellte Software bereitstellen und gleichzeitig die Kompatibilität mit vorhandener Software aufrechterhalten. Dieser Abschnitt unterstützt Windows auch bei der Bereitstellung einer höheren Kompatibilität in zukünftigen Versionen von Windows. Beispielsweise wird eine Anwendung, die im Abschnitt Kompatibilität die Unterstützung nur für Windows 7 deklarieren, weiterhin das Verhalten von Windows 7 in zukünftigen Versionen von Windows erhalten.

## <a name="manifestation-of-change"></a>Änderungsmanifest

Anwendungen ohne Kompatibilitätsabschnitt in ihrem Manifest erhalten standardmäßig Windows Vista-Verhalten unter Windows 7 und zukünftigen Windows-Versionen. Beachten Sie, dass Windows XP und Windows Vista diesen Manifestabschnitt ignorieren und sich nicht darauf auswirken.

Die folgenden Windows-Komponenten bieten abweichendes Verhalten basierend auf dem Abschnitt Kompatibilität in Windows 7:

**RPC-Standardthreadpool**

-   **Windows 7:** Um die Skalierbarkeit zu verbessern und die Threadanzahl zu reduzieren, wurde RPC zum NT-Threadpool (Standardpool) umgeschaltet. Für Windows Vista hat RPC einen privaten Threadpool verwendet.
    -   Für Binärdateien, die für Win7 kompiliert wurden, wird der Standardpool verwendet.
    -   Wenn I \_ RpcMgmtEnableDedicatedThreadPool aufgerufen wird, bevor eine RPC-API aufgerufen wird, wird der private Threadpool verwendet (Vista-Verhalten).
    -   Wenn I \_ RpcMgmtEnableDedicatedThreadPool nach einem RPC-Aufruf aufgerufen wird, wird der Standardpool verwendet. I \_ RpcMgmtEnableDedicatedThreadPool gibt den Fehler 1764 zurück, und der angeforderte Vorgang wird nicht unterstützt.
-   **Windows Vista (Standard):** Für Binärdateien, die für Windows Vista und darunter kompiliert wurden, wird der private Pool verwendet.

**DirectDraw-Sperre**

-   **Windows 7:** Anwendungen, die für Windows 7 manifestiert wurden, können die Sperr-API in DDRAW nicht aufrufen, um den primären Desktopvideopuffer zu sperren. Dies führt zu einem Fehler, und **der NULL-Zeiger** für das primäre Wird zurückgegeben. Dieses Verhalten wird auch dann erzwungen, wenn Desktopfenster-Manager Composition nicht aktiviert ist. Windows 7-kompatible Anwendungen dürfen den primären Videopuffer nicht zum Rendern sperren.
-   **Windows Vista (Standard):** Anwendungen können eine Sperre für den primären Videopuffer abrufen, da ältere Anwendungen von diesem Verhalten abhängen. Die Ausführung der Anwendung deaktiviert Desktopfenster-Manager.

**DirectDraw Bit Block Transfer (Blt) to Primary without Clipping Window**

-   **Windows 7:** Anwendungen, die für Windows 7 manifestiert werden, werden daran gehindert, Blts ohne Clippingfenster im primären Desktopvideopuffer auszuführen. Dies führt zu einem Fehler, und der Blt-Bereich wird nicht gerendert. Windows erzwingt dieses Verhalten auch dann, wenn Sie Desktopfenster-Manager Composition nicht aktivieren. Windows 7-kompatible Anwendungen müssen in ein Clippingfenster passen.
-   **Windows Vista (Standard):** Anwendungen müssen ohne Clippingfenster in der Lage sein, die primäre Anwendung zu verwenden, da legacy-Anwendungen von diesem Verhalten abhängen. Wenn Sie diese Anwendung ausführen, wird die Desktopfenster-Manager deaktiviert.

**GetOverlappedResult-API**

-   **Windows 7:** Löst eine Racebedingung auf, bei der eine Multithread-App mit GetOverlappedResult zurückgeben kann, ohne das Ereignis in der überlappenden Struktur zurückzusetzen, wodurch der nächste Aufruf dieser Funktion vorzeitig zurückgegeben wird.
-   **Windows Vista (Standard):** Stellt das Verhalten mit der Racebedingung bereit, von der Anwendungen möglicherweise abhängig sind. Anwendungen, die dieses Race vor dem Windows 7-Verhalten vermeiden möchten, sollten auf das überlappende Ereignis warten und getOverlappedResult bei Signalisierung mit bWait == **FALSE** aufrufen.

**Programmkompatibilitäts-Assistent (PCA)**

-   **Windows 7:** Im Abschnitt Anwendungen mit Kompatibilität wird die PCA-Entschärfung nicht behandelt.
-   **Windows Vista (Standard):** Anwendungen, die unter bestimmten Umständen nicht ordnungsgemäß installiert werden oder während der Laufzeit abstürzten, erhalten die PCA-Entschärfung. Weitere Informationen finden Sie im Referenzabschnitt.

## <a name="leveraging-feature-capabilities"></a>Nutzen von Featurefunktionen

Aktualisieren Sie das Anwendungsmanifest mit den neuesten Kompatibilitätsinformationen für die Betriebssystemunterstützung. Im Abschnitt werden die Ergänzungen zum Manifest beschrieben:

-   **Namespace:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)

-   **Abschnittsname:** Kompatibilität (neuer Abschnitt)

-   **SupportedOS:** GUID des unterstützten Betriebssystems: Die GUIDs, die den unterstützten Betriebssystemen zugeordnet sind, lauten:

    -   {e2011457-1546-43c5-a5fe-008deee3d3f0} für Windows Vista: Dies ist der Standardwert für den Switchbackkontext.
    -   {35138b9a-5d96-4fbd-8e2d-a2440225f93a} für Windows 7: Anwendungen, die diesen Wert im Anwendungsmanifest festlegen, erhalten das Windows 7-Verhalten.

    > [!Note]  
    > Microsoft generiert und post-GUIDs für zukünftige Windows-Versionen nach Bedarf.

     

Im Folgenden wird ein Beispiel für ein aktualisiertes Manifest beschrieben.

> [!Note]  
> Bei den Attribut- und Tagnamen im Anwendungsmanifest wird die Groß-/Kleinschreibung beachtet.

 


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



Der Wert des Hinzufügens von GUIDs für beide Betriebssysteme im obigen Beispiel ist die Bereitstellung von Downlevelunterstützung. Anwendungen, die beide Plattformen unterstützen, benötigen keine separaten Manifeste für jede Plattform.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Benutzerfreundlichkeitstests

1.  Testen Sie die Anwendung mit dem neuen Kompatibilitätsabschnitt, und `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` stellen Sie sicher, dass die Anwendung ordnungsgemäß funktioniert, indem Sie das neueste Windows 7-Verhalten verwenden.
2.  Testen Sie die Anwendung mit dem neuen Kompatibilitätsabschnitt und (oder ohne diesen Abschnitt vollständig), um sicherzustellen, dass die Anwendung mithilfe des Windows Vista-Verhaltens unter `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` Windows 7 ordnungsgemäß funktioniert.

## <a name="known-issues"></a>Bekannte Probleme

**Kontextkonflikt** Eine Anwendung wird in einem Windows Vista-Kontext statt in einem Windows 7-Kontext auf einem Computer ausgeführt, auf dem eine x64-Edition von Windows 7 oder Windows Server 2008 R2 ausgeführt wird.

**Lösung** Updates sind verfügbar, um dies für alle unterstützten x64-basierten Versionen von Windows 7 und Windows Server 2008 R2 sowie für alle unterstützten Itanium-basierten Versionen von Windows Server 2008 R2 zu korrigieren. Wechseln Sie zur Microsoft-Support-Seite für [KB 978637:](https://support.microsoft.com/kb/978637) Eine Anwendung wird in einem Windows Vista-Kontext statt in einem Windows 7-Kontext auf einem Computer ausgeführt, auf dem eine x64-Edition von Windows 7 oder Windows Server 2008 R2 ausgeführt wird, um weitere Details zu erhalten und die richtige Version für Ihr System herunterzuladen.

**Diagnose des Absturzabbilds blockiert**

**Lösung** Wechseln Sie zur Microsoft-Support-Seite für [KB 976038:](https://support.microsoft.com/kb/976038) Ausnahmen, die von einer Anwendung ausgelöst werden, die in einer 64-Bit-Version von Windows ausgeführt wird, werden für weitere Details ignoriert.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [**QueryActCtxW-Funktion**](/windows/win32/api/winbase/nf-winbase-queryactctxw)
-   [UAC-Manifest](/previous-versions/bb756929(v=msdn.10))
-   [Anwendungsmanifesten für Windows-Anwendungen](../sbscs/application-manifests.md)
-   [Desktopfenster-Manager (DWM)](../dwm/dwm-overview.md)
-   [Kontextkonfliktaktualisierung](https://support.microsoft.com/kb/978637)

 

 
