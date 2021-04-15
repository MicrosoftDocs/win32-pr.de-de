---
title: Srdelayed.exe
description: Anwendungen, die Systemstatus Wiederherstellungs Vorgänge früh beim Start des Betriebssystems ausführen, können möglicherweise die Dateiverwaltungsfunktionen nicht verwenden, um den Kurznamen bestimmter Systemdateien zu verschieben, zu löschen oder festzulegen.
ms.assetid: cedeb48e-bc1d-48d1-9bee-0b8b0132c3e5
keywords:
- Srdelayed.exe Sicherung
- Sicherung der Systemstatus Wiederherstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a5f6b281c07f5b0ad8d6cd7e59b4f93ec9208a5
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "104474571"
---
# <a name="srdelayedexe"></a>Srdelayed.exe

Anwendungen, die Systemstatus Wiederherstellungs Vorgänge früh beim Start des Betriebssystems ausführen, können möglicherweise die Dateiverwaltungsfunktionen nicht verwenden, um den Kurznamen bestimmter Systemdateien zu verschieben, zu löschen oder festzulegen. Srdelayed.exe ist eine ausführbare Datei, die mit der Funktion Windows Server-Sicherung (WSB) in Windows Server 2008 bereitgestellt wird, mit der Systemstatus-Wiederherstellungs Anwendungen den Kurznamen von Systemdateien verschieben, löschen und festlegen können.

Das srverzögert-Tool ist für Systemstatus-Wiederherstellungs Anwendungen vorgesehen. die Dateiverwaltungsfunktionen werden nicht ersetzt. Dieses Tool sollte nur verwendet werden, wenn die Anwendung nicht in der Lage ist, den Kurznamen einer Systemdatei mithilfe der Funktionen [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa), [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea)und [**setfileshortname**](/windows/desktop/api/winbase/nf-winbase-setfileshortnamea) zu verschieben, zu löschen oder festzulegen. Während der Wiederherstellung des Systemstatus und des Neustarts wird Srdelayed.exe von der Systemwiederherstellung verwendet. das Befehlszeilen Tool wbadmin.exe verwendet, um den Kurznamen für bestimmte Systemdateien zu verschieben, zu löschen und festzulegen. Srverzögert kann daher für Entwickler nützlich sein, die die Möglichkeit haben, diese Systemdateien in ihren eigenen Systemstatus-Wiederherstellungs Anwendungen wiederherzustellen.

Mit srverzögert können die folgenden Vorgänge durchgeführt werden:

-   Ein Vorgang zum Verschieben einer Datei, der der [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) -Funktion mit dem Flag " **MoveFile \_ Delay \_ until \_ Reboot** " ähnelt
-   Ein Vorgang zum Löschen einer Datei ähnlich der [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) -Funktion
-   Ein Kurznamen-Vorgang, der der Funktion [**setfileshortname**](/windows/desktop/api/winbase/nf-winbase-setfileshortnamea) ähnelt.

Zur Verwendung von srverzögert benötigt die Anwendung den vollständigen Pfad zum Speicherort der Srdelayed.exe Datei und den vollständigen Pfad zu einer von Ihnen erstellten Unicode-Textdatei, die die Informationen enthält, die das Tool benötigt, um alle angeforderten Datei Verwaltungsvorgänge auszuführen. Die Anwendung ist dafür verantwortlich, sicherzustellen, dass diese Textdatei keine redundanten Anforderungen für einen Vorgang enthält und dass Sie jede erforderliche Reihenfolge der Datei Verwaltungsvorgänge behandelt. Da ein Ordner z. b. leer sein muss, um gelöscht zu werden, muss die Anwendung sicherstellen, dass in der Textdatei das Entfernen aller Dateien im Ordner angegeben ist, bevor der Ordner gelöscht wird.

Wenn der Eintrag **SetupExecute** nicht bereits in der Registrierung vorhanden ist, muss die Anwendung einen **reg \_ \_ MultiSZ** -typeintrag mit dem Namen **SetupExecute** unter dem folgenden Registrierungsschlüssel erstellen: **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager**.

