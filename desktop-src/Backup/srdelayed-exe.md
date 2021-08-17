---
title: Srdelayed.exe
description: Anwendungen, die systemstatuswiederherstellungsvorgänge frühzeitig beim Start des Betriebssystems ausführen, können die Dateiverwaltungsfunktionen möglicherweise nicht verwenden, um den Kurznamen bestimmter Systemdateien zu verschieben, zu löschen oder fest zu legen.
ms.assetid: cedeb48e-bc1d-48d1-9bee-0b8b0132c3e5
keywords:
- Srdelayed.exe-Sicherung
- Systemstatuswiederherstellung – Sicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdf95ff77fd17a578b85e6037c71146666eae9522d066bc1c4629fb9a2c24e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835538"
---
# <a name="srdelayedexe"></a>Srdelayed.exe

Anwendungen, die systemstatuswiederherstellungsvorgänge frühzeitig beim Start des Betriebssystems ausführen, können die Dateiverwaltungsfunktionen möglicherweise nicht verwenden, um den Kurznamen bestimmter Systemdateien zu verschieben, zu löschen oder fest zu legen. Srdelayed.exe ist eine ausführbare Datei, die mit der WSB-Funktion (Windows Server Backup) in Windows Server 2008 bereitgestellt wird, die es Anwendungen zur Wiederherstellung des Systemstatus ermöglichen kann, systemstatuswiederherstellungsanwendungen zu verschieben, zu löschen und den Kurznamen von Systemdateien fest zu setzen.

Das srdelayed-Tool ist für Anwendungen zur Wiederherstellung des Systemstatus vorgesehen. Die Dateiverwaltungsfunktionen werden nicht ersetzt. Dieses Tool sollte nur verwendet werden, wenn die Anwendung den Kurznamen einer Systemdatei mithilfe der [**Funktionen MoveFileEx,**](/windows/desktop/api/winbase/nf-winbase-movefileexa) [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea)und [**SetFileShortName**](/windows/desktop/api/winbase/nf-winbase-setfileshortnamea) nicht verschieben, löschen oder festlegen kann. Während einer Wiederherstellung und eines Neustarts des Systemstatus wird Srdelayed.exe von der Systemwiederherstellung und dem wbadmin.exe-Befehlszeilentool verwendet, um den Kurznamen für bestimmte Systemdateien zu verschieben, zu löschen und fest zu legen. Srdelayed kann daher für Entwickler nützlich sein, die die Möglichkeit benötigen, diese Systemdateien in ihren eigenen Anwendungen zur Wiederherstellung des Systemstatus wiederherzustellen.

Srdelayed kann die folgenden Vorgänge ausführen:

-   Ein Vorgang zum Verschieben einer Datei ähnlich der [**MoveFileEx-Funktion**](/windows/desktop/api/winbase/nf-winbase-movefileexa) mit dem **Flag MOVEFILE \_ DELAY UNTIL \_ \_ REBOOT**
-   Ein Löschvorgang ähnlich der [**DeleteFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea)
-   Ein Set-Short-Name-Vorgang, der der [**SetFileShortName-Funktion**](/windows/desktop/api/winbase/nf-winbase-setfileshortnamea) ähnelt

Um Srdelayed verwenden zu können, benötigt Ihre Anwendung den vollständigen Pfad zum Speicherort der Srdelayed.exe-Datei und den vollständigen Pfad zu einer Unicode-Textdatei, die Sie erstellt haben, um die Informationen zu enthalten, die das Tool zum Ausführen aller angeforderten Dateiverwaltungsvorgänge benötigt. Ihre Anwendung ist dafür verantwortlich, sicherzustellen, dass diese Textdatei keine redundanten Anforderungen für einen Vorgang enthält und dass alle erforderlichen Reihenfolgen der Dateiverwaltungsvorgänge verarbeitet werden. Da beispielsweise ein Ordner leer sein muss, um gelöscht zu werden, muss Ihre Anwendung sicherstellen, dass die Textdatei das Entfernen aller Dateien innerhalb des Ordners angibt, bevor der Ordner gelöscht werden soll.

