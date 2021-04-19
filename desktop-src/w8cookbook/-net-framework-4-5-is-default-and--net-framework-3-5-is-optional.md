---
title: Standardeinstellungen .NET Framework
description: .NET Framework 4,5 ist Standard, und .NET Framework 3,5 ist optional.
ms.assetid: 19B53C82-812A-49AC-87C6-C08E7C199208
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1f91acc8739b2c660bfb1ba1392ea192511d1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "106338098"
---
# <a name="net-framework-45-is-default-and-net-framework-35-is-optional"></a>.NET Framework 4,5 ist Standard, und .NET Framework 3,5 ist optional.

## <a name="platforms"></a>Plattformen

**Clients**   Windows 8  
**Server**   Windows Server 2012  

## <a name="description"></a>BESCHREIBUNG

.NET Framework 4,5 ist in Windows 8 standardmäßig aktiviert. Windows 8 umfasst .NET 3,5 nicht standardmäßig, aber die Dateien für .NET 3,5 sind auf dem Windows 8-Installationsmedium als optionales Feature verfügbar.

Wenn für den Benutzer ein Upgrade von Windows 7 auf Windows 8 ausgeführt wird, ist .NET Framework 3,5 vollständig aktiviert, um sicherzustellen, dass alle apps auf dem Computer weiterhin ordnungsgemäß funktionieren.

## <a name="manifestation"></a>Ausstrahlung

Wenn der Benutzer eine Neuinstallation von Windows 8 durchführt und dann apps installiert, für die .NET Framework 3,5 (oder 2,0) erforderlich ist, wird eine Anforderung für die erforderlichen .NET 3,5-Dateien auslöst. Normalerweise werden die fehlenden Dateien von Windows Update heruntergeladen (nachdem der Benutzer zur Berechtigung aufgefordert wurde), aber wenn der Zugriff auf Windows Update nicht möglich ist, schlägt die Aktivierung von .NET Framework 3,5 fehl, es sei denn, es wurde eine alternative Quelle für die fehlenden Dateien angegeben.

## <a name="mitigation"></a>Minderung

So aktivieren Sie .NET Framework 3,5 nur auf Testcomputern mit einer sauberen Installation von Windows 8:

1.  Kopieren \\ \\ Sie die Quellen SxS \\ aus dem Image des bereitgestellten Betriebssystem-Build ISO in dotnet35 oder einen ähnlichen Ordner. Beispiel:
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  Führen Sie diese Befehlszeile mit Administrator Berechtigungen aus:
    ```
    Dism.exe /online /enable-feature /featurename:NetFX3 /All /Source:c:\dotnet35 /LimitAccess

    ```



> [!Note]  
> Der Ordner "Sources \\ SxS" darf nicht als Verteilungsmechanismus verwendet werden, da dies kein unterstützter Mechanismus ist.



## <a name="solution"></a>Lösung

**Für Consumer:**

Windows 8 umfasst einen Mechanismus, der .NET Framework 3,5 automatisch aktiviert, wenn versucht wird, das verteilbare Paket zu installieren, oder wenn ein Anwendungsinstallations Programm, das .NET 3,5 benötigt, das verteilbare Paket aufruft.

**Für App-Entwickler (und IT-Administratoren):**

IT-Administratoren können .NET 3,5-apps so konfigurieren, dass Sie entweder unter .NET 3,5 oder .NET 4,5 ausgeführt werden (je nachdem, was bereits installiert ist). Um eine verwaltete App entweder auf 3,5 oder 4,5 auszuführen, fügen Sie einfach einen Abschnitt in der Anwendungs Konfigurationsdatei hinzu. Dadurch wird sichergestellt, dass die APP, wenn .NET 3,5 installiert ist, auf .NET 3,5 ausgeführt wird. Andernfalls wird die APP unter .NET 4,5 ausgeführt. Ein Beispiel für den zusätzlichen Abschnitt in der Konfigurationsdatei finden Sie unten:


```
<configuration>
   <startup>
      <supportedRuntime version="v2.0.50727"/>
      <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5"/>
   </startup>
</configuration>
```



**Für Unternehmens OEMs:**