Die Anwendung sollte das folgende Format verwenden, um den Wert von **SetupExecute** auf den vollständigen Pfad zum Speicherort der Srdelayed.exe Datei und den vollständigen Pfad zum Speicherort der Textdatei festzulegen. Stellen \\ \\ \\ Sie dem Pfad der Textdatei das Präfix "??" folgendermaßen voran:

*Vollständiger Pfad zu Srdelayed.exe* \\ \\ ?? \\ *Vollständiger Pfad zur Textdatei*  


Der folgende Wert für **SetupExecute** gibt beispielsweise an, dass sich die Srdelayed.exe im Ordner System32 befindet und die Textdatei den Namen delayedoperations hat:

C: \\ Windows \\ system32 \\srdelayed.exe \\ \\ ?? \\ C: \\ Temp \\ delayedoperations  


Leerzeichen im Pfad und Namen müssen hexadezimal codiert sein. Codieren Sie z. b. für *Programmdateien* den Pfad in " \\ \\ ?? \\ C:Program%20dateien \\a.dll ".

Wenn die Registrierung oder das System nach dem Neustart wieder hergestellt wird, muss die Anwendung sicherstellen, dass **SetupExecute** in der richtigen Registrierungs Struktur geschrieben wird. Die Wiederherstellung der Registrierung wird ausgeführt, bevor Srdelayed.exe ausgeführt wird. Die Anwendung muss **SetupExecute** in die wiederhergestellte Version der Registrierung schreiben, da dies die gelesene Version ist.

## <a name="format-for-the-srdelayed-input-file"></a>Format für die srverzögert-Eingabedatei

Alle Informationen, die für die Ausführung von Datei Verwaltungsvorgängen erforderlich sind, werden als Zeichenfolge von Unicode-Zeichen in einer Unicode-Textdatei angegeben. Die Zeichenfolge von Unicode-Zeichen wird in Datensätze partitioniert, die selbst jeweils in vier Felder partitioniert sind. Jeder Datensatz gibt eine einzelne Datei zum Verschieben, löschen oder Festlegen eines Kurznamens an. Die vier Felder der einzelnen Datensätze enthalten die Parameter für den Vorgang. Srdelayed.exe führt jeden Vorgang in der Reihenfolge aus, in der die Datensätze in der Zeichenfolge auftreten. Die Anwendung sollte alle doppelten Datensätze in dieser Datei überprüfen und die Duplikate entfernen.

Die folgende Zeichenfolge veranschaulicht das Format einer Datei, die zwei Vorgänge anfordert und aus zwei Datensätzen besteht. Jedes Parameterfeld endet mit einem einzelnen L- \\ Zeichen (0). Ein Datensatz besteht aus vier aufeinander folgenden Feldern. Ein zusätzliches einzelnes L- \\ Zeichen ' 0 ' wird an das Ende aller Datensätze angehängt.

`<ParamA1>L'\0'<ParamA2>L'\0'<ParamA3>L'\0'<ParamA4>L'\0'<ParamB1>L'\0'<ParamB2>L'\0'<ParamB3>L'\0'<ParamB4>L'\0'L'\0'`  
`|-----------------------RecordA------------------------|------------------------RecordB------------------------|`  


Die Bedeutung der ersten, zweiten, dritten und vierten Parameter Felder hängt davon ab, ob der Datensatz einen Vorgang zum Verschieben, löschen oder Festlegen eines Kurznamens beschreibt.

## <a name="format-for-a-move-file-record"></a>Format für einen Verschiebungs Datei-Datensatz

Feld 1 identifiziert dies als Anforderung zum Verschieben einer Datei. Der Wert in diesem Feld lautet immer L "muvefile", und es wird die Groß-/Kleinschreibung beachtet.

Field 2 gibt den Quell Speicherort der Datei an. Der srverzögert-Vorgang zum Verschieben von Dateien unterstützt nicht das Verschieben eines Ordners. In diesem Feld muss eine Datei angegeben werden. Der Wert für dieses Feld ist der vollständige Pfad der Datei, die an " \\ \\ ??" angehängt wird \\ , es sei denn, der Pfad enthält eine Globally Unique Identifier (GUID), die " \\ \\ ? \\ " als Präfix verwendet. Entfernen \\ \\ Sie "? \\ ", bevor Sie an " \\ \\ ?? \\ " Anhängen.