Wenn der **Eintrag SetupExecute** noch nicht in der Registrierung vorhanden ist, muss Ihre Anwendung einen **REG MULTI \_ \_ SZ-Typeintrag** namens **SetupExecute** unter dem folgenden Registrierungsschlüssel erstellen: **HKEY LOCAL \_ \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control Session** \\ **Manager**.

Ihre Anwendung sollte das folgende Format verwenden, um den Wert von **SetupExecute** auf den vollständigen Pfad zum Speicherort der Srdelayed.exe-Datei und den vollständigen Pfad zum Speicherort der Textdatei zu setzen. Stellen Sie \\ \\ dem Pfad der Textdatei das Präfix "??" \\ wie folgt voran:

*Vollständiger Pfad zum Srdelayed.exe* \\ \\ ?? \\ *Vollständiger Pfad zur Textdatei*  


Der folgende Wert für **SetupExecute** gibt beispielsweise an, dass sich die Srdelayed.exe im Ordner System32 und die Textdatei delayedOperations befindet:

C: \\ Windows \\ System32 \\srdelayed.exe \\ \\ ?? \\ C: \\ temp \\ DelayedOperations  


Leerzeichen im Pfad und Namen sollten hexadezimal codiert sein. Codieren Sie z. *B.* für Programme den Pfad als " \\ \\ ?? \\ C:Program%20Files \\a.dll".

Wenn die Registrierung oder das System beim Neustart wiederhergestellt wird, muss Ihre Anwendung sicherstellen, dass **SetupExecute** in die richtige Registrierungsstruktur geschrieben wird. Die Wiederherstellung der Registrierung wird ausgeführt, bevor Srdelayed.exe ausgeführt wird. Die Anwendung muss **SetupExecute in die** wiederhergestellte Version der Registrierung schreiben, da dies die Version ist, die gelesen wird.

## <a name="format-for-the-srdelayed-input-file"></a>Format für die srdelayed-Eingabedatei

Alle Informationen, die srdelayed zum Ausführen von Dateiverwaltungsvorgängen benötigt, werden als Unicode-Zeichenzeichenfolge in einer Unicode-Textdatei angegeben. Die Unicode-Zeichenzeichenfolge wird in Datensätze partitioniert, die jeweils in vier Felder partitioniert sind. Jeder Datensatz gibt eine einzelne Aktion zum Verschieben, Löschen oder Festlegen eines Kurznamens an. Die vier Felder jedes Datensatzes enthalten die Parameter für den Vorgang. Srdelayed.exe führt jeden Vorgang in der Reihenfolge aus, in der die Datensätze in der Zeichenfolge auftreten. Ihre Anwendung sollte auf doppelte Datensätze in dieser Datei überprüfen und die Duplikate entfernen.

Die folgende Zeichenfolge veranschaulicht das Format für eine Datei, die zwei Vorgänge angibt und aus zwei Datensätzen besteht. Jedes Parameterfeld endet mit einem einzelnen \\ L'0'-Zeichen. Ein Datensatz besteht aus vier aufeinander folgenden Feldern. Am Ende aller Datensätze wird ein zusätzliches einzelnes \\ L'0'-Zeichen angefügt.

`<ParamA1>L'\0'<ParamA2>L'\0'<ParamA3>L'\0'<ParamA4>L'\0'<ParamB1>L'\0'<ParamB2>L'\0'<ParamB3>L'\0'<ParamB4>L'\0'L'\0'`  
`|-----------------------RecordA------------------------|------------------------RecordB------------------------|`  


Die Bedeutung des ersten, zweiten, dritten und vierten Parameterfelds hängt davon ab, ob der Datensatz einen Vorgang zum Verschieben, Löschen oder Festlegen eines Kurznamens beschreibt.

## <a name="format-for-a-move-file-record"></a>Format für einen Dateidatensatz verschieben

