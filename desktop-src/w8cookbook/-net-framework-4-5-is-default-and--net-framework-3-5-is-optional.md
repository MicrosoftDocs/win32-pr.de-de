---
title: .NET Framework Standardeinstellungen
description: .NET Framework 4.5 ist standard und .NET Framework 3.5 optional.
ms.assetid: 19B53C82-812A-49AC-87C6-C08E7C199208
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b45aef294e035f5fb7e647c49b22206ac8aadd
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883128"
---
# <a name="net-framework-45-is-default-and-net-framework-35-is-optional"></a>.NET Framework 4.5 ist standard und .NET Framework 3.5 optional.

## <a name="platforms"></a>Plattformen

**Clients** Windows 8     
**Server** Windows Server 2012     

## <a name="description"></a>Beschreibung

.NET Framework 4.5 ist standardmäßig in der Windows 8. Windows 8 enthält standardmäßig nicht .NET 3.5, aber die Dateien für .NET 3.5 sind auf den Windows 8-Installationsmedien als optionales Feature verfügbar.

Wenn der Benutzer ein Upgrade von Windows 7 auf Windows 8, ist .NET Framework 3.5 vollständig aktiviert, um sicherzustellen, dass alle Apps auf dem Computer weiterhin ordnungsgemäß funktionieren.

## <a name="manifestation"></a>Manifestation

Wenn der Benutzer eine Neuinstallation von Windows 8 ausführt und dann Apps installiert, die .NET Framework 3.5 (oder 2.0) erfordern, löst er eine Anforderung für die erforderlichen .NET 3.5-Dateien aus. Normalerweise werden die fehlenden Dateien von Windows Update heruntergeladen (nachdem der Benutzer um die Berechtigung gebeten wurde), aber wenn der Zugriff auf Windows Update nicht möglich ist, ist die Aktivierung von .NET Framework 3.5 nicht möglich, es sei denn, es wurde eine alternative Quelle für die fehlenden Dateien angegeben.

## <a name="mitigation"></a>Minderung

So aktivieren .NET Framework 3.5 nur auf Testcomputern mit bereinigten Installationen Windows 8:

1.  Kopieren Sie SX-Quellen aus dem bereitgestellten Betriebssystem, und erstellen Sie \\ \\ das \\ ISO-Image in den Ordner dotnet35 oder einen ähnlichen Ordner. Beispiel:
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  Führen Sie diese Befehlszeile mit Administratorrechten aus:
    ```
    Dism.exe /online /enable-feature /featurename:NetFX3 /All /Source:c:\dotnet35 /LimitAccess

    ```



> [!Note]  
> Der \\ SxS-Quellenordner darf nicht als Verteilungsmechanismus verwendet werden, da dies kein unterstützter Mechanismus ist.



## <a name="solution"></a>Lösung

**Für Verbraucher:**

Windows 8 enthält einen Mechanismus, der .NET Framework 3.5 automatisch aktiviert, wenn versucht wird, das verteilbare Paket zu installieren, oder wenn ein Anwendungsinstallationsprogramm, das .NET 3.5 benötigt, das weiterverteilte Paket aufruft.

**Für App-Entwickler (und IT-Administratoren):**

IT-Administratoren können .NET 3.5-Apps für die Ausführung unter .NET 3.5 oder .NET 4.5 konfigurieren (je nachdem, was bereits installiert ist). Um eine verwaltete App unter 3.5 oder 4.5 ausführen zu können, fügen Sie einfach einen Abschnitt in der Anwendungskonfigurationsdatei hinzu. Dadurch wird sichergestellt, dass die App unter .NET 3.5 ausgeführt wird, wenn .NET 3.5 installiert ist. Andernfalls wird die App unter .NET 4.5 ausgeführt. Ein Beispiel für den zusätzlichen Abschnitt in der Konfigurationsdatei finden Sie unten:


```
<configuration>
   <startup>
      <supportedRuntime version="v2.0.50727"/>
      <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5"/>
   </startup>
</configuration>
```



**Für Unternehmens-OEMs:**

