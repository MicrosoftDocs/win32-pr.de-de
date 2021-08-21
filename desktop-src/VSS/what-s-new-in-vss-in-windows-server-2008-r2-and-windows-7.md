---
description: Windows Server 2008 R2 und Windows 7 führen die folgenden Änderungen an der Volumeschattenkopie-Dienst ein.
ms.assetid: 1287f175-29e4-40be-804b-d78542e76efc
title: 'Neuerungen: VSS in Windows Server 2008 R2 & Windows 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eeaaf42a82e13c5766ee3cfa6ba9fe73a36a783824497482ac97fc20d058a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121526"
---
# <a name="whats-new-vss-in-windows-server-2008-r2--windows-7"></a>Neuerungen: VSS in Windows Server 2008 R2 & Windows 7

Windows Server 2008 R2 und Windows 7 führen die folgenden Änderungen an der Volumeschattenkopie-Dienst ein.

## <a name="new-vss-interfaces"></a>Neue VSS-Schnittstellen

<dl>

[**IVssBackupComponentsEx3**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)  
[**IVssComponentEx2**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)  
[**IVssCreateExpressWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)  
[**IVssExpressWriter**](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)  
</dl>

## <a name="new-vss-classes"></a>Neue VSS-Klassen

<dl>

[**CVssWriterEx2**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex2)  
</dl>

## <a name="new-vss-enumerations"></a>Neue VSS-Enumerationen

<dl>

[**\_VSS-WIEDERHERSTELLUNGSOPTIONEN \_**](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)  
</dl>

## <a name="new-vss-functions"></a>Neue VSS-Funktionen

<dl>

[**CreateVssExpressWriter**](/windows/desktop/api/VsWriter/nf-vswriter-createvssexpresswriter)  
</dl>

## <a name="existing-vss-interface-modifications"></a>Vorhandene VSS-Schnittstellenänderungen

<dl>

[**IVssHardwareSnapshotProviderEx-Schnittstelle**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)<dl> Methode hinzugefügt: [ **ResyncLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)  
</dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a>VSS-Ereignisablaufverfolgung und -protokollierung

Ab Windows Server 2008 R2 und Windows 7 können Sie das VssTrace-Tool, das Logman-Tool oder das Tracelog-Tool verwenden, um Ablaufverfolgungsinformationen für die VSS-Infrastruktur zu sammeln. Weitere Informationen finden Sie unter [Verwenden von Ablaufverfolgungstools mit VSS.](using-tracing-tools-with-vss.md)

## <a name="lun-resynchronization"></a>LUN-Neusynchronisierung

In Windows Server 2008 R2 und Windows 7 können VSS-Anforderer ein Hardwareschattenkopie-Anbieter-Feature namens LUN-Neusynchronisierung (oder LUN-Neusynchronisierung) verwenden. Dies ist ein Schema für die schnelle Wiederherstellung, mit dem ein Anwendungsadministrator Daten aus einer Schattenkopie in der ursprünglichen logischen Einheitennummer (LOGICAL Unit Number, LUN) oder in einer neuen LUN wiederherstellen kann. Bei der Schattenkopie kann es sich um einen vollständigen Klon oder eine differenzielle Schattenkopie handeln. In beiden Fällen hat die Ziel-LUN am Ende der erneuten Synchronisierung denselben Inhalt wie die Schattenkopie-LUN. Während der erneuten Synchronisierung erstellt das Array eine Kopie auf Blockebene aus der Schattenkopie in die Ziel-LUN. Weitere Informationen finden Sie unter

-   [LUN Resync : Ein schnelles Wiederherstellungsszenario in Server 2008 R2](https://blogs.technet.com/filecab/archive/2009/04/11/lun-resync-a-fast-recovery-scenario-in-server-2008-r2.aspx)
-   "Verwendung von Schattenkopien" in [Volumeschattenkopie-Dienst](/windows-server/storage/file-server/volume-shadow-copy-service)
-   [Allgemeine LUN-Neusynchronisierungs-Fehler](https://blogs.msdn.com/gregd/archive/2009/07/27/common-lun-resync-gotchas.aspx)

## <a name="express-writers"></a>Express Writer

In Windows Server 2008 R2 und Windows 7 ermöglicht die VSS Express-Schnittstelle einer Anwendung, den Speicherort ihrer Datendateien zu registrieren, ohne einen VSS Writer zu implementieren. Weitere Informationen finden Sie unter [Volumeschattenkopie-Dienst Express Writer (VSS).](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx)

## <a name="new-vss-writers"></a>Neue VSS Writer

Windows Server 2008 R2 und Windows 7 führen die folgenden VSS Writer ein:

-   Performance Counters Writer
-   Taskplaner Writer
-   VSS Metadata Store Writer

Diese neuen Writer sind in [In-Box VSS Writers](in-box-vss-writers.md)dokumentiert.

 

 
