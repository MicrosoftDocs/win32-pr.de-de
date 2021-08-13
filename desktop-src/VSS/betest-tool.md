---
description: BETest ist eine VSS-Anfordernde, die erweiterte Sicherungs- und Wiederherstellungsvorgänge testet.
ms.assetid: a6cc7308-a9fa-4a84-9e7c-4d0adda28db5
title: BETest-Tool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5f37e8bfc224061a8205bf0759cbba4798b0d53227e4f12d89b1e9ddf629d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471150"
---
# <a name="betest-tool"></a>BETest-Tool

BETest ist eine VSS-Anfordernde, die erweiterte Sicherungs- und Wiederherstellungsvorgänge testet. Dieses Tool kann verwendet werden, um zu testen, ob eine Anwendung komplexe VSS-Features wie die folgenden verwendet:

-   Inkrementelle und differenzielle Sicherung
-   Komplexe Wiederherstellungsoptionen, z. B. autoritative Wiederherstellung
-   Rollforwardoptionen

> [!Note]  
> BETest ist im Microsoft Windows Software Development Kit (SDK) für Windows Vista und höher enthalten. Das VSS 7.2 SDK enthält eine Version von BETest, die nur auf Windows Server 2003 ausgeführt wird. In diesem Thema wird die Windows SDK-Version von BETest beschrieben, nicht die Windows Server 2003-Version, die im VSS 7.2 SDK enthalten ist. Informationen zum Herunterladen des Windows SDK und des VSS 7.2 SDK finden Sie [unter Volumeschattenkopie-Dienst.](volume-shadow-copy-service-portal.md)

 

In der Windows SDK-Installation finden Sie das BETest-Tool unter `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (für 64-Bit-Windows) und `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (für 32-Bit-Windows).

## <a name="running-the-betest-tool"></a>Ausführen des BETest-Tools

Verwenden Sie die folgende Syntax, um das BETest-Tool über die Befehlszeile auszuführen:

 *BETest-Befehlszeilenoptionen*

Das folgende Verwendungsbeispiel zeigt, wie Sie das BETest-Tool zusammen mit dem [VSS Test Writer-Tool](vss-test-writer-tool.md)verwenden, bei dem es sich um einen VSS Writer handelt.

**Beispiel für die Verwendung des BETest-Tools**

