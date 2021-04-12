---
description: Wenn Sie Ihre eigene VSS-Anwendung entwickeln, sollten Sie die folgenden Richtlinien und Einschränkungen beachten.
ms.assetid: d4edc16c-f768-4095-9b2a-b706f19f9e61
title: VSS-Anwendungskompatibilität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9cc19b6a6d88365a67569bc4729855077c9da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343579"
---
# <a name="vss-application-compatibility"></a>VSS-Anwendungskompatibilität

Wenn Sie Ihre eigene VSS-Anwendung entwickeln, sollten Sie die folgenden Richtlinien und Einschränkungen beachten. Möglicherweise ist es hilfreich, auf den Beispielcode für VSS-Anforderer, Anbieter und Writer zu verweisen, die im Microsoft Windows Software Development Kit (SDK) bereitgestellt werden.

> [!Note]  
> Der Windows SDK kann verwendet werden, um VSS-Anwendungen nur für Windows Vista-und spätere Windows-Betriebssystemversionen zu entwickeln. Sie kann nicht verwendet werden, um VSS-Anforderer, Anbieter oder Writer für Windows Server 2003 R2, Windows Server 2003 oder Windows XP zu entwickeln.

 

**Windows Server 2003 R2, Windows Server 2003 und Windows XP:** VSS ist im SDK für Volumeschattenkopie-Dienst 7,2 verfügbar, das Sie unter herunterladen können [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490) . Beachten Sie, dass die 64-Bit-Vssapi. lib-Dateien in den Verzeichnissen unter dem \\ Verzeichnis Win2003 obj für die 64-Bit-Versionen von Windows Server 2003 R2, Windows Server 2003 und Windows XP verwendet werden können. Dieses SDK stellt außerdem Beispielcode für VSS-Anforderer, Anbieter und Writer bereit.

## <a name="compiling-vss-applications"></a>Kompilieren von VSS-Anwendungen

Beim Entwickeln eines Anforderers, z. b. einer Sicherungs Anwendung:

-   Fügen Sie die folgenden Header ein: <dl> VSS. h  
    Vswriter. h  
    Vsbackup. h  
    </dl>
-   Link the following library: <dl> Vssapi. lib  
    </dl>

Wenn Sie einen Writer entwickeln:

-   Fügen Sie die folgenden Header ein: <dl> VSS. h  
    Vswriter. h  
    </dl>
-   Link the following library: <dl> Vssapi. lib  
    </dl>

## <a name="supported-configurations-and-restrictions"></a>Unterstützte Konfigurationen und Einschränkungen

In der folgenden Liste werden die unterstützten Konfigurationen und Einschränkungen beschrieben:

-   VSS wird in Versionen des Windows-Betriebssystems ab Windows XP bereitgestellt und unterstützt.
-   In der folgenden Tabelle werden Kompatibilitätsinformationen in Windows-Versionen zusammengefasst. Beachten Sie Folgendes: Wenn eine VSS-Anwendung "kompiliert für" eine angegebene Windows-Version ist, bedeutet dies, dass die Anwendung mit den Header Dateien und Bibliotheken kompiliert wurde, die für diese Version spezifisch sind.

    > [!Note]  
    > Hardware Anbieter können nur unter Windows Server-Betriebssystemversionen ausgeführt werden. Sie können nicht unter Versionen von Windows-Client Betriebssystemen ausgeführt werden.

     

    > [!Note]  
    > In den folgenden Tabellen sollte Windows Server 2008 mit Service Pack 2 (SP2) als identisch mit Windows Server 2008 betrachtet werden. Weitere Informationen zu Windows Server 2008 mit SP2 finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=178730> . Windows Server 2003 R2 sollte als identisch mit Windows Server 2003 betrachtet werden.

     

    > [!Note]  
    > Wenn eine VSS-Anwendung für Windows Server 2003 oder höher kompiliert wird, wird Sie auch unter neueren Versionen von Windows ausgeführt.

     

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>VSS-Anforderer, Writer und Anbieter, die für kompiliert wurden</th>
    <th>Wird ausgeführt auf</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Windows Server 2008 R2 (64 Bit), Windows 7 (64-Bit), Windows Server 2008 (64-Bit) und Windows Vista (64-Bit)</td>
    <td>Windows Server 2008 R2 (64 Bit), Windows 7 (64-Bit), Windows Server 2008 (64-Bit) und Windows Vista (64-Bit)</td>
    </tr>
    <tr class="even">
    <td>Windows Server 2008 R2 (32 Bit), Windows 7 (32-Bit), Windows Server 2008 (32-Bit) und Windows Vista (32-Bit)</td>
    <td>Windows Server 2008 R2 (32 Bit), Windows 7 (32-Bit), Windows Server 2008 (32-Bit) und Windows Vista (32-Bit)</td>
    </tr>
    <tr class="odd">
    <td>Windows Server 2003 (64-Bit)</td>
    <td>Windows Server 2008 R2 (64-Bit), Windows 7 (64-Bit), Windows Server 2008 (64-Bit), Windows Vista (64 Bit) und Windows Server 2003 (64-Bit)</td>
    </tr>
    <tr class="even">
    <td>Windows Server 2003 (32-Bit)</td>
    <td>Windows Server 2008 R2 (32-Bit), Windows 7 (32-Bit), Windows Server 2008 (32-Bit), Windows Vista (32 Bit) und Windows Server 2003 (32-Bit) <blockquote>
    [!Note]<br />
