---
description: BETest ist ein VSS-Anforderer, der erweiterte Sicherungs-und Wiederherstellungs Vorgänge testet.
ms.assetid: a6cc7308-a9fa-4a84-9e7c-4d0adda28db5
title: Test Tool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7559c304532b337214108435b740595897694f7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868768"
---
# <a name="betest-tool"></a>Test Tool

BETest ist ein VSS-Anforderer, der erweiterte Sicherungs-und Wiederherstellungs Vorgänge testet. Dieses Tool kann verwendet werden, um die Verwendung komplexer VSS-Funktionen einer Anwendung zu testen, wie z. b.:

-   Inkrementelle Sicherung
-   Komplexe Wiederherstellungsoptionen wie autorisierende Wiederherstellung
-   Roll Forward-Optionen

> [!Note]  
> BETest ist im Microsoft Windows Software Development Kit (SDK) für Windows Vista und höher enthalten. Das VSS 7,2 SDK enthält eine Version von "BETest", die nur unter Windows Server 2003 ausgeführt wird. In diesem Thema wird die Windows SDK Version von BETest und nicht die Windows Server 2003-Version beschrieben, die im VSS 7,2 SDK enthalten ist. Weitere Informationen zum Herunterladen der Windows SDK und des VSS 7,2 SDK finden Sie unter [Volumeschattenkopie-Dienst](volume-shadow-copy-service-portal.md).

 

In der Windows SDK-Installation befindet sich das Tool "BETest" unter `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (für 64-Bit-Windows) und `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (für 32-Bit-Windows).

## <a name="running-the-betest-tool"></a>Ausführen des Tools "BETest"

Verwenden Sie die folgende Syntax, um das Tool "BETest" über die Befehlszeile auszuführen:

*Befehlszeilenoptionen* für **BETest**

Im folgenden Verwendungs Beispiel wird gezeigt, wie das Tool "BETest" mit dem [VSS-testwriter-Tool](vss-test-writer-tool.md)verwendet wird, das eine VSS Writer ist.

**Verwendungs Beispiel für das BETest-Tool**