Field 3 gibt das Ziel der Datei an. Der Vorgang zum Verschieben von Dateien funktioniert nur innerhalb eines Volumes. Quelle und Ziel müssen sich auf demselben Volume befinden. Der Wert für dieses Feld ist der vollständige Pfad der Datei, die an " \\ \\ ??" angehängt wird \\ , es sei denn, der Pfad enthält eine Globally Unique Identifier (GUID), die " \\ \\ ? \\ " als Präfix verwendet. Entfernen \\ \\ Sie "? \\ ", bevor Sie an " \\ \\ ?? \\ " Anhängen.

In Feld 4 werden Statusinformationen von srverzögert empfangen. Der Wert in diesem Feld sollte für einen neuen Datensatz auf L "notexecuted" festgelegt werden.

Im folgenden Beispiel wird auf die Datei nach Laufwerks Pfad verwiesen. Wenn der Pfad und der Name der Quelle C: \\ Stage \\a.dll sind, fordert dieser Datensatz an, dass srverzögertes verschieben in c: \\ Tempa.dll erfolgt \\ .

\\ \\ ? \\ C: \\ Stufen \\a.dll \\ \\ ?? \\ C: \\ Temp \\a.dll notexecuted  


Im folgenden Beispiel wird auf die Datei mit dem GUID-Pfad des Volumes verwiesen. Wenn der Pfad und der Name der Quelle sind \\ \\ ? \\ Volume {26a21bda-a627-11d7-9931-806e6f6e6963}- \\ Phasen \\a.dll. dieser Datensatz fordert die Anforderung an, dass Sie von srverzögert verschoben wird \\ \\ ? \\ Volume {26a21bda-a627-11d7-9931-806e6f 6e6963} \\ Temp \\a.dll

 \\ \\ ? \\ Volume {26a21bda-a627-11d7-9931-806e6l6e6963} \\ Phase \\a.dll \\ \\ ? \\ Volume {26a21bda-a627-11d7-9931-806e6f 6e6963} \\ Temp \\a.dll notexecuted  


## <a name="format-for-a-delete-file-record"></a>Format für einen Lösch Datei Daten Satz

Feld 1 identifiziert dies als Anforderung zum Löschen einer Datei. Der Wert in diesem Feld lautet immer L "DeleteFile", und es wird die Groß-/Kleinschreibung beachtet.

Feld 2 wird nicht verwendet. Der Wert in diesem Feld sollte auf L "nicht verwendet" festgelegt werden.

Field 3 gibt die zu entfernende Datei an. Ein Ordner muss leer sein, um entfernt werden zu können. Verwenden Sie Vorgänge zum Löschen von Dateien, um alle Dateien im Ordner zu entfernen, bevor Sie den Ordner entfernen. Der Wert für dieses Feld ist der vollständige Pfad der Datei, die an " \\ \\ ??" angehängt wird \\ , es sei denn, der Pfad enthält eine Globally Unique Identifier (GUID), die " \\ \\ ? \\ " als Präfix verwendet. Entfernen \\ \\ Sie "? \\ ", bevor Sie an " \\ \\ ?? \\ " Anhängen.

In Feld 4 werden Statusinformationen von srverzögert empfangen. Der Wert in diesem Feld sollte für einen neuen Datensatz auf L "notexecuted" festgelegt werden.

Im folgenden Beispiel wird auf die Datei nach Laufwerks Pfad verwiesen. Wenn der Pfad und der Name C: \\ Temp \\b.dll sind, fordert dieser Datensatz an, dass die Datei von srverzögert gelöscht wird.

DeleteFile nicht verwendet \\ \\ ?? \\ C: \\ Temp \\b.dll notexecuted  