Anfordernde Personen werden auch unter Windows Server 2003 (64-Bit) ausgeführt.
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td>Windows XP 64-Bit-Edition</td>
    <td>Windows Server 2003 (64 Bit) und Windows XP 64-Bit Edition</td>
    </tr>
    <tr class="even">
    <td>Windows XP (32-Bit)</td>
    <td>Windows XP (32-Bit)</td>
    </tr>
    </tbody>
    </table>

    

     

    

    | So kompilieren Sie eine VSS-Anforderer, einen Writer oder einen Anbieter für        | Zweck                                                                                                                                       |
    |------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
    | Windows Server 2008 R2 oder Windows 7                        | Windows SDK für Windows 7 (verfügbar im [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).)                |
    | Windows Server 2008 oder Windows Vista                       | Windows SDK für Windows Server 2008 (verfügbar über das [Windows SDK Developer Center](https://msdn.microsoft.com/windows/bb980924.aspx).) |
    | Windows Server 2003 R2, Windows Server 2003 oder Windows XP | [Volumeschattenkopie-Dienst 7,2-SDK](https://www.microsoft.com/download/details.aspx?id=23490)                                                      |

    

     

-   Alle 32-Bit-VSS-Anwendungen (Requester, Anbieter und Writer) müssen als native 32-Bit-oder 64-Bit-Anwendungen ausgeführt werden. Die Ausführung unter WOW64 wird nicht unterstützt.

    **Windows Server 2003 und Windows XP:** Das Ausführen von 32-Bit-VSS-Anforderern unter WOW64 wird unterstützt, jedoch nicht für Sicherungen des Systemstatus. Das Ausführen von 32-Bit-VSS-Anbietern und-Writern unter WOW64 wird nicht unterstützt. Unterstützung für die Ausführung von 32-Bit-Anforderern unter WOW64 wurde in Windows Vista und nachfolgenden Versionen entfernt.

-   Eine Schatten Kopie, die auf Windows Server 2003 R2 oder Windows Server 2003 erstellt wurde, kann nicht auf einem Computer verwendet werden, auf dem Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird. Eine Schatten Kopie, die auf Windows Server 2008 R2 oder Windows Server 2008 erstellt wurde, kann nicht auf einem Computer verwendet werden, auf dem Windows Server 2003 ausgeführt wird. Eine Schatten Kopie, die auf Windows Server 2008 erstellt wurde, kann jedoch auf einem Computer verwendet werden, auf dem Windows Server 2008 R2 ausgeführt wird, und umgekehrt.
-   Um Schatten Kopien zu unterstützen, muss ein System, auf dem VSS ausgeführt wird, mindestens ein NTFS-Dateisystem aufweisen. Dieses Dateisystem hostet den Bereich "diff" der Schatten Kopie. Weitere Informationen finden Sie unter [System Anbieter](providers.md).
-   Aufgrund des Vorhandenseins eines NTFS-Dateisystems und der entsprechenden Auswahl von Kontext (siehe [Kontext Konfigurationen für Schatten Kopien](shadow-copy-context-configurations.md)) können alle unterstützten lokalen Dateisysteme mit Schatten Kopien kopiert werden.
-   Sie können Schatten Kopien nur für lokal eingebundene Dateisysteme erstellen. Remote Freigaben und andere bereitgestellte Dateisysteme können von dem System, von dem Sie bereitgestellt werden, nicht durch Schatten Kopien kopiert werden. Diese Dateisysteme können nur von den Systemen, die die Dateisysteme bedienen, als Schatten Kopien kopiert werden.
-   Writer und Anforderer sollten nur lokale Ressourcen angeben. Lokale Ressourcen sind Sätze von Dateien, deren absoluter Pfad mit einem Laufwerk Buchstaben beginnt und der Laufwerk Buchstabe einem bereitgestellten Ordner auf einer Remote Freigabe nicht zugeordnet werden kann.
-   Die maximale Anzahl von Software Schatten Kopien beträgt 512. Standardmäßig können Sie jedoch nur 64 Schattenkopien verwalten, die vom Feature „Schattenkopien von freigegebenen Ordnern“ verwendet werden. Verwenden Sie den Registrierungsschlüssel " [maxshadowkopien](../backup/registry-keys-for-backup-and-restore.md) ", um das Limit für die Funktion "Schatten Kopien von freigegebenen Ordnern" zu ändern.
-   Die Sicherungs Komponenten Infrastruktur unterstützt nicht das Sichern von Cluster Ressourcen als Writer-Komponenten. Zum Sichern von Cluster Ressourcen sollten Anwendungen davon ausgehen, dass der Pfad für einen bestimmten Cluster Knoten lokal ist.
-   [!Note]  
    > Microsoft bietet keinen technischen Support für Entwickler oder IT-Experten für die Implementierung von Online-Systemstatus Wiederherstellungen unter Windows (alle Versionen).

     

    Wenn Sie den Systemstatus sichern und wiederherstellen, empfiehlt es sich, zusätzlich zu den Dateien, die von den systemstatuswritern aufgelistet werden, die System-und Startvolumes zu sichern und wiederherzustellen.

    > [!Note]  
    > Systemstatuswriter sind Writer, für die das [**VSS \_ Usage \_ Type**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) -Attribut entweder auf VSS- \_ UT \_ bootablesystemstate oder VSS \_ UT \_ Systemservice festgelegt ist.

     

 

 