So aktivieren sie .NET Framework 3.5 für DIEP-Builds und für Anwendungen, die keinen Zugriff auf Windows haben:

1.  Kopieren \\ Sie \\ SX-Quellen aus dem bereitgestellten ISO-Image für den \\ Betriebssystem-Build in den Ordner dotnet35 oder einen ähnlichen Ordner. Beispiel:
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  Legen Sie den Hauptschlüssel fest:
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]
     LocalSourcePath = c:\dotnet35
    ```



**Für Unternehmen:**

Für Computer, die für die Verwendung von WSUS für die Wartung konfiguriert sind, können Sie einen Registrierungseintrag festlegen, um dem Computer die Verwendung von Windows Update zum Aktivieren von .NET 3.5 anstelle von WSUS zu ermöglichen .NET 3.5 (die Wartung wird in diesem Fall weiterhin von WSUS durchgeführt).

-   Legen Sie den Hauptschlüssel fest:
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]  RepairContentServerSource =DWORD(2)
    ```



Dieser Registrierungseintrag kann auch über Gruppenrichtlinie (Richtlinie für lokale Computer -> Computerkonfiguration -> Administrative Vorlagen -> Festgelegt werden. Wählen Sie die Einstellung Einstellungen für optionale Komponenteninstallation und Komponentenreparatur angeben aus.

Wenn Sie direkt kontaktieren Windows Update auswählen, um Reparaturinhalte anstelle von Windows Server Update Services (WSUS) herunterzuladen, lösen alle Versuche, Windows-Features (z. B. .NET Framework 3.5) oder Reparaturfeatures hinzuzufügen, Dateidownloads von Windows Update aus. Zielcomputer benötigen internet- und WU-Zugriff für diese Option. Bei normalen Wartungsvorgängen wird WSUS weiterhin verwendet, wenn es als Quelle konfiguriert wurde.

**Hinweis zum Festlegen des lokalen Quellspeicherorts über Registrierungseinträge**

IT-Administratoren können lokale Quellspeicherort(en) für .NET 3.5-Dateien über einen Registrierungseintrag festlegen, sodass Benutzer das Dialogfeld Windows-Funktionen hinzufügen/entfernen verwenden können, um Features mit fehlender Nutzlast zu aktivieren, ohne einen Quellspeicherort angeben zu müssen. Der Wert des Registrierungseintrags kann über eine Gruppenrichtlinie gesteuert werden.

Dieser Registrierungseintrag wird unterstützt:



<table>
<thead>
<tr class="header">
<th>Eingabe</th>
<th>Typ</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lokaler Quellpfad</td>
<td>REG_EXPAND_SZ</td>
<td>Standardmäßig zu verwendende lokale Quellpfade. Es können mehrere Pfade angegeben werden. sie sollten durch getrennt werden; . Standorte werden in der Reihenfolge durchsucht, in der sie angegeben sind. <br/> Lokale Quellspeicherorte, die in der DISM-Befehlszeile angegeben sind, haben Vorrang vor den in diesem Registrierungseintrag angegebenen Speicherorten. Ordnerspeicherorte können in diesem Registrierungseintrag angegeben werden. <br/> WIMs können verwendet werden, aber der Pfad muss zur WIM-Datei sein. es ist nicht notwendig, es zu mounten, z. B.: <br/> <dl> wim: \\ machine\share\file.wim:1<br />
</dl> Beachten Sie die 1 am Ende. Sie müssen den numerischen Index des Bilds angeben, das Sie in der WIM-Datei verwenden möchten. <br/> Bei einem bereitgestellten WIM muss der Quellpfad auf das Windows-Verzeichnis des bereitgestellten Images verweisen, nicht auf den Bereitstellungspunkt (z. B. /source: mount_point \windows anstelle von &lt; &gt; /source: &lt; mount_point &gt; ). <br/></td>
</tr>
</tbody>
</table>





## <a name="resources"></a>Ressourcen

<dl>

[Implementieren einer registrierungsbasierten Richtlinie](/previous-versions/windows/desktop/Policy/implementing-registry-based-policy)  
</dl>