Im folgenden Beispiel wird auf die Datei mit der VolumeGuid verwiesen. Wenn Pfad und Name \\ \\ ? \\ Volume {26a21bda-a627-11d7-9931-806e6bda-a d e6fi6e6963} temporäre \\ \\b.dll. dieser Datensatz fordert an, dass srverzögert die Datei entfernt.

DeleteFile nicht verwendet \\ \\ ?? \\ Volume {26a21bda-a627-11d7-9931-806e6f 6e6963} \\ Temp \\b.dll\\ notexecuted  


## <a name="format-for-set-short-name-record"></a>Format für Short-Name Datensatz festlegen

Feld 1 identifiziert dies als Anforderung zum Festlegen des Kurznamens einer Datei. Der Wert in diesem Feld lautet immer L "setfileshortname", und es wird die Groß-/Kleinschreibung beachtet.

Feld 2 gibt den Kurznamen an.

Feld 3: gibt den Pfad und den langen Namen an, um den Kurznamen zu erhalten. Der Wert für dieses Feld ist der Pfad und der lange Name der Datei, die an " \\ \\ ??" angehängt wird \\ , es sei denn, der Pfad enthält eine Globally Unique Identifier (GUID), die " \\ \\ ? \\ " als Präfix verwendet. Entfernen \\ \\ Sie "? \\ ", bevor Sie an " \\ \\ ?? \\ " Anhängen.

In Feld 4 werden Statusinformationen von srverzögert empfangen. Der Wert in diesem Feld sollte für einen neuen Datensatz auf L "notexecuted" festgelegt werden.

Im folgenden Beispiel wird auf die Datei nach Laufwerks Pfad verwiesen. Wenn der Pfad und der Name der Datei C: \\ Temp \\ShortFileName.dll sind, fordert dieser Datensatz an, dass die Datei einen Kurznamen, shortn ~1.dll erhält.

Setfileshortname-shortn ~1.dll \\ \\ ?? \\ C: \\ Temp \\ShortFileName.dll notexecuted  


Im folgenden Beispiel wird auf die Datei mit der VolumeGuid verwiesen. Wenn der Pfad und der Name der Datei \\ \\ ? \\ Volume {26a21bda-a627-11d7-9931-806e6bda-a d e6f 6e6963} temporäre \\ \\ShortFileName.dll\\ . dieser Datensatz fordert an, dass die Datei einen Kurznamen, shortn ~1.dll erhält.

Setfileshortname-shortn ~1.dll \\ \\ ?? \\ Volume {26a21bda-a627-11d7-9931-806e6f 6e6963} \\ Temp \\ShortFileName.dll\\ notexecuted  


## <a name="srdelayed-operations-status"></a>Status der srverzögerten Vorgänge

Srverzögert schreibt die Zeichenfolge L "SC =*xxxxxxx*" in das vierte Feld jedes Datensatzes der Textdatei, wobei *xxxxxxx* ein Hexadezimalwert ist, der den Status des angeforderten Vorgangs angibt. Der Wert NULL gibt an, dass der Vorgang erfolgreich war.

Srverzögert erstellt einen Registrierungsschlüssel mit dem Namen **SystemRestore** unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** , um das Ergebnis des gesamten Wiederherstellungs Vorgangs zu protokollieren. Wenn srverzögert alle angeforderten Vorgänge erfolgreich ausführt, wird der Name restorestatus result unter diesem Schlüssel mit einem Wert von 0 (null) geschrieben. Wenn srverzögert keine der angeforderten Vorgänge ausführen kann, werden die Namen restorestatus result und restorestatus Details unter diesem Schlüssel mit Werten ungleich NULL geschrieben. Der Name restorestatus Details wird nur unter diesem Schlüssel geschrieben, wenn srverzögert keine angeforderten Vorgänge ausführen kann. Wenn ein Vorgang zum Festlegen des Kurznamens einer Datei nicht erfolgreich ist, wird srverzögert mit dem nächsten Vorgang fortgesetzt. Bei srverzögert werden die Vorgänge "Datei verschieben" und "Datei löschen" als kritisch angesehen und nicht fortgesetzt, wenn ein verschiebe-oder Löschvorgang nicht erfolgreich ist.

 

 