1.  Erstellen Sie ein Testverzeichnis mit dem Namen C: \\ BETest. Kopieren Sie die folgenden Dateien in dieses Verzeichnis:
    -   betest.exe
    -   vswriter.exe
    -   [BetestSample.xml](#sample-xml-configuration-file-betestsamplexml)
    -   [VswriterSample.xml](#sample-xml-configuration-file-vswritersamplexml)
2.  Erstellen Sie ein Verzeichnis mit dem Namen C: \\ TestPath. Speichern Sie einige Testdatendateien in diesem Verzeichnis.
3.  Erstellen Sie ein Verzeichnis mit dem Namen C: \\ BackupDestination. Lassen Sie dieses Verzeichnis leer.
4.  Öffnen Sie zwei Befehlsfenster mit erhöhten Rechten, und legen Sie jeweils das Arbeitsverzeichnis auf C: \\ BETest fest.
5.  Starten Sie im ersten Befehlsfenster das [VSS Test Writer-Tool](vss-test-writer-tool.md) wie folgt:

    **vswriter.exe VswriterSample.xml**

    Die vswriterSample.xml-Datei konfiguriert das VSS Test Writer-Tool (vswriter), um den Inhalt des Verzeichnisses c: TestPath als Vorbereitung auf einen \\ Sicherungsvorgang zu melden. Beachten Sie, dass das VSS Test Writer-Tool erst dann eine Ausgabe erzeugt, wenn es Aktivitäten von einem Anfordernden wie BETest erkennt. Drücken Sie STRG+C, um das VSS Test Writer-Tool zu beenden.

6.  Verwenden Sie im zweiten Befehlsfenster das BETest-Tool, um einen Sicherungsvorgang wie folgt auszuführen:

    **betest.exe /B /S backup.xml /D C: \\ BackupDestination /X BetestSample.xml**

    BETest gesichert die Dateien aus dem Verzeichnis C: \\ TestPath im Verzeichnis C: \\ BackupDestination. Das Sicherungskomponentendokument wird in C: \\ BETest-backup.xml. \\

7.  Wenn der Sicherungsvorgang erfolgreich ist, löschen Sie den Inhalt des Verzeichnisses C: TestPath, und verwenden Sie das BETest-Tool, um einen Wiederherstellungsvorgang \\ wie folgt durchzuführen:

    **betest.exe /R /S backup.xml /D C: \\ BackupDestination /X BetestSample.xml**

## <a name="betest-tool-command-line-options"></a>BETest-Tool Command-Line Optionen

Das BETest-Tool verwendet die folgenden Befehlszeilenoptionen, um die auszuführende Arbeit zu identifizieren.

<dl> <dt>

<span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**
</dt> <dd>

Führt einen autoritativen Wiederherstellungsvorgang für Active Directory oder den Active Directory-Anwendungsmodus aus.

**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.

</dd> <dt>

<span id="_B"></span><span id="_b"></span>**/B**
</dt> <dd>

Führt einen Sicherungsvorgang aus, führt jedoch keine Wiederherstellung durch.

</dd> <dt>

<span id="_BC"></span><span id="_bc"></span>**/BC**
</dt> <dd>

Führt nur den Sicherungsvorgang aus.

**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.

</dd> <dt>

<span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span>**/C Dateiname** 
</dt> <dd>

> [!Note]  
> Diese Befehlszeilenoption wird nur aus Gründen der Abwärtskompatibilität bereitgestellt. Stattdessen sollte die Befehlszeilenoption **/X** verwendet werden.

 

Wählt die Zu sichernden oder wiederherzustellenden Komponenten basierend auf dem Inhalt der Konfigurationsdatei aus, die von *Dateiname angegeben wird.* Diese Datei darf nur ANSI-Zeichen im Bereich von 0 bis 127 enthalten und darf nicht größer als 1 MB sein. Jede Zeile in der Datei muss das folgende Format verwenden:

*WriterId* : *ComponentName*;

Dabei *ist WriterId* die Writer-ID und *ComponentName* der Name einer der Komponenten des Writers. Die Writer-ID und komponentennamen müssen in Anführungszeichen gesetzt werden, und es müssen Leerzeichen vor und nach dem Doppelpunkt (:). Wenn mindestens zwei Komponenten angegeben werden, müssen sie durch Kommas getrennt werden. Beispiel:

"5affb034-969f-4919-8875-88f830d0ef89" : "TestFiles1", "TestFiles2", "TestFiles3";

</dd> <dt>

<span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D-Pfad** 
</dt> <dd>

Speichern Sie die gesicherten Dateien in dem sicherungsverzeichnis, das unter Pfad angegeben ist, oder stellen Sie sie *wieder her.*

</dd> <dt>

<span id="_NBC"></span><span id="_nbc"></span>**/NBC**
</dt> <dd>

Lässt den Sicherungsvorgang aus.

**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.

</dd> <dt>

<span id="_O"></span><span id="_o"></span>**/O**
</dt> <dd>

Gibt an, dass die Sicherung einen startbaren Systemstatus enthält.

</dd> <dt>

<span id="_P"></span><span id="_p"></span>**/P**
</dt> <dd>

Erstellt eine persistente Schattenkopie.

**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.

</dd> <dt>

<span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span>**/Pre** *Filename*
</dt> <dd>

Wenn der in der Befehlszeilenoption **/T** angegebene Sicherungstyp INCREMENTAL oder DIFFERENTIAL ist, legen Sie das Sicherungsdokument auf die Datei fest, die durch *Dateiname* für die vorherige vollständige oder inkrementelle Sicherung angegeben wird.

**Windows Server 2003 und Windows XP:** Diese Befehlszeilenoption wird nicht unterstützt.

</dd> <dt>

<span id="_R"></span><span id="_r"></span>**/R**
</dt> <dd>

Führt eine Wiederherstellung durch, führt jedoch keine Sicherung durch. Muss zusammen mit der **Befehlszeilenoption /S** verwendet werden.

</dd> <dt>

<span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**
</dt> <dd>

Erstellt eine Schattenkopie, die für das Anwendungsrollback verwendet werden kann.

**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.

</dd> <dt>

<span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *Dateiname*
</dt> <dd>

Im Falle einer Sicherung speichert das Sicherungsdokument in der Datei, die unter *Dateiname angegeben ist.* Nur bei der Wiederherstellung lädt das Sicherungsdokument aus dieser Datei.

</dd> <dt>

<span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**
</dt> <dd>

Erstellt eine Volumeschattenkopie, führt aber keine Sicherung oder Wiederherstellung durch.

**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.

</dd> <dt>

<span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**
</dt> <dd>

Beendet BETest, wenn der erste Writerfehler auftritt.

**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.

</dd> <dt>

<span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *BackupType*
</dt> <dd>

Gibt den Sicherungstyp an. *BackupType* kann FULL, LOG, COPY, INCREMENTAL oder DIFFERENTIAL sein. Weitere Informationen zu Sicherungstypen finden Sie unter [**VSS \_ BACKUP \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_backup_type).

</dd> <dt>

<span id="_V"></span><span id="_v"></span>**/V**
</dt> <dd>

Generiert eine ausführliche Ausgabe, die für die Problembehandlung verwendet werden kann.

**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.

</dd> <dt>

<span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span>**/X** *Dateiname*
</dt> <dd>

Wählt die Zu sichernden oder wiederherzustellenden Komponenten basierend auf dem Inhalt der XML-Konfigurationsdatei aus, die von *Dateiname angegeben wird.* Diese Datei darf nur ANSI-Zeichen im Bereich von 0 bis 127 enthalten. Das Format der XML-Datei wird durch das Schema in der datei BETest.xml definiert. Eine Beispielkonfigurationsdatei finden Sie unter BetestSample.xml. Beide Dateien befinden sich im Verzeichnis vsstools.

> [!Note]  
> Sie können die BETest.xml-Datei in Internet Explorer anzeigen. Bevor Sie diese Datei öffnen, stellen Sie sicher, dass sich die Datei xdr-schema.xsl im selben Verzeichnis wie BETest.xml befindet. Die Datei xdr-schema.xsl enthält Renderinganweisungen, die die BETest.xml Datei lesbarer machen.

 

**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.

</dd> </dl>

## <a name="sample-xml-configuration-file-betestsamplexml"></a>XML-Beispielkonfigurationsdatei: BetestSample.xml

Die folgende Beispielkonfigurationsdatei, BetestSample.xml, befindet sich im Verzeichnis Vsstools.

``` syntax
<BETest>
    <Writer writerid="5affb034-969f-4919-8875-88f830d0ef89">
        <Component componentName="TestFiles">
        </Component>
    </Writer>
</BETest>
```

In diesem Beispiel einer einfachen Konfigurationsdatei wird eine Komponente ausgewählt, die gesichert oder wiederhergestellt werden soll.

## <a name="sample-xml-configuration-file-vswritersamplexml"></a>XML-Beispielkonfigurationsdatei: VswriterSample.xml

Die folgende Beispielkonfigurationsdatei, VswriterSample.xml, befindet sich im Verzeichnis Vsstools.

``` syntax
<TestWriter   usage="USER_DATA"
                    deleteFiles="no">

    <RestoreMethod method="RESTORE_IF_CAN_BE_REPLACED" 
                   writerRestore="always"
                   rebootRequired="no" />
    
    <Component componentType="filegroup" 
               componentName="TestFiles">
               <ComponentFile path="c:\TestPath" filespec="*" recursive="no" />
    </Component>

</TestWriter>
```

Das Stammelement in dieser Konfigurationsdatei heißt TestWriter. Alle anderen Elemente werden unter dem TestWriter-Element angeordnet.

Das erste TestWriter-Attribut ist das Verwendungsattribut. Dieses Attribut gibt den Verwendungstyp an, der über die [**IVssExwriterMetadata::GetIdentity-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) gemeldet wird. Einer der möglichen Werte für dieses Attribut ist USER \_ DATA.

Das zweite Attribut ist das deleteFiles-Attribut. Dieses Attribut wird unter [Konfigurieren von Writerattributen](vss-test-writer-tool.md)beschrieben.

Das erste untergeordnete Element des Stammelements ist ein RestoreMethod-Element. Dieses Element gibt Folgendes an:

-   Die Wiederherstellungsmethode (in diesem Fall RESTORE \_ IF \_ CAN BE \_ \_ REPLACED)
-   Gibt an, ob der Writer Wiederherstellungsereignisse erfordert (in diesem Fall immer).
-   Gibt an, ob nach der Wiederherstellung des Writers ein Neustart erforderlich ist (in diesem Fall nein).

Dieses Element kann optional eine Zuordnung alternativer Speicherorte angeben. (In diesem Fall wird kein alternativer Speicherort angegeben.) Weitere Informationen finden Sie unter [Angeben alternativer Speicherortzuordnungen.](vss-test-writer-tool.md)

Das zweite untergeordnete Element ist ein Component-Element. Dieses Element bewirkt, dass der Writer den Metadaten eine Komponente hinzufügt. Ein Component-Element enthält Attribute, um die Komponente und untergeordnete Elemente zu beschreiben, um den Inhalt der Komponente zu beschreiben, z. B.:

-   componentType, um anzugeben, ob es sich um eine Dateigruppe oder eine Datenbank handelt (in diesem Fall eine Dateigruppe).
-   logicalPath für den logischen Pfad der Komponente (in diesem Fall wird keine angegeben)
-   componentName für den Namen der Komponente (in diesem Fall "TestFiles")
-   Auswählbar, um den Sicherungsstatus anzugeben, der ausgewählt werden kann

Das Component-Element verfügt auch über ein untergeordnetes Element mit dem Namen ComponentFile, um dieser Komponente eine Dateispezifikation hinzuzufügen. (Ein Component-Element kann über eine beliebige Anzahl von ComponentFile-Elementen verfügen, die für jede Komponente angegeben werden können.) Dieses ComponentFile-Element weist die folgenden Attribute auf:

-   path="c: \\ TestPath"
-   filespec=" \* "
-   recursive="no"

 

 



