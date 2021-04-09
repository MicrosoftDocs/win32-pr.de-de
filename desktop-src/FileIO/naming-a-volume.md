---
description: Eine Bezeichnung ist ein benutzerfreundlicher Name, der einem Volume zugewiesen wird, normalerweise von einem Endbenutzer, um die Erkennung zu vereinfachen. Ein Volume kann eine Bezeichnung, einen Laufwerk Buchstaben, beides oder keines von beiden aufweisen. Um die Bezeichnung für ein Volume festzulegen, verwenden Sie die Funktion setvolumelabel.
ms.assetid: f640f42d-a703-4e2e-a6d3-09cbe989cd11
title: Benennen eines Volumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6435b6b5c7283cf2fb9a98951698f79646dfdffa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867315"
---
# <a name="naming-a-volume"></a>Benennen eines Volumes

Eine Bezeichnung ist ein benutzerfreundlicher Name, der einem Volume zugewiesen wird, normalerweise von einem Endbenutzer, um die Erkennung zu vereinfachen. Ein Volume kann eine Bezeichnung, einen Laufwerk Buchstaben, beides oder keines von beiden aufweisen. Um die Bezeichnung für ein Volume festzulegen, verwenden Sie die Funktion [**setvolumelabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) .

Mit mehreren Faktoren kann es schwierig werden, bestimmte Volumes zu identifizieren, die nur Laufwerk Buchstaben und Bezeichnungen verwenden. Eine davon ist, dass ein Volume nicht erforderlich ist, um einen Laufwerk Buchstaben oder eine Bezeichnung zu haben. Eine andere Möglichkeit besteht darin, dass zwei verschiedene Volumes dieselbe Bezeichnung aufweisen können, sodass Sie mit Ausnahme des Laufwerk Buchstabens nicht unterschieden werden können. Ein dritter Faktor ist, dass sich die Zuweisungen von Laufwerk Buchstaben ändern können, wenn Volumes dem Computer hinzugefügt und daraus entfernt werden.

Um dieses Problem zu beheben, verwendet das Betriebssystem *Volume-GUID-Pfade* zur Identifizierung von Volumes. Dabei handelt es sich um Zeichen folgen in dieser Form:

"\\\\?\\ Volume {*GUID*} \\ "

Dabei ist *GUID* eine Globally Unique Identifier (GUID), die das Volume identifiziert.

Ein Volume-GUID-Pfad wird manchmal als eindeutiger *Volumename* bezeichnet, da ein Volume-GUID-Pfad nur auf ein Volume verweisen kann. Dieser Begriff ist jedoch irreführend, da ein Volume mehr als einen VolumeGuid-Pfad aufweisen kann.

Das \\ \\ \\ Präfix "?" deaktiviert die Pfad Verarbeitung und wird nicht als Teil des Pfads betrachtet. Weitere Informationen zum \\ \\ Präfix "? \\ " finden Sie unter [Benennen einer Datei oder eines Verzeichnisses](naming-a-file.md).

Sie müssen vollständige Pfade angeben, wenn Sie VolumeGuid-Pfade mit dem \\ \\ \\ Präfix "?" verwenden.

Ein bereitgestellter *Ordner* ist eine Zuordnung zwischen einem Ordner auf einem Volume und einem anderen Volume, sodass der Ordner Pfad für den Zugriff auf das Volume verwendet werden kann. Wenn Sie z. b. die [**setvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) -Funktion verwenden, um einen bereitgestellten Ordner zu erstellen, der das Volume "d:" \\ dem Ordner "C: \\ mountd \\ " zuordnet, können Sie entweder den Pfad ("d: \\ " oder "C: \\ mountd \\ ") verwenden, um auf das Volume "d:" zuzugreifen \\ .

Ein *volumeeinstellungspunkt* ist ein beliebiger benutzermoduspfad, der für den Zugriff auf ein Volume verwendet werden kann. Es gibt drei Arten von volumeinstellungspunkten:

-   Einen Laufwerk Buchstaben, z. b. "C: \\ ".
-   Einen VolumeGuid-Pfad, z. b. " \\ \\ ? \\ Volume {26a21bda-a627-11d7-9931-806e6f 6e6963} \\ ".
-   Ein bereitgestellter Ordner, z. b. "C: \\ mountd \\ ".

Alle Funktionen für Volumes und bereitgestellte Ordner, die einen Volume-GUID-Pfad als Eingabeparameter annehmen, erfordern den nachfolgenden umgekehrten Schrägstrich. Alle Volumes und bereitgestellten Ordner Funktionen, die einen Volume-GUID-Pfad zurückgeben, stellen den nachfolgenden umgekehrten Schrägstrich bereit. Dies ist jedoch [**nicht der Fall bei der Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) "Funktion". Sie können ein Volume öffnen, indem Sie **CreateFile** aufrufen und den nachfolgenden umgekehrten Schrägstrich aus dem von Ihnen angegebenen Volumenamen weglassen. " **Kreatefile** " verarbeitet einen VolumeGuid-Pfad mit angefügtem umgekehrten Schrägstrich als Stammverzeichnis des Volumes.

Das Betriebssystem weist einem Volume einen VolumeGuid-Pfad zu, wenn das Volume zum ersten Mal installiert wird und wenn das Volume formatiert ist. Die Funktionen Volume und bereitgestellter Ordner verwenden VolumeGuid-Pfade, um auf Volumes zuzugreifen. Zum Abrufen des Volume-GUID-Pfads für ein Volume verwenden Sie die [**getvolumenameforvolumemountpoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) -Funktion.

Die Pfadlängen können ein Problem sein, wenn ein bereitgestellter Ordner erstellt wird, der ein Volume mit einer Deep Directory-Struktur mit einem Verzeichnis auf einem anderen Volume verknüpft. Dies liegt daran, dass der Pfad des Volumes mit dem Pfad des Verzeichnisses verkettet ist. Der global definierte Konstante **Max- \_ Pfad** definiert die maximale Anzahl von Zeichen, die ein Pfad aufweisen kann. (Weitere Informationen zum **maximalen \_ Pfad** finden Sie unter [Benennen einer Datei oder eines Verzeichnisses](naming-a-file.md)). Sie können diese Einschränkung vermeiden, indem Sie eine der folgenden Aktionen ausführen:

-   Weitere Informationen finden Sie unter Volumes mit ihren VolumeGuid-Pfaden.
-   Verwenden Sie die Unicode-Versionen (W) der Dateifunktionen, die das \\ \\ Präfix "?" unterstützen \\ .

 

 