Feld 1 identifiziert dies als Anforderung zum Verschieben einer Datei. Der Wert in diesem Feld ist immer L"MoveFile" und berücksichtigt die Kleinschreibung.

Feld 2 gibt den Quellspeicherort der Datei an. Der Srdelayed-Vorgang zum Verschieben von Dateien unterstützt das Verschieben eines Ordners nicht. In diesem Feld muss eine Datei angegeben werden. Der Wert für dieses Feld ist der vollständige Pfad der Datei, die an " ?? " angefügt ist, es sei denn, der Pfad enthält einen \\ \\ guiD (Globally Unique Identifier), der " ? " als Präfix \\ \\ \\ \\ verwendet. Entfernen Sie " \\ \\ ? " vor dem \\ Anfügen an " \\ \\ ?? \\ ".

Feld 3 gibt das Ziel der Datei an. Der Vorgang zum Verschieben einer Datei funktioniert nur innerhalb eines Volumes. Quelle und Ziel müssen sich auf demselben Volume befingen. Der Wert für dieses Feld ist der vollständige Pfad der Datei, die an " ?? " angefügt ist, es sei denn, der Pfad enthält einen \\ \\ guiD (Globally Unique Identifier), der " ? " als Präfix \\ \\ \\ \\ verwendet. Entfernen Sie " \\ \\ ? " vor dem \\ Anfügen an " \\ \\ ?? \\ ".

Feld 4 empfängt Statusinformationen von Srdelayed. Der Wert in diesem Feld sollte für einen neuen Datensatz auf L"NotExecuted" festgelegt werden.

Im folgenden Beispiel wird auf die Datei nach Laufwerkpfad verwiesen. Wenn der Pfad und name der Quelle C: Stagea.dll ist, fordert dieser Datensatz an, dass Srdelayed ihn in \\ \\ C: \\ temp \\a.dll.

MoveFile \\ \\ ?? \\ C: \\ Stage \\a.dll \\ \\ ?? \\ C: \\ temp \\a.dll NotExecuted  


Im folgenden Beispiel wird auf die Datei nach Volume-GUID-Pfad verwiesen. Wenn der Pfad und name der Quelle \\ \\ ist? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} Stagea.dll: Dieser Datensatz fordert \\ \\ an, dass Srdelayed \\ \\ es nach ? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\a.dll

 MoveFile \\ \\ ?? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} \\ Stage \\a.dll \\ \\ ?? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\a.dll NotExecuted  


## <a name="format-for-a-delete-file-record"></a>Format für einen Dateidatensatz löschen

Feld 1 identifiziert dies als Anforderung zum Löschen einer Datei. Der Wert in diesem Feld ist immer L"DeleteFile" und berücksichtigt die Kleinschreibung.

Feld 2 wird nicht verwendet. Der Wert in diesem Feld sollte auf L"Unused" festgelegt werden.

Feld 3 gibt die zu entfernende Datei an. Ein Ordner muss leer sein, um entfernt zu werden. Verwenden Sie Dateilöschvorgänge, um alle Dateien im Ordner zu entfernen, bevor Sie den Ordner entfernen. Der Wert für dieses Feld ist der vollständige Pfad der Datei, die an " ?? " angefügt ist, es sei denn, der Pfad enthält einen \\ \\ guiD (Globally Unique Identifier), der " ? " als Präfix \\ \\ \\ \\ verwendet. Entfernen Sie " \\ \\ ? " vor dem \\ Anfügen an " \\ \\ ?? \\ ".

Feld 4 empfängt Statusinformationen von Srdelayed. Der Wert in diesem Feld sollte für einen neuen Datensatz auf L"NotExecuted" festgelegt werden.

Im folgenden Beispiel wird auf die Datei nach Laufwerkpfad verwiesen. Wenn pfad und name C: tempb.dll ist, fordert dieser Datensatz \\ \\ an, dass Srdelayed die Datei löscht.

