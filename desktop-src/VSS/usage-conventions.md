---
description: Wenn Sie Ihre eigene VSS-Anwendung entwickeln, sollten Sie die folgenden Richtlinien und Einschränkungen beachten.
ms.assetid: d4edc16c-f768-4095-9b2a-b706f19f9e61
title: VSS-Anwendungskompatibilität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca1f6f3013856087e70247aed21d8f35aa4cf09
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483016"
---
# <a name="vss-application-compatibility"></a>VSS-Anwendungskompatibilität

Wenn Sie Ihre eigene VSS-Anwendung entwickeln, sollten Sie die folgenden Richtlinien und Einschränkungen beachten. Möglicherweise ist es hilfreich, sich auf den Beispielcode für VSS-Anfordernde, -Anbieter und -Writer zu beziehen, der im Microsoft Windows Software Development Kit (SDK) bereitgestellt wird.

> [!Note]  
> Das Windows SDK kann nur für die Entwicklung von VSS-Anwendungen für Windows Vista und höher Windows Betriebssystemversionen verwendet werden. Es kann nicht verwendet werden, um VSS-Anfordernde, -Anbieter oder Writer für Windows Server 2003 R2, Windows Server 2003 oder Windows XP zu entwickeln.

 

**Windows Server 2003 R2, Windows Server 2003 und Windows XP:** VSS ist im Volumeschattenkopie-Dienst 7.2 SDK verfügbar, das Sie unter herunterladen [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490) können. Beachten Sie, dass die 64-Bit-Vssapi.lib-Dateien in den Verzeichnissen unter dem Verzeichnis Win2003 Obj für \\ die 64-Bit-Versionen von Windows Server 2003 R2, Windows Server 2003 und Windows XP verwendet werden können. Dieses SDK stellt auch Beispielcode für VSS-Anforderungsanbieter, -Anbieter und -Writer bereit.

## <a name="compiling-vss-applications"></a>Kompilieren von VSS-Anwendungen

Beim Entwickeln eines Anfordernden, z. B. einer Sicherungsanwendung:

-   Schließen Sie die folgenden Header ein: <dl> Vss.h  
    VsWriter.h  
    VsBackup.h  
    </dl>
-   Link the following library: <dl> VssApi.Lib  
    </dl>

Beim Entwickeln eines Writers:

-   Schließen Sie die folgenden Header ein: <dl> Vss.h  
    VsWriter.h  
    </dl>
-   Link the following library: <dl> VssApi.lib  
    </dl>

## <a name="supported-configurations-and-restrictions"></a>Unterstützte Konfigurationen und Einschränkungen

In der folgenden Liste werden die unterstützten Konfigurationen und Einschränkungen beschrieben:

-   VSS wird für Versionen des Betriebssystems bereitgestellt und unterstützt Windows xp ab Windows XP.
-   In der folgenden Tabelle sind die Kompatibilitätsinformationen für Windows zusammengefasst. Wenn eine VSS-Anwendung für eine angegebene Windows-Version "kompiliert" wird, bedeutet dies, dass die Anwendung mit den Headerdateien und Bibliotheken kompiliert wurde, die für diese Version spezifisch sind.

    > [!Note]  
    > Hardwareanbieter werden nur auf Windows Serverbetriebssystemversionen ausgeführt. Sie werden nicht auf Windows Clientbetriebssystemversionen ausgeführt.

     

    > [!Note]  
    > In den folgenden Tabellen sollte Windows Server 2008 mit Service Pack 2 (SP2) als identisch mit Windows Server 2008 betrachtet werden. Weitere Informationen zu Windows Server 2008 mit SP2 finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=178730> . Windows Server 2003 R2 sollte als identisch mit server 2003 Windows Server 2003 betrachtet werden.

     

    > [!Note]  
    > Wenn eine VSS-Anwendung für Windows Server 2003 oder höher kompiliert wird, wird sie auch in späteren Versionen von Windows.

     

    

    
