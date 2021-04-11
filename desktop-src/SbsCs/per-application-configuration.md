---
description: Die Konfiguration pro Anwendung leitet die Abhängigkeit einer bestimmten Anwendung von einer Version einer parallelen Assembly zu einer anderen Version der Assembly um.
ms.assetid: b7988385-c87e-443c-8ec3-84ab3c172eab
title: Konfiguration pro Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b17543c9972deefe2a2beda1f5eeba1c5ace2ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217795"
---
# <a name="per-application-configuration"></a>Konfiguration pro Anwendung

Die Konfiguration pro Anwendung leitet die Abhängigkeit einer bestimmten Anwendung von einer Version einer parallelen Assembly zu einer anderen Version der Assembly um. Eine Konfiguration pro Anwendung ist möglicherweise erforderlich, wenn der korrekte Betrieb einer bestimmten Anwendung eine Assemblyversion erfordert, die sich von der Version unterscheidet, die normalerweise als [Standardkonfiguration](default-configuration.md) oder [Verleger Konfiguration](publisher-configuration.md)angegeben ist. Beispielsweise kann ein globales Update der Assemblyversion durch den Verleger die Assembly beheben, diese spezielle Anwendung jedoch unterbrechen. In diesem Fall kann die Konfiguration pro Anwendung verwendet werden, damit die Anwendung weiterhin mit der vorherigen Assemblyversion ausgeführt werden kann.

Ab Windows Server 2003 überschreibt die Konfiguration pro Anwendung immer die [Standardkonfiguration](default-configuration.md) pro Anwendung. Die Konfiguration pro Anwendung überschreibt die [Verleger Konfiguration](publisher-configuration.md) nur auf Anwendungs Basis, wenn in der [Anwendungs Konfigurationsdatei](application-configuration-files.md) *Apply = "No"* in **publisherPolicy** angegeben wird und ein entsprechender Eintrag in der Anwendungskompatibilitäts-Datenbank vorhanden ist.

> [!Note]  
> Unter Windows XP überschreibt die Konfiguration pro Anwendung sowohl die [Standardkonfiguration](default-configuration.md) als auch die [Verleger Konfiguration](publisher-configuration.md) pro Anwendung. Weitere Informationen finden Sie unter [Konfiguration pro Anwendung unter Windows XP](per-application-configuration-on-windows-xp.md).

 

Ab Windows Server 2003 setzt eine Konfiguration pro Anwendung eine [Verleger Konfiguration](publisher-configuration.md) außer Kraft, wenn in der [Anwendungs Konfigurationsdatei](application-configuration-files.md) *Apply = "yes"* in **publisherPolicy** angegeben wird und das Flag enableappconfig für die Anwendung in der Anwendungskompatibilitäts-Datenbank festgelegt ist. Diese Möglichkeit, eine Verleger Konfiguration mit einer Konfiguration pro Anwendung außer Kraft zu setzen, ermöglicht das Ausführen der Anwendung in safemode. Weitere Informationen zur Anwendungskompatibilitäts-Datenbank und zu safemode finden Sie im Windows-Anwendungskompatibilitäts-Toolkit. Sie können das Windows-Anwendungskompatibilitäts-Toolkit von abrufen [https://www.microsoft.com/downloads](https://www.microsoft.com/Downloads/) .

> [!Note]  
> Wenn Sie Komponenten mit einer [Anwendungs Konfigurationsdatei](application-configuration-files.md) (config-Datei) bereitstellen, die *Apply = "No"* in **publisherPolicy** angibt, führt dies dazu, dass die Generierung des Aktivierungs Kontexts fehlschlägt. Die Konfiguration pro Anwendung wird ignoriert, wenn Sie Komponenten mit einer config-Datei bereitstellen, die *Apply = "yes"* in **publisherPolicy** angibt.

 

Anwendungs Administratoren können eine Konfiguration pro Anwendung implementieren, indem Sie Anwendungs Konfigurationsdateien erstellen und installieren und die Anwendungskompatibilitäts-Datenbank aktualisieren. Die Anwendungs Konfigurationsdatei sollte dann im selben Ordner wie die ausführbare Datei der Anwendung bereitgestellt und installiert werden. Eine Auflistung des Datei Schemas finden Sie unter [Schema der Anwendungs Konfigurationsdatei](application-configuration-file-schema.md). Die Anwendungskompatibilitäts-Datenbank muss wie im Anwendungskompatibilitäts-Toolkit beschrieben verteilt werden.

> [!Note]  
> Wenn Ihre Anwendung in safemode ausgeführt wird, erhalten Sie keine wichtigen Sicherheitskorrekturen oder Fehlerbehebungen, die der Herausgeber der Assembly als Verleger Konfigurationsdateien ausgeben kann. Eine Anwendung, die die Konfiguration pro Anwendung verwendet, ist daher möglicherweise unsicher oder auch nach dem Anwenden einer neuen Assembly mit diesen Korrekturen auf das System weiterhin fehlerhaft. Aus diesem Grund sollten Anwendungsentwickler niemals eine Anwendung mit einer Konfiguration pro Anwendung versenden. Die Konfiguration pro Anwendung sollte nur von Unternehmens Administratoren als temporäre Korrektur verwendet werden, wenn die Anwendung durch eine Verleger Konfiguration beschädigt ist. In diesem Fall besteht die permanente Lösung darin, dass die Entwickler der Assembly und die Entwickler der Anwendung zusammenarbeiten müssen, um sicherzustellen, dass die Assemblys mit der Verleger Konfiguration vollständig abwärts kompatibel sind.

 

Im folgenden finden Sie ein Beispiel für eine Anwendungs Konfigurationsdatei. Weitere Informationen finden Sie unter Anwendungs Konfigurationsdateien.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<configuration>
 <windows>
  <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
   <assemblyIdentity  processorArchitecture="X86" name="Microsoft.Windows.mysampleApp" type="win32" version="1.0.0.0"/>
   <publisherPolicy apply="no"/>                     
   <dependentAssembly>
    <assemblyIdentity type="win32" processorArchitecture="x86" name="Microsoft.Windows.SampleAssembly" publicKeyToken="0000000000000000"/>
    <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
   </dependentAssembly>
  </assemblyBinding>
 </windows>
</configuration>
```

Der Anwendungs Administrator sollte die erforderlichen Einträge der Anwendungskompatibilitäts-Datenbank hinzufügen. Herunterladen und Installieren des Windows-Anwendungskompatibilitäts-Toolkit 2,6 von [https://www.microsoft.com/downloads](https://www.microsoft.com/Downloads/) . Erstellen Sie eine neue benutzerdefinierte Datenbank, oder aktualisieren Sie Ihre vorhandene Datenbank mit dem Kompatibilitäts Administrator, wie im Toolkit beschrieben. Der Kompatibilitäts Fehler, den Sie für die Kompatibilitäts Ebene Ihrer Anwendung auswählen möchten, ist enableappconfig. Sie müssen Anwendungen immer testen, bevor Sie eine neue Kompatibilitätsdatenbank installieren.

 

 