DeleteFile Unused \\ \\ ?? \\ C: \\ temp \\b.dll NotExecuted  


Im folgenden Beispiel wird auf die Datei nach Volume-GUID verwiesen. Wenn der Pfad und name \\ \\ ist? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} tempb.dll. Dieser Datensatz fordert \\ \\ an, dass Srdelayed die Datei entfernt.

DeleteFile Unused \\ \\ ?? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\b.dll\\ NotExecuted  


## <a name="format-for-set-short-name-record"></a>Format für Set Short-Name Record

Feld 1 identifiziert dies als Anforderung zum Festlegen des Kurznamens einer Datei. Der Wert in diesem Feld ist immer L"SetFileShortName" und berücksichtigt die Kleinschreibung.

Feld 2 gibt den Kurznamen an.

Feld 3 gibt den Pfad und den langen Namen an, um den Kurznamen zu erhalten. Der Wert für dieses Feld ist der Pfad und der lange Name der Datei, die an " ?? " angefügt ist, es sei denn, der Pfad enthält einen \\ \\ \\ guiD (Globally Unique Identifier), der "?" als Präfix \\ \\ \\ verwendet. Entfernen Sie " \\ \\ ? " vor dem \\ Anfügen an " \\ \\ ?? \\ ".

Feld 4 empfängt Statusinformationen von Srdelayed. Der Wert in diesem Feld sollte für einen neuen Datensatz auf L"NotExecuted" festgelegt werden.

Im folgenden Beispiel wird auf die Datei nach Laufwerkpfad verwiesen. Wenn der Pfad und der Name der Datei C: tempShortFileName.dll ist, fordert dieser Datensatz an, dass die Datei den Kurznamen \\ \\ ShortN~1.dll.

SetFileShortName ShortN~1.dll \\ \\ ?? \\ C: \\ temp \\ShortFileName.dll NotExecuted  


Im folgenden Beispiel wird auf die Datei nach Volume-GUID verwiesen. Wenn der Pfad und der Name der Datei \\ \\ ist? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} tempShortFileName.dlldieser Datensatz fordert an, dass die Datei einen \\ \\ Kurznamen, \\ ShortN~1.dll.

SetFileShortName ShortN~1.dll \\ \\ ?? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\ShortFileName.dll\\ NotExecuted  


## <a name="srdelayed-operations-status"></a>Status von überdelayierten Vorgängen

Srdelayed schreibt die Zeichenfolge L"SC=*xxxxxxx*" in das vierte Feld jedes Datensatzes der Textdatei, wobei *xxxxxxx* ein Hexadezimalwert ist, der den Status des angeforderten Vorgangs angibt. Der Wert 0 (null) gibt an, dass der Vorgang erfolgreich war.

Srdelayed erstellt unter **HKEY \_ LOCAL \_ MACHINE** Software Microsoft Windows NT CurrentVersion einen Registrierungsschlüssel namens **SystemRestore,** um das Ergebnis des gesamten Wiederherstellungsvorgang \\  \\  \\  \\  zu protokollieren. Wenn Srdelayed alle angeforderten Vorgänge erfolgreich ausführt, wird der Name RestoreStatusResult unter diesem Schlüssel mit einem Wert von 0 (null) geschrieben. Wenn Srdelayed keine der angeforderten Vorgänge ausführen kann, werden die Namen RestoreStatusResult und RestoreStatusDetails unter diesem Schlüssel mit Werten ungleich 0 (null) geschrieben. Der Name RestoreStatusDetails wird nur unter diesem Schlüssel geschrieben, wenn Srdelayed keine angeforderten Vorgänge ausführen kann. Wenn ein Vorgang zum Festlegen des Kurznamens einer Datei nicht erfolgreich ist, fährt Srdelayed mit dem nächsten Vorgang fort. Srdelayed betrachtet die Vorgänge zum Verschieben und Löschen von Dateien als kritisch und wird nicht fortgesetzt, wenn ein Verschieben oder Löschen nicht erfolgreich ist.

 

 