---
description: Mit Windows Server 2008 R2 und Windows 7 werden die folgenden Änderungen am Volumeschattenkopie-Dienst eingeführt.
ms.assetid: 1287f175-29e4-40be-804b-d78542e76efc
title: 'Neuerungen: VSS in Windows Server 2008 R2 & Windows 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3677f89517a770a4519369ae11f2eed7e7985414
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350442"
---
# <a name="whats-new-vss-in-windows-server-2008-r2--windows-7"></a>Neuerungen: VSS in Windows Server 2008 R2 & Windows 7

Mit Windows Server 2008 R2 und Windows 7 werden die folgenden Änderungen am Volumeschattenkopie-Dienst eingeführt.

## <a name="new-vss-interfaces"></a>Neue VSS-Schnittstellen

<dl>

[**IVssBackupComponentsEx3**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)  
[**IVssComponentEx2**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)  
[**Ivsskreateexpressschreitermetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)  
[**Ivssexpresswriter**](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)  
</dl>

## <a name="new-vss-classes"></a>Neue VSS-Klassen

<dl>

[**CVssWriterEx2**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex2)  
</dl>

## <a name="new-vss-enumerations"></a>Neue VSS-Enumerationen

<dl>

[**VSS- \_ Wiederherstellungs \_ Optionen**](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)  
</dl>

## <a name="new-vss-functions"></a>Neue VSS-Funktionen

<dl>

[**"Kreatevssexpresswriter"**](/windows/desktop/api/VsWriter/nf-vswriter-createvssexpresswriter)  
</dl>

## <a name="existing-vss-interface-modifications"></a>Vorhandene Änderungen der VSS-Schnittstelle

<dl>

[**Ivsshardwaresnapshotproviderex**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex) -Schnittstelle<dl> Hinzugefügte Methode: [ **resyncluns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)  
</dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a>VSS-Ereignis Ablauf Verfolgung und Protokollierung

Ab Windows Server 2008 R2 und Windows 7 können Sie das vsstrace-Tool, das Logman-Tool oder das tracelog-Tool verwenden, um Ablauf Verfolgungs Informationen für die VSS-Infrastruktur zu sammeln. Weitere Informationen finden Sie unter [Verwenden von Ablauf Verfolgungs Tools mit VSS](using-tracing-tools-with-vss.md).

## <a name="lun-resynchronization"></a>LUN-Neusynchronisierung

In Windows Server 2008 R2 und Windows 7 können VSS-Anforderer ein Hardwareschattenkopie-Anbieter-Feature namens LUN-Neusynchronisierung (oder LUN-Neusynchronisierung) verwenden. Dies ist ein schnelles Wiederherstellungs Schema, das es einem Anwendungs Administrator ermöglicht, Daten aus einer Schatten Kopie in die ursprüngliche logische Gerätenummer (Logical Unit Number, LUN) oder in eine neue LUN wiederherzustellen. Bei der Schattenkopie kann es sich um einen vollständigen Klon oder eine differenzielle Schattenkopie handeln. In beiden Fällen hat die Ziel-LUN am Ende der erneuten Synchronisierung denselben Inhalt wie die Schattenkopie-LUN. Während der erneuten Synchronisierung erstellt das Array eine Kopie auf Blockebene aus der Schattenkopie in die Ziel-LUN. Weitere Informationen finden Sie unter

-   [LUN Resync: ein schnelles Wiederherstellungs Szenario auf Server 2008 R2](https://blogs.technet.com/filecab/archive/2009/04/11/lun-resync-a-fast-recovery-scenario-in-server-2008-r2.aspx)
-   "Wie Schatten Kopien verwendet werden" in [Volumeschattenkopie-Dienst](/windows-server/storage/file-server/volume-shadow-copy-service)
-   [Allgemeine LUN-Neusynchronisierungs Probleme](https://blogs.msdn.com/gregd/archive/2009/07/27/common-lun-resync-gotchas.aspx)

## <a name="express-writers"></a>Express Writer

In Windows Server 2008 R2 und Windows 7 ermöglicht die VSS Express-Schnittstelle einer Anwendung, den Speicherort Ihrer Datendateien zu registrieren, ohne eine VSS Writer zu implementieren. Weitere Informationen finden Sie unter [Volumeschattenkopie-Dienst (VSS) Express Writer](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx).

## <a name="new-vss-writers"></a>Neue VSS-Writer

Mit Windows Server 2008 R2 und Windows 7 werden die folgenden VSS-Writer eingeführt:

-   Leistungsindikatoren Writer
-   Taskplaner Writer
-   VSS-Metadatenspeicher-Writer

Diese neuen Writer sind in den [in-Box-VSS-Writern](in-box-vss-writers.md)dokumentiert.

 

 