| VSS-Anfordernde, Writer und Anbieter, die für kompiliert wurden | Wird unter ausgeführt | 
|-----------------------------------------------------|-------------|
| Windows Server 2008 R2 (64 Bit), Windows 7 (64 Bit), Windows Server 2008 (64 Bit) und Windows Vista (64 Bit) | Windows Server 2008 R2 (64 Bit), Windows 7 (64 Bit), Windows Server 2008 (64 Bit) und Windows Vista (64 Bit) | 
| Windows Server 2008 R2 (32 Bit), Windows 7 (32 Bit), Windows Server 2008 (32 Bit) und Windows Vista (32 Bit) | Windows Server 2008 R2 (32 Bit), Windows 7 (32 Bit), Windows Server 2008 (32 Bit) und Windows Vista (32 Bit) | 
| Windows Server 2003 (64-Bit) | Windows Server 2008 R2 (64 Bit), Windows 7 (64 Bit), Windows Server 2008 (64 Bit), Windows Vista (64 Bit) und Windows Server 2003 (64 Bit) | 
| Windows Server 2003 (32-Bit) | Windows Server 2008 R2 (32 Bit), Windows 7 (32 Bit), Windows Server 2008 (32 Bit), Windows Vista (32 Bit) und Windows Server 2003 (32 Bit)    <blockquote>    [!Note]<br />    Anfordernde Personen werden auch auf Windows Server 2003 (64-Bit) ausgeführt.    </blockquote><br /> | 
| Windows XP 64-Bit Edition | Windows Server 2003 (64-Bit) und Windows XP 64-Bit Edition | 
| Windows XP (32-Bit) | Windows XP (32-Bit) | 


    

     

    

    | So kompilieren Sie einen VSS-Anfinger, Writer oder Anbieter für        | Zweck                                                                                                                                       |
    |------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
    | Windows Server 2008 R2 oder Windows 7                        | Windows SDK für Windows 7 (verfügbar im [Windows Download Center.)](https://www.microsoft.com/download/details.aspx?id=8279)                |
    | Windows Server 2008 oder Windows Vista                       | Windows SDK für Windows Server 2008 (verfügbar im [Windows SDK Developer Center).](https://msdn.microsoft.com/windows/bb980924.aspx) |
    | Windows Server 2003 R2, Windows Server 2003 oder Windows XP | [Volumeschattenkopie-Dienst 7.2 SDK](https://www.microsoft.com/download/details.aspx?id=23490)                                                      |

    

     

-   Alle 32-Bit-VSS-Anwendungen (Anfordernde, Anbieter und Writer) müssen als native 32-Bit- oder 64-Bit-Anwendungen ausgeführt werden. Die Ausführung unter WOW64 wird nicht unterstützt.

    **Windows Server 2003 und Windows XP:** Das Ausführen von 32-Bit-VSS-Anfordernden unter WOW64 wird unterstützt, aber nicht für Systemstatussicherungen. Das Ausführen von 32-Bit-VSS-Anbietern und Writern unter WOW64 wird nicht unterstützt. Die Unterstützung für die Ausführung von 32-Bit-Requestern unter WOW64 wurde in Windows Vista und nachfolgenden Versionen entfernt.

-   Eine Schattenkopie, die auf Windows Server 2003 R2 oder Windows Server 2003 erstellt wurde, kann nicht auf einem Computer verwendet werden, auf dem Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird. Eine Schattenkopie, die auf Windows Server 2008 R2 oder Windows Server 2008 erstellt wurde, kann nicht auf einem Computer verwendet werden, auf dem Windows Server 2003 ausgeführt wird. Eine Schattenkopie, die auf Windows Server 2008 erstellt wurde, kann jedoch auf einem Computer mit Windows Server 2008 R2 und umgekehrt verwendet werden.
-   Um Schattenkopien zu unterstützen, muss ein System, auf dem VSS ausgeführt wird, über mindestens ein NTFS-Dateisystem verfügen. Dieses Dateisystem hosten den "Diff Area" der Schattenkopie. Weitere Informationen finden Sie unter [Systemanbieter](providers.md).
-   Bei Vorhandensein eines NTFS-Dateisystems und bei entsprechender [](shadow-copy-context-configurations.md)Kontextauswahl (siehe Schattenkopiekontextkonfigurationen) kann jedes unterstützte lokale Dateisystem schattenkopiert werden.
-   Sie können Schattenkopien nur für lokal bereitgestellte Dateisysteme erstellen. Remotefreigaben und andere übergemountete Dateisysteme können nicht vom System, das sie ein mountt, schattenkopiert werden. Diese Dateisysteme können nur von den Systemen, die die Dateisysteme bedienen, schattenkopiert werden.
-   Writer und Anfordernde sollten nur lokale Ressourcen angeben. Lokale Ressourcen sind Sätze von Dateien, deren absoluter Pfad mit einem Laufwerkbuchstaben beginnt und der Laufwerkbuchstaben nicht einem bereitgestellten Ordner auf einer Remotefreigabe zugeordnet werden kann.
-   Die maximale Anzahl von Softwareschattenkopien für jedes Volume beträgt 512. Standardmäßig können Sie jedoch nur 64 Schattenkopien verwalten, die vom Feature „Schattenkopien von freigegebenen Ordnern“ verwendet werden. Verwenden Sie den [Registrierungsschlüssel MaxShadowCopies,](../backup/registry-keys-for-backup-and-restore.md) um den Grenzwert für das Feature Schattenkopien freigegebener Ordner zu ändern.
-   Die Sicherungskomponenteninfrastruktur unterstützt das Sichern von Clusterressourcen als Writerkomponenten nicht. Zum Sichern von Clusterressourcen sollten Anwendungen davon ausgehen, dass der Pfad zu einem bestimmten Clusterknoten lokal ist.
-   [!Note]  
    > Microsoft bietet keinen technischen Support für Entwickler oder IT-Mitarbeiter bei der Implementierung von Online-Systemstatuswiederherstellungen auf Windows (alle Releases).

     

    Beim Sichern und Wiederherstellen des Systemstatus empfiehlt es sich, die System- und Startvolumes zusätzlich zu den von den Systemstatusschreibern aufzählten Dateien zu sichern und wiederhergestellt zu werden.

    > [!Note]  
    > Systemstatusschreiber sind Writer, deren [**VSS \_ USAGE \_ TYPE-Attribut**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) entweder auf VSS \_ UT \_ BOOTABLESYSTEMSTATE oder VSS \_ UT \_ SYSTEMSERVICE festgelegt ist.

     

 

 
