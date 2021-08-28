---
description: Überlegungen zum Verschieben und Ersetzen von Dateien mithilfe der Funktionen CopyFileEx, CreateFile, Replacefile und MoveFileEx.
ms.assetid: 4872af0d-42e8-4576-9aa9-4b8671375f2e
title: Verschieben und Ersetzen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35c78085865006d1dfbbe322239c4704d215d038897b81d1f139d66d06f65bbc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696010"
---
# <a name="moving-and-replacing-files"></a>Verschieben und Ersetzen von Dateien

Bevor ein Kopiervorgang ausgeführt werden kann, muss die Quelldatei geschlossen oder nur zum Lesen geöffnet werden. In keinem Thread kann die Quelldatei zum Schreiben geöffnet werden. Um eine vorhandene Datei in eine neue zu kopieren, verwenden Sie die [**CopyFile-**](/windows/desktop/api/WinBase/nf-winbase-copyfile) oder [**CopyFileEx-Funktion.**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) Anwendungen können angeben, **ob CopyFile und** **CopyFileEx** fehlschlagen, wenn die Zieldatei bereits vorhanden ist. Wenn die Zieldatei vorhanden und geöffnet ist, muss sie mit den entsprechenden Freigabeberechtigungen geöffnet worden sein. Weitere Informationen finden Sie unter [**CreateFile.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)

Mit [**der CopyFileEx-Funktion**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) kann eine Anwendung auch die Adresse einer Rückruffunktion angeben (siehe [**CopyProgressRoutine**](/windows/desktop/api/WinBase/nc-winbase-lpprogress_routine)), die jedes Mal aufgerufen wird, wenn ein anderer Teil der Datei kopiert wurde. Die Anwendung kann diese Informationen verwenden, um einen Indikator anzuzeigen, der die Gesamtzahl der kopierten Bytes als Prozent der Gesamtdateigröße zeigt.

Die [**ReplaceFile-Funktion**](/windows/desktop/api/WinBase/nf-winbase-replacefilea) ersetzt eine Datei durch eine andere Datei mit der Option, eine Sicherungskopie der ursprünglichen Datei zu erstellen. Die Funktion behält Attribute der ursprünglichen Datei bei, z. B. erstellungszeit, ACLs und Verschlüsselungsattribut.

Eine Datei muss ebenfalls geschlossen werden, bevor eine Anwendung sie verschieben kann. Die [**Funktionen MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile) und [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) kopieren eine vorhandene Datei an einen neuen Speicherort und löschen die ursprüngliche Datei.

Mit [**der MoveFileEx-Funktion**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) kann eine Anwendung auch angeben, wie die Datei bewegt werden soll. Die Funktion kann eine vorhandene Datei ersetzen, eine Datei über Volumes hinweg verschieben und das Verschieben der Datei verzögern, bis das Betriebssystem neu gestartet wird.

 

 