1.  Erstellen Sie ein Test Verzeichnis mit dem Namen C: \\ BETest. Kopieren Sie die folgenden Dateien in dieses Verzeichnis:
    -   betest.exe
    -   vswriter.exe
    -   [BetestSample.xml](#sample-xml-configuration-file-betestsamplexml)
    -   [VswriterSample.xml](#sample-xml-configuration-file-vswritersamplexml)
2.  Erstellen Sie ein Verzeichnis mit dem Namen C: \\ TestPath. Fügen Sie einige Test Datendateien in dieses Verzeichnis ein.
3.  Erstellen Sie ein Verzeichnis mit dem Namen "C: \\ backupdestination". Lassen Sie dieses Verzeichnis leer.
4.  Öffnen Sie zwei Befehlsfenster mit erhöhten Rechten, und legen Sie für das Arbeitsverzeichnis jeweils C: \\ BETest fest.
5.  Starten Sie im ersten Befehlsfenster das [VSS-testwriter-Tool](vss-test-writer-tool.md) wie folgt:

    **vswriter.exe VswriterSample.xml**

    Die vswriterSample.xml Datei konfiguriert das VSS-testwriter-Tool (vswriter) so, dass der Inhalt des Verzeichnisses "c: \\ TestPath" als Vorbereitung für einen Sicherungs Vorgang gemeldet wird. Beachten Sie, dass das VSS-testwriter-Tool erst dann eine Ausgabe erzeugt, wenn es eine Aktivität von einer Anforderer wie z. b. betest Um das VSS-testwriter-Tool anzuhalten, drücken Sie STRG + C.

6.  Verwenden Sie im zweiten Befehlsfenster das Tool "BETest", um einen Sicherungs Vorgang wie folgt auszuführen:

    **betest.exe/B/S backup.xml/D C: \\ backupdestination/X BetestSample.xml**

    Mit "BETest" werden die Dateien aus dem Verzeichnis "c: \\ TestPath" in das Verzeichnis "c: \\ backupdestination" gesichert. Das Sicherungs Komponenten Dokument wird in C: \\ BETest- \\backup.xml gespeichert.

7.  Wenn der Sicherungs Vorgang erfolgreich ist, löschen Sie den Inhalt des Verzeichnisses "C: \\ TestPath", und verwenden Sie das Tool "BETest", um einen Wiederherstellungs Vorgang wie folgt auszuführen:

    **betest.exe/R/S backup.xml/D C: \\ backupdestination/X BetestSample.xml**

## <a name="betest-tool-command-line-options"></a>Command-Line Optionen für das betesttool

Das Tool "BETest" verwendet die folgenden Befehlszeilenoptionen zur Identifizierung der auszuführenden Aufgaben.

<dl> <dt>

<span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**
</dt> <dd>

Führt einen autorisierenden Wiederherstellungs Vorgang für Active Directory oder Active Directory Anwendungsmodus aus.

**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.

</dd> <dt>

<span id="_B"></span><span id="_b"></span>**/B**
</dt> <dd>

Führt einen Sicherungs Vorgang aus, führt jedoch keine Wiederherstellung aus.

</dd> <dt>

<span id="_BC"></span><span id="_bc"></span>**/BC**
</dt> <dd>

Führt nur den Vorgang zum Abschluss der Sicherung aus.

**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.

</dd> <dt>

<span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span>**/C** *Dateiname*
</dt> <dd>

> [!Note]  
> Diese Befehlszeilenoption wird nur aus Gründen der Abwärtskompatibilität bereitgestellt. Stattdessen sollte die Befehlszeilenoption **/X** verwendet werden.

 

Wählt die zu sichernden oder wiederherzustellenden Komponenten basierend auf dem Inhalt der durch *filename* angegebenen Konfigurationsdatei aus. Diese Datei darf nur ANSI-Zeichen im Bereich zwischen 0 und 127 enthalten und darf nicht größer als 1 MB sein. Jede Zeile in der Datei muss das folgende Format aufweisen:

" *Write ID* ": " *componentname*;"

Dabei ist " *Write ID* " die Writer-ID und " *componentname* " der Name einer der Writer-Komponenten. Die Writer-ID und die Komponentennamen müssen in Anführungszeichen stehen, und es muss Leerzeichen vor und nach dem Doppelpunkt (:). Wenn mindestens zwei Komponenten angegeben sind, müssen diese durch Kommas getrennt werden. Beispiel:

"5affb034-969f -4919-8875-88f 830d0ef89": "TestFiles1", "TestFiles2", "TestFiles3";

</dd> <dt>

<span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D** - *Pfad*
</dt> <dd>

Speichern Sie die gesicherten Dateien, oder stellen Sie Sie aus dem durch *path* angegebenen Sicherungs Verzeichnis wieder her.

</dd> <dt>

<span id="_NBC"></span><span id="_nbc"></span>**/NBC**
</dt> <dd>

Lässt den Vorgang zum Abschluss der Sicherung aus.

**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.

</dd> <dt>

<span id="_O"></span><span id="_o"></span>**/O**
</dt> <dd>

Gibt an, dass die Sicherung einen Start fähigen Systemstatus enthält.

</dd> <dt>

<span id="_P"></span><span id="_p"></span>**/P**
</dt> <dd>

Erstellt eine persistente Schatten Kopie.

**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.

</dd> <dt>

<span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span>**/Pre** *Dateiname*
</dt> <dd>

Wenn der in der Befehlszeilenoption **/T** angegebene Sicherungstyp inkrementell oder Differenziell ist, legen Sie das Sicherungs Dokument auf die Datei fest, die für eine vorherige vollständige oder inkrementelle Sicherung von *filename*

**Windows Server 2003 und Windows XP:** Diese Befehlszeilenoption wird nicht unterstützt.

</dd> <dt>

<span id="_R"></span><span id="_r"></span>**/R**
</dt> <dd>

Führt eine Wiederherstellung durch, führt jedoch keine Sicherung aus. Muss in Verbindung mit der Befehlszeilenoption **/S** verwendet werden.

</dd> <dt>

<span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**
</dt> <dd>

Erstellt eine Schatten Kopie, die für das Anwendungs Rollback verwendet werden kann.

**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.

</dd> <dt>

<span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *Dateiname*
</dt> <dd>

Bei der Sicherung speichert das Sicherungs Dokument in der durch *filename* angegebenen Datei. Bei nur Restore wird das Sicherungs Dokument aus dieser Datei geladen.

</dd> <dt>

<span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**
</dt> <dd>

Erstellt eine Volumeschattenkopie, führt aber keine Sicherung oder Wiederherstellung aus.

**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.

</dd> <dt>

<span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**
</dt> <dd>

Beendet Tests, wenn der erste Writer-Fehler auftritt.

**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.

</dd> <dt>

<span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *backuptype*
</dt> <dd>

Gibt den Sicherungstyp an. *Backuptype* kann vollständig, protokolliert, kopiert, inkrementell oder Differenziell sein. Weitere Informationen zu Sicherungs Typen finden Sie unter [**VSS \_ - \_ Sicherungstyp**](/windows/desktop/api/Vss/ne-vss-vss_backup_type).

</dd> <dt>

<span id="_V"></span><span id="_v"></span>**/V**
</dt> <dd>

Generiert eine ausführliche Ausgabe, die für die Problembehandlung verwendet werden kann.

**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.

</dd> <dt>

<span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span>**/X** *Dateiname*
</dt> <dd>

Wählt die zu sichernden oder wiederherzustellenden Komponenten basierend auf dem Inhalt der durch *filename* angegebenen XML-Konfigurationsdatei aus. Diese Datei darf nur ANSI-Zeichen im Bereich von 0 bis 127 enthalten. Das Format der XML-Datei wird durch das Schema in der BETest.xml-Datei definiert. Eine Beispielkonfigurationsdatei finden Sie unter BetestSample.xml. Beide Dateien befinden sich im vshocker-Verzeichnis.

> [!Note]  
> Sie können die BETest.xml Datei in Internet Explorer anzeigen. Bevor Sie diese Datei öffnen, stellen Sie sicher, dass sich die Datei XDR-Schema. xsl im gleichen Verzeichnis wie BETest.xml befindet. Die Datei XDR-Schema. xsl enthält Renderinganweisungen, mit denen die BETest.xml-Datei besser lesbar wird.

 

**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.

</dd> </dl>

## <a name="sample-xml-configuration-file-betestsamplexml"></a>Beispiel-XML-Konfigurationsdatei: BetestSample.xml

Die folgende Beispielkonfigurationsdatei (BetestSample.xml) finden Sie im vshocker-Verzeichnis.

``` syntax
<BETest>
    <Writer writerid="5affb034-969f-4919-8875-88f830d0ef89">
        <Component componentName="TestFiles">
        </Component>
    </Writer>
</BETest>
```

Dieses Beispiel einer einfachen Konfigurationsdatei wählt eine Komponente aus, die gesichert oder wieder hergestellt werden soll.

## <a name="sample-xml-configuration-file-vswritersamplexml"></a>Beispiel-XML-Konfigurationsdatei: VswriterSample.xml

Die folgende Beispielkonfigurationsdatei (VswriterSample.xml) finden Sie im vshocker-Verzeichnis.

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

Das Stamm Element in dieser Konfigurationsdatei hat den Namen testwriter. Alle anderen Elemente werden unter dem testwriter-Element angeordnet.

Das erste Attribut, das testwriter zugeordnet ist, ist das Usage-Attribut. Dieses Attribut gibt den Verwendungstyp an, der über die [**ivssexaminewrite Metadata:: GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) -Methode gemeldet wird. Einer der möglichen Werte für dieses Attribut sind Benutzer \_ Daten.

Das zweite Attribut ist das DeleteFiles-Attribut. Dieses Attribut wird unter [Konfigurieren von Writer-Attributen](vss-test-writer-tool.md)beschrieben.

Das erste untergeordnete Element des Root-Elements ist ein restoremethod-Element. Dieses Element gibt Folgendes an:

-   Die Restore-Methode (in diesem Fall Restore \_ , \_ Wenn \_ ersetzt werden kann \_ )
-   Gibt an, ob der Writer Wiederherstellungs Ereignisse erfordert (in diesem Fall immer).
-   Gibt an, ob ein Neustart erforderlich ist, nachdem der Writer wieder hergestellt wurde (in diesem Fall Nein).

Dieses Element kann optional eine Zuordnung alternativer Orte angeben. (In diesem Fall wird kein alternativer Speicherort angegeben.) Weitere Informationen finden Sie unter [angeben](vss-test-writer-tool.md)von Zuordnungen für Alternative Speicherorte.

Das zweite untergeordnete Element ist ein Komponenten Element. Dieses Element bewirkt, dass der Writer seinen Metadaten eine Komponente hinzufügt. Ein Component-Element enthält Attribute, mit denen die Komponente und die untergeordneten Elemente beschrieben werden, um den Inhalt der Komponente zu beschreiben, wie z. b. Folgendes:

-   componentType, um anzugeben, ob es sich um eine Datei Gruppe oder eine Datenbank handelt (in diesem Fall eine Datei Gruppe)
-   LogicalPath für den logischen Pfad der Komponente (in diesem Fall ist keine angegeben)
-   componentname für den Namen der Komponente (in diesem Fall "testfiles")
-   auswählbar zum Angeben des Status für die auswählbare Sicherung

Das Component-Element weist auch ein untergeordnetes Element mit dem Namen "componentfile" auf, um dieser Komponente eine Datei Spezifikation hinzuzufügen. (Ein Komponenten Element kann eine beliebige Anzahl von componentfile-Elementen aufweisen, die für jede Komponente angegeben werden können.) Dieses componentfile-Element weist die folgenden Attribute auf:

-   Path = "c: \\ TestPath"
-   file spec = " \* "
-   rekursiv = "Nein"

 

 



