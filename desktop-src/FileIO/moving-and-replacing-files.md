---
description: Überlegungen zum Verschieben und Ersetzen von Dateien mithilfe der CopyFileEx-, der-Funktion, der ReplaceFile-Funktion und der-Funktion von "muvefileex".
ms.assetid: 4872af0d-42e8-4576-9aa9-4b8671375f2e
title: Verschieben und Ersetzen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d7f08d2bd8d07645076620e839d7d12f5969502
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "106354283"
---
# <a name="moving-and-replacing-files"></a>Verschieben und Ersetzen von Dateien

Bevor ein Kopiervorgang ausgeführt werden kann, muss die Quelldatei geschlossen oder nur zum Lesen geöffnet werden. Die Quelldatei kann nicht zum Schreiben geöffnet werden. Um eine vorhandene Datei in eine neue Datei zu kopieren, verwenden Sie die Funktion [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) oder [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) . Anwendungen können angeben, ob **CopyFile** und **CopyFileEx** fehlschlagen, wenn die Zieldatei bereits vorhanden ist. Wenn die Zieldatei vorhanden ist und geöffnet ist, muss Sie mit anwendbaren Freigabe Berechtigungen geöffnet worden sein. Weitere Informationen finden Sie unter " [**kreatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)".

Mit der [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) -Funktion kann eine Anwendung auch die Adresse einer Rückruffunktion angeben (siehe [**copyprogressroutine**](/windows/desktop/api/WinBase/nc-winbase-lpprogress_routine)), die jedes Mal aufgerufen wird, wenn ein anderer Teil der Datei kopiert wurde. Die Anwendung kann diese Informationen verwenden, um einen Indikator anzuzeigen, der die Gesamtzahl der Bytes anzeigt, die als Prozentsatz der Gesamt Dateigröße kopiert wurden.

Die [**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea) -Funktion ersetzt eine Datei durch eine andere Datei. die Option besteht darin, eine Sicherungskopie der ursprünglichen Datei zu erstellen. Die Funktion behält Attribute der ursprünglichen Datei bei, z. b. die Erstellungszeit, die ACLs und das Verschlüsselungs Attribut.

Eine Datei muss auch geschlossen werden, bevor Sie von einer Anwendung verschoben werden kann. Die Funktionen " [**muvefile**](/windows/desktop/api/WinBase/nf-winbase-movefile) " und " [**muvefileex**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) " kopieren eine vorhandene Datei an einen neuen Speicherort und löschen den ursprünglichen.

Mit der [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) -Funktion kann eine Anwendung auch angeben, wie die Datei verschoben werden soll. Die Funktion kann eine vorhandene Datei ersetzen, eine Datei zwischen Volumes verschieben und das Verschieben der Datei verzögern, bis das Betriebssystem neu gestartet wird.

 

 