So aktivieren Sie .NET Framework 3,5 für EEAP-Builds und für Anwendungen, die keinen Zugriff auf Windows Update haben:

1.  Kopieren \\ Sie die Quellen \\ SxS \\ aus dem Image des bereitgestellten Betriebssystem-Build ISO in den Ordner dotnet35 oder einen ähnlichen Ordner Beispiel:
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  Legen Sie den RegKey fest:
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]
     LocalSourcePath = c:\dotnet35
    ```



**Für Unternehmen:**

Für Computer, die für die Verwendung von WSUS für die Wartung konfiguriert sind, können Sie einen Registrierungs Eintrag festlegen, um zuzulassen, dass der Computer Windows Update für die Aktivierung von .NET 3,5 anstelle von WSUS verwendet (wenn Sie dies tun), erfolgt die Wartung weiterhin von WSUS.

-   Legen Sie den RegKey fest:
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]  RepairContentServerSource =DWORD(2)
    ```



Dieser Registrierungs Eintrag kann auch über Gruppenrichtlinie (lokale Computer Richtlinie > Computerkonfiguration-> administrative Vorlagen-> System festgelegt werden. Wählen Sie die Einstellung Einstellungen für die Installation optionaler Komponenten und die Reparatur von Komponenten angeben aus.

Wenn Sie die Option Kontakt Windows Update direkt zum Herunterladen von Reparatur Inhalt anstelle von Windows Server Update Services (WSUS) auswählen, werden bei jedem Versuch, Windows-Features hinzuzufügen (z. b. .NET Framework 3,5) oder Reparatur Features, Dateidownloads aus Windows Update auslöst. Zielcomputer benötigen Internet-und Wu-Zugriff für diese Option. Bei normalen Wartungs Vorgängen wird WSUS weiterhin verwendet, wenn es als Quelle konfiguriert wurde.

**Hinweis zum Festlegen des lokalen Quell Speicher Orts über Registrierungseinträge**

IT-Administratoren können lokale Quell Speicherorte für .NET 3,5-Dateien mithilfe eines Registrierungs Eintrags festlegen, sodass Benutzer das Dialogfeld "Windows-Funktionen hinzufügen/entfernen" verwenden können, um Funktionen mit fehlender Nutzlast zu aktivieren, ohne einen Quell Speicherort angeben zu müssen. Der Wert des Registrierungs Eintrags kann über eine Gruppenrichtlinie gesteuert werden.

Dieser Registrierungs Eintrag wird unterstützt:



<table>
<thead>
<tr class="header">
<th>Eingabe</th>
<th>type</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lokaler Quellpfad</td>
<td>REG_EXPAND_SZ</td>
<td>Lokale Quell Pfade, die standardmäßig verwendet werden sollen. Es können mehrere Pfade angegeben werden. Sie sollten durch, getrennt werden. Standorte werden in der Reihenfolge durchsucht, in der Sie angegeben sind. <br/> Lokale Quell Standorte, die in der Befehlszeile des Befehlszeile angegeben sind, haben Vorrang vor den in diesem Registrierungs Eintrag angegebenen Positionen. Ordner Speicherorte können in diesem Registrierungs Eintrag angegeben werden. <br/> Wims können verwendet werden, aber der Pfad muss in die WIM-Datei gesetzt werden. Es ist nicht erforderlich, es zu installieren, z. b.: <br/> <dl> Wim: \\ machine\share\file.Wim: 1<br />
</dl> Beachten Sie den 1 am Ende. Sie müssen den numerischen Index des Abbilds angeben, das Sie in der WIM-Datei verwenden möchten. <br/> Bei einer bereitgestellten WIM muss der Quellpfad auf das Windows-Verzeichnis des bereitgestellten Images statt auf den Einfügepunkt verweisen (z. b.:/Source: <mount_point> \Windows anstelle von/Source: <mount_point> ). <br/></td>
</tr>
</tbody>
</table>





## <a name="resources"></a>Ressourcen

<dl>

[Implementieren der Registrierungs basierten Richtlinie](/previous-versions/windows/desktop/Policy/implementing-registry-based-policy)  
</dl>